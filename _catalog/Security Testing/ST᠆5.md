---
title: ST᠆5
permalink: /catalog/st/st-5/
variant: markdown
description: ""
third_nav_title: Security Testing
---
# ST-5: Vulnerability Management

* **Group:** [Security Testing](/catalog/st)

## Control Statement

Triage and then remediate or risk accept all true positive vulnerability findings discovered through security testing within the following timeframe based on severity:
 * Critical: [st-5_prm_1] day(s)
 * High: [st-5_prm_2] day(s)
 * Medium: [st-5_prm_3] day(s)
 * Low: [st-5_prm_4] day(s)


## Control Recommendations

Seek approval from the appropriate approving authority for risk acceptance.

## Risk Statement

Failure to promptly remediate vulnerabilities increases the risk of potential exploits, security breaches, and prolonged exposure to known vulnerabilities in the system.



### Parameters

| ID | Type | Description |
| -- | ---- | ----------- |
| st-5_prm_1 | time period (days) | The time period in days to remediate or risk accept critical vulnerability findings. |
| st-5_prm_2 | time period (days) | The time period in days to remediate or risk accept high vulnerability findings. |
| st-5_prm_3 | time period (days) | The time period in days to remediate or risk accept medium vulnerability findings. |
| st-5_prm_4 | time period (days) | The time period in days to remediate or risk accept low vulnerability findings. |

### References


 * [MVSP 3.4: Time to fix vulnerabilities](https://mvsp.dev/)
 * [IM8 Cloud Security (IaaS and PaaS): 1.8/S3](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 Cloud Security (IaaS and PaaS): 1.8/S4](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 On-Premise ADS (Non-S): 5.1/S3](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/On-Premise/Topics/Application-Development-Security-(For-Non-S).aspx)