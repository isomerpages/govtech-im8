---
title: Low Risk Saas
permalink: /system-security-plans/low-risk-saas/
variant: markdown
description: ""
---
# Low-Risk Software as a Service (SaaS)

## Overview

The Low-Risk Software as a Service (SaaS) System Security Plan template includes controls that are recommended as the default controls for low-risk systems that utilise SaaS as the primary component and classified up to official (closed) and non-sensitive, excluding National Emergency (NE) Critical, Critical Information Infrastructure (CII), Significant Information Infrastructure (SII). For systems that utilise SaaS as part of a larger system then it is recommended to use the more general security plans (e.g. low risk cloud).

<p>
  <a href="/low-risk-software-as-a-service-(saas)-ssp.xlsx">
    <button>
      Download as Excel
    </button>
  </a>
</p>

## Parties

| Name | Type |
| ---- | ---- |
| Agency | organization |
| System Owners | organization |
| System Administrators | organization |
| System Developers | organization |


## System Characteristics

* **Name:** Low-Risk Software as a Service System
* **Description:** A generic system hosted on the cloud by a third-party service provider.
* **Security Sensitivity Level:** Official (Closed), Non-Sensitive

## System Implementation

| Id | Type | Description |
| -- | ---- | ----------- |
| System | this-system | The system. |
| Source Code | software | Defines the instructions executed by the system's assets. |
| Service Level Agreement | agreement | An agreement between a service provider and its customers for aspects of its service. |
| System Security Plan | plan | Defines a system's characteristics and security control implementation. |
| Project Cybersecurity Risk Assessment | validation | Assesses the cybersecurity risks to the system and documents mitigating measures. |


## Control Implementation

### PM-2: Project Cybersecurity Risk Assessment

* **Group:** [Security Programme Management](/catalog/pm)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Develop and document a project-level cybersecurity risk assessment prior to initial full release that includes:
 * Risk scenario;
 * Likelihood (from 1-5);
 * Impact (from 1-5);
 * Risk Level (Likelihood * Impact; 1-4: Low, 5-9: Medium, 10-14: Medium High, 15-19: High, 20-25: Critical)
 * Mitigating Measures


#### Control Recommendations

Refer to the Cyber Security Agency of Singapore [Cybersecurity Toolkit for IT Teams](https://www.csa.gov.sg/our-programmes/support-for-enterprises/sg-cyber-safe-programme/cybersecurity-toolkits/cybersecurity-toolkit-for-it-teams) for an example of a risk assessment template and modify accordingly. For potential risk scenarios, consider examples from the Government Commercial Cloud [Cloud Security Risk Register](https://cloudplaybook.in.tech.gov.sg/confluence/display/CPP/3%29+Cloud+Security+Risk+Assessment).

#### Risk Statement

Without developing and documenting a project-level cybersecurity risk assessment before the initial full release, there's an increased risk of overlooking potential security threats, vulnerabilities, and regulatory compliance issues, compromising the overall security posture of the project.




#### Responsible Roles and Parties

* Asset-owner:
  * Agency


#### By Components

* Project Cybersecurity Risk Assessment: The agency develops and documents a project cybersecurity risk assessment.
#### References


 * [MVSP 1.3: Self-assessment](https://mvsp.dev/)
 * [IM8 Cloud Security (IaaS and PaaS): 1.1/S1](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
### PM-3: System Security Plan (SSP) Development

* **Group:** [Security Programme Management](/catalog/pm)
* **Profile:** [Low-Risk - Level 0](/profiles/low-risk/level-0), [Sandbox - Level 0](/profiles/sandbox/level-0)

#### Control Statement

Develop and maintain a comprehensive System Security Plan (SSP) that accurately reflects the system characteristics and security controls in place for the organisation's systems and environments.

#### Control Recommendations

The SSP should be detailed, covering all aspects of security controls, roles, responsibilities, and operational processes. Regular updates are necessary to reflect changes in the security landscape and system evolution.

#### Risk Statement

Failure to develop a comprehensive SSP can result in inadequate documentation and security controls, leading to increased vulnerability to cyber threats and non-compliance with regulatory requirements.




#### Responsible Roles and Parties

* Asset-owner:
  * System Owners


#### By Components

* System Security Plan: The system owner develops, documents, and disseminates a system security plan.
### PM-4: Approval of Policy Deviations

* **Group:** [Security Programme Management](/catalog/pm)
* **Profile:** [Low-Risk - Level 0](/profiles/low-risk/level-0), [Sandbox - Level 0](/profiles/sandbox/level-0)

#### Control Statement

Approve all deviations from the Level 1 Profile by the relevant agency approval authority and document these deviations in the customised SSP.

#### Control Recommendations

Agencies should seek approval for deviation from their IDSC or delegated approval authority such as the agency CIO or CISO.

#### Risk Statement

Unauthorised deviations from the policy can lead to an increased risk of security vulnerabilities and other compliance issues.




#### Responsible Roles and Parties

* Asset-owner:
  * System Owners


#### By Components

* System Security Plan: The system owner seeks approval for deviations in the system security plan.
### PM-5: Central Submission of Approved System Security Plan (SSP)

* **Group:** [Security Programme Management](/catalog/pm)
* **Profile:** [Low-Risk - Level 0](/profiles/low-risk/level-0), [Sandbox - Level 0](/profiles/sandbox/level-0)

#### Control Statement

Submit approved SSPs centrally to maintain a unified and up-to-date repository of security plans and practices.

#### Control Recommendations

Reference the IM8 Portal for submitting all approved SSPs.

#### Risk Statement

Inconsistent or decentralised submission of the SSP can lead to decreased visibility of security and compliance adoption across Government.




#### Responsible Roles and Parties

* Asset-owner:
  * System Owners


#### By Components

* System Security Plan: The system owner submits the system security plan centrally.
#### References


 * [Centralised SSP Management Guidelines]()
### PM-7: Certification

* **Group:** [Security Programme Management](/catalog/pm)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Ensure that the Software as a Service (SaaS) provider is certified with [pm-7_prm_1: CSA STAR or ISO 27001].

#### Control Recommendations

Ensure that the certification is up-to-date. Avoid certifications that are only attestations without a pass/fail element.

#### Risk Statement

Third-party certification provides assurance that security controls have been properly implemented in the Software as a Service (SaaS) provider.




#### Responsible Roles and Parties

* Asset-owner:
  * System Owners


#### By Components

* System: The SaaS provider obtain the ceritifcations for the system.
### DP-1: Data Residency

* **Group:** [Data Protection](/catalog/dp)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Enforce data residency of primary data in Singapore.

#### Control Recommendations

Use the Singapore region of cloud service providers for compute and storage of primary data, such as ap-southeast-1 for AWS.

#### Risk Statement

Failure to enforce data residency of primary data in Singapore may lead to legal and regulatory compliance issues, privacy concerns, and potential unauthorised access or storage of sensitive data outside the jurisdiction, increasing the risk of legal consequences and data breaches.




#### Responsible Roles and Parties

* Asset-owner:
  * System Owners


#### By Components

* System: The SaaS provider enforces data residency of the system's primary data in Singapore.
#### References


 * [MVSP 1.6: Compliance](https://mvsp.dev/)
 * [IM8 Cloud Security (IaaS and PaaS): 1.3/S3](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 On-Premise IS (Non-S): 1.1/S1a](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/On-Premise/Topics/Infrastructure-Security-(For-Non-S).aspx)
### AC-1: Principle of Least Privilege

* **Group:** [Access Control](/catalog/ac)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Deny access by default and grant only the minimum permissions required for authorised accounts or processes to perform a specific function.

#### Control Recommendations

Consider attribute- or feature-based access control for greater customisability and granularity.

#### Risk Statement

Violating the principle of least privileges increases the risk of unauthorised access, privilege escalation, and potential security breaches due to unnecessary permissions, compromising the overall security posture.




#### Responsible Roles and Parties

* Asset-administrator:
  * System Administrators


#### By Components

* System: Administrators maange accounts and access rights for the SaaS based on the principle of least privilege.
#### References


 * [MVSP 4.2: Logical access](https://mvsp.dev/)
 * [IM8 Cloud Security (IaaS and PaaS): 1.4/S7](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 Cloud Security (IaaS and PaaS): 1.5/S4e](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 Cloud Security (IaaS and PaaS): 1.7/S1b](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
### AC-2: Multi-Factor Authentication (MFA)

* **Group:** [Access Control](/catalog/ac)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Require MFA for remote developer, maintainer, or administrator access.

#### Control Recommendations

Ensure that the authentication factors are different and independent of the accessing device.

#### Risk Statement

Without requiring phishing-resistant Multi-Factor Authentication (MFA) for remote access, there is an increased risk of unauthorised access, credential theft, and potential compromise of sensitive systems, especially for users with elevated privileges.




#### Responsible Roles and Parties

* Asset-administrator:
  * System Administrators


#### By Components

* System: Administrators configure the SaaS to require phishing-resistant MFA for remote developer, maintainer, or administrator access.
#### References


 * [MVSP 4.2: Logical access](https://mvsp.dev/)
 * [IM8 Cloud Security (IaaS and PaaS): 1.4/S20a](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 On-Premise ADS (Non-S): 2.4/S2]()
### AC-3: Inactive and Expired Accounts

* **Group:** [Access Control](/catalog/ac)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Disable or remove accounts with developer, maintainer, or administrator access within [ac-3_prm_1: 7 days] day(s) from last day of authorised use or have not been used for [ac-3_prm_2: 90 days] day(s).

#### Control Recommendations

Use automated checks such as AWS Config iam-user-unused-credentials-check to identify accounts and credentials that should be disabled. Consider using automated workflows such as System for Cross-domain Identity Management (SCIM) or identity lifecycle management tools.

#### Risk Statement

Failure to disable or remove unused accounts or credentials with elevated access increases the risk of unauthorised access, as dormant accounts may become targets for exploitation, compromising the security of the system.




#### Responsible Roles and Parties

* Asset-administrator:
  * System Administrators


#### By Components

* System: Administrators disable or remove inactive developer, maintainer and administrator accounts in the SaaS.
#### References


 * [MVSP 4.2: Logical access](https://mvsp.dev/)
 * [IM8 Cloud Security (IaaS and PaaS): 1.4/S15](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 Cloud Security (IaaS and PaaS): 1.4/S18b](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 On-Premise ADS (Non-S): 2.3/S2, 2.3/S3](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/On-Premise/Topics/Application-Development-Security-(For-Non-S).aspx)
### AC-4: Access Review

* **Group:** [Access Control](/catalog/ac)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Perform an access review every [ac-4_prm_1: 365] day(s) and remove unauthorised or unintended access rights within [ac-4_prm_2: 7] day(s).

#### Control Recommendations

Use tools such as AWS IAM Access Advisor or Azure AD Access Review to facilitate and manage access reviews.

#### Risk Statement

Without regular access reviews and prompt removal of unauthorised or unintended access rights, there is an increased risk of lingering access, potential misuse of privileges, and compromised security, impacting the confidentiality and integrity of sensitive data.




#### Responsible Roles and Parties

* Asset-administrator:
  * System Administrators


#### By Components

* System: Administrators perform regular access reviews in the SaaS.
#### References


 * [MVSP 4.2: Logical access](https://mvsp.dev/)
 * [IM8 Cloud Security (IaaS and PaaS): 1.4/S13](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 On-Premise ADS (Non-S): 2.3/S1, 2.3/S6](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/On-Premise/Topics/Application-Development-Security-(For-Non-S).aspx)
### AC-6: Default Credentials

* **Group:** [Access Control](/catalog/ac)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Change default credentials prior to first use.

#### Control Recommendations

Identify any default credentials used in any system components before deploying and change them. Configure end-user systems to prompt for password change on first login after account creation or reset.

#### Risk Statement

Failure to change default credentials prior to first use increases the risk of unauthorised access, as default credentials are often well-known and targeted by attackers, compromising the security of the system or device.




#### Responsible Roles and Parties

* Maintainer:
  * System Administrators


#### By Components

* System: Administrators change default credentials in any component in the SaaS.
#### References


 * [NIST SP 800-53 IA-5: Authenticator Management](https://doi.org/10.6028/NIST.SP.800-53r5)
 * [IM8 Cloud Security (IaaS and PaaS): 1.4/S1c](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 Cloud Security (IaaS and PaaS): 1.4/S2c](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 On-Premise ADS (Non-S): 2.2/S1d, 2.3/S5](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/On-Premise/Topics/Application-Development-Security-(For-Non-S).aspx)
### AC-8: Automate account provisioning

* **Group:** [Access Control](/catalog/ac)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Implement automation of cloud and application account provisioning and deprovisioning using an account management tool.

#### Control Recommendations

Adopt Single Sign-On (SSO) with just-in-time provisioning or account lifecycle management tools (such as SCIM or CAM) to assist with account management. For systems unable to use SSO, it is recommended to leverage account management lifecycle tools with HR records (such as CAM) to automatically provision and de-provision accounts.

#### Risk Statement

Manual account and access provisioning can introduce errors and weaknesses, thus making access control measures ineffective and unreliable.




#### Responsible Roles and Parties

* Maintainer:
  * System Administrators


#### By Components

* System: Administrators integrate the SaaS with automated provisioning and deprovisioning.
#### References


 * [IM8 Cloud Security (IaaS and PaaS): 1.4/S18a](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 On-Premise ADS (Non-S): 2.3/S7](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/On-Premise/Topics/Application-Development-Security-(For-Non-S).aspx)
### AC-12: Single Sign-On (SSO) for Internal Users

* **Group:** [Access Control](/catalog/ac)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Use Single Sign-On (SSO) for internal users and services.

#### Control Recommendations

Configure multi-factor authentication (MFA) at the Single-Sign On (SSO) identity provider (IdP) and ensure that access to the system is only granted after the IdP authenticates the user. WOG AAD is recommended for public officers and TechPass AAD for developers.

#### Risk Statement

Without Single Sign-On (SSO), there is an increased risk of unauthorized access and compromised user credentials, as users may resort to using weak passwords or reusing credentials across multiple systems, thereby exposing sensitive information to potential security breaches.




#### Responsible Roles and Parties

* Maintainer:
  * System Administrators


#### By Components

* System: Administrators integrate the SaaS with the SSO IdP.
#### References


 * [IA-2(10): Single Sign-on](https://doi.org/10.6028/NIST.SP.800-53r5)
 * [IM8 Cloud Security (IaaS and PaaS): 1.4/S18c](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
### AS-5: Password Requirements

* **Group:** [Application Security](/catalog/as)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Where SSO or passwordless is not supported, verify that user-defined passwords are at least [as-5_prm_1: 8] characters in length and [as-5_prm_2: include a number or special character].

#### Control Recommendations

Latest NIST [SP 800-63B](https://doi.org/10.6028/NIST.SP.800-63b) guidelines found that password length is a primary factor in determining the strength of a password while composition and complexity rules provide marginal security benefits.

#### Risk Statement

Short or commonly used passwords increase the vulnerability to unauthorised access, potentially leading to compromised accounts and unauthorised activities on the system.




#### Responsible Roles and Parties

* Provider:
  * System Developers


#### By Components

* System: SaaS providers implement password requirements in the SaaS.
#### References


 * [MVSP 2.4: Password policy](https://mvsp.dev/)
 * [NIST SP 800-53 IA-5(1): Password-based Authentication](https://doi.org/10.6028/NIST.SP.800-53r5)
 * [IM8 Cloud Security (IaaS and PaaS): 1.4/S1a](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 Cloud Security (IaaS and PaaS): 1.4/S2a](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 On-Premise ADS (Non-S): 2.2/S1](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/On-Premise/Topics/Application-Development-Security-(For-Non-S).aspx)
### DP-2: Data at Rest Encryption

* **Group:** [Data Protection](/catalog/dp)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Encrypt data at rest.

#### Control Recommendations

Many CSP services encrypt data at rest by default but this should be confirmed and validated depending on service usage.

#### Risk Statement

Without encrypting data at rest, there's an increased risk of unauthorised access and data exposure in the event of physical theft, unauthorised access to storage media, or compromised security controls, compromising the confidentiality of stored information.




#### Responsible Roles and Parties

* Provider:
  * System Developers


#### By Components

* System: SaaS providers encrypt the system's data at rest.
#### References


 * [MVSP 2.8: Encryption](https://mvsp.dev/)
 * [IM8 Cloud Security (IaaS and PaaS): 1.3/S2a](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 On-Premise ADS (Non-S): 1.1/S1h](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/On-Premise/Topics/Application-Development-Security-(For-Non-S).aspx)
### DP-3: Data in Transit Encryption

* **Group:** [Data Protection](/catalog/dp)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Encrypt data in transit.

#### Control Recommendations

While some CSP services transparently encrypt data in transit at the network layer, data at the application layer should be encrypted using protocols such as Transport Layer Security (TLS).

#### Risk Statement

Failure to encrypt data in transit increases the risk of unauthorised interception and eavesdropping, potentially leading to data breaches, unauthorised access, and compromise of sensitive information during transmission.




#### Responsible Roles and Parties

* Provider:
  * System Developers


#### By Components

* System: SaaS providers encrypt the system's data in transit.
#### References


 * [MVSP 2.8: Encryption](https://mvsp.dev/)
 * [IM8 Cloud Security (IaaS and PaaS): 1.3/S2b](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 On-Premise ADS (Non-S): 3.1/S3](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/On-Premise/Topics/Application-Development-Security-(For-Non-S).aspx)
### LM-7: Security Event Logging

* **Group:** [Logging and Monitoring](/catalog/lm)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Log security events on hosts and other cloud resources.

#### Control Recommendations

Security events include operating system security events, authentication and audit logs, and endpoint detection and response alerts.

#### Risk Statement

Neglecting to log security events on hosts and other cloud resources increases the risk of undetected security incidents, compromises incident response capabilities, and hinders forensic analysis, limiting the ability to identify and mitigate potential threats.




#### Responsible Roles and Parties

* Maintainer:
  * System Administrators


#### By Components

* System: Administrators configure logging of security events in the SaaS.
#### References


 * [IM8 Cloud Security (IaaS and PaaS): 1.9/S2](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
### LM-12: Government Cyber Security Operations Centre (GCSOC)

* **Group:** [Logging and Monitoring](/catalog/lm)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Subscribe and send security logs to GCSOC for central threat monitoring.

#### Control Recommendations

Logs that are sent to GCC Central Logs are forwarded to GCSOC.

#### Risk Statement

Failure to subscribe and send security logs to the Government Cyber Security Operations Centre (GCSOC) impedes central threat monitoring, increasing the risk of delayed or unnoticed security incidents, hindering effective response, and compromising the overall cybersecurity posture.




#### Responsible Roles and Parties

* Maintainer:
  * System Administrators


#### By Components

* System: Administrators send security logs and alerts to GCSOC.
#### References


 * [IM8 Cloud Security (IaaS and PaaS): 1.9/S3](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 On-Premise IS (Non-S): 7.1/S3](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/On-Premise/Topics/Infrastructure-Security-(For-Non-S).aspx)
### BR-1: Backup

* **Group:** [Backup and Recovery](/catalog/br)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Regularly backup all important data and systems, and store backups in a secure and separate location.

#### Control Recommendations

Use default CSP-managed backup services (e.g., AWS Backup, Azure Backup, GCP Backup and DR Service). Consider alternative backup services only when default CSP services cannot be used. Store backups and snapshots separately to primary data storage with data encrypted-at-rest.

#### Risk Statement

Without regular backups stored in a secure and separate location, there is an increased risk of data loss, system failures, and extended downtime in the event of accidental deletion, hardware failures, or malicious attacks.




#### Responsible Roles and Parties

* Maintainer:
  * System Administrators


#### By Components

* : Administrators configure regular backups.
#### References


 * [MVSP 4.4: Backup and Disaster recovery](https://mvsp.dev/)
 * [IM8 Cloud Security (IaaS and PaaS): 1.2/S2](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 On-Premise IS (Non-S): 1.5/S1](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/On-Premise/Topics/Infrastructure-Security-(For-Non-S).aspx)
### BR-2: Recovery Testing

* **Group:** [Backup and Recovery](/catalog/br)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Conduct regular testing of recovery processes to ensure their effectiveness.

#### Control Recommendations

Ensure each test verifies the system's ability to fully restore all data and services.

#### Risk Statement

Failure to regularly test recovery processes may result in ineffective response during actual incidents, increasing the risk of prolonged downtime, data loss, and compromised business continuity in the event of a disaster or system failure.




#### Responsible Roles and Parties

* Maintainer:
  * System Administrators


#### By Components

* : Administrators regularly test the disaster recovery plan.
#### References


 * [MVSP 4.4: Backup and Disaster recovery](https://mvsp.dev/)
 * [IM8 Cloud Security (IaaS and PaaS): 1.2/S1d](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 On-Premise IS (Non-S): 1.5/S1d](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/On-Premise/Topics/Infrastructure-Security-(For-Non-S).aspx)
### PM-8: Software as a Service (SaaS) Service Level Agreement

* **Group:** [Security Programme Management](/catalog/pm)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Obtain a service level agreement with the Software as a Service (SaaS) provider that covers uptime, response times, downtime notifications, support avenues, and support content.

#### Control Recommendations

Ensure that the service level agreement is regularly checked for compliance.

#### Risk Statement

Without a service level agreement the availability of the Software as a Service (SaaS) system may be poorly maintained by the provider.




#### Responsible Roles and Parties

* Provider:
  * System Developers


#### By Components

* Service Level Agreement: SaaS providers provide a service level agreement.
