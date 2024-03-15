---
title: BR᠆3
permalink: /catalog/br/br-3/
variant: markdown
description: ""
third_nav_title: Backup and Recovery
---
# BR-3: Backup Retention

* **Group:** [Backup and Recovery](/catalog/br)

## Control Statement

Prevent backups from being modified or deleted for [br-3_prm_1] day(s) or as stipulated in the agency&#39;s data retention policies.

## Control Recommendations

Use S3 Object Lock or immutable storage for Azure Blob Storage to enforce time-based retention policies.

## Risk Statement

Lack of prevention measures against the modification or deletion of backups for the specified duration increases the risk of data loss, unauthorised alterations, and potential inability to recover from incidents, compromising the integrity and availability of critical information.



### Parameters

| ID | Type | Description |
| -- | ---- | ----------- |
| br-3_prm_1 | time period (days) | The time period in days of backup retention. |

### References


 * [MVSP 4.4: Backup and Disaster recovery](https://mvsp.dev/)
 * [IM8 Cloud Security (IaaS and PaaS): 1.2/S1b](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 On-Premise IS (Non-S): 1.5/S2c](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/On-Premise/Topics/Infrastructure-Security-(For-Non-S).aspx)