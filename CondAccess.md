![](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSu_LHXQ7ucR3-MQZM3NO-a4_WRckjsP9FcUA&usqp=CAU)

## **Ways of working**
First decision point - how are we going to do this?
Questions to help you determine this are:

1.   Is it small or a large Tenancy?
2.   Do we want to avoid CAB approval process for a PoC?
3.   Need it done right now to address a strategic problem?
4.   Do we want to go fast, or take our time?
5.   If you are a Partner or MSSP please choose the "As-Code" method

Result:

* Fast and quick - start with telemetry below and do it on the fly using the 14 default Policies in ReportOnly Mode, iterate from there...
    [View 14 x CA Policy Templates](https://portal.azure.com/#view/Microsoft_AAD_ConditionalAccess/CaTemplates.ReactView)
* Larger implmentations - please take the time to review the process below to enable via "CA-as-Code" as the ROI is well worth it - especially if doing it for more than one customer or tenant :wink:


## **Enable Telemetry**
!!! warning "**NOTE: please be aware there is no inherent "BLOCK" by default**"
    You need to make sure you are BLOCKING by default unless explicitly allowing access - walk thru the 14 default Policies to better understand this. To make sure that you are fully covered please use this PowerBI based tool **<https://github.com/AzureAD/AzureADAssessment>** 
    **Confirm your maturity based on this Tool ^^^^^^**
     ![](./images/AzureADAssessmentTool.png)

## **Alternative way to check CA policies**
<https://idpowertoys.com/>
Use the "CA Documentor" link on the left & click on "Manual Generation" to be able to submit via JSON if you are concerned about the level of permissions required to generate as an App
![](https://idpowertoys.com/assets/whatsnew/cadocgen.png)


!!! Note
    **UPDATE** 142 Page - CA demystified Whitepaper - still to be reviewed 
    <https://github.com/kennethvs/cabaseline202212/blob/main/Conditional%20Access%20demystified-v1.4%20-%20December%202022.pdf>
  

## **The Microsoft content**

-   Design
<https://learn.microsoft.com/en-us/azure/architecture/guide/security/conditional-access-design>
-   Architecture
<https://learn.microsoft.com/en-us/azure/architecture/guide/security/conditional-access-architecture>
-   Framework
<https://learn.microsoft.com/en-us/azure/architecture/guide/security/conditional-access-framework>
-   API
<https://learn.microsoft.com/en-us/azure/active-directory/conditional-access/howto-conditional-access-apis>
-   Deployment
<https://github.com/Azure-Samples/azure-ad-conditional-access-apis/tree/main/03-deploy>
-   Plan
<https://learn.microsoft.com/en-us/azure/active-directory/conditional-access/plan-conditional-access>
-   CA for Cloud Apps
<https://learn.microsoft.com/en-us/azure/active-directory/conditional-access/concept-conditional-access-cloud-apps>
-   Concept for CA Policies
<https://learn.microsoft.com/en-us/azure/active-directory/conditional-access/concept-conditional-access-policies>
-   Docs
<https://learn.microsoft.com/en-us/azure/active-directory/conditional-access/>
-   Powershell syntax and examples
<https://learn.microsoft.com/en-us/powershell/module/azuread/get-azureadmsconditionalaccesspolicy?view=azureadps-2.0>
-   Deep dive: How does Conditional Access block Legacy Authentication?
<https://techcommunity.microsoft.com/t5/itops-talk-blog/deep-dive-how-does-conditional-access-block-legacy/ba-p/3265345>


!!! Note 
    Here is a great companion for Sentinel:

    <https://danielchronlund.com/2022/04/21/a-powerfull-conditional-access-change-dashboard-for-microsoft-sentinel/>
>

## **Automation of "CA-as-Code"**

-   Thomas N. - <https://www.cloud-architekt.net/speaking/> The most recent deck -- 2022-06-11 Scottish Summit 2022 "Deploying and Managing Conditional Access at Scale" [Slides](https://github.com/Cloud-Architekt/meetups/blob/master/2022-06-10%20ScottishSummit-Deploying-and-Managing-ConditionalAccess-at-Scale.pdf)

-   Excellent article here that is really worth the time reading as this will highlight how to enable this in detail: <https://www.cloud-architekt.net/aadops-conditional-access/>

![](https://www.cloud-architekt.net/assets/images/2021-08-11-aadops-conditional-access/aadops4.png)

!!! Tip
    He also points out the others that have done great work in this space:

-   Fortigi/ConditionalAccess
<https://github.com/Fortigi/ConditionalAccess> 
-   AlexFilipin/ConditionalAccess
<https://github.com/AlexFilipin/ConditionalAccess>
-   DanielChronlund/DCToolbox: Tools for Microsoft cloud fans <https://github.com/DanielChronlund/DCToolbox>

!!! Info
    One other important point -- don't get caught up trying to manage GUID's:
-   [Fortigi has published some build scripts on GitHub](https://github.com/Fortigi/ConditionalAccess) to convert those GUIDs to readable display names.
-   This also covers known GUIDs such as AAD Role and Application ID to DisplayName.

## **Validate and Test**

-   Use the WhatIf tool
<https://learn.microsoft.com/en-us/azure/active-directory/conditional-access/what-if-tool>

-   Thomas's page on AAD Ops
<https://www.cloud-architekt.net/aadops-conditional-access/>


## **Enable Reporting**

-   How to enable Reporting for CA
<https://learn.microsoft.com/en-us/azure/active-directory/conditional-access/howto-conditional-access-insights-reporting>

## **Review and Improve as needed**

-   Rerun check with AzureAD Assessment Tool

-   Possible alternative to AAD Assessment tool - [CAOptics](<https://github.com/jsa2/caOptics>) 

## **Troubleshooting**

-   Troubleshoot Conditional Access policy
<https://learn.microsoft.com/en-us/azure/active-directory/conditional-access/plan-conditional-access#troubleshoot-conditional-access-policy>

-   Check for common misconfigurations
<https://www.trustedsec.com/blog/common-conditional-access-misconfigurations-and-bypasses-in-azure/>
