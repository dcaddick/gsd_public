## MDI (Microsoft Defender for Identity):

## Ways of working
First decision point - do you have **ANY** Domain Controllers within your environment? If so then you should install MDI **NOW** and make it the very top of your Security ToDo list.

Anecdotes:

-   Small Customer in 2018, back when this was called "Azure ATP", installed only as a PoC and in under 48 hours it had identified a mis-configured Server that was exposed to the internet and was being brute-forced via RDP from Eastern Europe.
-   Larger environment 2020, client not sure but was wanting to lock down Legacy Auth, suggested that as they had E5 **strong recommendation** to deploy MDI ASAP across DC's. After getting CAB Approval to deploy, and with less than 10% coverage of DC's in just over a week it popped up with "NTDIS Exfil via SMB"
-   Security Value = **Priceless**

## Enable Telemetry

Start here - <https://learn.microsoft.com/en-us/defender-for-identity/prerequisites>

1.  Capacity planning - <https://learn.microsoft.com/en-us/defender-for-identity/capacity-planning>
2.   Download the Sizing tool - <https://github.com/microsoft/ATA-AATP-Sizing-Tool/releases>
3.   Download the Sensor - <https://learn.microsoft.com/en-us/defender-for-identity/download-sensor>
4.   Install the Sensor on DC's - <https://learn.microsoft.com/en-us/defender-for-identity/install-sensor>
5.   Basic Settings that you should review **NOW** - <https://www.microsoft.com/videoplayer/embed/RWFVEX>

This will do for now, especially if you are in a crisis mode, check the console for the DC's being online - now move on to validation below.
Please follow up with all other Configuration steps as soon as practible, especially if you also have ADFS in play. 
For ADFS please also check - <https://learn.microsoft.com/en-us/defender-for-identity/active-directory-federation-services>

![](https://learn.microsoft.com/en-us/defender-for-identity/media/architecture-topology.png)

## Validate and Test

Be conscious that if you are testing that MDI is working correctly that this may trigger **high impact** Alerts to your Blue Team or existing SecOps IF it's already installed and being monitored - or for that matter if another tooling is in place to monitor the same behaviour - so if doing some major testing it's worthwhile letting them know before hand? And on that, make sure you schedule some time to review afterwards about what testing/alerting was created & what was visible from a SecOps perspective? 

This would be valuable lessons on effectiveness - even more so if there is missing alerts?? :( 

-   Specific Validation information - <https://learn.microsoft.com/en-us/defender-for-identity/configure-sensor-settings#validate-installations>
-   Make sure that Advanced Settings has Integration enabled - <https://learn.microsoft.com/en-us/defender-for-identity/classic-integrate-mde>
-   Make doubly sure this Integration is enabled between ALL elements of MDI, MDE, MDO, MDCA and the M365 Defender Console
![](https://learn.microsoft.com/en-us/defender-for-identity/media/msde-enable.png)
-   Use Attack Simulations to **validate MDI is installed correctly** and Alerts are being surfaced accurately:
    <https://learn.microsoft.com/en-us/defender-for-identity/playbooks>
-   Use Labs for **in depth checking**: <https://learn.microsoft.com/en-us/defender-for-identity/playbook-lab-overview>
-   <https://learn.microsoft.com/en-us/defender-for-identity/playbook-domain-dominance>
-   Go to <https://portal.atp.azure.com> and if you see this, it's not been installed correctly
![](./images/image3.png)

## Enable Reporting

Once enabled you should now have a lot more visibility into the Security Posture of the onPrem environment - including the following:

-    Domain controllers with Print Spooler service available
-    Dormant entities in sensitive groups
-    Entities exposing credentials in clear text
-    Microsoft LAPS usage
-    Legacy protocols usage
-    Riskiest lateral movement paths (LMP)
-    Unmonitored domain controllers
-    Unsecure account attributes
-    Unsecure domain configurations
-    Unsecure Kerberos delegation
-    Unsecure SID History attributes
-    Weak cipher usage

More details can be found here & example below - <https://learn.microsoft.com/en-us/defender-for-identity/security-assessment#assessment-reports>
![](https://learn.microsoft.com/en-us/defender-for-identity/media/select-assessment.png)

## Review and Improve as needed

-   Review Security Assessments to validate what potentially needs remediation: <https://learn.microsoft.com/en-us/defender-for-identity/security-assessment#assessment-reports>
-   Full list of the 44 Alerts that are being checked on your behalf when fully deployed: <https://learn.microsoft.com/en-us/defender-for-identity/alerts-overview>
-   If you do not use the default Administrator account (ideally have it disabled?) then please add it to the Honeytoken account list: <https://learn.microsoft.com/en-us/defender-for-identity/entity-tags#honeytoken-tags>
-   Audit checking via Sentinel for MDI - <https://thalpius.com/2022/12/14/microsoft-defender-for-identity-auditing-checker-using-sentinel>

## Troubleshooting

-   <https://learn.microsoft.com/en-us/defender-for-identity/troubleshooting-known-issues>
-   <https://learn.microsoft.com/en-us/defender-for-identity/troubleshooting-using-logs>


