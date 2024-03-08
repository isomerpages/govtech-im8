---
title: AC᠆3
permalink: /catalog/ac/ac-3/
variant: markdown
description: ""
third_nav_title: Access Control
---
# AC-3: Inactive and Expired Accounts

* **Group:** [Access Control](/catalog/ac)

## Control Statement

Disable or remove accounts with developer, maintainer, or administrator access within [ac-3_prm_1] day(s) from last day of authorised use or have not been used for [ac-3_prm_2] day(s).

## Control Recommendations

Use automated checks such as AWS Config iam-user-unused-credentials-check to identify accounts and credentials that should be disabled. Consider using automated workflows such as System for Cross-domain Identity Management (SCIM) or identity lifecycle management tools.

## Risk Statement

Failure to disable or remove unused accounts or credentials with elevated access increases the risk of unauthorised access, as dormant accounts may become targets for exploitation, compromising the security of the system.



### Parameters

| ID | Type | Description |
| -- | ---- | ----------- |
| ac-3_prm_1 | time period (days) | The time period in days after account expiry. |
| ac-3_prm_2 | time period (days) | The time period in days of account inactivity. |

### References


 * [MVSP 4.2: Logical access](https://mvsp.dev/)
 * [IM8 Cloud Security (IaaS and PaaS): 1.4/S15](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 Cloud Security (IaaS and PaaS): 1.4/S18b](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 On-Premise ADS (Non-S): 2.3/S2, 2.3/S3](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/On-Premise/Topics/Application-Development-Security-(For-Non-S).aspx)
