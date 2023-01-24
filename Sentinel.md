## **Sentinel Tips from the Field**

![Microsoft Sentinel](https://learn.microsoft.com/en-us/azure/sentinel/media/best-practices/azure-sentinel-and-other-services.png)

!!! tip "You want SOAR?" 

    -   Most folks skip Defender in preference for Sentinel...  
    -   Start from the desired outcome and work your way back from there
    -   What is it that SecOps need? - more automation, less manual work ;-)
    -   What does that look like? Showcase an example from Contoso Hotels
    -   Enable Automated Investigation & Remediation (AIR) at MDI, MDO, MDE and M365 Defender console levels - **don't skip this!** - as this enables SOAR "at source"
    -   Now that we have the first level triage in place, let's now move on to Sentinel...

### **Ways of working**

-   Raw logs by their very nature have a significant cost related to **"data gravity"** - the more Customers move/copy the logs the more complex the environment as well as more expensive the solution becomes - the design principle that should be recommend is to adhere to the MS Best Practices as much as possible.
    <https://learn.microsoft.com/en-us/azure/sentinel/best-practices-data>
-   Should there be any business justification or requirement for "raw logs" please consider a much more efficient method is the ability to stream "advanced hunting" events
-   Please make sure that any request from SecOps for **anything** more than Alerts/Incidents (like request for raw data) is balanced against cost via Business Case Justification
-   Why ingest or duplicate massive data sets across multiple systems based on a "just in case" scenario
-   A much more efficient system would be to define the "advanced hunting" event that is being searched for and as and when matches are discovered the event is forwarded
-   This process will respect data gravity and reduce costs significantly
-   More information can be found here: [Advanced hunting event collection](https://docs.microsoft.com/en-us/azure/sentinel/microsoft-365-defender-sentinel-integration#advanced-hunting-event-collection)

#### **Reducing TTR**
-   General recommendation is for Customers to focus efforts on increasing efficiency and reducing TTR (time to remediate) via Automation & SOAR natively within Microsoft Sentinel will naturally improve C3 (SecOps) efficiency without the need for any additional tools.
    -   **More information:**
    -   [CISO series: Lessons learned from the Microsoft SOC---Part 3a: Choosing SOC tools](https://www.microsoft.com/security/blog/2019/10/07/ciso-series-lessons-learned-from-the-microsoft-soc-part-3a-choosing-soc-tools/)
    -   [CISO series: Lessons learned from the Microsoft SOC---Part 3b: A day in the life](https://www.microsoft.com/security/blog/2019/12/23/ciso-series-lessons-learned-from-the-microsoft-soc-part-3b-a-day-in-the-life/)
    -   [CISO Series: Lessons learned from the Microsoft SOC---Part 3c: A day in the life part 2](https://www.microsoft.com/security/blog/2020/05/04/lessons-learned-microsoft-soc-part-3c/)

-   Focus on bringing all source logging relevant to the Users Device into the one location where it can be corelated quickly and seamlessly into a SOAR process to reduce friction and improve TTR times for SecOps
-   More information
<https://docs.microsoft.com/en-us/azure/sentinel/microsoft-365-defender-sentinel-integration>


### **Enable Telemetry**

-   Best practices for Microsoft Sentinel
<https://learn.microsoft.com/en-us/azure/sentinel/best-practices>
-   Best practices for designing a Microsoft Sentinel or Azure Defender for Cloud workspace
<https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/best-practices-for-designing-a-microsoft-sentinel-or-azure/ba-p/832574>
-   Extend Microsoft Sentinel across workspaces and tenants
<https://learn.microsoft.com/en-us/azure/sentinel/extend-sentinel-across-workspaces-tenants>
-   Microsoft Sentinel workspace architecture best practices
<https://learn.microsoft.com/en-us/azure/sentinel/best-practices-workspace-architecture>

### **Validate and Test**

-   How to Generate Microsoft Sentinel Incidents for Testing and Demos
<https://rodtrent.substack.com/p/how-to-generate-microsoft-sentinel>

-   Microsoft Sentinel — Testing detection rules like a Ninja
<https://rogierdijkman.medium.com/microsoft-sentinel-testing-detection-rules-like-a-ninja-cac612944dd1>

-   Learning with the Microsoft Sentinel Training Lab
<https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/learning-with-the-microsoft-sentinel-training-lab/ba-p/2953403>

### **Enable Reporting**

-   Tutorial: Create a Power BI report from Microsoft Sentinel data
<https://learn.microsoft.com/en-us/azure/sentinel/powerbi>

-   Investigate incidents with Microsoft Sentinel
<https://learn.microsoft.com/en-us/azure/sentinel/investigate-cases> 

-   Automatically create incidents from Microsoft security alerts
<https://learn.microsoft.com/en-us/azure/sentinel/create-incidents-from-alerts>

### **Review and Improve as needed**

-   Need to migrate from your old SIEM?
<https://learn.microsoft.com/en-us/azure/sentinel/migration>

#### **Filtering Logs** 

   Can be used to reduce data noise, reduce ingestion and retention/storage costs with the goal being to focus on the logs and events that are relevant - This is typically performed by one of the methods for the following scenarios:

   -   Server Log Ingestion - Azure Monitor Agent Directly can filter out logs that are not relevant for Microsoft Sentinel 
   <https://docs.microsoft.com/en-us/azure/sentinel/best-practices-data#filter-your-logs-before-ingestion>

   -    Syslog and CEF Ingestion -- Using a log forwarder such as Logstash can parse the logs based on Customers defined rules
   <https://docs.microsoft.com/en-us/azure/sentinel/best-practices-data#filter-your-logs-before-ingestion>

   -    Custom REST API Ingestion -- Via the Function or Logic App, data can be stripped away prior to sending to Microsoft sentinel - please see following two links
   <https://learn.microsoft.com/en-us/azure/sentinel/data-transformation>
   <https://learn.microsoft.com/en-us/azure/sentinel/configure-data-transformation>


### **Cost Optimization**
-   Who knew? right ;) everyone  who has installed this finds it's too expensive?
-   It's actually not - **IF** you're diligent and methodical about how you care and look after your Sentinel deployment **AFTER** it's deployed
-   Almost like any piece of software - it needs to have an SDLC approach - once deployed (and indeed, every time you add another Data Connector) set a calendar reminder to go back and review costs/storage/trends a month later - exactly 
-   Here's some other tips...

-   Free data sources
<https://learn.microsoft.com/en-us/azure/sentinel/billing?tabs=free-data-meters#free-data-sources>
-   View costs by using cost analysis
<https://learn.microsoft.com/en-us/azure/sentinel/billing-monitor-costs#view-costs-by-using-cost-analysis>
-   Run KQL queries to understand your data ingestion
<https://learn.microsoft.com/en-us/azure/sentinel/billing-monitor-costs#run-queries-to-understand-your-data-ingestion>
-   Deploy a workbook to visualize data ingestion
<https://learn.microsoft.com/en-us/azure/sentinel/billing-monitor-costs#deploy-a-workbook-to-visualize-data-ingestion>
-   Separate non-security data in a different workspace
<https://learn.microsoft.com/en-us/azure/sentinel/billing-reduce-costs#separate-non-security-data-in-a-different-workspace>
-   Optimize Log Analytics costs with dedicated clusters
<https://learn.microsoft.com/en-us/azure/sentinel/billing-reduce-costs#optimize-log-analytics-costs-with-dedicated-clusters>
-   Filter your logs before ingestion
<https://learn.microsoft.com/en-us/azure/sentinel/best-practices-data#filter-your-logs-before-ingestion>


**Sentinel Free Data ingestion:** always remember "data collection" is NOT detection!!

-   Microsoft Sentinel **benefit** for Microsoft 365 E5 Customers
<https://azure.microsoft.com/en-us/offers/sentinel-microsoft-365-offer/>
-   Security Data Types inc. in **500Mb daily allowance**
<https://docs.microsoft.com/en-us/azure/defender-for-cloud/enhanced-security-features-overview#what-data-types-are-included-in-the-500-mb-data-daily-allowance>
-   Cost Optimization tips from Rod Trent
<https://github.com/rod-trent/Azure-Sentinel-Cost-Troubleshooting-Kit>
    -   [Managing Costs for Azure Monitor Logs]("https://github.com/rod-trent/Azure-Sentinel-Cost-Troubleshooting-Kit/blob/main/Docs/Managing%20Costs%20for%20Azure%20Monitor%20Logs.md") 
    -   [Pricing Calculators](https://github.com/rod-trent/Azure-Sentinel-Cost-Troubleshooting-Kit/blob/main/Docs/Notes-and-Resources.md)
    -   [KQL Queries](https://github.com/rod-trent/Azure-Sentinel-Cost-Troubleshooting-Kit/tree/main/KQL-Queries)
    -   [Clive's Workspace Workbook](https://github.com/rod-trent/Azure-Sentinel-Cost-Troubleshooting-Kit/blob/main/Workbooks/External-Resource-List.md)


This recent addition below looks adventerous - but you might at least want to review the logic and have an alert sent to the team when you should be **prompted** to review or change the pricing tier? Don't forget to make sure the LAW is changed as well at the same time :)

-   Automatically auto-scale your Sentinel pricing tiers:
<https://koosg.medium.com/auto-scale-your-sentinel-pricing-tiers-3d1f46b4c6ce>

The following table shows how Microsoft Sentinel and Log Analytics costs appear in the Service name and Meter columns of your Azure bill for free data services. For more information, see [View Data Allocation Benefits](https://docs.microsoft.com/en-us/azure/azure-monitor/usage-estimated-costs#view-data-allocation-benefits).

> ![](./images/image8.png)

### **Sentinel - Recommendation to enable M365 Defender Connector**
- More information: <https://docs.microsoft.com/en-us/azure/sentinel/microsoft-365-defender-sentinel-integration>


### **Troubleshooting**

-   [Troubleshoot your CEF or Syslog data connector](https://learn.microsoft.com/en-us/azure/sentinel/troubleshooting-cef-syslog?tabs=cef)

-   [Troubleshoot Jupyter notebooks](https://learn.microsoft.com/en-us/azure/sentinel/notebooks-troubleshoot)

-   [Troubleshoot AWS S3 connector issues](https://learn.microsoft.com/en-us/azure/sentinel/aws-s3-troubleshoot)

-   [Troubleshooting your Microsoft Sentinel Solution for SAP deployment](https://learn.microsoft.com/en-us/azure/sentinel/sap/sap-deploy-troubleshoot)


### **Azure Log Management**

-   [Design a Log Analytics workspace architecture - Azure Monitor](https://learn.microsoft.com/en-us/azure/azure-monitor/logs/workspace-design)

-   [Workspace architecture best practices for Microsoft Sentinel](https://learn.microsoft.com/en-us/azure/sentinel/best-practices-workspace-architecture)

-   [Best practices for data collection in Microsoft Sentinel](https://learn.microsoft.com/en-us/azure/sentinel/best-practices-data)

-   [Incident creation rules](https://learn.microsoft.com/en-us/azure/sentinel/microsoft-365-defender-sentinel-integration#microsoft-365-defender-incidents-and-microsoft-incident-creation-rules) that need to be mindful of to avoid creating multiple Incidents

-   [Bi-directional Sync](https://learn.microsoft.com/en-us/azure/sentinel/microsoft-365-defender-sentinel-integration#working-with-microsoft-365-defender-incidents-in-microsoft-sentinel-and-bi-directional-sync) between M365 Defender & Sentinel


 

