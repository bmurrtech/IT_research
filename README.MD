## <span id="h.jam6jg2d41m4">BizTech New IT Hire Documentation & Reference Guide</span>

## <span id="h.qt9lysx9sp59">List of Helpful Onsite IT Tools</span>


-HDMI Cable


-Portable monitor


-Mouse & keyboard


-Ethernet checker


-Ethernet cables


-Network switch


-Power strip with extension cord


-Box opener or pocket knife


-Screwdriver set


-Powered small drill (with bit set)


-USB-C to USB-A


-VGA to HDMI adapter


-(Skinny) USB stick w/ RMM & Screenshare


-Sticky notes (for client notes)

## <span id="h.7eii4vwjpe6i">Multi Brave Profiles (for more bookmarks)</span>

### <span id="h.15f1ianodein">Brave Sync</span>


Using the Brave "Sync" function, you can create multiple profiles and use keyboard shortcuts to change profiles.

### <span id="h.n61bgq468af4">Profile Switching Hotkeys</span>


Type in `CTRL +``Shift``+ M` to open the profile menu. From there, you can use the UP & DOWN arrow keys to select the profile you want to open and press `ENTER`.


\*Find server in N-Central (make sure it is a server before remoting on)


\*Click the TakeControl button (green with monitor icon)


\*Once in, click on the "Remote Desktop" dropdown menu, and click "Send <span style='color:rgb(255, 255, 255);background-color:rgb(51, 51, 51)'>CTRL + ALT +</span> <span style='color:rgb(255, 255, 170);background-color:rgb(51, 51, 51)'>DEL</span>" and this will unlock the server to enter the login credentials


\*Logon to ITGlue > navigate to the client’s profile (i.e. Health Solutions Network) > Passwords (see left-side pane) > look for "SLT Admin" creds from the list > copy (<span style='color:rgb(255, 255, 255);background-color:rgb(51, 51, 51)'>CTRL +</span> <span style='color:rgb(252, 194, 140);background-color:rgb(51, 51, 51)'>C</span>) the password > paste it into password field inside the remote session on the server (<span style='color:rgb(255, 255, 170);background-color:rgb(51, 51, 51)'>CTRL</span> <span style='color:rgb(255, 255, 255);background-color:rgb(51, 51, 51)'>+ V</span> will not work, use <span style='color:rgb(255, 255, 255);background-color:rgb(51, 51, 51)'>CTRL +</span> <span style='color:rgb(255, 255, 170);background-color:rgb(51, 51, 51)'>SHIFT</span> <span style='color:rgb(255, 255, 255);background-color:rgb(51, 51, 51)'>+ X</span>) > logon

### <span id="h.249quuyjnvtz">Locked Out of Login | Sign-in | Too Many Attempts</span>


> RMM > Client > Actions > Domain User Management > Click on the domain (i.e. ASH.local) > Wait for list to populate > Scroll until you find enduser (i.e. bts_admin) and click check box > Click "ENABLE'' button at the top of screen

### <span id="h.s9rlkg6ynhbq">ScreenConnect Backstage</span>


\*Go to [https://biztech.screenconnect.com/](https://biztech.screenconnect.com/)


\*Click on "Connect with Office365"


\*Click on Access


\*Search for the endpoint


\*Right-click the name of the endpoint


\*Select "Join with Options"


\*Select [Backstage] & click "Join Session" to endpoint, then wait for screenconnect to load up

### <span id="h.y34gswfmu2ws">Fix TakeControl Not Working on Endpoint (Server)</span>


<span style='color:rgb(33, 33, 33)'>Source:</span> [https://success.n-able.com/kb/solarwinds_n-central/How-to-clean-re-install-the-Take-Control-agent-on-N-central](https://success.n-able.com/kb/solarwinds_n-central/How-to-clean-re-install-the-Take-Control-agent-on-N-central)


<span style='color:rgb(33, 33, 33)'>(Note: the CLI commands do not seem to work)</span>


<span style='color:rgb(33, 33, 33)'>In order to access the endpoint, you must remote on to the VM/Server through the Domain Controller ("DC"). But before that, you need to stop RMM from trying to automatically install TakeControl (BeAnywhere).</span>

#### <span id="h.8i4vjbt99h3b">Disabling Automatic TakeControl Installation:</span>


<span style='color:rgb(33, 33, 33)'>-Access the endpoint in RMM</span>


<span style='color:rgb(33, 33, 33)'>-Uncheck "Install Take Control" (Remote Control Settings > General) and "Save"</span>


<span style='color:rgb(33, 33, 33)'>-Click the "Add Task" dropdown and click "Update Asset Info" to force the RMM to push the changes and stop trying to install</span>


<span style='color:rgb(33, 33, 33)'>-Check the processes (Tools > Processes) for anything that has "BA" in the name (this is the Be Anywhere TakeControl application) and kill all those processes.</span>


<span style='color:rgb(33, 33, 33)'>-Now, you must remote onto the server and manually delete the remnant files which are preventing TakeControl from installing.</span>


<span style='color:rgb(33, 33, 33)'>-How do you access a server without TakeControl? You can access it through the DC which can access the VMWare ESX host which hosts the VM/server (see below).</span>

#### <span id="h.bfrp10uvd4ez">How to Access VM/Server when TakeControl is Down:</span>


<span style='color:rgb(33, 33, 33)'>-Find the company’s DC (>RMM > Company > Search for "DC" > Launch Remote Control)</span>


<span style='color:rgb(33, 33, 33)'>-Remote onto DC (>Remote Desktop > Send CTRL + SHIFT + DELETE)</span>


<span style='color:rgb(33, 33, 33)'>-Locate login credentials in ITGlue (Company > Passwords > SLT Doman Admin) and login.</span>


<span style='color:rgb(33, 33, 33)'>-Enter the IP address of the VMWare ESX host and login (search ITGlue for "VMWare" or "ESX" root access credentials to log into the ESX host).</span>


<span style='color:rgb(33, 33, 33)'>-Once logged into VMWare ESX, click on anything that resembles "Virtual Machines" from the navigation menu, and look for the name of the endpoint.</span>


<span style='color:rgb(33, 33, 33)'>-Launch a web console to remote onto this device (note: you cannot use paste features for credentials, therefore, you will have to manually enter the creds to login to the endpoint).</span>

#### <span id="h.82dta7djapr4">Delete All Remnants of BeAnywhere Files</span>


<span style='color:rgb(33, 33, 33)'>These remnants "BA" files can be located in the following directories:</span>


If existing, delete the ProgramData folder and the BA Agent folder respectively:


C:\ProgramData\GetSupportService_N-Central


C:\Program Files (x86)\BeAnywhere Support Express\GetSupportService_N-Central


Delete anything with the name "BA" in it otherwise, the new installation will fail (for some reason it fails to overwrite these corrupted files, and needs to write new ones to install properly).

#### <span id="h.f1b3u01x1c2">Reinstall TakeControl</span>


-After you have successfully, manually deleted all the BA Agent files, you can now re-enable the  <span style='color:rgb(33, 33, 33)'>"Install Take Control" (Remote Control Settings > General) and "Save" within the RMM of the endpoint without TakeControl.</span>


<span style='color:rgb(33, 33, 33)'>-Again, click the "Add Task" dropdown and click "Update Asset Info" to force the RMM to push the changes and reinstall the TakeControl agent.</span>

### <span id="h.dl91m03mhw29">File Transfer Process</span>


\*Go to [https://ncentral.biztech.io/](https://ncentral.biztech.io/)


\*Search for the endpoint


\*Click on the name


\*Click on "Tools" tab within the N-central endpoint screen


\*Navigate to file transfer


\*Send the file to the endpoint folder of your choice (ideally `<span style='color:rgb(255, 255, 255);background-color:rgb(51, 51, 51)'>C:/Windows/System32/Temp</span>`)


\*Now go to [Backstage](undefined) from Screen Connect (alternatively you can use the command prompt tool within N-Central, but it is buggy and unreliable)

### <span id="h.cvzn75y1o74n">Server Restart Procedure</span>


\*Go ScreenConnect portal: [https://biztechhelp.me](https://biztechhelp.me)


\*Check activity of endpoints


\*\*If user is listed, check the idle status. If idle status is > 3 days, it may be safe to do a remote restart without disrupting the user’s work.


> Note: If enduser RDP’s into an idle endpoint, the ScreenConnect


\*If the it is an application server/important/critical (app, database, SQL, webserver, file server, etc.), we must contact the primary contact of the company before restarting.


\*\*If no response from the primary contact person, contact the AM to see who to contact.

### <span id="h.9q6g0nggz7j">Check if Server Is Critical Service before Restart</span>


\*Using N-Central, navigate to tools > applications and search for applications in question (use search engine for applications you are unsure about)


\*TakeControl to remote onto the server (no enduser permission needed for servers) right click start or search for "computer management" > shared folders > shares > check the "Client Connection" column to check if any enduser is actively using the share files


\*If you determine that the server is critical, reach out to the primary contact and suggest a time to restart after business hours, but double-check with the client offer 2 options:


\*\*1. "I can schedule an automated restart of the server after hours at 3AM. Let me know if this is okay with you."


> If you notice that the last time the server has been restarted is > 15 days, only offer the manual restart option because of a higher potential of reboot failure.


\*\*2. "If you are concerned about rebooting properly, I can remote on [insert ideal after hour time for me] to perform a manual restart to ensure that the server restarts and is fully operational. Please note: this manual restart option will be billed outside of the agreement and incur after hours expense. Are you okay with additional fees for this option?"

### <span id="h.cv50qwjlatbm">Check if Server Is Print Server</span>


\*Search for "Print Management" from the list of applications


\*\*If it has printers listed, do NOT restart because enduser needs access. Need to check with client to see when we can restart.


\*\*If primary contact gives us an after hour time to perform restart, see NOC Lead for automation script.

## <span id="h.pbdvon71izdi">Antivirus AV Defender</span>

### <span id="h.cx8wwqw3y5wz">Uninstall/Re-install AV Defender</span>


 1. Determine if AVD is corrupted (i.e. AVD error which reads: "failed to evaluate profile and apply result")
 2. Turn off Security Manager for a moment: RMM > Company > Endpoint > Settings > Security Manager > Uncheck the "Enable Security Manager" box
     1. If you skip this step, the RMM will try to install AVD before you get a chance to run the AVD cleaner script.
    
 3. Uninstall AVD from endpoint: RMM > Company > Endpoint > Settings > Custom Properties > Change (BTS) AV Defender Status from "CLIENT DEFAULT" to "UNINSTALL"
 4. Allow the uninstall to run and refresh the Overview status until AVD Status has changed (i.e. "AVD not installed")
 5. Run AVD Cleanup Protocol: RMM > Company > Endpoint > Tools > Task Execution > Type Dropdown change to "Scripting" > Select: Invoke-AVDCleanupRoutine
     1. As safe measure, can run the following PS script to remove AVD file/folder remnants (if the clean up protocol in the RMM did not work):
    

```
del "C:\Program Files(x86)\N-able Technologies\Windows Agent\AVDefender"
del "C:\Program Files\N-able Technologies\AVDefender"
del "C:\ProgramData\N-Able Technologies"

powershell -command "Restart-Service 'Windows Agent Service' -Force"
```


 1. Also need to clear the registry 


 1. Re-enable Security Manager: RMM > Company > Endpoint > Settings > Security Manager > Re-check the "Enable Security Manager" box
 2. Re-install AVD: RMM > Company > Endpoint > Settings > Custom Properties > Change (BTS) AV Defender Status from "CLIENT DEFAULT" to "UNINSTALL"
 3. Invoke a Reboot for AVD re-install to fully complete: RMM > Company > Endpoint > Tools > Task Execution > Type: Automation Policy (dropdown) > Repository Item (dropdown) and select: "Invoke-RestartOrShutdownOnDateTime" > Set to 3:00 (or ask enduser when can reboot) > Enter Gitlab API Token (select BTS Gitlab API Token from dropdown) > Run
 4. Check back the next day to see if AVD was properly reinstalled (you should get a changed AVD status indicating the installation process is in progress if everything was executed properly and this is a standard AVD issue).


Note: If all else fails, you can follow N-Central’s guide to uninstall, clean, and reinstall AV Defender on endpoint by following the instructions provided here: 


 1. <span style='color:rgb(33, 33, 33)'>Manual AVD Uninstall</span> [https://documentation.n-able.com/N-central/troubleshooting/Content/kb/N-Central-How-to-remove-and-reinstall-AV-Defender.htm](https://documentation.n-able.com/N-central/troubleshooting/Content/kb/N-Central-How-to-remove-and-reinstall-AV-Defender.htm)
 2. <span style='color:rgb(33, 33, 33)'>AVD Cleaner Tool Download</span> [https://success.n-able.com/kb/nable_n-central/Where-to-download-the-latest-AV-Defender-removal-tool](https://success.n-able.com/kb/nable_n-central/Where-to-download-the-latest-AV-Defender-removal-tool)

### <span id="h.6kw23yioo9s8">Submit Ticket | Vendor Contact (N-Central Support)</span>


-Refer to ITG documentation: [https://biztech.itglue.com/2728430/docs/7456042#version=published&documentMode=view](https://biztech.itglue.com/2728430/docs/7456042#version=published&documentMode=view)


-Go to the N-Central support portal: [https://success.n-able.com/](https://success.n-able.com/)


-Click on the "Need Assistance" button and open a new ticket


-N-Central needs some information to provide support. You will need to enter the following information in the required fields:


<b>Product</b>:  N-able N-Central


<b>Category</b>:  <Whatever is most applicable, AV Defender, Patching, etc>


<b>Subject</b>:  <Subject of ticket>


<b>Description</b>:  <Description of problem>


<b>Severity</b>:  <Typically "Normal", if not you should call-in>


<b>Version</b>:  <This can be found within the RMM by clicking on "Help" in the bottom-left corner and then choose "Version Information">

![](https://lh5.googleusercontent.com/Khoykhc4ka1W4IC4lY1kKeV9GQS1ncx43YDwo-GmCxnowmFTQ9wBw2LZg0LSuFLDREsNmjGvAebfeG3yoY6ZZFMyxC5Z-Fp72Yx2Qv3lxrNzf_q17GJNX0WuhvmduzrDX2KdqwKvpjNXuPbr-w-1bqta5RdidChcYOuQY_rwvJaArKA4pzjokYDfpZIfwNSA7WMroRU "")

![](https://lh4.googleusercontent.com/1D4x1hkoDzh9Fi1ZaNkKxkvkM7UBv9sQUuMP17YvVLX3Mke2yQ9xGjaoxuviqq1aNjtT30z-kC1UXzpqwbvohwX6wb4hSQwBwfbDtD9UBe8PAe_UQBiRtTxA-3mr_Dr9r7uqnr6pS4E4Kp5D-Dv-eim4VumYkIe99OWAkHXO3x00uHGb8B8y8D8-J-Ws3VqfwdTB-rA "")


<b>Customer Name</b>:  <Name of client from upper-left corner>


<b>Device Name</b>:  <Name of the workstation/server you're working on>


<b>N-Central Server Name</b>: ncentral.biztech.io

### <span id="h.plfjf8exvrz4">Submit Ticket with Corvid (Sentinel One | S1)</span>


 1. Go to Corvid’s Zendesk portal and login [https://corvidcd.zendesk.com/hc/en-us/](https://corvidcd.zendesk.com/hc/en-us/)
     1. Login credentials can be found in ITG > BizTech > Passwords > "[Corvid Support Account](https://biztech.itglue.com/2728430/passwords/12188337)"
     2. Additional vendor contact info can be found at ITG > BizTech > Vendors > [Corvid](https://biztech.itglue.com/2728430/assets/85349-vendors/records/17969773)
    
 2. Create a new ticket by clicking "Submit a request"

![](https://lh5.googleusercontent.com/8oI1o3HBJ0-3KnoeVTFbWGSZ0aJBqOFXNRlLYFCXlYgiiikXwqof_LPQ9ow2o3EQXqE_uWOXvty8WZE5x2X1v_UcTqVisNRUWSd7s1FSNQ65CcLFYgqSCGx1pGX2dxPSLI9Ixb2ACZTQicGd4EByZ4XurNG8pIYwYN5FvjhhdsLlXESMCoIVZHuepTvgkdrFWsV3Kc4 "")


 1. Enter a subject (it is helpful to reference the ticket #, name of endpoint, & short description)
 2. Enter a priority level (low, normal ~8hr response, high ~4hr response, urgent ~20m response) appropriate for the situation
 3. Compose a message to the vendor (describe the issue as reported by the AV status error in detail and ask for steps to resolve)
 4. (Optional) Attache any logs/screenshots/files for support team to reference

### <span id="h.6tgcv2ghv6wi">Run AV Scan via CMD & Backstage</span>


Source (for more commands and options): [https://www.bitdefender.com/business/support/en/77209-36849-using-the-command-line-interface.html](https://www.bitdefender.com/business/support/en/77209-36849-using-the-command-line-interface.html)


Typically, you can run the AV scan through the RMM (Add Task > Security Manager Scan > Run an AV Defender Full Scan), however, if the RMM is not executing and the job shows as "pending" you can always use Backstage to run a scan on the C:/ drive.


<span style='background-color:rgb(244, 204, 204)'>WARNING</span>: This action will be resource intensive, take a while to complete ( 20+ minutes), and <span style='background-color:rgb(255, 255, 170)'>will cause the enduser's endpoint to slow down dramatically</span>. Therefore it is best to run this command while the enduser is away or put the scan into low priority mode (see below).


<span style='color:rgb(33, 33, 33)'>cd to: > C:/ > Program Files > N-Able Technologies > AVDefender ></span> <span style='color:rgb(33, 33, 33)'><b>product.console.exe</b></span>


<span style='color:rgb(33, 33, 33)'>To run system scan type:</span>

```
FileScan.OnDemand.RunScanTask custom path="C:\Program Files"
```


<span style='color:rgb(33, 33, 33)'>To set</span> <span style='color:rgb(33, 33, 33)'><ins>low priority scan</ins></span><span style='color:rgb(33, 33, 33)'>, add the following string:</span>


<span style='color:rgb(255, 255, 255);background-color:rgb(51, 51, 51)'>lowPriority=true|false</span> <span style='color:rgb(33, 33, 33)'>(default value is false)</span>


<span style='color:rgb(33, 33, 33)'>Example:</span>

```
FileScan.OnDemand.RunScanTask custom lowPriority=true path="C:\Program Files"
```


<span style='color:rgb(33, 33, 33);background-color:rgb(255, 255, 255)'>If you just scan</span> `path="C:\Program Files"` <span style='color:rgb(33, 33, 33);background-color:rgb(255, 255, 255)'>the AV no-scan in X amount of days status will be cleared. However, if you wish to scan multiple paths (i.e. more than one disk drive) add:</span>

```
path="<path1>" path="<path2>"
```


You can check the endpoints mounted drives via RMM > Endpoint > Tools > File System (see screenshot)

![](https://lh3.googleusercontent.com/wwgEfZeH5K1pj0Fg-5UxsI_L_7AYQMM52L0vdTEde_K__yGkE3fCSPsLxhHv_JS8Bt5A8EMZ2Ixm8sZ2DIHkDL7J3rH9F1aBor6KvSncvrC4YvhLjlQ62cIroBBMyg2pxktt54yCwk-Kw0RA_LzLEAqehkTwEn9noP7f4wg8BINateGcoehige0WK62GoN3LyioaPow "")


Example:

```
FileScan.OnDemand.RunScanTask custom path="C:\" path="D:\" path="E:\"
```

### <span id="h.17oxc61w6sdi">Third-party Antivirus Install Detected Error</span>


To fix this error, try to first uninstall the AVG using automation scripts.


RMM > Endpoint > Tools > Task Execution > Select "Uninstall AVG" from the "Repository Item" dropdown menu (see image below).

![](https://lh3.googleusercontent.com/n9cVZgoG2PnUCNJDSIxLKFimoSK8QBoqH0lyRf6sw1ak5oO-cy7Nz8Q5e4A40VdCdoL6vF4zNuSjImOweYXF43Ojh11iR2u0runzONau_ZQbpKrpzsnBPKU7MFPb-plQHjIOcuQDDfDQOkVfn6kSz_jg31PmWVIvAz54kJCWF5YHq51A800GG07yWJYJa_GygsDbhh0 "")


If this fails (even if the status shows "Success"), then you need to change some additional settings.


To change the "Competitor AV Cleanup" to "No Removal"


RMM >  > Endpoint > Settings > Security Manager > ""Competitor AV Cleanup" change dropdown menu to "No Removal"


Give the endpoint some time to see if this automatically resolves the issue.

### <span id="h.cwetwrnm9gqw">Run a AV Defender Scan</span>


<span style='color:rgb(33, 33, 33)'>-If endpoint is showing a "failed" AV status (hover over the AV status to see popup) due to no scan within the last X amount of days (i.e. 30d), then you need to run a scan on the endpoint.</span>

![](https://lh3.googleusercontent.com/9jDmSt-njtldyerbvbmV9jO4VEbI-Ex5smagn_rW2woTD0dJkJLrO9ST51mJs-XH65rwse9KNq3ozWghmg7_gAR5DR7NDW4NKfKP794Stnt4d54wf3uszD_Gw8eUuQtnUz9HpduZeO3y8ymza1oiRSJ7W1gUwKpIymT4YjAipBmEvkz5N4Li-JlUT8mZv5Qmszu7b4w "")


<span style='color:rgb(33, 33, 33)'>-You can check the scan log to see when the last scan was performed: RMM Tool > Monitoring > Security Events > Scan Log</span>

![](https://lh4.googleusercontent.com/OdGlUdLp7cialB1JTsKrXd3ZbQma2qD4ED7QM3-m4O7p3H8CjBo4DKtwvqFG11Wb7CMyuSWG7IeRhsWoYNG--AlUQ0qvdMkhS3NEgJkBEX4wMWE8Z01EDcm9bOu6DRo49SDQmjcSNnCIyCofCzNOwldLsLeJ3G2ZR6XiL7u6iERWV3aJMzV41kx2g3EE5Hvz2Dgz4Oo "")


<span style='color:rgb(33, 33, 33)'>-First check if the end user is actively using or not as the scan can affect performance and slow the PC and can potentially cause customer complaints and new tickets.</span>


<span style='color:rgb(33, 33, 33)'>-Use N-Central RMM tool to run a scan: N-Central RMM > Company > Endpoint > Add Task [top right corner dropdown] > Security Manager Scan > Run AV Defender...Scan</span>


<span style='color:rgb(33, 33, 33);background-color:rgb(255, 255, 170)'>FUNCTIONALITY NOTE: The AV scan option is not available in RMM unless navigated into the company-specific filter (i.e. cannot execute scans from BizTech overview).</span>


<span style='color:rgb(33, 33, 33)'>-You will be taken to a new screen. Check under the "Targets" tab that the correct endpoint is selected (under "Selected Devices")</span>


<span style='color:rgb(33, 33, 33)'>-Click on the "Schedule" tab and check that the type is set to "Now" from the dropdown menu. Alternatively, if the enduser is actively using the PC, you can edit the parameters to try a scan at another time if it fails.</span>


<span style='color:rgb(33, 33, 33)'>-If all the parameters are set, click the green "Save" button and it will queue up the task to execute a scan.</span>


<span style='color:rgb(33, 33, 33)'><b>Tip</b></span><span style='color:rgb(33, 33, 33)'>: You can have the RMM system email you upon completion of a successful scan. Click on the "Notifications" tab and then add your name/email to the "Selected Recipients" column.</span>

### <span id="h.i7qc4s5r8gd7">Outdated Agent Status</span>


<span style='color:rgb(33, 33, 33)'>If Agent is outdated (i.e. 2022.2.0.77), then check the settings to see if updates have been set to "Always" or not. If not, this must be changed as it is sometimes set to "Now" which will not update the agent.</span>


<span style='color:rgb(33, 33, 33)'>To change this go to:</span>


<span style='color:rgb(33, 33, 33)'>RMM > Endpoint > Settings > Local Agent > Change "Update new version" dropdown to "Always" and make sure to hit the SAVE button.</span>

### <span id="h.5uyp4cwtoa0d">Removal of Agent/Probe on Windows (Disable RMM Tickets Spawning)</span>


<span style='color:rgb(33, 33, 33)'>Source:</span> [https://documentation.n-able.com/N-central/troubleshooting/Content/kb/Manual-Removal-of-the-Agent-Probe-on-Windows.htm](https://documentation.n-able.com/N-central/troubleshooting/Content/kb/Manual-Removal-of-the-Agent-Probe-on-Windows.htm)

### <span id="h.4irhejx18hw7">Prevent Laptops from Sleeping</span>


You need to disable the when lid closes to "do nothing" therefore, you can change it manually (see below) or run this batch file.

```
@echo off 

for /f "tokens=4 delims= " %%i IN ('powercfg -q ^| find "Power Scheme GUID:"') do Set StrOne=%%i

for /f "tokens=3 delims= " %%i IN ('powercfg -q ^| find "(Power buttons and lid)"') do Set StrTwo=%%i

for /f "tokens=4 delims= " %%i IN ('powercfg -q ^| find "(Lid close action)"') do Set StrThree=%%i

powercfg -SETACVALUEINDEX %StrOne% %StrTwo% %StrThree% 000
```


Note: You need to change %%i to %i if trying to run these commands directly in a command prompt (outside of a batch).


If you want to run a script on-demand, you can use File Explorer or Command Prompt. To run a script file with Command Prompt on Windows 10, use these steps:


 1. Open Start.
 2. Search for Command Prompt, right-click the top result, and select the Run as administrator option.
 3. CD to the file path of the .bat file
 4. Type out the full name of the .bat file (ex. C:\PATH\TO\FOLDER\nosleep.bat)


<span style='color:rgb(33, 24, 60)'><b>Source</b></span><span style='color:rgb(33, 24, 60)'>:</span> [https://www.windows10compatible.com/blog/how-to-configure-windows-10-action-when-laptop-lid-is-closed/](https://www.windows10compatible.com/blog/how-to-configure-windows-10-action-when-laptop-lid-is-closed/)


<b>Do nothing</b> – When you choose this option Windows doesn’t do anything when you close the laptop’s lid.


In order to configure your preferred Windows 10 action when you close your laptop’s lid you must follow the steps given below:


 1. Sign-in to your Windows 10 computer with your account.
 2. Right-click the Start button from the desktop window.
 3. Click <b>Power Options</b> from the context menu that appears.


 1. On the <b>Power Options</b> window from the left pane click <b>Choose what closing the lid does</b>.


 1. From the <b>System Settings</b> window from under the <b>Power and sleep buttons and lid settings</b> section from the <b>When I close the lid</b> drop-down lists under the <b>On battery</b> and <b>Plugged in</b> columns choose your preferred Windows’ action when you close your laptop’s lid.


 1. Once selected click the <b>Save changes</b> button from the bottom.


 1. Close all the opened windows and boxes.
 2. Run the command prompt to ensure the laptop will not sleep when plugged into power


REM Disabling all Sleep Parameters

```
 @echo off 

powercfg /x -hibernate-timeout-ac 0

powercfg /x -hibernate-timeout-dc 0

powercfg /x -disk-timeout-ac 0

powercfg /x -disk-timeout-dc 0

powercfg /x -monitor-timeout-ac 0

powercfg /x -monitor-timeout-dc 0

powercfg /x -standby-timeout-ac 0

powercfg /x -standby-timeout-dc 0

Pause
```

| <span style='color:rgb(255, 255, 255);background-color:rgb(51, 51, 51)'>powercfg -x -standby-timeout-ac 0</span> |
| ---------------------------------------------------------------------------------------------------------------- |



(somehow the switch <span style='color:rgb(255, 255, 255);background-color:rgb(51, 51, 51)'>-x</span> doesn't work for me so I've changed it to <span style='color:rgb(255, 255, 255);background-color:rgb(51, 51, 51)'>/x</span> and it works. the rest of the switches stay -standby-timeout-ac)


As shown on Microsoft's Technet page "Powercfg Command-Line Options" (https://technet.microsoft.com/en-us/library/cc748940(v=ws.10).aspx), the command is:


> powercfg -x setting value (the value you're looking at is "standby")


therefore: > powercfg -x -standby-timeout-ac minutes (disable = 0 minutes)


NOTE: ac = connected to electric power / dc = works on battery (so if you want to disable sleep mode while working on battery power, replace the "ac" with "dc" in the command, so it will look like <span style='color:rgb(255, 255, 255);background-color:rgb(51, 51, 51)'>powercfg -x -standby-timeout-dc 0</span>)

## <span id="h.agxrpep75di">DNS Filter Status</span>

### <span id="h.pc94hj59li7w">Troubleshooting DNS</span>


First go through the <i>things to check</i> in this SOP: [https://biztech.itglue.com/2728430/docs/10769420](https://biztech.itglue.com/2728430/docs/10769420)


Note: If determined that the endpoint does not support DNS Filtering (i.e. non-Intel/AMD CPU or Windows 8.1 and older [only Windows 10 and newer is supported]), then you must drill down to the company-specific level in the RMM to turn off DNS. Otherwise, the toggle switch is grayed out.


 1. Check if the device class is set/classified as "workstation" (i.e. laptop or desktop).
     1. RMM > Endpoint > Settings > Properties > Check "Device Class"
     2. If endpoint is classified as "desktop/laptop" then proceed to check other settings.
    
 2. Check if DNS rules are in place:
     1.  Via RMM > Endpoint > Monitoring > Associations > Rules (scroll down) > (BTS) Deploy-NAbleDNSFilter - Enable (SLT Default)
    
 3. If DNS rule is listed, check that the "Enable DNS Filtering" toggle is ON:
     1. Via RMM > Endpoint > Settings > DNS Filtering
    
 4. Check if "DNS Agent" is installed
     1. RMM > Endpoint > Asset > Applications (or if the endpoint is online…)
     2. RMM > Endpoint > Tools > Applications > "DNS Agent"
     3.  If it is not listed in RMM, you can confirm that DNS is not installed by:
         1. Remoting on to the endpoint hit
         2. `WIN``+``R` to open the Run app
         3. Type:`appwiz.cpl`
         4. Alternatively, you can get to the same screen via Control Panel > Programs > Programs and Features.
         5. Then check for DNS in the list to see if it is installed or not
        
    

![](https://lh4.googleusercontent.com/eQ3OuuXciDd2m9PUIX87o3EbG4QGfrucGNp9EqQgpYjrrCF3sh1ElBNtR1uq4ycxLFyeR5R7ps3_bViZkM8QjGLCA3NtuhYzmCYwXBjWMvQnnndUZlqeUad1VsivE6zCiq4e_6eWIsU7lXISMMXOyo6s3PuZ78ZAFhEyIlYeLvcm7m3jtDOukYPEWIBBqyQRqaEKAwc "")

### <span id="h.7pkfcra787zu">Reinstall DNS Agent</span>


If all the rules and settings are set correctly and DNS Agent is still not installing automatically then a manual DNS clear/flush is required (not the same as CLI DNS flush command). There are two ways to reinstall the DNS agent; A) Via RMM Task Execution or B) Backstage and PowerShell (see below).


<b>Option A (Via RMM)</b>


 1. Navigate to RMM > Endpoint > Tools > Task Execution
 2. Find the dropdown option that says <span style='color:rgb(33, 33, 33);background-color:rgb(255, 255, 255)'>"remediationfor"</span>
 3. <span style='color:rgb(33, 33, 33);background-color:rgb(255, 255, 255)'>Scroll down and select # associated with DNS clearing PS code (TBD, see NOC Lead)</span>
 4. <span style='color:rgb(33, 33, 33);background-color:rgb(255, 255, 255)'>Hit Run</span>


<span style='color:rgb(33, 33, 33);background-color:rgb(255, 255, 255)'><b>Option B (Backstage PowerShell)</b></span>


Run the following script in PowerShell:

```
del "C:\program files (x86)\N-Able Technologies\Windows Agent\Config\ExecutionerConfig.xml"
del "C:\program files (x86)\N-Able Technologies\Windows Agent\Config\ExecutionerConfig.xml.backup"
del "C:\ProgramData\SolarWinds MSP\Ecosystem Agent\Config\EcocutionerConfig.xml"
del "C:\ProgramData\SolarWinds MSP\Ecosystem Agent\Config\EcocutionerConfig.xml.backup"
sc delete "EcosystemAgent"
sc delete "EcosystemAgentMaintenance"
powershell -command "Restart-Service 'Windows Agent Service' -Force"
```

## <span id="h.5kqnf3h88a75">Restarts/Reboots</span>

### <span id="h.o2vvll3uqooz">Reboot Automation</span>


Refer to: [https://biztech.itglue.com/2728430/docs/6491230](https://biztech.itglue.com/2728430/docs/6491230)


Additionally, check the rules for that particular endpoint to see if reboot rules are in force or not. RMM > Endpoint > Settings > Custom Properties > Search for "(BTS) Reboot Status" > Check if "Value" is set to "Client Default"


Note: If the endpoint is see to anything other than "Client Default" then reboots should happen automatically as determined by RMM rules set by NOC Lead. If it is set to anything else, do not change it without first checking the "Notes" and consulting with NOC Lead. there could be a valid reason for reboots not being enabled on servers (i.e. client does not want server to reboot ever).

### <span id="h.gpfe96h04fs5">Boot in Safe Mode on a Server</span>


<span style='background-color:rgb(244, 204, 204)'>></span><span style='background-color:rgb(244, 204, 204)'><b>WARNING</b></span><span style='background-color:rgb(244, 204, 204)'>: Do not boot servers without a backup server/hypervisor to access it (see</span> [how to access servers in safe mode documentation](undefined) <span style='background-color:rgb(244, 204, 204)'>to</span> <span style='background-color:rgb(244, 204, 204)'><ins>check if there is a backup server BEFORE setting a server to safe mode</ins></span><span style='background-color:rgb(244, 204, 204)'>.) Also, do not boot</span> [critical servers](undefined) <span style='background-color:rgb(244, 204, 204)'>into safe mode without</span> <span style='background-color:rgb(244, 204, 204)'><ins>first contacting the client to schedule the downtime</ins></span><span style='background-color:rgb(244, 204, 204)'>. Causing a server to reboot into safe mode will make it inaccessible to TakeControl (safe mode will not work with TakeControl), therefore, the tech must use the client’s backup server (i.e. "HNS-VEEAM (backup)") to remotely access the the server that is in safe mode.</span>


<b>\*</b>After you have remoted into the server (see [Access Server](undefined)), run command prompt in administrator mode (right click cmd application and click "run as administrator").


\*Copy and paste the following in cmd: `<span style='color:rgb(255, 255, 255);background-color:rgb(51, 51, 51)'>bcdedit /set {default} safeboot minimal</span>` (w/o the indent marks). You should get a message in cmd saying, "The operation completed successfully."


\*Now reboot the server, and perform the required actions in Safe Mode


<span style='background-color:rgb(255, 242, 204)'>>IMPORTANT NOTE:</span> After you finish your task in Safe Mode, <ins>you MUST change the</ins> <span style='color:rgb(255, 255, 170);background-color:rgb(51, 51, 51)'><ins>bcedit</ins></span> <ins>registry back to boot in Normal Mode</ins> (or else the server will reboot in Safe Mode automatically in a loop). To do this, open a command prompt in admin mode like before, and enter the following: `<span style='color:rgb(255, 255, 255);background-color:rgb(51, 51, 51)'>bcdedit /deletevalue {default} safeboot</span>` (again, without the indents, just the text), and hit `<span style='color:rgb(255, 255, 170);background-color:rgb(51, 51, 51)'>ENTER</span>`. Assuming you did everything correctly, the server should reboot as normal after you restart (please ensure it does before closing out of the remote session or else crucial applications may break and cause issues for the client).

## <span id="h.weqdytynpqic">Disk Space Warnings</span>

### <span id="h.xfh5w0pu1b86">Run CC Cleaner Silently</span>


CLI Ref. [https://support.piriform.com/hc/en-us/articles/360047885872-Command-line-parameters-for-CCleaner-for-Windows#command-line-parameters-for-ccleaner-for-windows-0-0](https://support.piriform.com/hc/en-us/articles/360047885872-Command-line-parameters-for-CCleaner-for-Windows#command-line-parameters-for-ccleaner-for-windows-0-0)


Batch File to Silently Install, Run Auto Cleaner, & Uninstall from Endpoint:

```
REM # Silent Install CC Cleaner #

path %path%;C:\Temp\ccsetup607.exe /S

REM # Add CC Cleaner To Windows Path #

path %path%;C:\Program Files\CCleaner;C:\Program Files (x86)\CCleaner

REM # Silent Update CC Cleaner #

ccleaner.exe /update

REM # Silent Run CC Cleaner With Default Settings #

ccleaner.exe /auto

REM # Silent UnInstall CC Cleaner #

C:\Program Files\CCleaner\uninst.exe /S

C:\Program Files (x86)\CCleaner\uninst.exe /S﻿
```


 1. Transfer the .bat file and the cccleanersetup.exe file to the C:\Temp path
 2. Run the .bat file (either by double-clicking or via CLI)

### <span id="h.t6pq3c8jbb1">DiskSpace Cleaner Tricks</span>


Windows installs system updates that can eat up GBs of storage. To delete these unneeded system files, run the native Windows application called "Disk Cleanup."


Note: DiskClean up is CPU intensive and may slow down enduser endpoint experience.

#### <span id="h.i9ab33ctdsnf">Run Disk Cleanup via CLI (CMD)</span>


Reference: [https://winaero.com/cleanmgr-exe-command-line-arguments-in-windows-10/#SAGESET](https://winaero.com/cleanmgr-exe-command-line-arguments-in-windows-10/#SAGESET)


 1. WIN to open start menu
 2. Type `cmd`to search for Command Prompt
 3. Press `CTRL +``SHIFT``+ ENTER` to launch Command Prompt as admin (or open PowerShell as admin)
 4. Create a "SAGESET" profile by assigning a number between 0–65535, for example: `cleanmgr.exe /sageset:0`
 5. You will be prompted to check all the boxes that you wish to clean/clear (see screenshot for reference, but you may wish to select all the boxes to clear the most amount of space).

![](https://lh6.googleusercontent.com/JXQ0tseTFI47WjXXluBqfypZjQk1iWu3fz_t5VrrtKXbmIbLykXzdHBq_pZSDYrL0IHpP4BSi36PEWgNgi-8n4cfihUPR2d3gn76DmQmqs3StTdiAmb4JxckIHydihCD_gDU3bQHssyBnTqZwylZhtCRAOGyiwuhrxgGTMmzCjhou_h8DwT6znFU0T1ZthRdQH526iE "")


 1. Once this SAGESET profile has been created, now you can run it delete the files according to the check boxes you selected by entering: `cleanmgr.exe /sagerun:0` (make sure to enter the number you assigned for this SAGESET profile).
 2. Type `cleanmgr.exe /verylowdisk /c` (this will start the clean process automatically)
 3. When process is finished, analyze system files left behind by a previous Windows by entering the following in CMD:
     1. `cleanmgr.exe /setup` (this will analyze the following locations)
    

```
C:$Windows.~BT\*
C:$Windows.~LS\*
C:$Windows.~WS\*
C:\ESD\Download\*
C:\ESD\Windows\*
C:$WINDOWS.~Q\*
C:$INPLACE.~TR\*
C:\Windows.old\*
C:\Windows\Panther
```


 1. And it saves two log files to inspect at these locations:

```
C:\Windows\System32\LogFiles\setupcln\setupact.log
C:\Windows\System32\LogFiles\setupcln\setuperr.log
```


 1. To automatically clean up these files left behind by the system, use `cleanmgr.exe /autoclean`

#### <span id="h.fzhi6z65kl45">Set Automatic Disk Manager Cleanup</span>


Ref: [https://www.groovypost.com/howto/windows-create-scheduled-task-run-disk-cleanup-automatically/](https://www.groovypost.com/howto/windows-create-scheduled-task-run-disk-cleanup-automatically/)


 1. WIN + S > "taskschd" (or "Task Scheduler") and open it
 2. Click on the Action tab > Create Basic Task
 3. Enter the description of the task you wish to create (i.e. Sys Disk Clean Up), and hit "Next" button.
 4. Select how often to run this task (i.e. weekly or "when computer starts" if it is a laptop) & click Next
 5. Choose the day and time to run this task (i.e. set to Friday after 5PM and before 3AM for servers) & hit Next.
 6. Check the "Start a program" radio button & hit Next.
 7. Type "cleanmgr.exe" in the CLI box under the "Program/script" field you see on screen. 
     1. In addition, you can also click Browse and go to C:\Windows\System32\cleanmgr.exe. Manually browsing the file shows its entire path in the Program/Script field.
    
 8. Enter "/sagerun:0" in the "Add arguments" field.

#### <span id="h.zfqvm2wg1i9n">Set Clean Up Process to High Priority</span>


To speed up the DiskClean process, you can set the priority to "high" in Task Manager. In the Task Manager 'Details' pane, find TiWorker.exe and right-click to show a pop-up menu. For 'Set Priority," choose "Above Normal," or even "High."

![](https://lh5.googleusercontent.com/ejQE5QFUSKGTqdttnmcJ_St3x_KrHHjdxc43rOy0RG-RyRSBh79Ay3bR8EArA1o6NJlaTeX6pRExBVm88pch8bkmC1FiGBiwFoNgTRsp0xpNVMkM5AqKA-gZnKBclvpRBesiDjd1EKg8n2VVX5GGtPB6o1Xf4pIJMgXt41N1MCMGh1dRZqaqDT5LHOVAJBuZDy1Icco "")

#### <span id="h.3qzn0uxs0agh">Clear PageFile.sys at Shutdown</span>


 1. > WIN + R > regedit > copy and paste the following in the navigation search:
     1. HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Session Manager\Memory Management
     2. REG ADD "HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Session Manager\Memory Management" /v "ClearPageFileAtShutdown" /t REG_DWORD /d 1
     3. REG ADD HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Session Manager\Memory Management /v ClearPageFileAtShutdown /t REG_DWORD /d 1
     4. [CLI Reference](https://www.howtogeek.com/677453/how-to-edit-the-windows-registry-from-the-command-prompt/) and edit syntax accordingly (ex. REG ADD "<KEY_PATH>" /f /v "<KEY_NAME>" /t REG_BINARY /d <BINARY_VALUE>)
    
 2. Double click "ClearPageFileAtShutdown"
 3. Edit registry value from "0" to "1"
 4. Click OK to save.

#### <span id="h.73wc6sl0rbpq">Outlook Cache to Cloud</span>


Note: This will sometimes cause email searches to run slower because all the files are in the cloud.


Launch Outlook > File > Account Settings > Manage Profiles (this will generate a popup) > Data Files > Settings > Advanced (tab) > Uncheck "Use Cached Exchange Mode" > Click "Apply" button (this will prompt to restart Outlook to apply changes) > Click "Ok"

#### <span id="h.5q1hu7i4a385">Rebuilding Windows.edb Search Index</span>


Ref. [https://digicruncher.com/windows-edb-file-is-huge-in-my-pc/](https://digicruncher.com/windows-edb-file-is-huge-in-my-pc/)


This trick can clear out GBs of data.


 1. Sometimes the "Windows.edb" file can be bloated. To remedy, you need to rebuild the Windows Search Index
 2. WIN + R > type `control srcadmin.dll` > Click "Rebuild"
 3. Alternatively you can do the following: 
     1. > WIN + S > Indexing Options app > Advanced button > Troubleshooting > Delete and rebuild index > Rebuild button > OK button
    
 4. Or run the following batch file in PS:

```
@echo off
net stop wsearch
del "%programdata%\microsoft\search\data\applications\windows\Windows.edb.bak"
move "%programdata%\microsoft\search\data\applications\windows\Windows.edb" "%programdata%\microsoft\search\data\applications\windows\Windows.edb.bak"
net start wsearch
```

#### <span id="h.ib0oyvnug6zh">Delete Old UvhdCleanupBin Files</span>


C:\Users\UvhdCleanupBin (this is a hidden folder and must be accessed via admin or admin-run TreeSize to delete folders)


Note: It [appears](https://social.technet.microsoft.com/Forums/en-US/bc514614-e4d2-47ae-833a-bc9022c3367a/uvhdcleanupbin-keeps-growing?forum=winserverTS) that all these files are caused by remote desktop sessions. The bug is that it does not delete user logs when the path limit is exceeded. [A security update back in Aug. 2017](https://www.ghacks.net/2017/08/08/microsoft-security-updates-august-2017-release/) should fix this issue. Other [users report no issue with deleting old folders](https://social.technet.microsoft.com/Forums/office/en-US/9f8de478-bac7-4cc2-b003-00b2bf05bd49/what-is-uvhdcleanupbin?forum=winserverTS) from this file location

#### <span id="h.gnezsv8e76nd">Lower Limit of Shadow Copies</span>


Note: This issue may only pertain to certain endpoints. If you find a large cache of "<ins>System Volume Information</ins>" files, then you can lower the limit of Shadow Copies that the System stores (otherwise you will have to open a ticket with the vendor).


 1. Open File Explorer & navigate to My PC
 2. Right click C: drive and click on "Configure Shadow Copies"
 3. Change the MB limit down <b>incrementally</b> (i.e. 50,000 to 40,000 to 30,000, etc.) until you get it down to 4,000MB.
     1. Each time you have to hit "OK" to apply the change
     2. You should immediately notice a change in the disk space when you perform the shadow copy limit
    

#### <span id="h.uec86voa32s0">Run a Shadow Copy Clean in Disk Cleanup</span>


If the above "Low Limit of Shadow Copies" did not work, you may wish to run a shadow copy clean up.


 1. Open Disk Cleanup
 2. Click "Clean up system files" button and wait for it to load
 3. Click on the new "More Options" tab that appears
 4. Do NOT run the "Programs and Features" clean up because this may remove critical applications on the endpoint
 5. Do run the clean up for "System Restore and Shadow Copies"

#### <span id="h.7niz8bingt50">Try a Smart Disk Cleanup Tool</span>


[https://apps.microsoft.com/store/detail/smart-disk-cleanup/9PM1SH8S2VQV?hl=en-us&gl=us](https://apps.microsoft.com/store/detail/smart-disk-cleanup/9PM1SH8S2VQV?hl=en-us&gl=us)


-Can be found using basic search in the Microsoft Store on the endpoint.

### <span id="h.6vkffjl7bc1o">Guidelines for Clearing Disk Space</span>


 1. Run TreeSize to identify largest files taking up storage space
 2. Determine if files are critical or personal to enduser
     1. If files are generated by enduser, do NOT delete without first getting permission from enduser or backing up those files and giving enduser access to those backup files.
     2. Be very careful of any files in Sys32
     3. NEVER modify or delete "WindowsSxS" (Windows Side by Side) files or folders
    
 3. If unsure about files/folders, do not delete. Instead, temporarily move files in question to a secondary drive (if available on endpoint).
 4. If no extra drive is available on endpoint, look for other servers on the network with enough free space to move files to
     1. `WIN + R` to open run, type in the server name as follows: `\\[server name]\[drive letter]$`
     2. <span style='background-color:rgb(255, 242, 204)'>Important Note</span>: Do NOT move files to any drive labeled "temporary" as any files stored here will be lost upon a server reboot
     3. You can search for the server name in RMM or ITGlue
    
 5. Lastly, schedule yourself to revisit the ticket and check the endpoint is running without issues (or if enduser calls in to report new issues caused by moving questionable files).

#### <span id="h.m7gxkq1pwpnx">Additional Guidelines from NOC Lead</span>


A "Temporary Storage" disk is a special disk in Azure, assigned to every Azure VM. It is non-persistent. If the VM is stopped, all contents stored on the disk are lost. It should only be used for very special use cases. Moving data around, to any drive, is rarely going to be a solution for a disk space ticket. That said, if your disk analysis on a SQL server, for example, showed that the SQL DB files were located on the C volume but there was an empty, unused, F volume that was named "SQL" then it's likely someone set it up incorrectly. But you would not move the files. You would reach out to a senior engineer for guidance.


In this particular screenshot, just follow the usual course... analysis of the C volume. If no data that obviously is temporary etc, then the disk probably is too small for the workload.


 - Look at the timestamp
 - They were modified almost a month ago, so probably fine to remove.
 - The location is also a clue
 - And the name
 - i.e. the inverse is also a clue
 - so like if the name or path contains "sql" then that's a clue the files are more sensitive and maybe need to research more what they are and ask a senior engineer etc
 - but the inverse is also true
 - since the path and the name don't include obvious key words, then there is a lower chance they are important or still needed
 - but the biggest clue is (1) they are .tmp files and (2) the last modified time was over a month ago
 - if that was like a few days ago, they might still be needed
 - and no, do not escalate to me
 - you can learn this stuff as you go
 - for general knowledge, such as how to identify if files are temp, you can ping a senior engineer
 - for general knowledge, such as how to identify if files are temp, you can ping a senior engineer
 - even an Engineer, to be honest
 - so like ping Raymond, William, Mike
 - even Josh W can be a good resource as he has grown a LOT since being here and has a good spectrum of knowledge
 - always take "tips" and knowledge from Technicians with a grain of salt though
 - if it doesn't sound right, it probably isn't!
 - you need to also leverage the power of google
 - but again there is so much misinformation out there, that you have to be careful with that
 - if you are not sure about interpreting the results of a disk analysis, run it past an Engineer
 - if the conclusion is no space can be reclaimed and the disk needs to be increased, then that will be an escalation to an Engineer to handle

### <span id="h.abcifsfe02vj">How to Access Servers in Safe Mode</span>


\*While a server is booted into safe mode, it will not be directly accessible with TakeControl tools. You have to use the client’s backup server to access it.


\*To check if the client has a backup server first go to [https://ncentral.biztech.io/](https://ncentral.biztech.io/) and find the client/customer (use the drop down menu).


\*Next, do a window search (`CTRL``+ F`) for "backup" and/or "veeam." You are looking for something that says mentions "backup server" (i.e. "HNS-VEEAM (backup server)").


\*Do a TakeControl session of this endpoint. It will prompt you for creds to enter.


\*Use ITGlue to find the right creds > Organizations > Passwords > Search for the name of that Veeam back up server which has the bts_admin creds.


\*Once you have gained access, open a web browser, search for a bookmark that says "VCSA" (if you don’t see a bookmark, enter the following in the URL address: `//vcsa.[abbreviation of the company name].local`). This should bring you to the VMWare’s launch page (see below).

![](https://lh4.googleusercontent.com/j8OnvD8p_gfB4qxl4OmXiLQ0Pp62B7I8gUiMsKlXTZTsJjgV6F4B2ojnts5u8om8xREReYrRMUdJB7O6qKscO92xEQd_HYF2wnqkj9MMraUvqslgqZdvrJytrLDRyPFmULus-7ScKu4Drd6epXB8r4nAM55s6NSVuGdtZna4Krp6EBgm_BVBOo_1q7RZX-rqaEe-sz8 "")


\*Click button to Launch the VSphere Client. You will now be prompted for a different set of creds to login to VSphere (whcih is customer specific).


\*Using ITGlue again, search for VSphere and grab the creds for that show "administrator" and "vsphere" in the username (see redacted example below).

![](https://lh5.googleusercontent.com/1XIXB8Uz6eh2nZ2WY08Rwgy-rSrgHh-DuHL-9zQ651FBFzycA3XUPPkbwIvh6YdLJnIw6bMIakiiF2TkzuoX4lf2o80DxOoCBjw5kj9D8yoDKqymNOpUSxCnwiHWsFzUoOPJSQl-2DZHPQELQyOBr6I7qoQSgtmdPxQoqFzgboC3RO-ktqm8G1gPOt97jJ2vNwCROE8 "")


\*Once you are in, look down the navigation tree on the left pane and locate the server you want to access, click on it and then click on the "Launch Console" icon to access the login screen.


\*That’s it! You are in! Just don’t forget to set the reboot back to normal by opening an admin cmd and entering: `<span style='color:rgb(255, 255, 255);background-color:rgb(51, 51, 51)'>bcdedit /deletevalue {default} safeboot</span>` and hit ``ENTER`` to set it.


>Tip: See [how to reboot endpoint via cmd here](undefined).


>Note: When ever you remote on to a server through a backup server like this, `CTRL +``SHIFT``+ X` paste will not work, therefore, you must manually enter the credentials to login.

## <span id="h.8tzlyvcyfff1">Useful Command Prompt Commands</span>


File Navigation

### <span id="h.16rbfm8ol5qi">Ping Seemingly Offline Endpoints</span>


<span style='color:rgb(33, 33, 33)'>S</span><span style='color:rgb(33, 33, 33)'>teps to ping endpoints that endusers report online, but RMM shows offline.</span>


 1. <span style='color:rgb(33, 33, 33)'>Get the IP Address of Endpoint</span>
     1. <span style='color:rgb(33, 33, 33)'>RMM > Endpoint > Hover over "Take Control" to get status of endpoint last online.</span>
     2. <span style='color:rgb(33, 33, 33)'>A quick glance of the endpoint details could provide the IP address, if not, check the hardware details:RMM > Endpoint > Asset > Hardware > Network Adapters (scroll down to look for "IP Address"</span>
    
 2. <span style='color:rgb(33, 33, 33)'>Remote onto location-specific DC to ping that IP address</span>
     1. <span style='color:rgb(33, 33, 33)'>Open CMD on the DC and type:</span> `ping [ip address of endpoint in question]`
     2. <span style='color:rgb(33, 33, 33)'>If the endpoint times out, then it may be offline or it may have firewall issues</span>
    
 3. <span style='color:rgb(33, 33, 33)'>If the endpoint cannot be reached by ping, then you need to instruct enduser to conduct a quick Google search (tell them to search for something arbitrary [i.e. "dog" "cat"] to make sure that Google site is not cached memory or have them run a speed test</span> [https://speedtest.net](https://speedtest.net)<span style='color:rgb(33, 33, 33)'>)</span>
     1. <span style='color:rgb(33, 33, 33)'>If the enduser reports that endpoint can search and reach other websites, it shows that the firewall permits for outbound/inbound traffic to the internet</span>
     2. <span style='color:rgb(33, 33, 33)'>If the enduser cannot reach webpages online, then perhaps there is a firewall issue set by Fortigate networking that must be changed in order for RMM to reach endpoint.</span>
    

### <span id="h.4cwdn7ze8z8">Force Reboot Windows Endpoint via CMD</span>


-Open cmd and enter: `<span style='color:rgb(255, 255, 255);background-color:rgb(51, 51, 51)'>shutdown /r /f</span><span style='color:rgb(33, 33, 33)'><i>`</i></span>


<span style='color:rgb(33, 33, 33)'>-If shutting down for routine maintenance, patching, and anti-virus updates, you can send a message to the enduser to see such as:</span>

```
shutdown /r /f /c Rebooting endpoint for routine maintenance, patching, and anti-virus updates.--BizTech
```


<span style='color:rgb(33, 33, 33);background-color:rgb(255, 242, 204)'>Restarted the wrong endpoint by mistake?</span> <span style='color:rgb(33, 33, 33)'>Type</span> <span style='color:rgb(255, 255, 255);background-color:rgb(51, 51, 51)'>shutdown /a</span> <span style='color:rgb(33, 33, 33)'>before the 30 second reset window expires to stop the restart from happening.</span>


<span style='color:rgb(33, 33, 33)'>>Note: If you do not want to force a reboot (which will delete any unsaved work by use), remove the `</span><span style='color:rgb(255, 255, 255);background-color:rgb(51, 51, 51)'>/f</span><span style='color:rgb(33, 33, 33)'><i>`</i></span> <span style='color:rgb(33, 33, 33)'>from the code. Additionally, `shutdown /a`</span> <span style='color:rgb(33, 33, 33)'>is very handy when windows update tries to force reboot your computer. You can run this command and cancel the reboot if you don’t want the reboot to happen at that time</span><span style='color:rgb(17, 17, 17);background-color:rgb(255, 255, 255)'>.</span>


Set a Shutdown Timer via CMD


WIN + R > "cmd" > Right-click "Run as administrator" > type the following:

```
shutdown /s /t [number of seconds until shutdown]
```


1hr = 3600


4hrs = 14400


6hrs = 21600

### <span id="h.kuocoabur8q9">Install Programs Undetected by Enduser via CLI</span>


\*Go to https://biztechhelp.me > Access > Search for the endpoint > Right-click the name of the endpoint > Select "Join with Options" > Select [Backstage] > Click "Join Session" to endpoint & wait for screenconnect to load up


\*Open PowerShell (PS)


\*<span style='color:rgb(255, 255, 170);background-color:rgb(51, 51, 51)'>cd</span> to the .exe file location (i.e. <span style='color:rgb(255, 255, 255);background-color:rgb(51, 51, 51)'>c:/users/[username]/documents/downloads</span>)


\*Use Tree to list files and grap the .exe file name you want to install. Type `<span style='color:rgb(255, 255, 170);background-color:rgb(51, 51, 51)'>tree</span> <span style='color:rgb(255, 255, 255);background-color:rgb(51, 51, 51)'>/f</span>`


\*Note the file name and type `<span style='color:rgb(255, 255, 255);background-color:rgb(51, 51, 51)'>.\[name of app you want to install].exe</span>`


> \*\*ENDUSER AFFECTED NOTE\*\*: A pop up will appear to the enduser and require the enduser to okay the installation before the app will install. Therefore, it is best to install new applications whilst the enduser is away or scheduled for remote access.

## <span id="h.1fnqwniwv4f">Installing Scoop, a CLI Installer</span>


Quick Guide Reference: [https://computingforgeeks.com/install-applications-from-command-line-windows/](https://computingforgeeks.com/install-applications-from-command-line-windows/)


Developer’s In-depth Guide: [https://github.com/ScoopInstaller/Scoop/wiki](https://github.com/ScoopInstaller/Scoop/wiki)


List of Apps via Scoop Installer: [https://scoop.sh/#/](https://scoop.sh/#/)

### <span id="h.n4a72mjk0r08">Antivirus CPU High Usage Workaround</span>


[https://github.com/ScoopInstaller/Scoop/wiki/Antivirus-and-Anti-Malware-Problems](https://github.com/ScoopInstaller/Scoop/wiki/Antivirus-and-Anti-Malware-Problems)


<span style='color:rgb(36, 41, 47)'>If you are experiencing</span> <span style='color:rgb(36, 41, 47)'><b>performance problems</b></span> <span style='color:rgb(36, 41, 47)'>during Scoop installs—like high CPU usage, or file access denied errors—it's possible that an anti-malware or anti-virus program is scanning files as they are being extracted and installed.</span>


<span style='color:rgb(36, 41, 47)'>You can exclude the directories that Scoop uses from real-time scanning by running this command as an administrator:</span>


### <span id="h.azl3uqf1akt8">Scoop Quickstart Guide</span>


[https://scoop-docs.vercel.app/docs/getting-started/Quick-Start.html#installing-scoop](https://scoop-docs.vercel.app/docs/getting-started/Quick-Start.html#installing-scoop)

### <span id="h.2d1p32rzh9hg">Install Scoop via PowerShell</span>


\*Install Scoop (a command-line installer for Windows)


> Scoop is installed on Windows using PowerShell (PS)


\*Login as Administrator user and launch PowerShell, by using ITGlue > Customer > Passwords


\*Once PS is active, use the following command to install scoop to its default location (<span style='color:rgb(255, 255, 255);background-color:rgb(51, 51, 51)'>C:\Users\<user>\scoop</span>)


```ps

```


\* Hit <span style='color:rgb(162, 252, 162);background-color:rgb(51, 51, 51)'>"y"</span> to confirm fingerprints and installation. PS will now download and install Scoop on the endpoint.


\* Confirm Scoop has been installed and operational by typing `<span style='color:rgb(255, 255, 255);background-color:rgb(51, 51, 51)'>scoop</span> <span style='color:rgb(255, 255, 170);background-color:rgb(51, 51, 51)'>help</span>`


-The installed applications are located on User’s home directory `<span style='color:rgb(255, 255, 255);background-color:rgb(51, 51, 51)'>~/scoop/apps</span>`


\* Use the `search` command to locate path of binary executable file. (ex. `<span style='color:rgb(255, 255, 255);background-color:rgb(51, 51, 51)'>scoop</span> <span style='color:rgb(252, 194, 140);background-color:rgb(51, 51, 51)'>search</span><span style='color:rgb(252, 194, 140);background-color:rgb(51, 51, 51)'>which</span>`)


\* Now install the desired app via <span style='color:rgb(255, 255, 255);background-color:rgb(51, 51, 51)'>`</span><span style='color:rgb(252, 194, 140);background-color:rgb(51, 51, 51)'>scoop install</span> <span style='color:rgb(255, 255, 255);background-color:rgb(51, 51, 51)'>[app_name]</span>`


\* Uninstall Scoop when finished by running: `<span style='color:rgb(255, 255, 170);background-color:rgb(51, 51, 51)'>scoop uninstall scoop</span>`


> Below is a list of Scoop commands:
