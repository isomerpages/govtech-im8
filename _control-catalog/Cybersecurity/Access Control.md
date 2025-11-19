---
title: Access Control
permalink: /control-catalog/cybersecurity/ac/
variant: markdown
description: ""
third_nav_title: Cybersecurity
---
Controls to protect against unauthorised access to agency systems.

| Controls                                                                                                                                   |
| ------------------------------------------------------------------------------------------------------------------------------------------ |
| [AC-1: Principle of Least Privilege](#ac-1-principle-of-least-privilege)                                                                   |
| [AC-2: Multi-Factor Authentication (MFA)](#ac-2-multi-factor-authentication-mfa)                                                           |
| [AC-3: Inactive and Expired Accounts](#ac-3-inactive-and-expired-accounts)                                                                 |
| [AC-4: Access Review](#ac-4-access-review)                                                                                                 |
| [AC-5: Endpoint Device Hardening](#ac-5-endpoint-device-hardening)                                                                         |
| [AC-6: Default Credentials](#ac-6-default-credentials)                                                                                     |
| [AC-7: Singpass/Corppass for Public Users](#ac-7-singpasscorppass-for-public-users)                                                        |
| [AC-8: Automated Account Lifecycle Management](#ac-8-automated-account-lifecycle-management)                                               |
| [AC-9: Endpoint Device Management](#ac-9-endpoint-device-management)                                                                       |
| [AC-10: Identity and Device-Based Access Control](#ac-10-identity-and-device-based-access-control)                                         |
| [AC-11: Single User Endpoints](#ac-11-single-user-endpoints)                                                                               |
| [AC-12: Single Sign-On (SSO) for Internal Services and Accounts](#ac-12-single-sign-on-sso-for-internal-services-and-accounts)             |
| [AC-13: Static Credential Expiry and Rotation](#ac-13-static-credential-expiry-and-rotation)                                               |
| [AC-14: Inventory of Accounts](#ac-14-inventory-of-accounts)                                                                               |
| [AC-15: Validation Testing of Automated Account Lifecycle Management](#ac-15-validation-testing-of-automated-account-lifecycle-management) |
| [AC-16: Separation of Duties](#ac-16-separation-of-duties)                                                                                 |

## AC-1: Principle of Least Privilege

**Group:** Access Control

### Control Statement

Deny access by default and grant only the minimum permissions required for authorised accounts or processes to perform a specific function based on the account inventory implemented.

### Control Recommendations

Consider attribute- or feature-based access control for greater customisability and granularity. Use automated tools such as AWS IAM Access Advisor or Azure AD Access Review to assist with granular permission management.

### Risk Statement

Violating the principle of least privileges increases the risk of unauthorised access, privilege escalation, and potential security breaches due to unnecessary permissions, compromising the overall security posture.

## AC-2: Multi-Factor Authentication (MFA)

**Group:** Access Control

### Control Statement

Require MFA for privileged accounts at login.

### Control Recommendations

Ensure that the authentication factors are different and independent of the accessing device. For additional security, consider MFA for privileged actions at the application level (such as step-up MFA challenges via PIM tools).

### Risk Statement

Without requiring phishing-resistant Multi-Factor Authentication (MFA) for remote access, there is an increased risk of unauthorised access, credential theft, and potential compromise of sensitive systems, especially for accounts with elevated privileges.

## AC-3: Inactive and Expired Accounts

**Group:** Access Control

### Control Statement

Disable or remove [ insert: param, ac-3_prm_3 ] accounts within [ insert: param, ac-3_prm_1 ] day(s) from last day of authorised use or have not been used for [ insert: param, ac-3_prm_2 ] day(s).

### Control Recommendations

Use automated checks to identify accounts and credentials that should be disabled. Consider using automated workflows such as System for Cross-domain Identity Management (SCIM) or identity lifecycle management tools. For cloud service provider accounts, use tools such as AWS Config iam-user-unused-credentials-check to manage Identity and Access Management (IAM) Users.

### Risk Statement

Failure to disable or remove unused accounts or credentials with elevated access increases the risk of unauthorised access, as dormant accounts may become targets for exploitation, compromising the security of the system.

### Parameters

| ID         | Type                     | Description                                    |
| ---------- | ------------------------ | ---------------------------------------------- |
| ac-3_prm_1 | time period (days) (int) | The time period in days after account expiry.  |
| ac-3_prm_2 | time period (days) (int) | The time period in days of account inactivity. |
| ac-3_prm_3 | type (str)               | The type of accounts.                          |

## AC-4: Access Review

**Group:** Access Control

### Control Statement

Perform an access review [ insert: param, ac-4_prm_1 ] and remove unauthorised or unnecessary access rights within [ insert: param, ac-4_prm_2 ] day(s).

### Control Recommendations

For application accounts, implement automated review workflows or reports. For cloud service provider accounts and roles, use tools such as AWS IAM Access Advisor or Azure AD Access Review to facilitate and manage access reviews.

### Risk Statement

Without regular access reviews and prompt removal of unauthorised or unnecessary access rights, there is an increased risk of lingering access, potential misuse of privileges, and compromised security, impacting the confidentiality and integrity of sensitive data.

### Parameters

| ID         | Type                                 | Description                                 |
| ---------- | ------------------------------------ | ------------------------------------------- |
| ac-4_prm_1 | organisation-defined frequency (str) | The access review frequency.                |
| ac-4_prm_2 | time period (days) (int)             | The time period in days for access removal. |

## AC-5: Endpoint Device Hardening

**Group:** Access Control

### Control Statement

Require hardened endpoint devices for remote developer, maintainer, or administrator access.

### Control Recommendations

Use Endpoint Management platforms to continuously check and enforce device security posture and deny access if the hardening requirements are not met.

### Risk Statement

Without requiring hardened endpoint devices for remote access, there&#39;s an increased risk of compromised endpoints, potential malware infections, and security breaches, which could lead to unauthorised access and compromise the integrity of systems.

## AC-6: Default Credentials

**Group:** Access Control

### Control Statement

Change default credentials prior to first use.

### Control Recommendations

Identify any default credentials used in any system components before deploying and change them. Configure end-user systems to prompt for password change on first login after account creation or reset.

### Risk Statement

Failure to change default credentials prior to first use increases the risk of unauthorised access, as default credentials are often well-known and targeted by attackers, compromising the security of the system or device.

## AC-7: Singpass/Corppass for Public Users

**Group:** Access Control

### Control Statement

Use Singpass or Corppass MFA for digital services that require high level of identity assurance for Public Users.

### Control Recommendations

For high impact or high risk transactions, use Singpass/Corppass to identify Public Users (e.g. citizens). Agency or internal Users should use Government managed Single Sign-on (SSO) solutions (such as WOG AAD).

### Risk Statement

Leverage on Singpass or Corppass to reduce duplication of effort and provide consistent end user experience.

## AC-8: Automated Account Lifecycle Management

**Group:** Access Control

### Control Statement

Automate account [ insert: param, ac-8_prm_1 ] for [ insert: param, ac-8_prm_3 ] using an account lifecycle management tool.

### Control Recommendations

Consider adopting Single Sign-On (SSO) with just-in-time provisioning or account lifecycle management protocols or tools such as [ insert: param, ac-8_prm_2 ]. Perform validation testing of the integration between systems and tools to ensure that accounts are provisioned and/or deprovisioned in a timely manner. Where applicable, configure the system to enhance management capabilities via automation.

### Risk Statement

Manual account and access lifecycle management can introduce errors and weaknesses, thus making access control measures ineffective and unreliable.

### Parameters

| ID         | Type          | Description                                             |
| ---------- | ------------- | ------------------------------------------------------- |
| ac-8_prm_1 | process (str) | The account lifecycle management processes to automate. |
| ac-8_prm_2 | tool (str)    | Recommended account lifecycle management tool.          |
| ac-8_prm_3 | type (str)    | The type of accounts.                                   |

## AC-9: Endpoint Device Management

**Group:** Access Control

### Control Statement

Implement and maintain an endpoint device management solution to ensure the security and integrity of endpoint devices used within the organisation.

### Control Recommendations

Mobile Device Management (MDM) platforms enable management, monitoring, and secure configuration of endpoint devices. This includes enforcing disk encryption, managing configuration, ensuring regular updates, and providing the ability to remotely wipe data in case of device loss or theft.

### Risk Statement

Unmanaged endpoint devices increase the risk of unauthorised access and potential loss of sensitive information due to the compromise of devices.

## AC-10: Identity and Device-Based Access Control

**Group:** Access Control

### Control Statement

Adopt Identity and Device-Based Access Control for secure and context-aware connectivity to private organisational resources.

### Control Recommendations

Use solutions such as Secure Service Edge (SSE), Identity Aware Proxies (IAP) or other Zero Trust services (Entra ID Conditional Access, Okta Device Trust, etc) that integrate identity and device management systems to provide granular access control to resources based on user identity and device posture.

### Risk Statement

Relying on direct connections or traditional VPNs for remote access can lead to vulnerabilities, as they do not always incorporate strong identity and device-based security measures. This increases the risk of unauthorised access and potential data breaches.

## AC-11: Single User Endpoints

**Group:** Access Control

### Control Statement

Assign each endpoint device to a single designated primary [ insert: param, ac-11_prm_1 ] and enforce the assignment to ensure accountability and enhance security monitoring.

### Control Recommendations

Implement measures such as user authentication and endpoint management with device enrolment to enforce the single primary user per endpoint. If secondary accounts for local device support or maintenance activities are used, consider securing them with endpoint privilege management tools.

### Risk Statement

Allowing multiple users to access a single endpoint device can lead to security risks such as data leakage, difficulty in tracking user activities, and increased vulnerability to insider threats.

### Parameters

| ID          | Type       | Description                   |
| ----------- | ---------- | ----------------------------- |
| ac-11_prm_1 | type (str) | The type of user or identity. |

## AC-12: Single Sign-On (SSO) for Internal Services and Accounts

**Group:** Access Control

### Control Statement

Use Single Sign-On (SSO) for internal services and accounts.

### Control Recommendations

Configure multi-factor authentication (MFA) at the Single-Sign On (SSO) identity provider (IdP) and ensure that access to the system is only granted after the IdP authenticates the user.

### Risk Statement

Without Single Sign-On (SSO), there is an increased risk of unauthorised access and compromised user credentials, as users may resort to using weak passwords or reusing credentials across multiple systems, thereby exposing sensitive information to potential security breaches.

## AC-13: Static Credential Expiry and Rotation

**Group:** Access Control

### Control Statement

Rotate long-lived static credentials such as API keys, access keys, and personal access tokens every [ insert: param, ac-13_prm_1 ] day(s) or use time-restricted credentials.

### Control Recommendations

Automate credential rotation where possible. Consider time-restricted alternatives to long-lived static credentials, such as AWS Security Token Service and IAM Identity Center authentication instead of IAM user access keys.

### Risk Statement

Failure to regularly rotate long-lived credentials or use time-restricted credentials increases the risk of unauthorised access from stolen or unrevoked credentials.

### Parameters

| ID          | Type                     | Description                                      |
| ----------- | ------------------------ | ------------------------------------------------ |
| ac-13_prm_1 | time period (days) (int) | The time period in days for credential rotation. |

## AC-14: Inventory of Accounts

**Group:** Access Control

### Control Statement

Establish and maintain an inventory of all accounts and their access rights managed within the system.

### Control Recommendations

Regularly review and update the account inventory to ensure accuracy and completeness. Implement automated tools where feasible to assist in tracking and managing accounts and their access rights.

### Risk Statement

Failure to maintain an accurate inventory of managed accounts increases the risk of unauthorised access, account misuse, and security breaches due to unmonitored or orphaned accounts.

## AC-15: Validation Testing of Automated Account Lifecycle Management

**Group:** Access Control

### Control Statement

Conduct validation tests on the system integrated with account management tools to ensure secure integration.

### Control Recommendations

Where possible, test cases should include verifying that: account provisioning occurs solely through the account management tool(s), not directly on the SaaS; accounts are deactivated on the final day of authorised use; accounts are provisioned only after validating that access is permitted to the defined boundaries; and access rights match the account&#39;s assigned role and functions.

### Risk Statement

Failure to conduct validation tests on the integration of account management tools with SaaS platforms increases the risk of unauthorised access, improper account provisioning, and potential security breaches.

## AC-16: Separation of Duties

**Group:** Access Control

### Control Statement

Implement and maintain separation of duties for access and privileges to prevent any single individual from having excessive control over key processes or systems.

### Control Recommendations

Implement multiple complementary controls to enforce separation of duties, including but not limited to role-based access control (RBAC), Privileged Identity Management (PIM), and Just-In-Time (JIT) access. Where perfect separation is not feasible, use compensating controls such as audit logging, alerting, and rate limits. Consider using tools like Azure AD Privileged Identity Management or AWS Organizations for managing separation of duties in cloud environments.

### Risk Statement

Failure to implement separation of duties increases the risk of fraud, errors, and misuse of systems due to excessive concentration of privileges, potentially compromising the integrity and security of critical operations.
