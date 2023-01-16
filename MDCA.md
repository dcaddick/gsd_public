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

[]!(./images/MDCA_EnableFileMonitoring.png)

### Validate and Test

- Enable MDI Integration
<https://learn.microsoft.com/en-us/defender-cloud-apps/mdi-integration>
- Govern discovered Apps using MDE (enables blocking of unwanted Apps)
<https://learn.microsoft.com/en-us/defender-cloud-apps/mde-govern>
- Investigating via Dashboard:
<https://learn.microsoft.com/en-us/defender-cloud-apps/investigate>
- Tune the system: 
<https://learn.microsoft.com/en-us/defender-cloud-apps/tutorial-suspicious-activity>
- Investigate & remediate risky OAuth Apps:
<https://learn.microsoft.com/en-us/defender-cloud-apps/investigate-risky-oauth>


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
-   Don't forget this is based on MDE
