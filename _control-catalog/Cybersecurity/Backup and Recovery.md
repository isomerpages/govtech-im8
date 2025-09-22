---
title: Backup and Recovery
permalink: /control-catalog/cybersecurity/br/
variant: markdown
description: ""
third_nav_title: Cybersecurity
---
Controls to support backup and disaster recovery.

| Controls                                                                 |
| ------------------------------------------------------------------------ |
| [BR-1: Backup](#br-1-backup)                                             |
| [BR-2: Recovery Testing](#br-2-recovery-testing)                         |
| [BR-3: Backup Retention](#br-3-backup-retention)                         |
| [BR-4: Disaster Recovery Plan](#br-4-disaster-recovery-plan)             |
| [BR-5: Business Continuity Plan](#br-5-business-continuity-plan)         |
| [BR-6: Business Continuity Exercise](#br-6-business-continuity-exercise) |

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

## BR-2: Recovery Testing

**Group:** Backup and Recovery

### Control Statement

Conduct testing of recovery processes at least every [ insert: param, br-2_prm_1 ] day(s) to ensure their effectiveness.

### Control Recommendations

Ensure each test verifies the system&#39;s ability to fully restore all data and services.

### Risk Statement

Failure to regularly test recovery processes may result in ineffective response during actual incidents, increasing the risk of prolonged downtime, data loss, and compromised business continuity in the event of a disaster or system failure.

### Parameters

| ID         | Type                     | Description                                   |
| ---------- | ------------------------ | --------------------------------------------- |
| br-2_prm_1 | time period (days) (int) | The time period in days for recovery testing. |

## BR-3: Backup Retention

**Group:** Backup and Recovery

### Control Statement

Prevent backups from being modified or deleted for [ insert: param, br-3_prm_1 ] day(s) or as stipulated in the agency&#39;s data retention policies.

### Control Recommendations

Use S3 Object Lock or Azure Blob Storage with immutability enabled to enforce time-based retention policies.

### Risk Statement

Lack of prevention measures against the modification or deletion of backups for the specified duration increases the risk of data loss, unauthorised alterations, and potential inability to recover from incidents, compromising the integrity and availability of critical information.

### Parameters

| ID         | Type                     | Description                                  |
| ---------- | ------------------------ | -------------------------------------------- |
| br-3_prm_1 | time period (days) (int) | The time period in days of backup retention. |

## BR-4: Disaster Recovery Plan

**Group:** Backup and Recovery

### Control Statement

Develop, maintain, and regularly test a disaster recovery plan that ensures critical functions and data can be restored within the Recovery Time Objective (RTO) and Recovery Point Objective (RPO) as determined by business requirements and risk assessments.

### Control Recommendations

The disaster recovery plan should include clearly defined roles and responsibilities, step-by-step recovery procedures, communication protocols during a disaster, and integration with the overall business continuity plan. Assess the effectiveness of the existing disaster recovery plan during disaster recovery exercises.

### Risk Statement

Absence of a comprehensive disaster recovery plan increases the risk of prolonged system downtime, data loss, and inability to maintain business continuity in the event of a disaster, potentially leading to significant financial losses and damage to organisational reputation.

## BR-5: Business Continuity Plan

**Group:** Backup and Recovery

### Control Statement

Develop a business continuity plan.

### Control Recommendations

Refer to the [Cyber Security Agency&#39;s Cybersecurity Toolkit for IT Teams](https://www.csa.gov.sg/our-programmes/support-for-enterprises/sg-cyber-safe-programme/cybersecurity-toolkits/cybersecurity-toolkit-for-it-teams) for a business continuity plan template.

### Risk Statement

Failure to develop a Business Continuity Plan may result in prolonged system downtime, loss of critical data, and diminished organisational resilience during disruptive events, increasing the risk of financial and reputational damage.

## BR-6: Business Continuity Exercise

**Group:** Backup and Recovery

### Control Statement

Conduct a business continuity exercise at least every [ insert: param, br-6_prm_1 ] day(s) to test the effectiveness of the business continuity plan.

### Control Recommendations

Conduct testing based on the business continuity plan which can include checklists, tabletop exercises, and simulations.

### Risk Statement

Failure to conduct regular business continuity exercises may lead to unpreparedness during an actual disruption, increasing response times, operational impact, and the risk of ineffective recovery, ultimately jeopardising business operations and stakeholder trust.

### Parameters

| ID         | Type                     | Description                                                        |
| ---------- | ------------------------ | ------------------------------------------------------------------ |
| br-6_prm_1 | time period (days) (int) | The time period in days of business continuity exercise frequency. |