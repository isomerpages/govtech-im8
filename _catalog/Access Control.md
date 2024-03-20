---
title: Access Control
permalink: /catalog/ac/
variant: markdown
description: ""
---
# Access Control

Controls to protect against unauthorised access to agency systems.

| Controls |
| ---- |
| [AC-1: Principle of Least Privilege](#ac-1) |
| [AC-2: Multi-Factor Authentication (MFA)](#ac-2) |
| [AC-3: Inactive and Expired Accounts](#ac-3) |
| [AC-4: Access Review](#ac-4) |
| [AC-5: Endpoint Device Hardening](#ac-5) |
| [AC-6: Default Credentials](#ac-6) |
| [AC-7: SingPass/CorpPass for External Users](#ac-7) |
| [AC-8: Automate account provisioning](#ac-8) |
| [AC-9: Endpoint Device Management](#ac-9) |
| [AC-10: Identity and Device-Based Access Control](#ac-10) |
| [AC-11: Single User Endpoints](#ac-11) |
| [AC-12: Single Sign-On (SSO) for Internal Users](#ac-12) |


<a id="ac-1"></a>
## AC-1: Principle of Least Privilege

### Control Statement

Deny access by default and grant only the minimum permissions required for authorised accounts or processes to perform a specific function.

### Control Recommendations

Consider attribute- or feature-based access control for greater customisability and granularity.

### Risk Statement

Violating the principle of least privileges increases the risk of unauthorised access, privilege escalation, and potential security breaches due to unnecessary permissions, compromising the overall security posture.



<a id="ac-2"></a>
## AC-2: Multi-Factor Authentication (MFA)

### Control Statement

Require MFA for remote developer, maintainer, or administrator access.

### Control Recommendations

Ensure that the authentication factors are different and independent of the accessing device.

### Risk Statement

Without requiring phishing-resistant Multi-Factor Authentication (MFA) for remote access, there is an increased risk of unauthorised access, credential theft, and potential compromise of sensitive systems, especially for users with elevated privileges.



<a id="ac-3"></a>
## AC-3: Inactive and Expired Accounts

### Control Statement

Disable or remove accounts with developer, maintainer, or administrator access within [ac-3_prm_1] day(s) from last day of authorised use or have not been used for [ac-3_prm_2] day(s).

### Control Recommendations

Use automated checks such as AWS Config iam-user-unused-credentials-check to identify accounts and credentials that should be disabled. Consider using automated workflows such as System for Cross-domain Identity Management (SCIM) or identity lifecycle management tools.

### Risk Statement

Failure to disable or remove unused accounts or credentials with elevated access increases the risk of unauthorised access, as dormant accounts may become targets for exploitation, compromising the security of the system.



#### Parameters

| ID | Type | Description |
| -- | ---- | ----------- |
| ac-3_prm_1 | time period (days) | The time period in days after account expiry. |
| ac-3_prm_2 | time period (days) | The time period in days of account inactivity. |

<a id="ac-4"></a>
## AC-4: Access Review

### Control Statement

Perform an access review every [ac-4_prm_1] day(s) and remove unauthorised or unintended access rights within [ac-4_prm_2] day(s).

### Control Recommendations

Use tools such as AWS IAM Access Advisor or Azure AD Access Review to facilitate and manage access reviews.

### Risk Statement

Without regular access reviews and prompt removal of unauthorised or unintended access rights, there is an increased risk of lingering access, potential misuse of privileges, and compromised security, impacting the confidentiality and integrity of sensitive data.



#### Parameters

| ID | Type | Description |
| -- | ---- | ----------- |
| ac-4_prm_1 | time period (days) | The time period in days of access review frequency. |
| ac-4_prm_2 | time period (days) | The time period in days of access removal deadline. |

<a id="ac-5"></a>
## AC-5: Endpoint Device Hardening

### Control Statement

Require hardened endpoint devices for remote developer, maintainer, or administrator access.

### Control Recommendations

Use Endpoint Management platfoms such as Security Suite for Engineering Endpoint Devices (SEED) to continuously check and enforce device security posture and deny access if the hardening requirements are not met.

### Risk Statement

Without requiring hardened endpoint devices for remote access, there's an increased risk of compromised endpoints, potential malware infections, and security breaches, which could lead to unauthorised access and compromise the integrity of systems with developer, maintainer, or administrator access.



<a id="ac-6"></a>
## AC-6: Default Credentials

### Control Statement

Change default credentials prior to first use.

### Control Recommendations

Identify any default credentials used in any system components before deploying and change them. Configure end-user systems to prompt for password change on first login after account creation or reset.

### Risk Statement

Failure to change default credentials prior to first use increases the risk of unauthorised access, as default credentials are often well-known and targeted by attackers, compromising the security of the system or device.



<a id="ac-7"></a>
## AC-7: SingPass/CorpPass for External Users

### Control Statement

Use SingPass or CorpPass MFA for digital services that require high level of identity assurance for external users.

### Control Recommendations

For high impact or high risk transactions, use SingPass/CorpPass to identify external users (e.g. citizens). Internal users should use Government managed Single Sign-on (SSO) solutions (such as WOG AAD).

### Risk Statement

Leverage on SingPass or CorpPass to reduce duplication of effort and provide consistent end user experience.



<a id="ac-8"></a>
## AC-8: Automate account provisioning

### Control Statement

Implement automation of cloud and application account provisioning and deprovisioning using an account management tool.

### Control Recommendations

Adopt Single Sign-On (SSO) with just-in-time provisioning or account lifecycle management tools (such as SCIM or CAM) to assist with account management. For systems unable to use SSO, it is recommended to leverage account management lifecycle tools with HR records (such as CAM) to automatically provision and de-provision accounts.

### Risk Statement

Manual account and access provisioning can introduce errors and weaknesses, thus making access control measures ineffective and unreliable.



<a id="ac-9"></a>
## AC-9: Endpoint Device Management

### Control Statement

Implement and maintain a Device Management solution to ensure the security and integrity of endpoint devices used within the organisation.

### Control Recommendations

Deploy an Mobile Device Management (MDM) solution that enables management, monitoring, and secure configuration of endpoint devices. This includes enforcing disk encryption, managing configuration, ensuring regular updates, and providing the ability to remotely wipe data in case of device loss or theft.

### Risk Statement

Unmanaged endpoint devices increase the risk of unauthorized access and potential loss of sensitive information due to the compromise of devices.



<a id="ac-10"></a>
## AC-10: Identity and Device-Based Access Control

### Control Statement

Adopt Identity and Device-Based Access Control for secure and context-aware connectivity to private organisational resources.

### Control Recommendations

Use solutions such as Secure Service Edge (SSE), Identity Aware Proxies (IAP) or other Zero Trust services (Entra ID Conditional Access, Okta Device Trust, etc) that integrate identity and device management systems to provide granular access control to resources based on user identity and device posture.

### Risk Statement

Relying on direct connections or traditional VPNs for remote access can lead to vulnerabilities, as they do not always incorporate strong identity and device-based security measures. This increases the risk of unauthorized access and potential data breaches.



<a id="ac-11"></a>
## AC-11: Single User Endpoints

### Control Statement

Assign each endpoint device to a single designated primary user and enforce the assignment to ensure accountability and enhance security monitoring.

### Control Recommendations

Implement measures such as user authentication and endpoint management with device enrollment to enforce the single primary user per endpoint. If secondary accounts for local device support or maintenance activities consider securing with endpoint privilege management tools.

### Risk Statement

Allowing multiple users to access a single endpoint device can lead to security risks such as data leakage, difficulty in tracking user activities, and increased vulnerability to insider threats.



<a id="ac-12"></a>
## AC-12: Single Sign-On (SSO) for Internal Users

### Control Statement

Use Single Sign-On (SSO) for internal users and services.

### Control Recommendations

Configure multi-factor authentication (MFA) at the Single-Sign On (SSO) identity provider (IdP) and ensure that access to the system is only granted after the IdP authenticates the user. WOG AAD is recommended for public officers and TechPass AAD for developers.

### Risk Statement

Without Single Sign-On (SSO), there is an increased risk of unauthorized access and compromised user credentials, as users may resort to using weak passwords or reusing credentials across multiple systems, thereby exposing sensitive information to potential security breaches.




