https://learn.microsoft.com/en-us/microsoft-365/security/office-365-security/eop-about?view=o365-worldwide#how-eop-works


Not everybody consumes info in the same way, but this is how I consume/manage the constant flow of info:
-   Text, links and graphics (pptx and pdf preferably) so that I can skim FAST
-   Others like Video, I find it too time consuming
-   Plus I focus on searching for the great content & then tracking the people that created that and build a network

· Infographic: #BeCyberSmart with Devices and Data
· Infographic: #BeCyberSmart with Phishing
· Infographic: #BeCyberSmart with Scams
· Infographic: #BeCyberSmart with Passwords
· Infographic: #BeCyberSmart with Cybersecurity 101
· Email: #BeCyberSmart with best practices for your organization
· Video Series: Learn how to #BeCyberSmart with these video tips and tricks
![image](https://user-images.githubusercontent.com/19640455/211226033-59cc6005-7616-4e5d-952d-5a632de478ac.png)


https://admin.microsoft.com/Adminportal/Home?Q=ADG#/SetupGuidance


Change over to different way of Processing to add support for .git
https://github.com/marketplace/actions/mkdocs-deployment
And
https://github.com/marketplace/actions/mkdocs-link-check

Defender Threat Intel
<https://ti.defender.microsoft.com/>

MDO Config Analyzer
<Aka.ms/defenseindepth> 

Insider Risk

Discussions: <https://github.com/dcaddick/gsd_public/discussions>

![](https://media.licdn.com/dms/image/C5622AQGykC2scwbozw/feedshare-shrink_800/0/1675345228382?e=1678320000&v=beta&t=Ld7lfnsrKkIHmcA-GaSm63mMs8knJLWUjPd1vo2lEAI)

<https://www.blimped.nl/managing-and-applying-purview-retention-labels-using-code/#conclusion>

check out other "saved posts" from LinkedIn
https://www.linkedin.com/my-items/saved-posts/

https://twitter.com/jeffreyappel7/status/1616196538337792009?s=61&t=4qPz80pQqXdQmuvndvnOPw


Automate from Outlook ToDo into Planner 
https://make.preview.powerautomate.com/galleries/public/templates/67477f30373611e7870df906aa521b7a/create-planner-tasks-for-flagged-emails-in-office-365?fromflowportal=true&environment=839eace6-59ab-4243-97ec-a5b8fcc104e4 

Expand on SOAR as a separate Heading
This covers M365 (think AIR) as well as Sentinel

Expand on Private Communities?


### **Ways of working**

### **Enable Telemetry**

### **Validate and Test**

### **Enable Reporting**

### **Review and Improve as needed**

### **Troubleshooting**



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
