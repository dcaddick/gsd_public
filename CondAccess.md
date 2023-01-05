## Conditional Access:

!!! warning "**NOTE: please be aware there is no inherent "BLOCK" by default**"
    You need to make sure you are BLOCKING by default unless explicitly allowing access - walk thru the 14 default Policies to better understand this. To make sure that you are fully covered please use this PowerBI based tool **<https://github.com/AzureAD/AzureADAssessment>** 
    **Confirm your maturity based on this Tool ^^^^^^**

!!! Note
    **UPDATE** 142 Page - CA demystified Whitepaper - still to be reviewed 
    <https://github.com/kennethvs/cabaseline202212/blob/main/Conditional%20Access%20demystified-v1.4%20-%20December%202022.pdf>
  

**The Microsoft content:**

-   Design - <https://learn.microsoft.com/en-us/azure/architecture/guide/security/conditional-access-design>
-   Architecture - <https://learn.microsoft.com/en-us/azure/architecture/guide/security/conditional-access-architecture>
-   Framework - <https://learn.microsoft.com/en-us/azure/architecture/guide/security/conditional-access-framework>
-   API - <https://learn.microsoft.com/en-us/azure/active-directory/conditional-access/howto-conditional-access-apis>
-   Deployment - <https://github.com/Azure-Samples/azure-ad-conditional-access-apis/tree/main/03-deploy>
-   Plan - <https://learn.microsoft.com/en-us/azure/active-directory/conditional-access/plan-conditional-access>
-   CA for Cloud Apps - <https://learn.microsoft.com/en-us/azure/active-directory/conditional-access/concept-conditional-access-cloud-apps>
-   Concept for CA Policies - <https://learn.microsoft.com/en-us/azure/active-directory/conditional-access/concept-conditional-access-policies>
-   Docs - <https://learn.microsoft.com/en-us/azure/active-directory/conditional-access/>
-   Powershell syntax and examples - <https://learn.microsoft.com/en-us/powershell/module/azuread/get-azureadmsconditionalaccesspolicy?view=azureadps-2.0>
-   Deep dive: How does Conditional Access block Legacy Authentication? - <https://techcommunity.microsoft.com/t5/itops-talk-blog/deep-dive-how-does-conditional-access-block-legacy/ba-p/3265345>


!!! Note 
    Here is a great companion for Sentinel: 
    <https://danielchronlund.com/2022/04/21/a-powerfull-conditional-access-change-dashboard-for-microsoft-sentinel/>
>

### Automation of "CA-as-Code"

-   Thomas N. - <https://www.cloud-architekt.net/speaking/> The most recent deck -- 2022-06-11 Scottish Summit 2022 "Deploying and Managing Conditional Access at Scale" [Slides](https://github.com/Cloud-Architekt/meetups/blob/master/2022-06-10%20ScottishSummit-Deploying-and-Managing-ConditionalAccess-at-Scale.pdf)

-   Excellent article here that is really worth the time reading as this will highlight how to enable this in detail: <https://www.cloud-architekt.net/aadops-conditional-access/>

!!! Tip
    He also points out the others that have done great work in this space:

-   Fortigi/ConditionalAccess: (https://github.com/Fortigi/ConditionalAccess)
-   AlexFilipin/ConditionalAccess: (https://github.com/AlexFilipin/ConditionalAccess)
-   DanielChronlund/DCToolbox: Tools for Microsoft cloud fans (https://github.com/DanielChronlund/DCToolbox)

!!! Info
    One other important point -- don't get caught up trying to manage GUID's:
-   [Fortigi has published some build scripts on GitHub](https://github.com/Fortigi/ConditionalAccess) to convert those GUIDs to readable display names.
-   This also covers known GUIDs such as AAD Role and Application ID to DisplayName.
