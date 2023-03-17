## ProxMox Hypervisor Installation 
![alt_text](./images/proxmox-setup.jpg)

- Download the latest "ProxMox ISO [version#] ISO installer" from the [official website](https://www.proxmox.com/en/downloads/category/iso-images-pve)
- Flash the ISO image to a USB drive (at least 8GB in size) using BalenaEtcher or Rufus (free Windows programs)
- Plug the flashed USB drive into the PC you wish to use as your hypervisor
> Note: Ensure that the device has a conenction to your local network so it can auto-poulate the IP settings.
- Press `F12` or `DEL` or the other BIOS key to enter your boot disk selection or BIOS.
- Force the PC to boot from the flash drive you created by selecting the flashdrive from the BIOS menu (google your PC BIOS for how to find the boot drive settings)
 - The installer page should popup. Proceed with "Install Proxmox VE"
 - Agree to the EULA
 - Select the target disk and continue (if you wish to create a ZFS pool with a second cached drive, see [below](creating-zfs-pool-and-cache) to modify the target drive.
> Note: This action will erase the drive. If you have files you don't want to lose, first back them up before proceeding.
 - Select your country and timezone.
 - Enter a password that you wish to use to access the Proxmox web UI (remember this).
 - Select your managment interface (if you have more than one NIC).
 - Enter your preferred hostname (FQDN is not required, "pve.lan" or "pve0.lan" will work).
 - Enter the static IP address you wish to use to connect to the Proxmox UI (ex. 192.168.1.100).
 - The DNS server and gateway should already be auto-populated. Typically, the default gateway for most routers is 192.168.1.1.
 - The final screen is the install screen (again, take note of the IP address, you will need this to access Proxmox.) Hit the install button and wait.
 - Remove the installer media after your computer finishes the install and successfully rebootsv (there's a confirmation screen at the end).
 - If everything was successfull, you should see a mostly black login screen (if you don't see this screen, skip to [Installation Issues](Installation-issues) below).
 - After ProxMox has finished installing, it will automatically reboot (reboot manually if it did not).
 - Now, enter the `https://[IP_address_you_set];8006` in a web browser on another machine connected to the same router and network.
 - Enter the IP address you set to access the Proxmox UI (ex. https://192.168.1.100:8006).

 > Don't forget to include "https://" and add ":8006" at the end of the IP address.

 - You will get a warning screen from your web browser telling you the URL address you went to is unsafe, but that's just because you don't have SSL for your ProxMox. It's a false alarm. Just click on whatever options you have to continue to the site.
 - Enter `root` for the username and enter the password you created at setup to access. Done!
- Next, you will be prompted to login to ProxMox. Input `root` for the username and enter the password you created at setup to gain access.

> Before deploying and VMs, you can consolidate and expand your storage. Do this *before* creating VMs.

#### Installation Issues
- If an install goes ary, you can always use the PrxoMox debug mode built into the bootable .iso installer.
- Try rebooting with the .iso installer plugged in, but this time select "Advance Options" (underneath "Install Proxmox VE") and choose the "Install Proxmox VE (Debug mode)" option.
- This will boot up in a Linux Debian CLI mode that allows you access to powerful CLI commands (i.e. wipe the drives and try reinstalling ProxMox). Type `exit` after it loads and the prompt is ready.
- You want to find the drive names. Drive names usually end in "1n1" or "0n1" depending on how many drives you have mounted.
- The drives are listed in the `/dev` folder path. Type `cd /dev` then type `ls` to list the contents of the folder to get the names of the disks (ex. `/dev/nvme0n1`). Take note of this as you will need it for the next drive wipe command.
- To wipe a corrupted install, type `wipefs -a /dev/[drive_name] [path_to_second_drive_if_applicable]`. After that, `exit` and `reboot` the endpoint and try the install again.
- Type `exit` again, wait a second, then type `reboot`. (Make sure the bootable drive is still attached.)
- The EULA should popup, and you can now attempt to reinstall Proxmox.
- You can also access BusyBox in dev/debug mode to fix a ZFS error, see below for the error message:

#### Boot fails and goes into busybox
If booting fails with something like:

```
No pool imported. Manually import the root pool
at the command prompt and then exit.
Hint: try: zpool import -R /rpool -N rpool
```
- This is because zfs is invoked too soon (it has happen sometime when connecting a SSD for future ZIL configuration).
- To prevent it, boot into debug mode, run Busybox (type `busybox` and hit `ENTER`), then try __ONE__ of the following:
 - a) edit /etc/default/grub and add "rootdelay=10" at GRUB_CMDLINE_LINUX_DEFAULT (i.e. GRUB_CMDLINE_LINUX_DEFAULT="rootdelay=10 quiet") and then issue a # update-grub
 - b) edit /etc/default/zfs, set ZFS_INITRD_PRE_MOUNTROOT_SLEEP='4', and then issue a "update-initramfs -k 4.2.6-1-pve -u"

## ZFS Configuration

#### Creating a ZFS Pool and Cache
> Note:  RAID0 forces stripped drives to the _smallest_ drive size (i.e. 2TB + 118GB = 118GB storage pool size).
> Note: RAID-Z or mirrored (RAID1) ZFS configurations will _not_ work with cache drive setups. 
- When selecting a disk, choose the primary (largest) disk and then click the options button.
- Change the file system type to the ZFS RAID0 configuration and max out the disk space allotted (should be maxed by default).
- Exclude the cache disk from the ZFS pool at this time (we will add it later).
- Choose the l4x compression, and finish out the disk wizard prompts.
- Finish the Proxmox installation, login, and open a shell to enter the following command `zpool add rpool cache [name_of_cache_drive]` and hit enter to add the cache drive to the ZFS pool created at install.
- You can check the status of the pool by typing `zpool status [name_of_pool]` (the default pool name is `rpool`). Or, you can check it in the UI. Navigate to Node (pve) > Disks > ZFS. You should see the cache drive in the pool.

#### Adding a Cache Drive
- Using SSH or the console, type the following: `zpool create rpool /dev/[primary_drive_name] cache /dev/[cache_drive_name]
- Type `zpool status tank` for an overivew of your new ZFS pool with cache.

#### Create ZFS Datasets
- You can view your current ZFS pool via `zpool list` and `zfs list`. Take note of the `mountpoint` name (if you created a ZFS pool at installation, this will be called `rpool` by default).
- To create datasets for storing `ISOs` and VM storage and more, type the following:
 - `zfs create [mountpoint_pool_name]/backups`
 - `zfs create [mountpoint_pool_name]/iso`
 - `zfs create [mountpoint_pool_name]/vm`
- These dataset will share the total pool size. It dynamically allocates disk space as needed.
- Now we need to mount/add these datasets at the `Datacenter` level:
 - Navigate to > Datacenter (node, left-most pane) > Storage (subset) > Add > Directory > Enter the name of the dataset (i.e. `backups`, `iso`, `vm`), and add them one at a time.
  - ID: `/rpool/iso` | Directory: `/rpool/iso` | Content: `ISO image` and `Container templates`
  - ID: `/rpool/vm` | Directory: `/rpool/vm` | Content: `Disk image` and `Container`
  - ID: `/rpool/backups` | Directory: `/rpool/backups` | Disk Image: `VZDump backup file` and `Snippets`

#### Move the Root Disk of VMs
- Navigate to > Datacenter > PVE Node > [VM] > Resources > Click on Root Disk > Click on Volume Action (button) > Move Storage > Target Storage (dropdown) > Select the `VM` dataset > Check the Delete source (box) > Move Volume (button).

#### Creating a Backup and Restore
- Now that you have created a place to store your backups, you can schedule and restore your VM or containers

> Restoring from a backup is also another way to change the number of the VM/Container.

- To create a backup repository, navigate to: Datacenter (left-most pane) > Backup (menu option) > Add (button) > Schedule: Everyday [3AM] > Selection mode: All > Storage: Backups > Create (button)
- To restore a backup, navigate to: Datacenter > [proxmox_node_name] > Click on Backups (ZFS dataset) > Backups (menu option on right) > Click on the backup file (ending in `.tar.zst`) > Click Restore (button, top) > Storage: VM (_not_ local) > CT: Enter the desired number (100-999) > Check the "Start after restore" box (if desired) > Do not change the default priviledge settings > Click Restore (button)
- Now, wait for the backup to be restored and you should eventraully see it populate under the Datacenter > Proxmox Node > [VM/Container_Name]


## VM Time, Baby!

> Before we can write an ISO file to our new ProxMox setup, we must edit the directory to allow `Disk Image`.

- Click on `Datacenter` (underneath the "Sever view" pane).
- Click on `Storage` from the list
- Click on the ID (the only ID listed should be "local" if you followed the previous step), and then click `Edit`.
- Click on the `Content` dropdown box and click on `Disk Image` to include it and allow it.

> If you want to create containers inside of ProxMox, then you should also click on `Containers` to include and allow them, too.

- Navigate to ISO Images (under the sever view dropdown menu, you have to click on the ProxMox node).
- Currently, the directory should be empty, so you will need to download your ISOs and then upload them by clicking `Upload`.
- After uploading the VM you want, now it's time to click on the blue button on the top right of the UI that says `Create VM`.
- Give the VM a name and click next.
- Select the ISO image you wish to install (ex. Ubuntu), and click next, and (if you don't want to change any of the default settings) click next again.
- Now, under the `Disks` tab, set the total disk size you wish to allocate to that VM instance, and hit next again.
- Now it is time to set the CPU usage for this VM. Set the number of CPUs you want to set apart for this VM and hit next.
- Now set the memory in MiB.
 
> Note: GB is to MiB *not* a 1:1 ratio like GB is to MB. Use [this conversion calculator for reference](https://mbtogb.com/128-gb-to-mb)

> Note: You can always edit the disk space, core, and memory allocations later.

- Now for network settings. By default, the VM will be bridged to your home network, so it will receive an IP address from your router. If you don't want that, then edit the network settings as desired.
- With everything configured, you are now at the final `Confirm` stage. If everything looks good to you, hit finish to spin up a new VM! Within seconds it will be ready to go. You can check on it from the `Server View`.

> Note: You will still have to go through the initial install and setup phase like you normally would when you first are installing a new OS. When you start the system, go through the necessary install process.

> About Creating Containers: You can also create Docker-like containers with ProxMox by downloading Linux container ISOs and uploading them to ProxMox, and then click on the `Create CT` blue button (right next to the `Create VM` button). The process for creating containers is the same as creating VMs.

## Reverse Proxy DDNS

#### Cloudflare DDNS Reverse Proxy
- [NetworkChuck made a video tutorial](https://www.youtube.com/watch?v=ey4u7OUAF3c) about this, but here's the steps:
- Buy a domain and create a Cloudflare Nameserver (DNS > Records > Nameservers).
- Copy the nameservers and add them to your domain registar (nameserver updates can take up to 24hrs, but it is usually updated within minutes).
- Using [ZeroTrust](https://one.dash.cloudflare.com/899e8be9fba8f3cc125ebdf9263380e0/home/quick-start) create a new tunnel: [ZeroTrust](https://i.imgur.com/FipaEgQ.png) (left navigation pane) > Cloudflare ZeroTrust (navigation pane) > Access (dropdown) > [Tunnels](https://i.imgur.com/nnONYTE.png) > Create at tunnel (button)
 - Enter the domain name you created...

[zero_trust](https://i.imgur.com/FipaEgQ.png)
[ztunnels](https://i.imgur.com/nnONYTE.png)
  
### Kemp LoadMaster
- An Enterprise Load-balancer Setup on ProxMox
> Note: [Cloudflare's Zero Trust automatically load-balances](https://developers.cloudflare.com/cloudflare-one/connections/connect-apps/routing-to-tunnel/) internet traffic. Kemp is not required, but is compatible with Cloudflare. 
- If you opt-out of using Cloudflare's Zero Trust loadbalancer, you can integrate Cloudflare's DNS records with Kemp to get the same load-balancing benefits. 
- First-off, why use a load-balancer?
  - **Industry-standard Epic-ness**: If you want to fit in with the cool kids (NASA, Harvard University, Apple, EA, Sony, US Army, JPMorgan, and more!) then you want the Kemp LoadMaster for your homelab.
  - **Custom Domain URL Access**: Access your Plex/Jellyfin server by entering a custom URL (ex. https://<your_custom_domain_name.com>). So, if you want to  access your homelab services (i.e. NAS files, Plex/Jellyfin media server, Prologue audiobooks, VMs, etc.) remotely (when you are not connected to your home network), you will want a load balancer.
  - **Security**: More ports = more network vulnerabilities! Hackers love ports. These digital pirates will growl, "Ahoy! I see me an open port" and then they sail right into your network with their malicious intent. So, if you self-host a website, watch Plex when away from home or at a friend's house, or you just want to access your NAS files outside your house, you must open up multiple ports which, in turn, exposes you to hackers. A load-balancer solves this problem. A load-balancer only requires *one* open port (443), greatly reducing your network vulnerability.
  - **Hide Your Public IP Address**: You *never* should share your public IP address! So, how can you hide it from attackers, and still want to share those amazing homelab apps you built and are so proud of without risking revealing your public IP? Two-words: "load balancer."
- Get a [*multi-compatible* domain name](https://www.a2hosting.com/domains?aid=presearchnode&bid=75dbf1c0) or use one you already have
- Get an enterprise-grade load-balancer called Kemp [get this 100% free version](https://freeloadbalancer.com/)
  - You will first need to create an account with Kemp and then verify your email to get to the download page.
  - You will notice that ProxMox is not listed among other Hypervisors, but that's not a problem. Kemp will still work! Here's how:
  - Select "VMware (OVF)" to download and agree to the terms (there's no difference in functionality, it is just packaged differently)
  - Next, unpack the downloaded zip file that contains the LoadMaster VM image. You can use a free tool like [WinRar](https://www.win-rar.com/start.html?&L=0) or [7-zip](https://www.7-zip.org/). You'll notice some *zip-insception* or *folder-inception* going on because there's another folder within the original folder, so just open both. After unzipping everything and getting to *Limbo-level-inception* you will find Mal--I mean--the files you really looking for.<br> ![alt_text](https://media.giphy.com/media/Ajf5GjjVwUYI8/giphy.gif)
  - Like Leonardo DiCaprio, you want to find something down in Limbo. Look for the `.ovf` and the `.vmdk` files. Got 'em? Good, you'll need to know the directory and files names so you can copy them into ProxMox using `ssh` and a SCP client.

  #### Copy Files with SCP
- Linux and macOS systems have a SCP client built in, but you will need to download [Git bash for Windows](https://git-scm.com/download/win). Or just run the following command in Windows Powershell and approve the install when prompted:
  
```sh
winget install --id Git.Git -e --source winget
```
  
<br>![alt_text](./images/gitbash-install.jpg)
  
- Next, using terminal or Windows Powershell, you want to `scp` the .ovf file to your ProxMox home folder. Type the following:
  
```sh
scp C:\Users\[user]\[directory]\Free-VLM-VMware-OVF-64bit\Free-VLM-VMware-OVF-64bit\[filename].ovf roo@[your_proxmox_ip]:/root/`
```
  
- Next, you need to run and `scp` copy command. We want to copy **2** files (the .ovf and the .vmdk files) from the PC with those files to the ProxMox home directory. First, let's get the `.ovf` file uploaded.
  
```sh
scp C:\Users\[user]\[directory]\Free-VLM-VMware-OVF-64bit\Free-VLM-VMware-OVF-64bit\[filename].ovf roo@[your_proxmox_ip]:/root/`
```

> Tip: Once you have spelled out (or copy & pasted it in the terminal window), you can start the first few letters of the file name and press `TAB` to auto-complete the file you want.

- This `scp` command will securely copy & transfer that file into the `/root/` dir of ProxMox. Now, lets send the other one:
  
```sh
scp C:\Users\[user]\[directory]\Free-VLM-VMware-OVF-64bit\Free-VLM-VMware-OVF-64bit\[filename].vmdk roo@[your_proxmox_ip]:/root/`
```
  
> If you fail to copy/transfer both files, you will get an error message saying the file could not be parsed. So make sure you upload both files.
  
> You can check if the file made it by `ssh` & `ls` into your ProxMox environment. <br> 
  
#### Deploying Kemp via `importovf` CLI

- Now we are ready to import Kemp into the ProxMox environment. You will need to use the `importovf` feature to delpoy Kemp.Use the following command:
  
  ```sh
  qm importovf [ID] LoadMaster-VLM-[VERSION].RELEASE-VMware-VBox-OVF-FREE.ovf [SERVER]
  ```
  
  > The `ID` number will be whatever the next ID for your VM is available (i.e. if you only made 1 VM then "101" is the next available ID, just check it in the `Server View` and `Datacenter` dropdown menu). The `SERVER` is name of the local storage listed in the `Data center`. It is probably just `local`.

> Note to self: Complete Cloudflare DDNS setup process.

#### Cloudflare Kemp Config
- After successfully setting up the Cloudflare DDNS reverse proxy, you should be able to access your Proxmox machine remotely using the custom domain you set up. If so, continue below:
-  Navigate to your [new domain settings pane](https://i.imgur.com/D8tQ69l.png) > SSL/TLS > Overview > "Full (__strict__)" (radio button)
-  Now, create a Certificate: Your domain settings pane > SSL/TLS > Origin Server > [Create Certificate](https://i.imgur.com/R1iIaQt.png) (button)
-  On the SSL/TLS > Origin Server screen > ["Use my private key and CSR"](https://i.imgur.com/3pz8lpI.png) (radio button) > Copy and paste your Kemp CSR into the text field > Create (button at the bottom)
-  Now, copy the "Origin Certiciate" that pops up and paste it to a text file (i.e. Notepad).
-  Save the text file type as follows: `[your_domain_name].pem`
-  Copy the RSA Private key from Kemp and paste it into another text file.
-  Save that text file type as follows: `[your_domain_name]priv.key`
-  Navigate to Kemp > Certificates & Security > SSL Certificates > Import Certificate (button on the top right)
-  Select and upload the `.pem` file you saved for the "Certificate File"
-  Select and upload the `.key` file you save for the "Key File"
-  Enter `Cloudflare_Origin_[domain]` in the "Certificate Identifer" field and save. You should get a message saying that the certificate was successfully saved.
-  [Download the Cloudflare Origin ECC PEM file](https://developers.cloudflare.com/ssl/static/origin_ca_ecc_root.pem), which should look look something like this: `origin_ca_ecc_root.pem`
-  Back on the Kemp loadmaster page >  Certificates & Security > SSL Certificates > "Add Intermediate" (button) > select and upload that `origin_ca_ecc_root.pem` file.
-  Enter `cloudflare_root_[domain]` in the Certificate Name field and hit the Add Certificate button. Now we have to add the newly created Cloudflare cert to the Kemp vitrual services.
-  Kemp > Virtual Services > Vew/Modify Services > Modify (button under the "Operation" column)
-  On the Properties screen, drop down the "SSL Properties" menu and check the "SSL Accelartion Enabled" box. This will propogate the Self Signed Certificate config.
-  Check the "Reencrypt" box. This will encrypt the traffic to and from your Proxmox server.
-  Click the arrows to add the `Cloudflare_Origin_[domain]` certificate and click the "Set Certificates" button.
- In __your router settings__ , you need to port-forward your [Kemp VIP](https://i.imgur.com/NjbzhgL.png). Enter the Kemp VIP and forward port `443`.

#### Kemp Content Rules
> The following content filter rules will enable the Kemp loadmaster to route traffic from 443 to the individual, specific ports of each web app/server/service you have running on Proxmox (i.e. port 32400 for a Plex server).
> You must mannually add the new A records for each subdomain and subequent IP address and port number that you wish Kemp to load balance (i.e. plex.[yourdomain].com IPV4 address + the required port of the server).
- To enalbe Kemp subdomain routing and filtering, navigate to Kemp > Rules & Checking > Content Rules > Create New Rule (button, top right).
- On the Create Rule screen:
 - Add a rule name (i.e. "Plex")
 - Enter `host` in the "Header Field"
 - Enter `^[subdomain_name].[your_domain.com]`
 - Check the "Ignore Case" box (to ignore case sensitivity).
 - Click "Create rule" (button)
- Now we need to add this new rule to the vitrual services. Navigate to:
 - Vitrual Services > View/Modify Services > Advance Properties (dropdown menu) > click on "Enable" (text) next to the "Content Switching" row. The fields should refresh and you should see: "Content Switching Enabled" now.
 - Now, scroll down to the bottom of this page to the "SubVSs" and open that dropdown menu. You should see the new rule(s) that you added here (if not, return to the Create Rule section).
  - Click on the "None" (grey button highlited in red) under the "Rules" column.
  - Change the Rule from "default" to the rule name you set (i.e. Plex), and click on the "Add" (button). Done.
 - Test the connection by entering `[subdomain_name].[your_domain.com]` in your browser.

> You could always get a free domain from Freenom, but the major drawback is that many free domains available (ending in `.tk`, `.ml`, `.cf`, `.gq`) **will not work** with some remote access applications like Apache Guacamole.
  
#### Modifying the Kemp Config
- When you first boot the "LoadMasterVLM" you will have problems. It will throw errors and reboot. The problem has to do with the SCSI Controller. By default, ProxMox runs it as LSI, so we need to change it to VMware PVSCSI. We can change that directly from the terminal:
  
```sh
nano etc/pve/qemu-server/[ID].conf
```

- Once you are in the .conf file, use the down arrow to toggle to the bottom line and add the following entry `scsihw: pvscsi` then press `CTRL + X` then `y` then `ENTER` to save this new configuration.
  
<br>![alt_text](./images/vmware-pvscsi-1.jpg)
  
- If that worked, you will see the change on the hardware screen.
  
<br>![alt_text](./images/vmware-pvscsi-2.jpg)
  
- Also, you wan to give Kemp LoadMaster an internet connection, so go ahead and add it while you are on this screen. Just click `Add` and add your `Network Device`.
- I also recommend adding additional CPU cores and RAM (at least 4GB) to help with running Kemp without a problem as some users mentioned issues when the RAM was below 2 cores and 4GB of RAM (by default, it will give Kemp only 2GB).
  
<br>![alt_text](./images/loadmaster-working.jpg)

 > I want to five credit to Lusk.blog for the helpful insights on setting up Kemp with ProxMox. You can [check out his blog here](https://lusk.blog/how-to/running-free-load-balancer-on-proxmox-or-preventing-a-kemp-loadmaster-boot-loop/). And I thought to leave his helpful last remarks here:
>> "While the free version of Kemp’s LoadMaster does limit the bandwidth to 20mbps, it’s quite sufficient for a lab environment. If you need something without the limitations and can’t afford (or don’t need) the LoadMaster Commercial version, or if you would just prefer to go with an open-source solution, [HAProxy](https://www.haproxy.org/) would be the tool of choice."

## RDP to VM via Cloudflare Tunnel
One great use-case of Cloudflare Tunnel is [Remote Desktop connection](https://developers.cloudflare.com/cloudflare-one/connections/connect-apps/use_cases/rdp/).
- iOS RDP options:
 - [Jump Desktop](https://jumpdesktop.com/), supports RD Gateway.
 - [RDP Lite](https://apps.apple.com/us/app/remote-desktop-rdp-lite/id288362576), supports traditional RDP. See the [connection steps](how-to-connect) below.
 - [Microsoft Moble RDP](https://apps.apple.com/us/app/microsoft-remote-desktop/id714464092)
 - [AnyDesk](https://apps.apple.com/us/app/anydesk-remote-desktop/id1176131273?platform=ipad), a client-server VNC.

#### How to Connect
After you’ve configured a published service on the VM, you can use an iOS app to connect to the VM over RDP. There are a number of RDP apps for iOS. To illustrate how these work, this example uses RDP Lite. RDP Lite contains all the functionality necessary to connect to a VM with standard RDP.

- Launch the RDP Lite app, and tap Add another PC in the left-hand menu. In the Configure tab, tap New to enter settings for this connection:RDPlite configuration
- In PC Address, enter the published services URL (such as “services-uswest.skytap.com”).
- In PC Port, use the port listed at the end of the public address generated by the VM published service (so if the public address was `[UUID].[yourdomain]:12345` you’d enter 12345).
- Enter the PC User name and PC Password for guest OS account you’re logging into.
- Tap Connect on the left-hand side and select your new connection.
- An RDP window opens and prompts you to login to the virtual machine guest OS. You’re now connected to the VM.

## Access an SMB drive through Cloudflare Tunnel
The ability to set up a [secure, public SMB drive](https://developers.cloudflare.com/cloudflare-one/connections/connect-apps/use_cases/smb/) is a powerful file sharing tool. Usually, firewalls and ISPs block SMB file shares, but Cloudflare fixes that problem! With Cloudflare Tunnel, you can provide secure and simple SMB access to users outside of your network. The [cloudflared client](https://developers.cloudflare.com/cloudflare-one/connections/connect-apps/install-and-setup/installation/) to both the server and any machine you wish to access the SMB file share.

#### Connect SMB Server to Cloudflare
> Note: Guest access to [SMB2 and SMB3 are disabled by default on Windows](https://learn.microsoft.com/en-us/troubleshoot/windows-server/networking/guest-access-in-smb2-is-disabled-by-default) machines, but since Cloudflare requires a sign-on to access the SMB share, this should not be an issue. 
- Create a Cloudflared Tunnel by following [this Cloudflare doc](https://developers.cloudflare.com/cloudflare-one/connections/connect-apps/install-and-setup/tunnel-guide/remote/)
- In the Public Hostnames tab, choose a domain from the drop-down menu and specify any subdomain (for example, smb.example.com).
- For Service, select _TCP_ and enter the SMB listening port (for example, localhost:445). SMB drives listen on port `139` or `445` by default.
- Select Save hostname.

#### Connect to SMB Server
- Install [cloudflared](https://developers.cloudflare.com/cloudflare-one/connections/connect-apps/install-and-setup/installation/) on the client machine.
- (Recommended) Add a self-hosted application to Cloudflare Access in order to manage access to your server.
- Run the following command to open an SMB listening port. You can specify any available port on the client machine. `cloudflared access tcp --hostname smb.example.com --url localhost:8445`
- This command can be wrapped as a desktop shortcut so that end users do not need to use the command line.
- [Open your SMB client](https://developers.cloudflare.com/cloudflare-one/connections/connect-apps/use_cases/smb/#3-connect-as-a-user) and configure the client to point to `smb://localhost:8445/sambashare`. Do not input the hostname.
- Sign in with the username and password created while setting up the server.
- (Recommended) Add a [self-hosted application](https://developers.cloudflare.com/cloudflare-one/applications/configure-apps/self-hosted-apps/) to Cloudflare Access in order to manage access to your server.

##### Windows-specific requirements
If you are using a Windows machine and cannot specify the port for SMB, you might need to disable the local server. The local server on a client machine uses the same default port `445` for CIFS/SMB. By listening on that port, the local server can block the `cloudflare access` connection.

> The Windows Server service supports share actions over a network like file, print, and named-pipe. Disabling this service can cause those actions to fail to start.
To disable the local server on a Windows machine:

- Select Win+R to open the Run window.
- Type `services.msc` and select Enter.
- Locate the local server process, likely called `Server`.
- Stop the service and set Startup type to _Disabled_.
- Repeat steps 3 and 4 for `TCP/IP NetBIOS Helper`.
