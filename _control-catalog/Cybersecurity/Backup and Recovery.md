---
title: Backup and Recovery
permalink: /control-catalog/br/
variant: markdown
description: ""
third_nav_title: Cybersecurity
---

Controls to support backup and disaster recovery.

| Controls                                                     |
| ------------------------------------------------------------ |
| [BR-1: Backup](#br-1-backup)                                 |
| [BR-2: Recovery Testing](#br-2-recovery-testing)             |
| [BR-3: Backup Retention](#br-3-backup-retention)             |
| [BR-4: Disaster Recovery Plan](#br-4-disaster-recovery-plan) |

## BR-1: Backup

**Group:** Backup and Recovery

### Control Statement

Backup all important data and systems at least every [ insert: param, br-1_prm_1 ] day(s), and store backups in a secure and separate location.

### Control Recommendations

Use default CSP-managed backup services (e.g., AWS Backup, Azure Backup, GCP Backup and DR Service). Consider alternative backup services only when default CSP services cannot be used. Store backups and snapshots separately to primary data storage with data encrypted-at-rest. For SaaS, ensure that SaaS provider is able to restore last backup.

### Risk Statement

Without regular backups stored in a secure and separate location, there is an increased risk of data loss, system failures, and extended downtime in the event of accidental deletion, hardware failures, or malicious attacks.

### Parameters

| ID         | Type                     | Description                         |
| ---------- | ------------------------ | ----------------------------------- |
| br-1_prm_1 | time period (days) (int) | The time period in days for backup. |

### References

- [MVSP 4.4: Backup and Disaster recovery](https://mvsp.dev/)
- [IM8 Cloud Security (IaaS and PaaS): 1.2/S2](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
- [IM8 On-Premise IS (Non-S): 1.5/S1]()

## BR-2: Recovery Testing

**Group:** Backup and Recovery

### Control Statement

Conduct testing of recovery processes at least every [ insert: param, br-2_prm_1 ] day(s) to ensure their effectiveness.

### Control Recommendations

Ensure each test verifies the system's ability to fully restore all data and services.

### Risk Statement

Failure to regularly test recovery processes may result in ineffective response during actual incidents, increasing the risk of prolonged downtime, data loss, and compromised business continuity in the event of a disaster or system failure.

### Parameters

| ID         | Type                     | Description                                   |
| ---------- | ------------------------ | --------------------------------------------- |
| br-2_prm_1 | time period (days) (int) | The time period in days for recovery testing. |

### References

- [MVSP 4.4: Backup and Disaster recovery](https://mvsp.dev/)
- [IM8 Cloud Security (IaaS and PaaS): 1.2/S1d](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
- [IM8 On-Premise IS (Non-S): 1.5/S1d]()

## BR-3: Backup Retention

**Group:** Backup and Recovery

### Control Statement

Prevent backups from being modified or deleted for [ insert: param, br-3_prm_1 ] day(s) or as stipulated in the agency's data retention policies.

### Control Recommendations

Use S3 Object Lock or Azure Blob Storage with immutability enabled to enforce time-based retention policies.

### Risk Statement

Lack of prevention measures against the modification or deletion of backups for the specified duration increases the risk of data loss, unauthorised alterations, and potential inability to recover from incidents, compromising the integrity and availability of critical information.

### Parameters

| ID         | Type                     | Description                                  |
| ---------- | ------------------------ | -------------------------------------------- |
| br-3_prm_1 | time period (days) (int) | The time period in days of backup retention. |

### References

- [MVSP 4.4: Backup and Disaster recovery](https://mvsp.dev/)
- [IM8 Cloud Security (IaaS and PaaS): 1.2/S1b](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
- [IM8 On-Premise IS (Non-S): 1.5/S2c]()

## BR-4: Disaster Recovery Plan

**Group:** Backup and Recovery

### Control Statement

Develop, maintain, and regularly test a disaster recovery plan that ensures critical functions and data can be restored within the Recovery Time Objective (RTO) and Recovery Point Objective (RPO) as determined by business requirements and risk assessments.

### Control Recommendations

The disaster recovery plan should include clearly defined roles and responsibilities, step-by-step recovery procedures, communication protocols during a disaster, and integration with the overall business continuity plan. Assess the effectiveness of the existing disaster recovery plan during disaster recovery exercises.

### Risk Statement

Absence of a comprehensive disaster recovery plan increases the risk of prolonged system downtime, data loss, and inability to maintain business continuity in the event of a disaster, potentially leading to significant financial losses and damage to organisational reputation.

### References

- [MVSP 4.4: Backup and Disaster recovery](https://mvsp.dev/)
- [SP 800-53 CP-2: Contingency Plan](https://doi.org/10.6028/NIST.SP.800-53r5)
- [Cloud Controls Matrix BCR-09: Disaster Response Plan](https://cloudsecurityalliance.org/artifacts/cloud-controls-matrix-v4)
