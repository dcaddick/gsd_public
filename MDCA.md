## MDCA (was MCAS):

![](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTQs2hcOLld13doGTbvIknglVMDxEoot1EJ3g&usqp=CAU)

### Ways of working
First decision point - Simple or Complex, i.e. do you need to be concerned about RBAC for instance becuase of the scale of the installation or the number of different parties that **may** need access to part or some parts of the console?  <https://learn.microsoft.com/en-us/defender-cloud-apps/manage-admins>



### Enable Telemetry

- Basic Setup --> Start here:
<https://learn.microsoft.com/en-us/defender-cloud-apps/general-setup>
<https://learn.microsoft.com/en-us/defender-cloud-apps/get-started>
- Tell it what the Corporate IP address's are: 
<https://learn.microsoft.com/en-us/defender-cloud-apps/ip-tags>
- Set the IP's in bulk if needed:
<https://learn.microsoft.com/en-us/defender-cloud-apps/api-data-enrichment-manage-script>
-   Enable File Monitoring:
<https://learn.microsoft.com/en-us/defender-cloud-apps/file-filters>
- Add native App Connectors: (Atlassian, Google, Azure, AWS, Box, DocuSign, Github, Okta, Salesforce, ServiceNow, Slack, Workday, etc... )
<https://learn.microsoft.com/en-us/defender-cloud-apps/enable-instant-visibility-protection-and-governance-actions-for-your-apps>
- Best Practices:
<https://learn.microsoft.com/en-us/defender-cloud-apps/best-practices>
- Daily Activities:
<https://learn.microsoft.com/en-us/defender-cloud-apps/daily-activities-to-protect-your-cloud-environment>

The best practices discussed in the link above include:

-   Discover and assess cloud apps
-   Apply cloud governance policies
-   Limit exposure of shared data and enforce collaboration policies
-   Discover, classify, label, and protect regulated and sensitive data stored in the cloud
-   Enforce DLP and compliance policies for data stored in the cloud
-   Block and protect download of sensitive data to unmanaged or risky devices
-   Secure collaboration with external users by enforcing real-time session controls
-   Detect cloud threats, compromised accounts, malicious insiders, and ransomware
-   Use the audit trail of activities for forensic investigations
-   Secure IaaS services and custom apps

!!! warning
    -   For best protection, we recommend selecting all Office 365 components.
    -   The Office 365 files component, requires the Office 365 activities component and Defender for Cloud Apps file monitoring (Settings > Files > Enable file monitoring).
    -   Make sure the **last** checkbox (Office 365 Files) in the image below is **"checked"** [link to more details](<https://learn.microsoft.com/en-us/defender-cloud-apps/connect-office-365>) 

![](https://learn.microsoft.com/en-us/defender-cloud-apps/media/connect-o365-components.png)

### Validate and Test

-   Enable MDE Integration
<https://learn.microsoft.com/en-us/defender-cloud-apps/mde-integration> 
-   Enable MDI Integration
<https://learn.microsoft.com/en-us/defender-cloud-apps/mdi-integration>
-   Govern discovered Apps using MDE (enables blocking of unwanted Apps)
<https://learn.microsoft.com/en-us/defender-cloud-apps/mde-govern>
-   Investigating via Dashboard:
<https://learn.microsoft.com/en-us/defender-cloud-apps/investigate>
-   Tune the system: 
<https://learn.microsoft.com/en-us/defender-cloud-apps/tutorial-suspicious-activity>
-   Investigate & remediate risky OAuth Apps:
<https://learn.microsoft.com/en-us/defender-cloud-apps/investigate-risky-oauth>

!!! note
    -   It takes up to two hours after you enable the integration for the data to show up in Defender for Cloud Apps.
    -   [List of supported Firewalls and Proxies](<https://learn.microsoft.com/en-us/defender-cloud-apps/set-up-cloud-discovery#supported-firewalls-and-proxies->)
    -   Follow link above for Integration steps with ZScaler, iboss, Menlo, etc...


![](https://learn.microsoft.com/en-us/defender-cloud-apps/media/mde-settings.png)

### Enable Reporting

- Investigate Apps discovered by MDE 
<https://learn.microsoft.com/en-us/defender-cloud-apps/mde-investigation>
- Governance for Connected Apps:
<https://learn.microsoft.com/en-us/defender-cloud-apps/governance-actions>
This is where this process gets really good, have a real good look at all the possibilities here to be able to be able to track what is being done with data inside the environment - don't jump in & start blocking things before you understand the full business implications. 
- Governance for discovered Apps:
<https://learn.microsoft.com/en-us/defender-cloud-apps/governance-discovery>
Now we can take this one step further and we can now determine which of the 26,000 SaaS Apps I want to allow or block - the only real limitation (to a certain extent) is that the user is using corporate credentials from our AAD via an endpoint enabled with MDE 

### Review and Improve as needed

- Add Conditional Access App Control into the mix - this is where we are starting to get more into Zero Trust - so don't jump in here first, make sure the rest of the Security settings are in place and then come back to this in a later phase
<https://learn.microsoft.com/en-us/defender-cloud-apps/proxy-intro-aad>

There is a lot more to be covered, but this will do for now, if you have questions please let us know?
<https://github.com/dcaddick/gsd_public/discussions>


### Troubleshooting

- Advanced Settings URL:
<https://security.microsoft.com/cloudapps/settings>
- Troubleshooting: 
<https://learn.microsoft.com/en-us/defender-cloud-apps/troubleshooting-cloud-discovery>

-   Apps list
-   Sanctioned/Unsanctioned
-   Don't forget this is based on MDE so go back and check the MDE integration link above
