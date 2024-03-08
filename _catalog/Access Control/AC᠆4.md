---
title: AC᠆4
permalink: /catalog/ac/ac-4/
variant: markdown
description: ""
third_nav_title: Access Control
---
# AC-4: Access Review

* **Group:** [Access Control](/catalog/ac)

## Control Statement

Perform an access review every [ac-4_prm_1] day(s) and remove unauthorised or unintended access rights within [ac-4_prm_2] day(s).

## Control Recommendations

Use tools such as AWS IAM Access Advisor or Azure AD Access Review to facilitate and manage access reviews.

## Risk Statement

Without regular access reviews and prompt removal of unauthorised or unintended access rights, there is an increased risk of lingering access, potential misuse of privileges, and compromised security, impacting the confidentiality and integrity of sensitive data.



### Parameters

| ID | Type | Description |
| -- | ---- | ----------- |
| ac-4_prm_1 | time period (days) | The time period in days of access review frequency. |
| ac-4_prm_2 | time period (days) | The time period in days of access removal deadline. |

### References


 * [MVSP 4.2: Logical access](https://mvsp.dev/)
 * [IM8 Cloud Security (IaaS and PaaS): 1.4/S13](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 On-Premise ADS (Non-S): 2.3/S1, 2.3/S6](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/On-Premise/Topics/Application-Development-Security-(For-Non-S).aspx)