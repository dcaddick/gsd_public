## ASD Essential 8 (now ACSC)

-   Great high level on all Essential 8 - <https://www.microsoft.com/en-au/business/topic/security/essential-eight/>
-   6 videos that walk thru - <https://info.microsoft.com/AU-SCRTY-CATALOG-FY21-02Feb-14-TheEssentialEightforSecurityinPractice-SRDEM61939_CatalogDisplayPage.html>
-   MCRA <https://aka.ms/MCRA> or <https://learn.microsoft.com/en-us/security/cybersecurity-reference-architecture/mcra>
-   General on Essential 8 - <https://www.microsoft.com/en-au/business/topic/security/>
-   Daily backups: <https://www.microsoft.com/en-au/business/topic/security/essential-eight/daily-backups/>
-   Australian IRAP - <https://learn.microsoft.com/en-us/azure/compliance/offerings/offering-australia-irap> & <https://servicetrust.microsoft.com/Viewpage/AustraliaIRAP>
-   Local Australian guide in Service Trust Portal <https://aka.ms/e8guides>

### Hardening Guidance from ACSC:

-   <https://www.cyber.gov.au/acsc/view-all-content/publications/hardening-microsoft-windows-10-version-21h1-workstations>
-   <https://www.cyber.gov.au/acsc/view-all-content/publications/hardening-microsoft-365-office-2021-office-2019-and-office-2016>
-   <https://www.cyber.gov.au/acsc/view-all-content/publications/microsoft-office-macro-security>
-   <https://github.com/microsoft/Intune-ACSC-Windows-Hardening-Guidelines>
-   [Windows Security Baseline (for use with ACSC Windows Hardening Guidelines)](https://github.com/microsoft/Intune-ACSC-Windows-Hardening-Guidelines/blob/main/policies/Windows%20Security%20Baseline%20(for%20use%20with%20ACSC%20Windows%20Hardening%20Guidelines).json)
-   [ACSC Windows Hardening Guidelines-Attack Surface Reduction](https://github.com/microsoft/Intune-ACSC-Windows-Hardening-Guidelines/blob/main/policies/ACSC%20Windows%20Hardening%20Guidelines-Attack%20Surface%20Reduction.json)
-   WDAC Policy creation from DTA - <https://desktop.gov.au/blueprint/abac/wdac-policy-creation.html>

### Hardening Azure AD:

-   [Secure your Azure AD identity infrastructure - Azure Active Directory](https://learn.microsoft.com/en-us/azure/security/fundamentals/steps-secure-identity)
-   Also worth reviewing our Essential 8 guidance, especially MFA (aka.ms/e8guides)
-   Microsoft Azure **Identity Security Compass** - [Microsoft Security Best Practices](https://learn.microsoft.com/en-us/security/compass/compass)
-   Active Directory - [Best Practices for Securing Active Directory](https://learn.microsoft.com/en-us/windows-server/identity/ad-ds/plan/security-best-practices/best-practices-for-securing-active-directory)

### AD onPrem:

A list of resources from DART perspective on Active Directory - courtesy
of Matt Zorich (Twitter @reprise99)
-   BloodHound Edges - <https://bloodhound.readthedocs.io/en/latest/data-analysis/edges.html>
-   AD Security - <https://adsecurity.org/?page_id=4031>
-   [http://ired.team](https://t.co/Y4BRxwdLu5) notes - [https://ired.team/offensive-security-experiments/active-directory-kerberos-abuse...](https://t.co/0w3Uo7TOSI)
-   SID History Persistence - [https://adsecurity.org/?p=1772](https://t.co/M7QX7w31Fw)
-   How AdminSdHolder & SDProp work - [https://techcommunity.microsoft.com/t5/ask-the-directory-services-team/five-common-questions-about-adminsdholder-and-sdprop/ba-p/396293...](https://t.co/5HPCBDnuZG)
-   Recovering from systemic identity compromise - [https://learn.microsoft.com/en-us/azure/security/fundamentals/recover-from-identity-compromise](https://t.co/Dfp1IWkS7z)
-   Abusing Active Directory ACLs/ACEs - [https://book.hacktricks.xyz/windows-hardening/active-directory-methodology/acl-persistence-abuse...](https://t.co/ZWUMlP58yv)
-   Defender for Identity Alerts Overview - [https://learn.microsoft.com/en-us/defender-for-identity/alerts-overview...](https://t.co/kkqqFsEB6i)
-   Best practices for securing AD - [https://learn.microsoft.com/en-us/windows-server/identity/ad-ds/plan/security-best-practices/best-practices-for-securing-active-directory](https://t.co/a2suvfmpZm)
-   Mimikatz DCSync Abuse - [https://adsecurity.org/?p=1729](https://t.co/K51OQsXWSy)
-   Kerberoasting Overview - [https://ired.team/offensive-security-experiments/active-directory-kerberos-abuse/t1208-kerberoasting...](https://t.co/EqWNu84RoG)
-   Monitoring AD for signs of compromise - [https://learn.microsoft.com/en-us/windows-server/identity/ad-ds/plan/security-best-practices/monitoring-active-directory-for-signs-of-compromise](https://t.co/enuOOAjAr1)

### Identity:

-   Best Practices: <https://learn.microsoft.com/en-us/security/compass/compass>
-   <https://jeffreyappel.nl/tips-for-preventing-against-new-modern-identity-attacks-aitm-mfa-fatigue-prt-oauth/>
    look at Partner section
-   MDCA (was MCAS) policies from AADIP P2 moving to D365 Console
-   <https://learn.microsoft.com/en-us/microsoft-365/security/defender/microsoft-365-security-center-defender-cloud-apps?view=o365-worldwide&WT.mc_id=AZ-MVP-5004291#control>
-   <https://www.linkedin.com/posts/sami-lamppu_microsoft-defender-for-cloud-apps-in-microsoft-activity-7011278821773471744-TcvX>?

### Exchange Permissions check:

-   <https://office365itpros.com/2020/03/16/exchange-online-mailbox-permissions/>
-    <https://github.com/12Knocksinna/Office365itpros/blob/master/ReportMailboxPermissionsMailboxes.PS1>
-   <https://office365itpros.com/2020/03/23/reporting-exchange-online-folder-permissions/>
-    <https://github.com/12Knocksinna/Office365itpros/blob/master/ReportPermissionsFolderLevel.PS1>
> The two are subtly different, the first is on mailboxes, the second is
> more focused on the Outlook Folders
