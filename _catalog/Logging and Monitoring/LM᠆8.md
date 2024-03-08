---
title: LM᠆8
permalink: /catalog/lm/lm-8/
variant: markdown
description: ""
third_nav_title: Logging and Monitoring
---
# LM-8: Security Log Retention

* **Group:** [Logging and Monitoring](/catalog/lm)

## Control Statement

Retain security logs for at least [lm-8_prm_1] day(s).

## Control Recommendations

Security logs include network flow logs, cloud management logs, access logs, database logs and host logs. Retain non-security logs (e.g. application, operations and performance logs) as long as needed for incident resolution and debugging. Consider log lifecycle management automation, such as Amazon S3 Lifecycle configurations.

## Risk Statement

Failure to retain security logs increases the risk of losing crucial historical data, hindering investigations, compliance audits, and the ability to identify and respond to security incidents that occurred beyond a limited timeframe.



### Parameters

| ID | Type | Description |
| -- | ---- | ----------- |
| lm-8_prm_1 | time period (days) | The time period in days of log retention. |

### References


 * [MVSP 2.7: Logging](https://mvsp.dev/)
 * [IM8 Cloud Security (IaaS and PaaS): 1.9/S3](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 Cloud Security (IaaS and PaaS): 1.9/S9](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 Cloud Security (IaaS and PaaS): 1.9/S13](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 On-Premise IS (Non-S): 7.2/S6](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/On-Premise/Topics/Infrastructure-Security-(For-Non-S).aspx)