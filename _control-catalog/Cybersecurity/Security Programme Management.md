---
title: Security Programme Management
permalink: /control-catalog/pm/
variant: markdown
description: ""
third_nav_title: Cybersecurity
---
Controls to implement cybersecurity governance, risk, and compliance processes and policies.

| Controls |
| ---- |
| [PM-1: Cybersecurity Incident Management Plan](#pm-1) |
| [PM-2: Risk Assessment](#pm-2) |
| [PM-3: System Security Plan (SSP) Development](#pm-3) |
| [PM-4: Approval of Residual Risks](#pm-4) |
| [PM-5: Central Submission of Approved System Security Plan (SSP)](#pm-5) |
| [PM-6: System Documentation](#pm-6) |
| [PM-7: Certification](#pm-7) |
| [PM-8: SaaS Whitelisting](#pm-8) |


<a id="pm-1"></a>
## PM-1: Cybersecurity Incident Management Plan

### Control Statement

Develop, document, and disseminate an agency-level cybersecurity incident management plan to respond to cybersecurity incidents.

### Control Recommendations

Refer to the Government Incident Reporting and Operations Centre (GIROC) ICT and Data Incident Reporting Resources for an incident management plan and best practices template.

### Risk Statement

Lack of a cybersecurity incident management plan increases the risk of ineffective response to cybersecurity incidents, hindering the ability to contain, mitigate, and recover from security breaches, potentially leading to extended downtime and data compromise.



<a id="pm-2"></a>
## PM-2: Risk Assessment

### Control Statement

Develop and document a risk assessment by [pm-2_prm_1] and get it approved by [pm-2_prm_2] prior to initial full release and conduct a review every [pm-2_prm_3] day(s).

### Control Recommendations

The Risk Assessment should cover Cyber Risk, Data Risk, Resiliency Risk, Business Risk, Project Risk, Offshore Risk and other types of risk where applicable. 

### Risk Statement

Without developing and documenting risk assessment before the initial full release, there's an increased risk of overlooking potential security threats, vulnerabilities, and regulatory compliance issues, compromising the overall security posture of the system.



#### Parameters

| ID | Type | Description |
| -- | ---- | ----------- |
| pm-2_prm_1 | system owner | The owner of the system. |
| pm-2_prm_2 | risk assessment approver | The approver of the risk assessment. |
| pm-2_prm_3 | time period (days) | The time period in days for risk assessment. |

<a id="pm-3"></a>
## PM-3: System Security Plan (SSP) Development

### Control Statement

Develop and maintain a comprehensive System Security Plan (SSP) that accurately reflects the system characteristics and security controls in place for the organisation's systems and environments.

### Control Recommendations

The SSP should be detailed, covering all aspects of security controls, roles, responsibilities, and operational processes. Regular updates are necessary to reflect changes in the security landscape and system evolution.

### Risk Statement

Failure to develop a comprehensive SSP can result in inadequate documentation and security controls, leading to increased vulnerability to cyber threats and non-compliance with regulatory requirements.



<a id="pm-4"></a>
## PM-4: Approval of Residual Risks

### Control Statement

Get acceptance and approval of the residual risks from agency's [pm-4_prm_1].

### Control Recommendations

Agencies should seek acceptance and approval from their [pm-4_prm_1] on the residual risks based on the SSP and inform GovTech of the approval.

### Risk Statement

Failure to seek the right level of authority to accept and approve the residual risks can lead to misalignment of the business implications and trade-offs from the controls set in the SSP with the Agency IDSC direction.



#### Parameters

| ID | Type | Description |
| -- | ---- | ----------- |
| pm-4_prm_1 | approving authority | The authority for approval of residual risks. |

<a id="pm-5"></a>
## PM-5: Central Submission of Approved System Security Plan (SSP)

### Control Statement

Submit approved SSPs centrally to maintain a unified and up-to-date repository of security plans and practices.

### Control Recommendations

Reference the IM8 Portal for submitting all approved SSPs.

### Risk Statement

Inconsistent or decentralised submission of the SSP can lead to decreased visibility of security and compliance adoption across Government.



<a id="pm-6"></a>
## PM-6: System Documentation

### Control Statement

Maintain detailed, up-to-date documentation of all system information and architecture.

### Control Recommendations

Example system documentation includes architecture and network diagrams, architecture decision records, hardware and software inventories, data flows, and configurations. This documentation should be regularly reviewed and updated to reflect changes in the environment. Documentation should be accessible to relevant personnel while ensuring sensitive information is protected. Adopt documentation-as-code practices and machine-readable formats (such as Markdown, JSON, YAML, etc), to facilitate version control, collaboration, and automation in maintaining documentation.

### Risk Statement

Comprehensive documentation of system architecture, components, configurations, and dependencies is essential for effective management, troubleshooting, and security auditing.



<a id="pm-7"></a>
## PM-7: Certification

### Control Statement

Ensure that the Software as a Service (SaaS) provider is certified with [pm-7_prm_1].

### Control Recommendations

Ensure that the certification is up-to-date. Avoid certifications that are only attestations without a pass/fail element.

### Risk Statement

Third-party certification provides assurance that security controls have been properly implemented in the Software as a Service (SaaS) provider.



#### Parameters

| ID | Type | Description |
| -- | ---- | ----------- |
| pm-7_prm_1 | certifications | The required certifications. |

<a id="pm-8"></a>
## PM-8: SaaS Whitelisting

### Control Statement

Whitelist SaaS before use.

### Control Recommendations

Refer to a centrally-maintained whitelist or whitelisting authority for authorised SaaS.

### Risk Statement

Failing to whitelist the SaaS may potentially expose sensitive data (e.g., Confidential (Cloud-Eligible) or SENSITIVE-HIGH data) to the risk of data breaches.