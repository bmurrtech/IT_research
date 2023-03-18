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

## Creating VMs and Containers

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

### Create Templates

> About Creating Containers: You can also create Docker-like containers with ProxMox by downloading Linux container ISOs and uploading them to ProxMox, and then click on the `Create CT` blue button (right next to the `Create VM` button). The process for creating containers is the same as creating VMs.

## Reverse Proxy DDNS

#### Cloudflare DDNS Reverse Proxy
- Instead of setting up Tailscale or enduring the ardous process of installing an enterprise-grade load-balancer like Kemp, you can get a DDNS and reverse proxy setup via CloudFlare in 15 minutes.
- [NetworkChuck made a video tutorial](https://www.youtube.com/watch?v=ey4u7OUAF3c) about this, but here's the steps:
- Buy a domain and create a Cloudflare Nameserver (DNS > Records > Nameservers).
- Copy the nameservers and add them to your domain registrar (nameserver updates can take up to 24hrs, but it is usually updated within minutes).
- Using [ZeroTrust](https://one.dash.cloudflare.com/899e8be9fba8f3cc125ebdf9263380e0/home/quick-start) create a new tunnel: [ZeroTrust](https://i.imgur.com/FipaEgQ.png) (left navigation pane) > Cloudflare ZeroTrust (navigation pane) > Access (dropdown) > [Tunnels](https://i.imgur.com/nnONYTE.png) > Create at tunnel (button)
 - Enter the domain name you created...

[zero_trust](https://i.imgur.com/FipaEgQ.png)
[ztunnels](https://i.imgur.com/nnONYTE.png)

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
