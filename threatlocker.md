![threatlocker_logo](https://i.imgur.com/nhMXLdH.png)

### Adding an Organization
1. From the Threatlocker dashboard, click New Organization.
2.  Enter the client/site details (General tab):
- Name - Client's legal name
- Identifier - Client's identifier (no spaces or odd characters)
  - This is primarily used in scripts and RMM tools
- Time zone - Defaults to your time zone, always double-check
3. Add in the client's default domain (domain tab). If the client has multiple domains, add them too.
- Enter the domain and click add (ex. wmwscaffolding.com)
4. The remaining tabs are:
- Security settings
  - If your client is subject to ITAR or other location-restricted regulations, check theITAR Compliantbox to prevent non-US users from accessing your client. We would also suggest raising the issue with ThreatLocker support to ensure compliance.
- Proxy Settings 
  - If your client uses a proxy server, you can enter that here
- Branding
  - If you want to use custom branding (similar to your RMM), enter the name and URLs to your icons here.

5. Click __Save__ at the top of the popup window to confirm your settings.
6. Wait for the loading popup window to disappear, indicating the new organization is created.

> The setup time takes about 60 seconds; don't be surprised if it looks like the popup window appears to "hang". Give it some time, and the setup will be completed properly.
> After the popup window disappears, you may need to refresh your page (F5 in Chromium browsers) before the new organization appears.

7. You can now click on __Manage__ next to the organization to continue management.

### Editing an Organization
1. Click on the Pencil icon to edit the organization.
2. Edit the organization with the following warnings:
- If you change the identifier, be sure your RMM uses the same identifier (if you follow ThreatLocker's steps on setup).
- If you change the time zone, remember that reports may be different due to the updated time change
- If you update the branding, you may have unpredicted results on previously-deployed agents. Check with ThreatLocker support before making this change.
- If you update theITAR Compliant settings, allow up to 30 minutes as a precaution, and test access just to ensure that users have normal access
- ThreatLocker is an international company -always check with ThreatLocker support if you (or your client) are subject to ITAR, DFARS, CMMC, or other sensitive regulatory controls.

### Deleting an Organization
__BEFORE YOU DELETE__, be sure to:
- Run any reports on the client you wish to keep for historical purposes.
  - Once the organization is gone, you will be unable to run reports on them!
-  Be sure all agents are uninstalled with the client.
  - ThreatLocker can become very challenging to remove if tamper-protection is enabled and the organization no longer exists (e.g. you may need to reload the OS).
-  As a precaution, check the last column Denied Count to ensure ThreatLocker has not taken any action in the last seven days.
  - This is a very easy way to determine if ThreatLocker is truly uninstalled from your client's workstations and servers.
- As always, this deletion is FINAL AND IRREVERSIBLE. Check, double check, and check one more time that this is what you want to do.
- If you need to delete an organization, click the checkbox next to the organization and select Delete.
