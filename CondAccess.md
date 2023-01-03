## Conditional Access:

> **NOTE: please be aware there is no inherent "BLOCK" by default**
>
> You need to make sure you are BLOCKING by default unless explicitly allowing access - walk thru the 14 default Policies to better understand this
> To make sure that you are fully covered please use this PowerBI based tool
**<https://github.com/AzureAD/AzureADAssessment> <-- confirm your maturity based on this**
>
> <https://www.linkedin.com/feed/update/urn:li:activity:7010866303682912256?utm_source=share&utm_medium=member_ios>
  

The Microsoft content:

-   Design - <https://learn.microsoft.com/en-us/azure/architecture/guide/security/conditional-access-design>
-   Architecture - <https://learn.microsoft.com/en-us/azure/architecture/guide/security/conditional-access-architecture>
-   Framework - <https://learn.microsoft.com/en-us/azure/architecture/guide/security/conditional-access-framework>
-   API - <https://learn.microsoft.com/en-us/azure/active-directory/conditional-access/howto-conditional-access-apis>
-   Deployment - <https://github.com/Azure-Samples/azure-ad-conditional-access-apis/tree/main/03-deploy>
-   Plan - <https://learn.microsoft.com/en-us/azure/active-directory/conditional-access/plan-conditional-access>
-   CA for Cloud Apps - <https://learn.microsoft.com/en-us/azure/active-directory/conditional-access/concept-conditional-access-cloud-apps>
-   Concept for CA Policies - <https://learn.microsoft.com/en-us/azure/active-directory/conditional-access/concept-conditional-access-policies>
-   <https://learn.microsoft.com/en-us/azure/active-directory/conditional-access/>
-   <https://learn.microsoft.com/en-us/powershell/module/azuread/get-azureadmsconditionalaccesspolicy?view=azureadps-2.0>
-   <https://techcommunity.microsoft.com/t5/itops-talk-blog/deep-dive-how-does-conditional-access-block-legacy/ba-p/3265345>


> Here is a great companion for Sentinel: 
<https://danielchronlund.com/2022/04/21/a-powerfull-conditional-access-change-dashboard-for-microsoft-sentinel/>
>

### Automation of "CA-as-Code"

-   Thomas N. - <https://www.cloud-architekt.net/speaking/> The most recent deck -- 2022-06-11 Scottish Summit 2022 "Deploying and Managing Conditional Access at Scale" [Slides](https://github.com/Cloud-Architekt/meetups/blob/master/2022-06-10%20ScottishSummit-Deploying-and-Managing-ConditionalAccess-at-Scale.pdf)

-   Excellent article here that is really worth the time reading as this will highlight how to enable this in detail: <https://www.cloud-architekt.net/aadops-conditional-access/>

> He also points out the others that have done great work in this space:

-   Fortigi/ConditionalAccess: (https://github.com/Fortigi/ConditionalAccess)
-   AlexFilipin/ConditionalAccess: (https://github.com/AlexFilipin/ConditionalAccess)
-   DanielChronlund/DCToolbox: Tools for Microsoft cloud fans (https://github.com/DanielChronlund/DCToolbox)
> One other important point -- don't get caught up trying to manage GUID's:
-   [Fortigi has published some build scripts on GitHub](https://github.com/Fortigi/ConditionalAccess) to convert those GUIDs to readable display names.
-   This also covers known GUIDs such as AAD Role and Application ID to DisplayName.
