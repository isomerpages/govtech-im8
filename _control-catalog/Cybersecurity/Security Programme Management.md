---
title: Security Programme Management
permalink: /control-catalog/pm/
variant: markdown
description: ""
third_nav_title: Cybersecurity
---
Controls to implement cybersecurity governance, risk, and compliance processes and policies.

| Controls                                                                                                                         |
| -------------------------------------------------------------------------------------------------------------------------------- |
| [PM-1: Cybersecurity Incident Management Plan](#pm-1-cybersecurity-incident-management-plan)                                     |
| [PM-2: Risk Assessment](#pm-2-risk-assessment)                                                                                   |
| [PM-3: System Security Plan (SSP) Development](#pm-3-system-security-plan-ssp-development)                                       |
| [PM-4: Approval of Residual Risks](#pm-4-approval-of-residual-risks)                                                             |
| [PM-5: Central Submission of Approved System Security Plan (SSP)](#pm-5-central-submission-of-approved-system-security-plan-ssp) |
| [PM-6: System Documentation](#pm-6-system-documentation)                                                                         |
| [PM-7: Certification](#pm-7-certification)                                                                                       |
| [PM-8: SaaS Whitelisting](#pm-8-saas-whitelisting)                                                                               |

## PM-1: Cybersecurity Incident Management Plan

**Group:** Security Programme Management

### Control Statement

Develop, document, and disseminate an agency-level cybersecurity incident management plan to respond to cybersecurity incidents.

### Control Recommendations

Refer to the Government Incident Reporting and Operations Centre (GIROC) ICT and Data Incident Reporting Resources for an incident management plan and best practices template.

### Risk Statement

Lack of a cybersecurity incident management plan increases the risk of ineffective response to cybersecurity incidents, hindering the ability to contain, mitigate, and recover from security breaches, potentially leading to extended downtime and data compromise.

## PM-2: Risk Assessment

**Group:** Security Programme Management

### Control Statement

Develop and document a risk assessment by [ insert: param, pm-2_prm_1 ] and get it approved by [ insert: param, pm-2_prm_2 ] prior to [ insert: param, pm-2_prm_3 ] and conduct a review every [ insert: param, pm-2_prm_4 ] day(s).

### Control Recommendations

The Risk Assessment should cover Cyber Risk, Data Risk, Resiliency Risk, Business Risk, Project Risk, Offshore Risk and other types of risk where applicable.

### Risk Statement

Without developing and documenting risk assessment before the initial full release, there&#39;s an increased risk of overlooking potential security threats, vulnerabilities, and regulatory compliance issues, compromising the overall security posture of the system.

### Parameters

| ID         | Type                           | Description                                  |
| ---------- | ------------------------------ | -------------------------------------------- |
| pm-2_prm_1 | system owner (str)             | The owner of the system.                     |
| pm-2_prm_2 | risk assessment approver (str) | The approver of the risk assessment.         |
| pm-2_prm_3 | risk assessment use case (str) | The use case of the risk assessment.         |
| pm-2_prm_4 | time period (days) (int)       | The time period in days for risk assessment. |

## PM-3: System Security Plan (SSP) Development

**Group:** Security Programme Management

### Control Statement

Develop and maintain a comprehensive System Security Plan (SSP) that accurately reflects the system characteristics and security controls in place for the organisation&#39;s systems and environments.

### Control Recommendations

The SSP should be detailed, covering all aspects of security controls, roles, responsibilities, and operational processes. Regular updates are necessary to reflect changes in the security landscape and system evolution.

### Risk Statement

Failure to develop a comprehensive SSP can result in inadequate documentation and security controls, leading to increased vulnerability to cyber threats and non-compliance with regulatory requirements.

## PM-4: Approval of Residual Risks

**Group:** Security Programme Management

### Control Statement

Get acceptance and approval of the residual risks from agency&#39;s [ insert: param, pm-4_prm_1 ].

### Control Recommendations

Agencies should seek acceptance and approval from their [ insert: param, pm-4_prm_1 ] on the residual risks based on the SSP and inform GovTech of the approval.

### Risk Statement

Failure to seek the right level of authority to accept and approve the residual risks can lead to misalignment of the business implications and trade-offs from the controls set in the SSP with the Agency IDSC direction.

### Parameters

| ID         | Type                      | Description                                   |
| ---------- | ------------------------- | --------------------------------------------- |
| pm-4_prm_1 | approving authority (str) | The authority for approval of residual risks. |

## PM-5: Central Submission of Approved System Security Plan (SSP)

**Group:** Security Programme Management

### Control Statement

Submit approved SSPs centrally to maintain a unified and up-to-date repository of security plans and practices.

### Control Recommendations

Reference the IM8 Portal for submitting all approved SSPs.

### Risk Statement

Inconsistent or decentralised submission of the SSP can lead to decreased visibility of security and compliance adoption across Government.

## PM-6: System Documentation

**Group:** Security Programme Management

### Control Statement

Maintain detailed, up-to-date documentation of all system information and architecture.

### Control Recommendations

Example system documentation includes architecture and network diagrams, architecture decision records, hardware and software inventories, data flows, and configurations. This documentation should be regularly reviewed and updated to reflect changes in the environment. Documentation should be accessible to relevant personnel while ensuring sensitive information is protected. Adopt documentation-as-code practices and machine-readable formats (such as Markdown, JSON, YAML, etc), to facilitate version control, collaboration, and automation in maintaining documentation.

### Risk Statement

Comprehensive documentation of system architecture, components, configurations, and dependencies is essential for effective management, troubleshooting, and security auditing.

## PM-7: Certification

**Group:** Security Programme Management

### Control Statement

Ensure that the Software as a Service (SaaS) provider is certified with [ insert: param, pm-7_prm_1 ].

### Control Recommendations

Ensure that the certification is up-to-date. Avoid certifications that are only attestations without a pass/fail element.

### Risk Statement

Third-party certification provides assurance that security controls have been properly implemented in the Software as a Service (SaaS) provider.

### Parameters

| ID         | Type                 | Description                  |
| ---------- | -------------------- | ---------------------------- |
| pm-7_prm_1 | certifications (str) | The required certifications. |

## PM-8: SaaS Whitelisting

**Group:** Security Programme Management

### Control Statement

Maintain and enforce a whitelist of authorised software and services.

### Control Recommendations

Refer to a centrally-maintained whitelist or [ insert: param, pm-8_prm_1 ] for authorised SaaS.

### Risk Statement

Failing to whitelist the SaaS may potentially expose sensitive data (e.g., Confidential (Cloud-Eligible) or SENSITIVE-HIGH data) to the risk of data breaches.

### Parameters

| ID         | Type                         | Description                 |
| ---------- | ---------------------------- | --------------------------- |
| pm-8_prm_1 | whitelisting authority (str) | The whitelisting authority. |
