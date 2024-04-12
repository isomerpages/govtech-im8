---
title: Security Programme Management
permalink: /catalog-temp/pm/
variant: markdown
description: ""
---
Controls to implement cybersecurity governance, risk, and compliance processes and policies.

| Controls |
| ---- |
| [PM-1: Cybersecurity Incident Management Plan](#pm-1) |
| [PM-2: Project Cybersecurity Risk Assessment](#pm-2) |
| [PM-3: System Security Plan (SSP) Development](#pm-3) |
| [PM-4: Approval of Policy Deviations](#pm-4) |
| [PM-5: Central Submission of Approved System Security Plan (SSP)](#pm-5) |
| [PM-6: System Documentation](#pm-6) |
| [PM-7: Certification](#pm-7) |
| [PM-8: Software as a Service (SaaS) Service Level Agreement](#pm-8) |


<a id="pm-1"></a>
## PM-1: Cybersecurity Incident Management Plan

### Control Statement

Develop, document, and disseminate an agency-level cybersecurity incident management plan to respond to cybersecurity incidents.

### Control Recommendations

Refer to the Government Incident Reporting and Operations Centre (GIROC) [ICT and Data Incident Reporting Resources](https://gccprod.sharepoint.com/sites/GOVTECH-digitalgov/GIROC/SitePages/Useful-Resources.aspx) for an incident management plan and best practices template.

### Risk Statement

Lack of a cybersecurity incident management plan increases the risk of ineffective response to cybersecurity incidents, hindering the ability to contain, mitigate, and recover from security breaches, potentially leading to extended downtime and data compromise.



<a id="pm-2"></a>
## PM-2: Project Cybersecurity Risk Assessment

### Control Statement

Develop and document a project-level cybersecurity risk assessment prior to initial full release that includes:
 * Risk scenario;
 * Likelihood (from 1-5);
 * Impact (from 1-5);
 * Risk Level (Likelihood * Impact; 1-4: Low, 5-9: Medium, 10-14: Medium High, 15-19: High, 20-25: Critical)
 * Mitigating Measures


### Control Recommendations

Refer to the Cyber Security Agency of Singapore [Cybersecurity Toolkit for IT Teams](https://www.csa.gov.sg/our-programmes/support-for-enterprises/sg-cyber-safe-programme/cybersecurity-toolkits/cybersecurity-toolkit-for-it-teams) for an example of a risk assessment template and modify accordingly. For potential risk scenarios, consider examples from the Government Commercial Cloud [Cloud Security Risk Register](https://cloudplaybook.in.tech.gov.sg/confluence/display/CPP/3%29+Cloud+Security+Risk+Assessment).

### Risk Statement

Without developing and documenting a project-level cybersecurity risk assessment before the initial full release, there's an increased risk of overlooking potential security threats, vulnerabilities, and regulatory compliance issues, compromising the overall security posture of the project.



<a id="pm-3"></a>
## PM-3: System Security Plan (SSP) Development

### Control Statement

Develop and maintain a comprehensive System Security Plan (SSP) that accurately reflects the system characteristics and security controls in place for the organisation's systems and environments.

### Control Recommendations

The SSP should be detailed, covering all aspects of security controls, roles, responsibilities, and operational processes. Regular updates are necessary to reflect changes in the security landscape and system evolution.

### Risk Statement

Failure to develop a comprehensive SSP can result in inadequate documentation and security controls, leading to increased vulnerability to cyber threats and non-compliance with regulatory requirements.



<a id="pm-4"></a>
## PM-4: Approval of Policy Deviations

### Control Statement

Approve all deviations from the Level 1 Profile by the relevant agency approval authority and document these deviations in the customised SSP.

### Control Recommendations

Agencies should seek approval for deviation from their IDSC or delegated approval authority such as the agency CIO or CISO.

### Risk Statement

Unauthorised deviations from the policy can lead to an increased risk of security vulnerabilities and other compliance issues.



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
## PM-8: Software as a Service (SaaS) Service Level Agreement

### Control Statement

Obtain a service level agreement with the Software as a Service (SaaS) provider that covers uptime, response times, downtime notifications, support avenues, and support content.

### Control Recommendations

Ensure that the service level agreement is regularly checked for compliance.

### Risk Statement

Without a service level agreement the availability of the Software as a Service (SaaS) system may be poorly maintained by the provider.