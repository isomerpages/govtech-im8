---
title: Pilot Sandbox
permalink: /system-security-plans/pilot-sandbox/
variant: markdown
description: ""
---
# Pilot Sandbox

## Overview

The Pilot Sandbox System Security Plan template covers systems: 1) With not more than 10,000 users or under the Digital Incubator Programme (DIP); 2) Classified up to Restricted, Sensitive Normal systems; 3) Excluding National Emergency (NE) Critical, Critical Information Infrastructure (CII), Significant Information Infrastructure (SII); and 4) Not connected to the intranet (i.e., not connected to GSIB or GEN). Systems that are not part of a pilot sandbox should use the more general security plans (e.g. low risk cloud). This System Security Plan also covers the requirements stated in PMO(SNDGO) Circular Minute No. 8/2021 'A more risk-based and cost-effective security testing requirements for pilot projects'.

<p>
  <a href="/pilot-sandbox-ssp.xlsx">
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

* **Name:** Pilot Sandbox System
* **Description:** A generic pilot sandbox system.
* **Security Sensitivity Level:** Restricted, Sensitive Normal

## System Implementation

| Id | Type | Description |
| -- | ---- | ----------- |
| System | this-system | The system. |
| Source Code | software | Defines the instructions executed by the system's assets. |
| Web Application Firewall | service | Monitors and filters web requests to the system. |
| Secrets Manager | service | Manages credentials and secrets used by the system. |
| Continuous Integration/Continuous Delivery Workflow | process-procedure | Defines the CI/CD jobs that build, test, and deploy the system. |
| Vulnerability Assessment Scanner | service | Scans the system's workloads for software vulnerabilities and network exposure. |
| Penetration Testing Process | process-procedure | Ensures the system undergoes a penetration test. |
| Compute Management Service | service | Manages compute instances of the system. |
| System Security Plan | plan | Defines a system's characteristics and security control implementation. |
| Project Cybersecurity Risk Assessment | validation | Assesses the cybersecurity risks to the system and documents mitigating measures. |


## Control Implementation

### AS-1: Input Validation

* **Group:** [Application Security](/catalog/as)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Validate all application inputs to ensure that they match the expected type, structure, or format.

#### Control Recommendations

Strictly validating inputs against a comprehensive schema prevents injection attacks caused by inserting special characters or content that would cause the application to perform incorrect operations.

#### Risk Statement

Without input validation, there's a heightened risk of injection attacks, data manipulation, or system crashes due to unexpected input, potentially leading to unauthorised access or disruption of services.




#### Responsible Roles and Parties

* Maintainer:
  * System Developers
* Provider:
  * System Developers


#### By Components

* Source Code: Developers implement input validation in the source code.
#### References


 * [MVSP 2.5: Security libraries](https://mvsp.dev/)
 * [IM8 Cloud Security (IaaS and PaaS): 1.7/S1c](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 Cloud Security (IaaS and PaaS): 1.7/S8b](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 On-Premise ADS (Non-S): 1.1/S1b](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/On-Premise/Topics/Application-Development-Security-(For-Non-S).aspx)
### AS-2: Parametrised Interfaces

* **Group:** [Application Security](/catalog/as)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Use parametrised interfaces for database queries or system commands.

#### Control Recommendations

Parametrised interfaces such Object-Relational Mapping (ORM) libraries ensure that parameters used in database queries or system commands are properly sanitised and prevent injection attacks.

#### Risk Statement

Failure to use parameterised interfaces increases the vulnerability to SQL injection or command injection attacks, posing a significant risk of unauthorised access, data manipulation, or even potential system compromise.




#### Responsible Roles and Parties

* Maintainer:
  * System Developers
* Provider:
  * System Developers


#### By Components

* Source Code: Developers use parametrised interfaces in the source code.
#### References


 * [MVSP 2.5: Security libraries](https://mvsp.dev/)
 * [IM8 Cloud Security (IaaS and PaaS): 1.7/S8c](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 On-Premise ADS (Non-S): 1.1/S1c](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/On-Premise/Topics/Application-Development-Security-(For-Non-S).aspx)
### AS-3: Output Sanitisation

* **Group:** [Application Security](/catalog/as)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Sanitise all application outputs that will be used to render a HTML document.

#### Control Recommendations

Any application outputs that are returned to the requester and used to render a HTML document can lead to cross-site scripting (XSS) attacks if they contain special characters that change the rendering of the HTML document by the browser.

#### Risk Statement

Lack of sanitisation for application outputs used in rendering HTML documents exposes the system to the risk of cross-site scripting (XSS) attacks, allowing malicious code execution in users' browsers.




#### Responsible Roles and Parties

* Maintainer:
  * System Developers
* Provider:
  * System Developers


#### By Components

* Source Code: Developers implement output sanitisation in the source code.
#### References


 * [MVSP 2.5: Security libraries](https://mvsp.dev/)
 * [IM8 Cloud Security (IaaS and PaaS): 1.7/S8e](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 On-Premise ADS (Non-S): 1.1/S1e,k,l](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/On-Premise/Topics/Application-Development-Security-(For-Non-S).aspx)
### AS-4: Authentication Mechanism Rate-Limiting

* **Group:** [Application Security](/catalog/as)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Apply rate-limiting on all authentication mechanisms to deter brute-force attacks.

#### Control Recommendations

Consider rate-limiting to a maximum of 3 consecutive failed authentication attempts within 15 minutes. Time delays between log-on attempts reduce the risk of successful brute-forcing attacks. Bot mitigation tools such as CAPTCHA can further reduce this risk.

#### Risk Statement

Without rate-limiting, there's an increased risk of unauthorised access as attackers may exploit weak credentials through repeated login attempts.




#### Responsible Roles and Parties

* Maintainer:
  * System Administrators
  * System Developers
* Provider:
  * System Developers


#### By Components

* Source Code: Developers implement authentication mechanism rate-limiting in the source code.
* Web Application Firewall: Maintainers configure authentication mechanism rate-limiting in the web application firewall.
#### References


 * [MVSP 2.4: Password policy](https://mvsp.dev/)
 * [IM8 Cloud ADS: 2.2/S1j, 2.2/S5b](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Application-Development-Security-(For-Cloud).aspx)
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

* Maintainer:
  * System Developers
* Provider:
  * System Developers


#### By Components

* Source Code: Developers implement password requirements in the source code.
#### References


 * [MVSP 2.4: Password policy](https://mvsp.dev/)
 * [NIST SP 800-53 IA-5(1): Password-based Authentication](https://doi.org/10.6028/NIST.SP.800-53r5)
 * [IM8 Cloud Security (IaaS and PaaS): 1.4/S1a](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 Cloud Security (IaaS and PaaS): 1.4/S2a](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 On-Premise ADS (Non-S): 2.2/S1](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/On-Premise/Topics/Application-Development-Security-(For-Non-S).aspx)
### AS-6: Password Salting and Hashing

* **Group:** [Application Security](/catalog/as)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Store passwords as salted hashes using a password hashing scheme that is resistant to offline attacks such as those described in NIST [SP 800-63b](https://doi.org/10.6028/NIST.SP.800-63b). The salt should be:
 * Generated using a cryptographically secure pseudo-random number generator in accordance with industry standards;
 * At least 32 bits long; and
 * Randomly generated for each account.


#### Control Recommendations

Refer to NIST [SP 800-90Ar1](https://doi.org/10.6028/NIST.SP.800-90Ar1) for suitable pseudo-random number generators. Refer to NIST [SP 800-63b](https://doi.org/10.6028/NIST.SP.800-63b) Memorized Secret Verifiers section for suitable hashing schemes, including Argon2, scrypt, and PBKDF2. For application source code, use a cryptographically secure pseudo-random number generator function instead of an insecure one, such as crypto.randomBytes instead of Math.random in Node.js and java.security.SecureRandom.nextBytes instead of java.util.Random in Java.

#### Risk Statement

Without salting and hashing, in case of a data breach, exposed passwords can be easily extracted, leading to potential compromise of user accounts and sensitive information.




#### Responsible Roles and Parties

* Maintainer:
  * System Developers
* Provider:
  * System Developers


#### By Components

* Source Code: Developers implement password salting and hashing in the source code.
#### References


 * [MVSP 2.4: Password policy](https://mvsp.dev/)
 * [IM8 Cloud Security (IaaS and PaaS): 1.4/S3](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 On-Premise ADS (Non-S): 2.2/S3](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/On-Premise/Topics/Application-Development-Security-(For-Non-S).aspx)
### AS-7: Access Control Check Enforcement

* **Group:** [Application Security](/catalog/as)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Perform access control checks on all authenticated requests.

#### Control Recommendations

Utilise authorisation filters or middleware to force all authenticated requests to undergo access control checks.

#### Risk Statement

Failure to perform access control checks on authenticated requests increases the risk of unauthorised access to sensitive data or functionalities, potentially leading to data breaches and misuse of system resources.




#### Responsible Roles and Parties

* Maintainer:
  * System Developers
* Provider:
  * System Developers


#### By Components

* Source Code: Developers enforce access control checks in the source code.
#### References


 * [MVSP 3.3: Vulnerability prevention](https://mvsp.dev/)
 * [IM8 Cloud Security (IaaS and PaaS): 1.7/S8a](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
### AS-8: Application Secrets Management

* **Group:** [Application Security](/catalog/as)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Encrypt and store application secrets in a secret management solution with appropriate access controls and do not hard-code secrets in source code.

#### Control Recommendations

Secret management solutions include cloud solutions like AWS Secrets Manager and Azure Key Vault as well as cloud-agnostic solutions like HashiCorp Vault and CyberArk Conjur.

#### Risk Statement

Exposure of sensitive information and unauthorised access to system credentials may occur if application secrets are stored without encryption or if hard-coded in source code.




#### Responsible Roles and Parties

* Maintainer:
  * System Administrators
  * System Developers
* Provider:
  * System Developers


#### By Components

* Source Code: Developers implement secrets manager usage and do not hard-code secrets in the source code.
* Secrets Manager: Maintainers configure secret storage and encryption in the secrets manager.
#### References


 * [IM8 Cloud Security (IaaS and PaaS): 1.7/S11](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 On-Premise ADS (Non-S): 1.1/S1f, 2.2/S4, 3.1/S1 and 3.1/S4](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/On-Premise/Topics/Application-Development-Security-(For-Non-S).aspx)
### AS-9: Content Security Policy (CSP)

* **Group:** [Application Security](/catalog/as)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Set minimally permissive CSP response headers to mitigate cross-site scripting attacks.

#### Control Recommendations

Utilise the relevant fetch directives such as `default-src`, `script-src`, `style-src`, `connect-src`, `img-src`, `media-src` and `object-src` to prevent loading of scripts from malicious sources. Refer to the [OWASP Secure Headers Project](https://owasp.org/www-project-secure-headers) Best Practices for recommended header values.

#### Risk Statement

Without minimally permissive Content Security Policy (CSP) headers, the risk of cross-site scripting attacks, leading to unauthorised script execution and potential data theft, is increased.




#### Responsible Roles and Parties

* Maintainer:
  * System Developers
* Provider:
  * System Developers


#### By Components

* Source Code: Developers implement Content Security Policy headers in the source code.
#### References


 * [MVSP 2.3: Security Headers](https://mvsp.dev/)
 * [IM8 Cloud Security (IaaS and PaaS): 1.7/G7](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
### AS-10: HTTP Strict Transport Security (HSTS)

* **Group:** [Application Security](/catalog/as)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Set HTTP Strict Transport Security (HSTS) response headers with a maximum age value of at least 1 year (31536000 seconds) to mitigate protocol downgrade attacks.

#### Control Recommendations

Refer to the [OWASP Secure Headers Project](https://owasp.org/www-project-secure-headers) Best Practices for recommended header values.

#### Risk Statement

Failure to implement HTTP Strict Transport Security (HSTS) with a sufficient maximum age may expose the system to protocol downgrade attacks, compromising the security of communication channels.




#### Responsible Roles and Parties

* Maintainer:
  * System Developers
* Provider:
  * System Developers


#### By Components

* Source Code: Developers implement HTTP Strict Transport Security headers in the source code.
#### References


 * [IM8 Cloud Security (IaaS and PaaS): 1.7/G4](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
### AS-11: Session Management

* **Group:** [Application Security](/catalog/as)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Require users to re-authenticate after their session exceeds [as-11_prm_1: 720] hour(s) or terminate the session.

#### Control Recommendations

NIST SP 800-63B recommends re-authentication once per 30 days for Authenticator Assurance Level 1, 12 hours or 30 minutes inactivity for Authenticator Assurance Level 2, and 12 hours or 15 minutes inactivity for Authenticator Assurance Level 3. In addition to time period, system can consider re-authentication when roles, authenticators or credentials change or when the execution of privileged functions occurs.

#### Risk Statement

Not verifying a user regularly and at suitable checkpoints could allow someone who has access to the user's account to carry out unauthorised actions.




#### Responsible Roles and Parties

* Maintainer:
  * System Developers
* Provider:
  * System Developers


#### By Components

* Source Code: Developers implement re-authentication conditions in the source code.
#### References


 * [NIST SP 800-53 AC-12: Session Termination](https://doi.org/10.6028/NIST.SP.800-53r5)
 * [NIST SP 800-53 IA-11: Re-authentication](https://doi.org/10.6028/NIST.SP.800-53r5)
 * [IM8 Cloud ADS: 2.5/S2](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Application-Development-Security-(For-Cloud).aspx)
 * [NIST SP 800-63B 4.2.3: Reauthentication](https://doi.org/10.6028/NIST.SP.800-63b)
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
### SD-4: Static Analysis

* **Group:** [Secure Development](/catalog/sd)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Set up a static analysis job in the development CI/CD pipeline that runs on each merge request, and remediate or risk accept true positive vulnerability findings before merging into the production branch.

#### Control Recommendations

Static analysis tools (such as SAST or IaC security scanners) check source code for common vulnerabilities and misconfigurations. By running static analysis tools earlier in the DevSecOps cycle, vulnerabilities can be detected and prevented from being deployed to production.

#### Risk Statement

Without setting up static analysis in the CI/CD pipeline for each merge request and addressing true positive vulnerability findings, there is an increased risk of deploying insecure code to the production branch, potentially leading to security breaches and compromise of the overall system.




#### Responsible Roles and Parties

* Maintainer:
  * System Developers
* Provider:
  * System Developers


#### By Components

* Continuous Integration/Continuous Delivery Workflow: Developers implement static analysis in the CI/CD workflow.
#### References


 * [IM8 Cloud ADS: 6.4/S2](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Application-Development-Security-(For-Cloud).aspx)
 * [IM8 On-Premise ADS (Non-S): 4.1/S1](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/On-Premise/Topics/Application-Development-Security-(For-Non-S).aspx)
### ST-1: Vulnerability Assessment

* **Group:** [Security Testing](/catalog/st)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Run [st-1_prm_1: agent-based] vulnerability assessment scans for eligible hosts.

#### Control Recommendations

Select agent-based or network-based scans as necessary. Use scanners such as Amazon Inspector that support continuous scanning. Use authenticated scans for greater coverage.

#### Risk Statement

Without regular vulnerability assessment scans, hosts remain exposed to undetected security vulnerabilities, increasing the risk of exploitation and unauthorised access to critical systems.




#### Responsible Roles and Parties

* Maintainer:
  * System Administrators
  * System Developers
* Provider:
  * System Developers


#### By Components

* Vulnerability Assessment Scanner: Maintainers set up continuous vulnerability assessment scans with the vulnerability assessment service.
#### References


 * [IM8 Cloud Security (IaaS and PaaS): 1.8/S1](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
### ST-4: Penetration Testing

* **Group:** [Security Testing](/catalog/st)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Conduct and document a penetration test by internal teams or independent external parties every [st-4_prm_1: 365] day(s).

#### Control Recommendations

A white-box penetration test should be performed to effectively test the application.

#### Risk Statement

Without conducting and documenting penetration tests, there's an increased risk of undetected security weaknesses, leaving the application susceptible to exploitation, data breaches, and unauthorised access.




#### Responsible Roles and Parties

* Asset-owner:
  * System Owners
* Asset-administrator:
  * System Administrators


#### By Components

* Penetration Testing Process: Owners and administrators arrange regular penetration testing of according to the recommended process.
#### References


 * [MVSP 1.4: External testing](https://mvsp.dev/)
 * [IM8 Cloud Security (IaaS and PaaS): 1.8/S1](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 On-Premise ADS (Non-S): 4.1/S1](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/On-Premise/Topics/Application-Development-Security-(For-Non-S).aspx)
### ST-5: Vulnerability Management

* **Group:** [Security Testing](/catalog/st)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Triage and then remediate or risk accept all true positive vulnerability findings discovered through security testing within the following timeframe based on severity:
 * Critical: [st-5_prm_1: 14] day(s)
 * High: [st-5_prm_2: 30] day(s)
 * Medium: [st-5_prm_3: 60] day(s)
 * Low: [st-5_prm_4: 60] day(s)


#### Control Recommendations

Seek approval from the appropriate approving authority for risk acceptance.

#### Risk Statement

Failure to promptly remediate vulnerabilities increases the risk of potential exploits, security breaches, and prolonged exposure to known vulnerabilities in the system.




#### Responsible Roles and Parties

* Maintainer:
  * System Administrators


#### By Components

* System: Maintainers triage and remediate vulnerability findings in the systems.
#### References


 * [MVSP 3.4: Time to fix vulnerabilities](https://mvsp.dev/)
 * [IM8 Cloud Security (IaaS and PaaS): 1.8/S3](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 Cloud Security (IaaS and PaaS): 1.8/S4](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 On-Premise ADS (Non-S): 5.1/S3](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/On-Premise/Topics/Application-Development-Security-(For-Non-S).aspx)
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

* System: Administrators configure the system to enforce the principle of least privilege.
#### References


 * [MVSP 4.2: Logical access](https://mvsp.dev/)
 * [IM8 Cloud Security (IaaS and PaaS): 1.4/S7](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 Cloud Security (IaaS and PaaS): 1.5/S4e](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 Cloud Security (IaaS and PaaS): 1.7/S1b](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
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

* Maintainer:
  * System Developers
  * System Administrators
* Provider:
  * System Developers


#### By Components

* System: Maintainers encrypt the system's data at rest.
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

* Maintainer:
  * System Developers
  * System Administrators
* Provider:
  * System Developers


#### By Components

* System: Maintainers encrypt the system's data in transit.
#### References


 * [MVSP 2.8: Encryption](https://mvsp.dev/)
 * [IM8 Cloud Security (IaaS and PaaS): 1.3/S2b](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 On-Premise ADS (Non-S): 3.1/S3](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/On-Premise/Topics/Application-Development-Security-(For-Non-S).aspx)
### IS-2: Automated Patch Management

* **Group:** [Infrastructure Security](/catalog/is)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Automate patching of operating systems and applications.

#### Control Recommendations

Apply patch baselines via the CSP node management service, unless the patch management process is automated as part of the build and deploy phase.

#### Risk Statement

Failure to automate patching of operating systems and applications increases the risk of delayed or missed security updates, leaving systems vulnerable to known exploits and potential security breaches, compromising the overall security of the environment.




#### Responsible Roles and Parties

* Maintainer:
  * System Administrators
  * System Developers
* Provider:
  * System Developers


#### By Components

* Compute Management Service: Maintainers automate patching in the compute management service.
#### References


 * [IM8 Cloud Security (IaaS and PaaS): 1.7/S12](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 Cloud Security (IaaS and PaaS): 1.8/S4](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
