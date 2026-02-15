## **ASD Essential 8 (now ACSC)**

- **Please start with this - ACSC Essential 8 – Health Report in Microsoft Sentinel**
<https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/acsc-essential-8-health-report-in-microsoft-sentinel/ba-p/3755702>
![](https://techcommunity.microsoft.com/t5/s/gxcuf89792/images/bS0zNzU1NzAyLTQ0NjUxNGkzM0RCODE5QjU4RjA2MEJB)

- Great high level on all Essential 8
<https://aka.ms/e8guides>
- Collection of Australian M365 content on Essential 8
<https://m365maps.com/australia.htm>
- Microsoft Cybersecurity Reference Architecture
 <https://aka.ms/MCRA> or <https://learn.microsoft.com/en-us/security/cybersecurity-reference-architecture/mcra>
- General on Essential 8
<https://learn.microsoft.com/en-us/compliance/anz/e8-overview>
- Daily backups
<https://learn.microsoft.com/en-us/compliance/anz/e8-backups>
- Australian IRAP
<https://learn.microsoft.com/en-us/azure/compliance/offerings/offering-australia-irap> & <https://servicetrust.microsoft.com/Viewpage/AustraliaIRAP>
- Implmenting Essential 8 with Microsoft tooling
![](./images/Essential-8.png)

**Local Australian E8 Guides**

- Microsoft Service Trust Portal has the local Essential 8 guides  <https://aka.ms/e8guides> here you will find the documentations covering the following specifics (dated Aug 2023)

- Microsoft General - Essential Eight - Config Macros
- Microsoft General - Essential Eight - User Application Hardening
- Microsoft General - Essential Eight - Restricting Admin Priv
- Microsoft General - Essential Eight - Patch OS
- Microsoft General - Essential Eight - Backup
- Microsoft General - Essential Eight - Patch Applications
- Microsoft General - Essential Eight - MFA

### **Hardening Guidance from ACSC**

- For Windows 10 21H1
<https://www.cyber.gov.au/acsc/view-all-content/publications/hardening-microsoft-windows-10-version-21h1-workstations>

- For Office
<https://www.cyber.gov.au/acsc/view-all-content/publications/hardening-microsoft-365-office-2021-office-2019-and-office-2016>

- For Macro's
  - Restricting Microsoft Office Macros <https://www.cyber.gov.au/resources-business-and-government/maintaining-devices-and-systems/system-hardening-and-administration/system-hardening/restricting-microsoft-office-macros> &
  - Technical example: Configure macro settings <https://www.cyber.gov.au/resources-business-and-government/essential-cyber-security/small-business-cyber-security/small-business-cloud-security-guide/technical-example-configure-macro-settings>

- For Intune
<https://github.com/microsoft/Intune-ACSC-Windows-Hardening-Guidelines>
- WDAC Policy creation from DTA
<https://desktop.gov.au/blueprint/abac/wdac-policy-creation.html>

### **AD onPrem**

A list of resources from DART perspective on Active Directory - courtesy
of Matt Zorich (X @reprise99)

- BloodHound Edges
<https://bloodhound.readthedocs.io/en/latest/data-analysis/edges.html>
- AD Security
<https://adsecurity.org/?page_id=4031>
- [iRed Team](https://t.co/Y4BRxwdLu5) notes
[https://ired.team/offensive-security-experiments/active-directory-kerberos-abuse...](https://t.co/0w3Uo7TOSI)
- SID History Persistence
[https://adsecurity.org/?p=1772](https://t.co/M7QX7w31Fw)
- How AdminSdHolder & SDProp work
[https://techcommunity.microsoft.com/t5/ask-the-directory-services-team/five-common-questions-about-adminsdholder-and-sdprop/ba-p/396293...](https://t.co/5HPCBDnuZG)
- Recovering from systemic identity compromise
[https://learn.microsoft.com/en-us/azure/security/fundamentals/recover-from-identity-compromise](https://t.co/Dfp1IWkS7z)
- Abusing Active Directory ACLs/ACEs
[https://book.hacktricks.xyz/windows-hardening/active-directory-methodology/acl-persistence-abuse...](https://t.co/ZWUMlP58yv)
- Defender for Identity Alerts Overview
[https://learn.microsoft.com/en-us/defender-for-identity/alerts-overview...](https://t.co/kkqqFsEB6i)
- Best practices for securing AD
[https://learn.microsoft.com/en-us/windows-server/identity/ad-ds/plan/security-best-practices/best-practices-for-securing-active-directory](https://t.co/a2suvfmpZm)
- Mimikatz DCSync Abuse
[https://adsecurity.org/?p=1729](https://t.co/K51OQsXWSy)
- Kerberoasting Overview
[https://ired.team/offensive-security-experiments/active-directory-kerberos-abuse/t1208-kerberoasting...](https://t.co/EqWNu84RoG)
- Monitoring AD for signs of compromise
[https://learn.microsoft.com/en-us/windows-server/identity/ad-ds/plan/security-best-practices/monitoring-active-directory-for-signs-of-compromise](https://t.co/enuOOAjAr1)

### **Exchange Permissions check**

These two are subtly different, the first is on mailboxes, the second is
more focused on the Outlook Folders

- <https://office365itpros.com/2020/03/16/exchange-online-mailbox-permissions/>
- <https://github.com/12Knocksinna/Office365itpros/blob/master/ReportMailboxPermissionsMailboxes.PS1>
- <https://office365itpros.com/2020/03/23/reporting-exchange-online-folder-permissions/>
- <https://github.com/12Knocksinna/Office365itpros/blob/master/ReportPermissionsFolderLevel.PS1>
