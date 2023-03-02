## **ASD Essential 8 (now ACSC)**

-   **Please start with this - ACSC Essential 8 – Health Report in Microsoft Sentinel**
<https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/acsc-essential-8-health-report-in-microsoft-sentinel/ba-p/3755702>
![](https://techcommunity.microsoft.com/t5/image/serverpage/image-id/446514i33DB819B58F060BA/image-size/large?v=v2&px=999)

-   Great high level on all Essential 8
<https://www.microsoft.com/en-au/business/topic/security/essential-eight/>
-   6 videos that walk thru
<https://info.microsoft.com/AU-SCRTY-CATALOG-FY21-02Feb-14-TheEssentialEightforSecurityinPractice-SRDEM61939_CatalogDisplayPage.html>
-   Microsoft Cybersecurity Reference Architecture
 <https://aka.ms/MCRA> or <https://learn.microsoft.com/en-us/security/cybersecurity-reference-architecture/mcra>
-   General on Essential 8
<https://www.microsoft.com/en-au/business/topic/security/>
-   Daily backups
<https://www.microsoft.com/en-au/business/topic/security/essential-eight/daily-backups/>
-   Australian IRAP
<https://learn.microsoft.com/en-us/azure/compliance/offerings/offering-australia-irap> & <https://servicetrust.microsoft.com/Viewpage/AustraliaIRAP>

**Local Australian E8 Guides**
-   Microsoft Service Trust Portal has the local Essential 8 guides  <https://aka.ms/e8guides> here you will find the PDF's covering the following specifics - the guides below can be accessed easy enough, but you will need to sign in using your own Tenant ID to access the IRAP docs ;)

- 	Microsoft General - Essential Eight - Config Macros - 2022-09
-   Microsoft General - Essential Eight - User Application Hardening - 2022-09
-   Microsoft General - Essential Eight - Restricting Admin Priv - 2022-09
- 	Microsoft General - Essential Eight - Patch OS - 2022-09
- 	Microsoft General - Essential Eight - Backup - 2022-09
-   Microsoft General - Essential Eight - Patch Applications - 2022-09
-   Microsoft General - Essential Eight - MFA - 2022-09

### **Hardening Guidance from ACSC**

-   For Windows 10 21H1
<https://www.cyber.gov.au/acsc/view-all-content/publications/hardening-microsoft-windows-10-version-21h1-workstations>
-   For Office
<https://www.cyber.gov.au/acsc/view-all-content/publications/hardening-microsoft-365-office-2021-office-2019-and-office-2016>
-   For Macro's
<https://www.cyber.gov.au/acsc/view-all-content/publications/microsoft-office-macro-security>
-   For Intune
<https://github.com/microsoft/Intune-ACSC-Windows-Hardening-Guidelines>
-   WDAC Policy creation from DTA
<https://desktop.gov.au/blueprint/abac/wdac-policy-creation.html>

### **Hardening Azure AD**

-   [Secure your Azure AD identity infrastructure - Azure Active Directory](https://learn.microsoft.com/en-us/azure/security/fundamentals/steps-secure-identity)
-   Also worth reviewing our Essential 8 guidance, especially MFA (aka.ms/e8guides)
-   Microsoft Azure **Identity Security Compass** - [Microsoft Security Best Practices](https://learn.microsoft.com/en-us/security/compass/compass)
-   Active Directory - [Best Practices for Securing Active Directory](https://learn.microsoft.com/en-us/windows-server/identity/ad-ds/plan/security-best-practices/best-practices-for-securing-active-directory)

### **AD onPrem**

A list of resources from DART perspective on Active Directory - courtesy
of Matt Zorich (Twitter @reprise99)

-   BloodHound Edges
<https://bloodhound.readthedocs.io/en/latest/data-analysis/edges.html>
-   AD Security
<https://adsecurity.org/?page_id=4031>
-   [iRed Team](https://t.co/Y4BRxwdLu5) notes
[https://ired.team/offensive-security-experiments/active-directory-kerberos-abuse...](https://t.co/0w3Uo7TOSI)
-   SID History Persistence
[https://adsecurity.org/?p=1772](https://t.co/M7QX7w31Fw)
-   How AdminSdHolder & SDProp work
[https://techcommunity.microsoft.com/t5/ask-the-directory-services-team/five-common-questions-about-adminsdholder-and-sdprop/ba-p/396293...](https://t.co/5HPCBDnuZG)
-   Recovering from systemic identity compromise
[https://learn.microsoft.com/en-us/azure/security/fundamentals/recover-from-identity-compromise](https://t.co/Dfp1IWkS7z)
-   Abusing Active Directory ACLs/ACEs
[https://book.hacktricks.xyz/windows-hardening/active-directory-methodology/acl-persistence-abuse...](https://t.co/ZWUMlP58yv)
-   Defender for Identity Alerts Overview
[https://learn.microsoft.com/en-us/defender-for-identity/alerts-overview...](https://t.co/kkqqFsEB6i)
-   Best practices for securing AD
[https://learn.microsoft.com/en-us/windows-server/identity/ad-ds/plan/security-best-practices/best-practices-for-securing-active-directory](https://t.co/a2suvfmpZm)
-   Mimikatz DCSync Abuse
[https://adsecurity.org/?p=1729](https://t.co/K51OQsXWSy)
-   Kerberoasting Overview
[https://ired.team/offensive-security-experiments/active-directory-kerberos-abuse/t1208-kerberoasting...](https://t.co/EqWNu84RoG)
-   Monitoring AD for signs of compromise
[https://learn.microsoft.com/en-us/windows-server/identity/ad-ds/plan/security-best-practices/monitoring-active-directory-for-signs-of-compromise](https://t.co/enuOOAjAr1)

### **Identity**

-   Best Practices
<https://learn.microsoft.com/en-us/security/compass/compass>
-   From Jeffrey Appel
<https://jeffreyappel.nl/tips-for-preventing-against-new-modern-identity-attacks-aitm-mfa-fatigue-prt-oauth/>
    look at Partner section
-   MDCA (was MCAS) policies from AADIP P2 moving to D365 Console
    -   <https://learn.microsoft.com/en-us/microsoft-365/security/defender/microsoft-365-security-center-defender-cloud-apps?view=o365-worldwide&WT.mc_id=AZ-MVP-5004291#control>
    -   <https://www.linkedin.com/posts/sami-lamppu_microsoft-defender-for-cloud-apps-in-microsoft-activity-7011278821773471744-TcvX>?

### **Exchange Permissions check**

These two are subtly different, the first is on mailboxes, the second is
more focused on the Outlook Folders

-   <https://office365itpros.com/2020/03/16/exchange-online-mailbox-permissions/>
-    <https://github.com/12Knocksinna/Office365itpros/blob/master/ReportMailboxPermissionsMailboxes.PS1>
-   <https://office365itpros.com/2020/03/23/reporting-exchange-online-folder-permissions/>
-    <https://github.com/12Knocksinna/Office365itpros/blob/master/ReportPermissionsFolderLevel.PS1>
