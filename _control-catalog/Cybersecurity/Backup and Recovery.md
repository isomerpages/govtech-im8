---
title: Backup and Recovery
permalink: /control-catalog/br/
variant: markdown
description: ""
third_nav_title: Cybersecurity
---
Controls to support backup and disaster recovery.

| Controls |
| ---- |
| [BR-1: Backup](#br-1) |
| [BR-2: Recovery Testing](#br-2) |
| [BR-3: Backup Retention](#br-3) |


<a id="br-1"></a>
## BR-1: Backup

### Control Statement

Regularly backup all important data and systems, and store backups in a secure and separate location.

### Control Recommendations

Use default CSP-managed backup services (e.g., AWS Backup, Azure Backup, GCP Backup and DR Service). Consider alternative backup services only when default CSP services cannot be used. Store backups and snapshots separately to primary data storage with data encrypted-at-rest.

### Risk Statement

Without regular backups stored in a secure and separate location, there is an increased risk of data loss, system failures, and extended downtime in the event of accidental deletion, hardware failures, or malicious attacks.



<a id="br-2"></a>
## BR-2: Recovery Testing

### Control Statement

Conduct regular testing of recovery processes to ensure their effectiveness.

### Control Recommendations

Ensure each test verifies the system's ability to fully restore all data and services.

### Risk Statement

Failure to regularly test recovery processes may result in ineffective response during actual incidents, increasing the risk of prolonged downtime, data loss, and compromised business continuity in the event of a disaster or system failure.



<a id="br-3"></a>
## BR-3: Backup Retention

### Control Statement

Prevent backups from being modified or deleted for [br-3_prm_1] day(s) or as stipulated in the agency's data retention policies.

### Control Recommendations

Use S3 Object Lock or immutable storage for Azure Blob Storage to enforce time-based retention policies.

### Risk Statement

Lack of prevention measures against the modification or deletion of backups for the specified duration increases the risk of data loss, unauthorised alterations, and potential inability to recover from incidents, compromising the integrity and availability of critical information.



#### Parameters

| ID | Type | Description |
| -- | ---- | ----------- |
| br-3_prm_1 | time period (days) | The time period in days of backup retention. |