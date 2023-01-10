
· Infographic: #BeCyberSmart with Devices and Data
· Infographic: #BeCyberSmart with Phishing
· Infographic: #BeCyberSmart with Scams
· Infographic: #BeCyberSmart with Passwords
· Infographic: #BeCyberSmart with Cybersecurity 101
· Email: #BeCyberSmart with best practices for your organization
· Video Series: Learn how to #BeCyberSmart with these video tips and tricks
![image](https://user-images.githubusercontent.com/19640455/211226033-59cc6005-7616-4e5d-952d-5a632de478ac.png)


WDAC
https://learn.microsoft.com/en-us/windows/security/threat-protection/windows-defender-application-control/create-initial-default-policy#create-a-custom-base-policy-to-minimize-user-impact-on-in-use-client-devices


!!! tip Most folks skip Defender in preference for Sentinel?  
    -   Start from the desired outcome and work your way back from there
    -   What is it that SecOps need? - more automation, less manual work ;-)
    - What does that look like? Showcase an example from Contoso Hotels
    - Enable Automated Investigation & Remediation (AIR) at MDI, MDO, MDE and M365 Defender console levels - **don't skip this!**
    -   Now that we have the first level triage in place, let's now move on to Sentinel...



Automate from Outlook ToDo into Planner 
https://make.preview.powerautomate.com/galleries/public/templates/67477f30373611e7870df906aa521b7a/create-planner-tasks-for-flagged-emails-in-office-365?fromflowportal=true&environment=839eace6-59ab-4243-97ec-a5b8fcc104e4 

Expand on SOAR as a separate Heading
This covers M365 (think AIR) as well as Sentinel

Expand on Private Communities?


Not everybody consumes info in the same way, but this is how I consume/manage the constant flow of info:
-   Text, links and graphics (pptx and pdf preferably) so that I can skim FAST
-   Others like Video, I find it too time consuming
-   Plus I focus on searching for the great content & then tracking the people that created that and build a network


M365 RBAC released
-   Shortcut to RBAC Permissions - https://security.microsoft.com/mtp_roles
-   Compare RBAC Roles - https://learn.microsoft.com/en-us/microsoft-365/security/defender/compare-rbac-roles?
-   Edit and Delete Roles - https://learn.microsoft.com/en-us/microsoft-365/security/defender/edit-delete-rbac-roles?
![image](./images/M365_SecOps_Permissions.png)
![image](./images/M365_SecConfig_Permissions.png)

**Technical Legacy Debt**
-   **Goal:** Understand who owns the legacy environment
-   Validate (again) if the legacy systems are actually required - absence of ownership is a good indicator that this platform may be considered for retirement
-   Consider passing on the cost of additional controls and operations burden - if the PROBLEM of legacy systems never have an owner, then the problem will never get solved.  And even if the problem is managed, if there is no additional cost burden, then there is less motivation to actually solve (i.e. retire) the legacy platform problem.
-   Use a scream test - shutdown legacy system and see who screams ;-)
-   **Goal:** Reduce the exposure by limiting the access
-   Move these systems to a controlled network environment - e.g. segregated network zone with firewalls to limit access - only allow the traffic absolutely essential for the legacy application
-   Deploy extensive monitoring of these systems - with high severity alerts being generated
-   Consider migrating these legacy systems off the production domain (goal is to reduce the legacy authentication protocols being run across the whole environment - perhaps they have their own segregated domain with constrained Trust relationships back to production)
-   Consider Applocker as another compensating control - intent is to only allow the legacy app to run, and NOTHING ELSE
-   Have limits and controls around remote access - MFA / jumphost etc - reduce the ability for non-authorised users to access these vulnerable systems