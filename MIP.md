
This page will also cover Data Loss Prevention (DLP), but we'll probably build out a whole new section on Purview as this site matures, thank you for your patience - please feel free to provide feedback via raising an issue in Github.

First up - to a certain degree, you will find a lot of what you need here in the OSS page for **"Purview Customer Experience Engineering"** page - please start here: [Microsoft Purview One-Stop-Shop (OSS)](<https://microsoft.github.io/ComplianceCxE/>) **<-- Start Here**

You might also note that it uses Material for MkDocs as well ;-)

### **Ways of working**
-   Look to enable Insider Risk & Communications compliance first
-   This will identify specific use cases & Business Value almost immediately
-   These can then be used to flesh out the current risks and security challenges that **need** to be addressed ASAP
-    Start using Adaptive Protection for DLP controls to address immediate needs and pivot from this quick start to flesh out additional use cases with Project Management


### **Latest update**
-   MIP/AIP - <https://techcommunity.microsoft.com/t5/security-compliance-and-identity/azure-information-protection-and-the-information-protection/ba-p/3671070>
-   Adaptive Protection (DLP rules based on Insider Risk)
-   Login as GA (or eqiv.) - <https://admin.microsoft.com/adminportal/home?Q=ADG#/modernonboarding/mipsetupguide>
-   ![](./images/image2.png)
-   Docs - <https://learn.microsoft.com/en-gb/microsoft-365/compliance/information-protection>
-   DLP - <https://learn.microsoft.com/en-gb/microsoft-365/compliance/dlp-learn-about-dlp>
-   What's new - <https://learn.microsoft.com/en-gb/microsoft-365/compliance/whats-new>

## **Naming evolution - AIP/MIP/MPIP**

Note that while some documentation still references "Azure Information Protection", management and usage of these capabilites from within the Azure Portal have been deprecated as of January 2023. Management of the Information Protection scanner's capability is now performed from within the [Information protection scanner](https://compliance.microsoft.com/compliancesettings) menu within the Purview Compliance portal but still requires the Azure Information Protection Unified Labeling Client. Click here for details on deployment of the [Unified Labeling Client](https://learn.microsoft.com/en-us/microsoft-365/compliance/deploy-scanner-configure-install).

The "Microsoft Information Protection" name, along with other compliance and unified data governance products, were updated in 2022 to include "Purview" name. As such it's now called "Microsoft Purview Information Protection". For additional updates to the renaming of our compliance products reference this [blog post](https://www.microsoft.com/en-us/security/blog/2022/04/19/the-future-of-compliance-and-data-governance-is-here-introducing-microsoft-purview/)

## **DLP products**
| Product / Service | Data Location | Use case |
|---|---|---|
| [Microsoft Purview Data Loss Prevention](https://compliance.microsoft.com/datalossprevention) | Endpoints, M365 data locations, bridged Data Connector locations | Provides DLP capabilities primarily for M365 locations (e.g. O365, OneDrive, Teams, Yammer, SharePoint, etc.), endpoints who have Microsoft Defender for Endpoint (MDE) onboarded,  as well as locations that have been bridged to Purview via the Data Connectors capability. |
| [Microsoft Purview Information Protection Scanner](https://compliance.microsoft.com/compliancesettings/scanner_onboarding) | Endpoint locations isolated from M365 SaaS services | Use of this scanner is typically used to scan on-premesis data locations such as a file shares that the MDE agent cannot be deployed on. Additionally, it can be used to deploy DLP policies for disconnected resources that are "air-gapped" or simply isolated from the M365 SaaS offerings. This requires a secondary server within the network segment. Using this scanner to provide DLP on cloud connected resources is redundant and requires more overhead to manage.|
| [Defender for Cloud Apps](https://security.microsoft.com/cloudapps) | Microsoft and non-Microsoft cloud | With the use of "File Policies" you can address DLP for data locations that include and extend beyond M3635. Note that deployment of MDE on endpoints is required for Defender for Cloud to function.|

While MDE is the primary agent that supports most of our Microsoft Security and Compliance suite solutions, some customers may have an alternative Anti-virust/Anti-malware (AV/AM) solution and wish to run MDE in passive mode. When MDE is running in passive mode, ONLY AV/AM enforcement policies are disabled. Alerting for AV/AM, along with alerting and policy enforcement for all other Microsoft Security and Compliance solutiongs (DCA, MPIP, DLP, etc..) that leverage the MDE agent will not be affected.

## **Ninja Security Training**

-   MPIP Ninja Training : <https://aka.ms/MIPNinja>

