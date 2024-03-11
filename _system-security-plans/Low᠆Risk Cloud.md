---
title: Low᠆Risk Cloud
permalink: /system-security-plans/low-risk-cloud/
variant: markdown
description: ""
---
# Low-Risk Cloud

## Overview

The Low-Risk Cloud System Security Plan template includes Level 0 and Level 1 baseline controls that are recommended as the default controls for low-risk cloud systems classified up to Restricted, Sensitive Normal systems, excluding National Emergency (NE) Critical, Critical Information Infrastructure (CII), Significant Information Infrastructure (SII). Agencies may customise this template to create their own system-specific System Security Plan or use it as a default System Security Plan for generic low-risk cloud systems.

<p>
  <a href="/low-risk-cloud-ssp.xlsx">
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

* **Name:** Low-Risk Cloud System
* **Description:** A generic system hosted on the cloud through a third-party Cloud Service Provider.
* **Security Sensitivity Level:** Restricted, Sensitive Normal

## System Implementation

| Id | Type | Description |
| -- | ---- | ----------- |
| System | this-system | The system. |
| Source Code | software | Defines the instructions executed by the system's assets. |
| Web Application Firewall | service | Monitors and filters web requests to the system. |
| Secrets Manager | service | Manages credentials and secrets used by the system. |
| Code Repository | service | Stores and manages the source code of the system using a version control system. |
| Continuous Integration/Continuous Delivery Workflow | process-procedure | Defines the CI/CD jobs that build, test, and deploy the system. |
| Continuous Integration/Continuous Delivery Platform | service | Executes and manages CI/CD workflows. Often overlaps with the code repository. |
| Vulnerability Assessment Scanner | service | Scans the system's workloads for software vulnerabilities and network exposure. |
| Cloud Security Posture Management Service | service | Scans the system's cloud asset configuration for insecure configurations. |
| Penetration Testing Process | process-procedure | Ensures the system undergoes a penetration test. |
| Virtual Networks | network | Contains and connects the hosts and services of the system. |
| Distributed Denial of Service Protection | service | Monitors and filters network and application layer traffic to the system. |
| Content Delivery Network | service | Distributes traffic geographically to the system. |
| Certificate Manager | service | Manages SSL/TLS certificates used by the system. |
| Backup Service | service | Automates and manages backups of the system. |
| Backup Storage | service | Stores backups of the system. |
| Disaster Recovery Plan | plan | Provides instructions on how to respond and restore access and functionality to the system after unplanned incidents. |
| Cloud Audit Logging Service | service | Logs audit in the cloud service provider. |
| Log Storage | service | Stores logs of the system. |
| Database | service | Stores data of the system. |
| Application Load Balancer | service | Routes traffic to the system at the request level (layer 7). |
| Security Monitoring Service | service | Monitors system assets for security events. |
| Resource Usage Monitoring Service | service | Monitors resource usage of the system. |
| Availability Monitoring Service | service | Monitors system assets for downtime. |
| Identity and Access Management Service | software | Manages access control and identity of the system's maintainers and administrators. |
| Endpoint Device | physical | Accesses remote developer, maintainer, or administrator resources. |
| Container Image Build Instructions | process-procedure | Lists commands to build a container image used in the system. |
| Container Image Registry | service | Manages and distributes container images used by the system. |
| Kubernetes Service | service | Manages the Kubernetes control planes and nodes of the system. |
| Cybersecurity Incident Management Plan | plan | Provides instructions on how to respond to cybersecurity incidents. |
| System Security Plan | plan | Defines a system's characteristics and security control implementation. |
| Project Cybersecurity Risk Assessment | validation | Assesses the cybersecurity risks to the system and documents mitigating measures. |
| Compute Management Service | service | Manages compute instances of the system. |
| Hosted Virtual Machine | service | Runs system workloads. |
| Software Asset | software | Performs computation, data storage, processing, and communication functions. |


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

### SC-1: Code Repository

* **Group:** [Software Supply Chain](/catalog/sc)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Manage the codebase in a central code repository with version control.

#### Control Recommendations

Use common platforms such as SHIP-HATS 2.0 GitLab or equivalents.

#### Risk Statement

Absence of centralised code repository and version control increases the risk of code inconsistencies, loss of code history, and difficulties in collaboration, potentially leading to errors and security vulnerabilities.




#### Responsible Roles and Parties

* Maintainer:
  * System Developers
* Provider:
  * System Developers



#### By Components

* Code Repository: Developers manage the codebase in the code repository.



#### References

 * [IM8 Cloud ADS: 7.1/S1](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Application-Development-Security-(For-Cloud).aspx)

### SC-2: Commit Signing

* **Group:** [Software Supply Chain](/catalog/sc)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Configure the code repository to reject unsigned commits.

#### Control Recommendations

Use GitLab's push rules, GitHub's branch protection rules or similar code repository controls to reject unsigned commits on push.

#### Risk Statement

Allowing unsigned commits in the code repository introduces the risk of unauthorised or malicious code changes, compromising the integrity and security of the software development process.




#### Responsible Roles and Parties

* Maintainer:
  * System Developers
* Provider:
  * System Developers



#### By Components

* Code Repository: Developers configure the code repository to reject unsigned commits.

### SC-3: Peer Review

* **Group:** [Software Supply Chain](/catalog/sc)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Require peer review and approval by a designated reviewer before merging into the default branch.

#### Control Recommendations

Use GitLab's protected branch and merge request settings, GitHub's branch protection settings or similar code repository controls to enforce this.

#### Risk Statement

Without peer review and approval before merging, there is an increased risk of introducing undetected coding errors, security vulnerabilities, and maintaining codebase consistency may become challenging.




#### Responsible Roles and Parties

* Maintainer:
  * System Developers
* Provider:
  * System Developers



#### By Components

* Code Repository: Developers configure the code repository to require peer review and approval.



#### References

 * [IM8 Cloud Security (IaaS and PaaS): 1.1/S2](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 Cloud ADS: 8.1/G1](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Application-Development-Security-(For-Cloud).aspx)

### SC-4: Dependency Manifest Version Pinning

* **Group:** [Software Supply Chain](/catalog/sc)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Pin direct and transitive dependency versions in the application's dependency manifest.

#### Control Recommendations

Dependency manifests such as package-lock.json for npm and Pipfile.lock for pipenv allow you to pin dependency versions.

#### Risk Statement

Failure to pin direct and transitive dependency versions in the application's manifest may lead to version drift, introducing compatibility issues, security vulnerabilities, and unpredictability in the software environment.




#### Responsible Roles and Parties

* Maintainer:
  * System Developers
* Provider:
  * System Developers



#### By Components

* Source Code: Developers pin versions in the dependency manifest.



#### References

 * [SLSA Build L1: Provenance exists](https://slsa.dev)
 * [IM8 Cloud ADS: 8.1/G4](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Application-Development-Security-(For-Cloud).aspx)

### SC-5: Software Composition Analysis

* **Group:** [Software Supply Chain](/catalog/sc)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Perform regular software composition analysis of application code that can be exported as a software bill of materials (SBOM).

#### Control Recommendations

Software composition analysis can be performed using tools such as Gitlab, Nexus IQ, or their equivalent, with output in a common SBOM format such as SPDX or CycloneDX.

#### Risk Statement

Without regular software composition analysis, the risk of using outdated or vulnerable third-party components in the application increases, potentially exposing it to security exploits.




#### Responsible Roles and Parties

* Maintainer:
  * System Developers
* Provider:
  * System Developers



#### By Components

* Continuous Integration/Continuous Delivery Workflow: Developers implement a software composition analysis job in the CI/CD workflow.



#### References

 * [SLSA Build L1: Provenance exists](https://slsa.dev)
 * [IM8 Cloud Security (IaaS and PaaS): 1.7/S8i](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 Cloud ADS: 6.1/S1c](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Application-Development-Security-(For-Cloud).aspx)
 * [IM8 On-Premise ADS (Non-S): 1.1/S1i](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/On-Premise/Topics/Application-Development-Security-(For-Non-S).aspx)

### SC-6: Automated Build and Deploy

* **Group:** [Software Supply Chain](/catalog/sc)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Provision and operate systems in a consistent manner using automation.

#### Control Recommendations

Deploy and maintain Infrastructure and Applications with automated and repeatable tools such as CI/CD Pipelines, Infrastructure as Code (IaC) and other scripts. Automated build and deploy pipelines allow for signing and validation of build artefacts. Do not make manual changes directly into production systems.

#### Risk Statement

Inconsistent system provisioning and operation, without automation, may lead to configuration drift, increased likelihood of errors, and heightened vulnerability to security breaches due to manual misconfigurations.




#### Responsible Roles and Parties

* Maintainer:
  * System Developers
* Provider:
  * System Developers



#### By Components

* Continuous Integration/Continuous Delivery Workflow: Developers implement automated build and deploy in the CI/CD workflow.



#### References

 * [MVSP 3.5: Build process](https://mvsp.dev/)
 * [SLSA Build L1: Provenance exists](https://slsa.dev)
 * [IM8 Cloud Security (IaaS and PaaS): 1.7/S22](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 Cloud ADS: 6.1/G4](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Application-Development-Security-(For-Cloud).aspx)

### SC-7: Dependency Installation during Deployment

* **Group:** [Software Supply Chain](/catalog/sc)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

When installing dependencies during deployment, only install pinned versions in the manifest.

#### Control Recommendations

Use package manager commands such as npm ci for npm and pipenv sync for pipenv that ensure only versions specified in the manifest are installed rather than the latest version.

#### Risk Statement

Failure to install only pinned versions of dependencies during deployment increases the risk of introducing unforeseen changes, compatibility issues, and potential security vulnerabilities into the deployed environment.




#### Responsible Roles and Parties

* Maintainer:
  * System Developers
* Provider:
  * System Developers



#### By Components

* Continuous Integration/Continuous Delivery Workflow: Developers configure the CI/CD workflow to only install pinned versions in the manifest.



#### References

 * [SLSA Build L1: Provenance exists](https://slsa.dev)

### SD-1: Push Protection for Secrets

* **Group:** [Secure Development](/catalog/sd)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Configure the code repository to prevent secrets from being pushed to the repository.

#### Control Recommendations

Use GitLab's push rules or GitHub's push protection to reject secrets on push.

#### Risk Statement

Failure to configure the code repository to prevent secrets from being pushed introduces the risk of inadvertent exposure, unauthorised access, and potential misuse of sensitive information, compromising the security of the codebase and associated systems.




#### Responsible Roles and Parties

* Maintainer:
  * System Developers
* Provider:
  * System Developers



#### By Components

* Code Repository: Developers configure the code repository to prevent secrets from being pushed.



#### References

 * [IM8 Cloud ADS: 6.4/G1](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Application-Development-Security-(For-Cloud).aspx)

### SD-2: Default Branch Push Permissions

* **Group:** [Secure Development](/catalog/sd)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Configure the code repository to prevent pushes (including force pushes) to the default branch.

#### Control Recommendations

Use GitLab's protected branch and merge request settings or GitHub's branch protection settings to enforce this.

#### Risk Statement

Without configuring the code repository to prevent pushes, including force pushes, to the default branch, there's an increased risk of unintentional or malicious changes, potential loss of code history, and compromised version control, impacting the integrity and reliability of the software development process.




#### Responsible Roles and Parties

* Maintainer:
  * System Developers
* Provider:
  * System Developers



#### By Components

* Code Repository: Developers configure the code repository to reject pushes to the default branch.

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

### SD-5: Dependency Scanning

* **Group:** [Secure Development](/catalog/sd)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Schedule a scan at least every [sd-5_prm_1: 7] day(s) in the CI/CD pipeline and/or repository to identify the use of vulnerable software libraries.

#### Control Recommendations

Dependency scanning checks the source code for dependencies with known vulnerabilities. By running scans regularly using bots or software composition analysis (SCA) tools, vulnerabilities arising from outdated dependencies can be quickly detected and patched. Triage and prioritise vulnerabilities against Common Vulnerability Scoring System (CVSS), Known Exploited Vulnerabilities (KEV) Catalog, Vulnerability Exploitability eXchange (VEX) and other sources.

#### Risk Statement

Failing to schedule regular scans in the CI/CD pipeline to identify vulnerable software libraries and address findings in a timely manner increases the risk of deploying applications with known vulnerabilities, potentially exposing the system to security exploits and compromise.




#### Responsible Roles and Parties

* Maintainer:
  * System Developers
* Provider:
  * System Developers



#### By Components

* Continuous Integration/Continuous Delivery Workflow: Developers implement dependency scanning in the CI/CD workflow.
* Code Repository: Developers configure a dependency scanning bot on the code repository.



#### References

 * [MVSP 2.6: Dependency Patching](https://mvsp.dev/)
 * [IM8 Cloud Security (IaaS and PaaS): 1.7/S8i](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 Cloud ADS: 8.1/S2](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Application-Development-Security-(For-Cloud).aspx)

### SD-6: Secret Detection Scanning

* **Group:** [Secure Development](/catalog/sd)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Set up a secret detection alert or job in the development CI/CD pipeline that runs on each commit and remediate true positives within [sd-6_prm_1: 1] day(s).

#### Control Recommendations

Ensure that the exposed secret is revoked and purged from the Git history.

#### Risk Statement

Without setting up secret detection alerts or jobs in the development CI/CD pipeline and addressing true positive findings promptly, there's an increased risk of exposing sensitive information, potential unauthorized access, and compromised security.




#### Responsible Roles and Parties

* Maintainer:
  * System Developers
* Provider:
  * System Developers



#### By Components

* Continuous Integration/Continuous Delivery Workflow: Developers implement secret detection scanning in the CI/CD workflow.
* Code Repository: Developers configure a secret detection alert on the code repository.



#### References

 * [IM8 Cloud Security (IaaS and PaaS): 1.7/S8f](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 Cloud ADS: 1.1/S1f](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Application-Development-Security-(For-Cloud).aspx)
 * [IM8 Cloud ADS: 6.4/G1b](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Application-Development-Security-(For-Cloud).aspx)

### SD-7: CI Environment Variable Secrets Management

* **Group:** [Secure Development](/catalog/sd)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Protect environment variable secrets used in CI jobs by limiting them to protected pipelines and masking them in job logs.

#### Control Recommendations

Use GitLab's CI/CD variable security settings or GitHub's encrypted secrets with the add-mask workflow command.

#### Risk Statement

Failing to protect environment variable secrets in CI jobs by limiting them to protected pipelines and masking them in job logs increases the risk of unauthorized access and exposure of sensitive information.




#### Responsible Roles and Parties

* Maintainer:
  * System Developers
* Provider:
  * System Developers



#### By Components

* Continuous Integration/Continuous Delivery Platform: Developers configure the CI/CD platform to protect environment variable secrets.

### SD-8: Deployment Environment Segregation

* **Group:** [Secure Development](/catalog/sd)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Segregate production and non-production environments including applications, services, data, secrets, roles, and networks.

#### Control Recommendations

Achieve segregation using separate Government on Commercial Cloud (GCC) accounts for environments such as production, development, test, and staging. Account segregation enhances security by limiting exposure, simplifies resource and cost management, maintains configuration integrity, facilitates compliance and auditing and streamlines operational tasks. Deploy and operate environments as similarly as possible to enhance debugging and time-to-market.

#### Risk Statement

Failure to segregate production and non-production environments increases the risk of unauthorized access, data leaks, and denial of service attacks, as compromises in non-production environments may lead to cascading impacts on production systems.




#### Responsible Roles and Parties

* Maintainer:
  * System Developers
* Provider:
  * System Developers



#### By Components

* System: Developers segregate production and non-production environments in the system.



#### References

 * [MVSP 4.2: Logical access](https://mvsp.dev/)
 * [IM8 Cloud Security (IaaS and PaaS): 1.4/S9](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)

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

### ST-2: Cloud Security Posture Management

* **Group:** [Security Testing](/catalog/st)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Set up cloud security posture management that performs continuous configuration scans on cloud assets.

#### Control Recommendations

Use cloud security posture management tools such as CloudSCAPE, AWS Security Hub, and Datadog Cloud Security Posture Management.

#### Risk Statement

Lack of continuous configuration scans through cloud security posture management increases the risk of misconfigurations in cloud assets, leading to security vulnerabilities, data breaches, and unauthorised access.




#### Responsible Roles and Parties

* Maintainer:
  * System Administrators
  * System Developers
* Provider:
  * System Developers



#### By Components

* Cloud Security Posture Management Service: Maintainers set up continuous configuration scans with the cloud security posture management service.



#### References

 * [IM8 Cloud Security (IaaS and PaaS): 1.1/S6](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)

### ST-3: Vulnerability Disclosure Programme

* **Group:** [Security Testing](/catalog/st)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Display a way to responsibly disclose vulnerabilities via the Government Vulnerability Disclosure Programme.

#### Control Recommendations

Add a link to https://go.gov.sg/report-vulnerability on all pages, such as in the footer.

#### Risk Statement

Publicly disclosing vulnerabilities without following a responsible disclosure process increases the risk of malicious exploitation; responsible disclosure via the Government Vulnerability Disclosure Programme ensures a coordinated and secure approach to addressing vulnerabilities.




#### Responsible Roles and Parties

* Maintainer:
  * System Developers
* Provider:
  * System Developers



#### By Components

* Source Code: Developers add a visible vulnerability disclosure element in the source code.



#### References

 * [MVSP 1.1: Vulnerability reports](https://mvsp.dev/)
 * [IM8 On-Premise ADS (Non-S): 5.1/S4](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/On-Premise/Topics/Application-Development-Security-(For-Non-S).aspx)

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

### NS-1: Public and Private Subnet Segmentation

* **Group:** [Network Security](/catalog/ns)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Place private resources (e.g., databases) in private subnets and public resources (e.g., reverse proxies, web servers) in public subnets within a virtual network.

#### Control Recommendations

This control does not apply to serverless resources (API Gateways), static sites or assets fronted by CDNs (e.g., CloudFlare, CloudFront) which are located outside of the virtual network. Private subnets do not allow direct connections from the internet while public subnets do. However, resources in private segments can connect to the internet via NAT Gateways in public subnets in the same virtual network.

#### Risk Statement

Failure to segregate private and public resources within distinct subnets in a virtual network increases the risk of unauthorised access to sensitive data, as private resources may be exposed to the public internet, compromising the overall security of the infrastructure.




#### Responsible Roles and Parties

* Maintainer:
  * System Developers
* Provider:
  * System Developers



#### By Components

* Virtual Networks: Developers segment public and private resources and subnets in the virtual networks.



#### References

 * [IM8 Cloud Security (IaaS and PaaS): 1.5/S1](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 Cloud Security (IaaS and PaaS): 1.5/S2](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 Cloud Security (IaaS and PaaS): 1.7/S14](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 On-Premise IS (Non-S): 4.2/S1a](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/On-Premise/Topics/Infrastructure-Security-(For-Non-S).aspx)
 * [IM8 On-Premise AAS (Non-S): 1.1/S1, 2.1/S1](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/On-Premise/Topics/Application-Architecture-Security-(For-Non-S).aspx)
 * [IM8 Cloud Security (IaaS and PaaS): 1.5/S6b](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)

### NS-2: Access Restrictions on CSP Resources Outside Virtual Network

* **Group:** [Network Security](/catalog/ns)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Restrict access to CSP resources outside of a virtual network (e.g., Lambda, DynamoDb, API Gateways, S3, CloudFront) using access controls or application layer authorisation.

#### Control Recommendations

Apply access restrictions appropriate to the resource type. Access through interface VPC endpoints is only required if the client is hosted in a private subnet. For example:

* Restrict access to DynamoDB with IAM policies.

* Restrict access to API Gateway with Lambda Authorizers or authorisation middlewares at the application layer. If the API Gateway is exposed to private subnets, create a [private API](https://docs.aws.amazon.com/apigateway/latest/developerguide/apigateway-private-apis.html).

* Restrict access to S3 Buckets with IAM policies and block public access from the internet.

#### Risk Statement

Lack of access restrictions raises the risk of unauthorised access, data exposure, and potential misuse of critical services, compromising the overall security posture.




#### Responsible Roles and Parties

* Maintainer:
  * System Developers
* Provider:
  * System Developers



#### By Components

* System: Developers implement access restrictions on CSP resources outside of the virtual networks.



#### References

 * [IM8 Cloud Security (IaaS and PaaS): 1.5/S2](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 Cloud Security (IaaS and PaaS): 1.5/S5](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 Cloud Security (IaaS and PaaS): 1.7/S23](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)

### NS-3: Deny by Default – Allow by Exception

* **Group:** [Network Security](/catalog/ns)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Deny network communications traffic by default and allow network communications traffic by exception at managed interfaces.

#### Control Recommendations

Configure network access control lists and security groups to deny all traffic by default. Only allow traffic to and from specific hosts and ports by exception. For egress traffic to the internet, consider whitelisting domains at the application layer or DNS resolver rather than just hosts or ports at the transport layer.

#### Risk Statement

Without network access controls, there's an increased risk of unauthorised or malicious network access, leading to potential security breaches and compromise of system integrity.




#### Responsible Roles and Parties

* Maintainer:
  * System Developers
* Provider:
  * System Developers



#### By Components

* Virtual Networks: Developers deny network communications traffic by default in the virtual networks.



#### References

 * [NIST SP 800-53 SC-7(5): Deny by Default – Allow by Exception](https://doi.org/10.6028/NIST.SP.800-53r5)
 * [IM8 Cloud Security (IaaS and PaaS): 1.5/S3](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 Cloud Security (IaaS and PaaS): 1.5/S5](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 Cloud Security (IaaS and PaaS): 1.6/S1h](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 Cloud Security (IaaS and PaaS): 1.7/S23b](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 On-Premise IS (Non-S): 4.2/S1b](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/On-Premise/Topics/Infrastructure-Security-(For-Non-S).aspx)
 * [IM8 On-Premise AAS (Non-S): 2.2/S1](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/On-Premise/Topics/Application-Architecture-Security-(For-Non-S).aspx)

### NS-4: Inter-Private Network Connectivity

* **Group:** [Network Security](/catalog/ns)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Route network traffic between private networks without going through the internet.

#### Control Recommendations

Use CSP Private endpoint services (e.g., AWS PrivateLink with VPC endpoints) when you want to allow one or more consumer VPCs unidirectional access to a specific service or set of instances in the service provider VPC. Otherwise, use VPC peering and Transit Gateway when you want to enable layer-3 IP connectivity between VPCs. Refer to the [Multi-VPC AWS Network Infrastructure Whitepaper](https://docs.aws.amazon.com/whitepapers/latest/building-scalable-secure-multi-vpc-network-infrastructure/vpc-to-vpc-connectivity.html) for further guidance.

#### Risk Statement

When routing through the internet, there's an increased risk of man-in-the-middle and spoofing attacks. Allowing bidirectional access between networks without fine-grained access controls increases the risk of unauthorized access, potential data exfiltration, and compromise of network security compared to unidirectional access to specific resources.




#### Responsible Roles and Parties

* Maintainer:
  * System Developers
* Provider:
  * System Developers



#### By Components

* Virtual Networks: Developers route network traffic privately between private virtual networks.



#### References

 * [IM8 Cloud Security (IaaS and PaaS): 1.5/S7](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 Cloud Security (IaaS and PaaS): 1.5/S4](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)

### NS-5: Network and Application Layer Filtering

* **Group:** [Network Security](/catalog/ns)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Filter direct traffic from the internet to protect against network and application layer attacks.

#### Control Recommendations

Deploy the following as required:

* Web Application Firewall

* Distributed Denial of Service Protection (e.g., AWS Shield)

* Content Delivery Network (e.g., CloudFront)

#### Risk Statement

Lack of filtering for direct traffic from the internet exposes the system to the risk of network and application layer attacks, increasing the likelihood of unauthorised access, denial-of-service incidents, and compromise of sensitive data.




#### Responsible Roles and Parties

* Maintainer:
  * System Administrators
  * System Developers
* Provider:
  * System Developers



#### By Components

* Web Application Firewall: Maintainers configure a web application firewall to filter traffic from the internet.
* Distributed Denial of Service Protection: Maintainers configure Distributed Denial of Service protection to filter traffic from the internet.
* Content Delivery Network: Maintainers configure a Content Delivery Network to distribute traffic from the internet.



#### References

 * [IM8 Cloud Security (IaaS and PaaS): 1.5/S5](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 On-Premise ADS (Non-S): 1.1/S4](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/On-Premise/Topics/Application-Development-Security-(For-Non-S).aspx)

### NS-6: Valid and Trusted SSL/TLS Certificates

* **Group:** [Network Security](/catalog/ns)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Ensure that deployed SSL/TLS certificates are:
 * signed by a trusted root Certificate Authority;
 * match the domain name of the service they are issued for;
 * not expired; and
 * not revoked.


#### Control Recommendations

Configure a certificate manager that auto-renews certificates and sends alerts at least [ns-6_prm_1: 30] day(s) before expiry (e.g., AWS Certificate Manager). Otherwise, automate these functions separately.

#### Risk Statement

Using invalid SSL/TLS certificates introduces the risk of compromised encryption, man-in-the-middle attacks, and potential unauthorised access to sensitive information.




#### Responsible Roles and Parties

* Maintainer:
  * System Administrators
  * System Developers
* Provider:
  * System Developers



#### By Components

* Certificate Manager: Maintainers configure a certificate manager to manage and monitor SSL/TLS certificates.



#### References

 * [IM8 Cloud Security (IaaS and PaaS): 1.5/S8](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)

### NS-8: Secure Government Enterprise Network (GEN) connectivity

* **Group:** [Network Security](/catalog/ns)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Route network traffic between on-premises systems and GCC systems through a secure intermediary.

#### Control Recommendations

Design and build secure communications to or from on-premises systems (e.g. Government Enterprise Network (GEN)) through a Gateway rather than direct connectivity (e.g. via API gateways, Application proxies or private endpoint services).

#### Risk Statement

Routing network traffic through a secure intermediary mitigates the risk of unauthorised access and cross-network compromise in the case of bridging or direct connectivity.




#### Responsible Roles and Parties

* Maintainer:
  * System Developers
* Provider:
  * System Developers



#### By Components

* Virtual Networks: Developers route network traffic between on-premises systems and GCC systems through a secure intermediary.

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
  * System Developers
* Provider:
  * System Developers



#### By Components

* Backup Service: Maintainers configure regular backups.
* Backup Storage: Maintainers stores backups in a secure and separate location.



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
  * System Developers
* Provider:
  * System Developers



#### By Components

* Disaster Recovery Plan: Maintainers regularly test the disaster recovery plan.



#### References

 * [MVSP 4.4: Backup and Disaster recovery](https://mvsp.dev/)
 * [IM8 Cloud Security (IaaS and PaaS): 1.2/S1d](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 On-Premise IS (Non-S): 1.5/S1d](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/On-Premise/Topics/Infrastructure-Security-(For-Non-S).aspx)

### BR-3: Backup Retention

* **Group:** [Backup and Recovery](/catalog/br)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Prevent backups from being modified or deleted for [br-3_prm_1: 365] day(s) or as stipulated in the agency's data retention policies.

#### Control Recommendations

Use S3 Object Lock or immutable storage for Azure Blob Storage to enforce time-based retention policies.

#### Risk Statement

Lack of prevention measures against the modification or deletion of backups for the specified duration increases the risk of data loss, unauthorised alterations, and potential inability to recover from incidents, compromising the integrity and availability of critical information.




#### Responsible Roles and Parties

* Maintainer:
  * System Administrators
  * System Developers
* Provider:
  * System Developers



#### By Components

* Backup Storage: Maintainers configure the backup storage to prevent backups from being modified or delete for a suitable time period.



#### References

 * [MVSP 4.4: Backup and Disaster recovery](https://mvsp.dev/)
 * [IM8 Cloud Security (IaaS and PaaS): 1.2/S1b](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 On-Premise IS (Non-S): 1.5/S2c](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/On-Premise/Topics/Infrastructure-Security-(For-Non-S).aspx)

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

* System: System owners enforce data residency of the system's primary data in Singapore.



#### References

 * [MVSP 1.6: Compliance](https://mvsp.dev/)
 * [IM8 Cloud Security (IaaS and PaaS): 1.3/S3](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 On-Premise IS (Non-S): 1.1/S1a](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/On-Premise/Topics/Infrastructure-Security-(For-Non-S).aspx)

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

### DP-4: Government on Commercial Cloud (GCC)

* **Group:** [Data Protection](/catalog/dp)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Host systems classified as CONFIDENTIAL (CLOUD-ELIGIBLE), RESTRICTED, OFFICIAL-CLOSED or OFFICIAL-OPEN on Commercial Cloud hosting environments in GCC.

#### Control Recommendations

GCC allows oversight to be maintained at the Whole-of-Government level and implements several controls by default.

#### Risk Statement

Hosting higher-sensitivity systems in Government on Commercial Cloud (GCC) ensures compliance with security classifications, reducing the risk of unauthorised access and maintaining data confidentiality according to government security standards.




#### Responsible Roles and Parties

* Asset-owner:
  * System Owners



#### By Components

* System: System owners host the system on Government Commercial Cloud.



#### References

 * [MVSP 1.6: Compliance](https://mvsp.dev/)
 * [IM8 Cloud Security (IaaS and PaaS): 1.1/S4](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)

### LM-1: Separate Log Storage

* **Group:** [Logging and Monitoring](/catalog/lm)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Store logs in a repository that is part of a different system or system component than the system or component being audited.

#### Control Recommendations

Send logs to the separate storage as soon as possible after the logged event. For cloud audit logs, store them in a separate service or account (such as AWS Organisation Cloudtrail in GCC). Sending logs to the Government Cyber Security Operations Centre (GCSOC) or the central Government Commercial Cloud (GCC) log bucket can also satisfy this control.

#### Risk Statement

Storing logs in a repository separate from the audited system or component enhances security by reducing the risk of tampering, unauthorised access, and manipulation of audit trails, ensuring the integrity and reliability of log data for forensic analysis and compliance purposes.




#### Responsible Roles and Parties

* Maintainer:
  * System Developers
  * System Administrators
* Provider:
  * System Developers



#### By Components

* Cloud Audit Logging Service: Maintainers store event logs in a separate account.
* Log Storage: Maintainers store audit logs in a different system or system component than the system or component being audited.



#### References

 * [MVSP 2.7: Logging](https://mvsp.dev/)
 * [NIST SP 800-53 AU-9(2): Store on Separate Physical Systems or Components](https://doi.org/10.6028/NIST.SP.800-53r5)
 * [IM8 On-Premise IS (Non-S): 7.2/S8](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/On-Premise/Topics/Infrastructure-Security-(For-Non-S).aspx)

### LM-2: Tamper-Resistant Log Storage

* **Group:** [Logging and Monitoring](/catalog/lm)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Protect logs from unauthorised access, modification, and deletion.

#### Control Recommendations

Apply access control policies to logs based on the principle of least privilege. As far as possible, only read access should be granted. Logs sent to GCC Central Logs are tamper-resistant.

#### Risk Statement

Without protection measures, logs are susceptible to unauthorised access, modification, or deletion, leading to the risk of tampering, loss of crucial audit information, and compromised forensic analysis capabilities during security incidents.




#### Responsible Roles and Parties

* Maintainer:
  * System Developers
  * System Administrators
* Provider:
  * System Developers



#### By Components

* Log Storage: Maintainers ensure the logs are tamper-resistant.



#### References

 * [IM8 Cloud Security (IaaS and PaaS): 1.9/S4](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 Cloud Security (IaaS and PaaS): 1.9/S5](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 Cloud Security (IaaS and PaaS): 1.9/S9d](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 On-Premise IS (Non-S): 7.1/S2](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/On-Premise/Topics/Infrastructure-Security-(For-Non-S).aspx)

### LM-3: Network Flow Logging

* **Group:** [Logging and Monitoring](/catalog/lm)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Log network traffic going to and from network interfaces.

#### Control Recommendations

Enable VPC Flow Logs for AWS or its equivalents.

#### Risk Statement

Failing to log network traffic going to and from network interfaces increases the risk of overlooking suspicious activities, potential security breaches, and the inability to trace and investigate network-related incidents effectively.




#### Responsible Roles and Parties

* Maintainer:
  * System Developers
  * System Administrators
* Provider:
  * System Developers



#### By Components

* Virtual Networks: Maintainers log network traffic flows.



#### References

 * [IM8 Cloud Security (IaaS and PaaS): 1.5/S6a](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)

### LM-4: Cloud Management Event Logging

* **Group:** [Logging and Monitoring](/catalog/lm)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Log management and audit events on cloud resources.

#### Control Recommendations

Configure CloudTrail for AWS or its equivalents to log management and audit events such as changes to IAM policies and resources.

#### Risk Statement

Neglecting to log and manage audit events on cloud resources increases the risk of undetected security incidents, compromises visibility into system activities, and hinders effective forensic analysis and compliance monitoring in cloud environments.




#### Responsible Roles and Parties

* Maintainer:
  * System Developers
  * System Administrators
* Provider:
  * System Developers



#### By Components

* Cloud Audit Logging Service: Maintainers log cloud management events.



#### References

 * [MVSP 2.7: Logging](https://mvsp.dev/)
 * [IM8 Cloud Security (IaaS and PaaS): 1.9/S7](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)

### LM-5: Database Logging

* **Group:** [Logging and Monitoring](/catalog/lm)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Log database audit events.

#### Control Recommendations

Enable RDS logging for AWS or its equivalents.

#### Risk Statement

Neglecting to log database audit events raises the risk of overlooking unauthorised activities, compromises in data security, and hinders the ability to track and investigate security incidents or compliance violations within the database environment.




#### Responsible Roles and Parties

* Maintainer:
  * System Developers
  * System Administrators
* Provider:
  * System Developers



#### By Components

* Database: Maintainers log database changes.



#### References

 * [MVSP 2.7: Logging](https://mvsp.dev/)
 * [IM8 Cloud Security (IaaS and PaaS): 1.9/S3](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)

### LM-6: Access Logging

* **Group:** [Logging and Monitoring](/catalog/lm)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Log access requests sent to web application firewalls, load balancers, proxies or web servers.

#### Control Recommendations

Enable AWS WAF logging, Application Load Balancer logging, API Gateways, or their equivalents.

#### Risk Statement

Failure to log access requests sent to web application firewalls, load balancers, proxies, or web servers increases the risk of overlooking potential security threats, unauthorised access attempts, and compromises visibility into the traffic that could lead to security incidents.




#### Responsible Roles and Parties

* Maintainer:
  * System Developers
  * System Administrators
* Provider:
  * System Developers



#### By Components

* Web Application Firewall: Maintainers log web requests at the web application firewall.
* Source Code: Maintainers log web requests at the application.
* Application Load Balancer: Maintainers log web requests at the application load balancer.



#### References

 * [MVSP 2.7: Logging](https://mvsp.dev/)
 * [IM8 Cloud Security (IaaS and PaaS): 1.6/S4e](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 Cloud Security (IaaS and PaaS): 1.9/S3](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 On-Premise IS (Non-S): 7.1/S3](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/On-Premise/Topics/Infrastructure-Security-(For-Non-S).aspx)

### LM-8: Security Log Retention

* **Group:** [Logging and Monitoring](/catalog/lm)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Retain security logs for at least [lm-8_prm_1: 365] day(s).

#### Control Recommendations

Security logs include network flow logs, cloud management logs, access logs, database logs and host logs. Retain non-security logs (e.g. application, operations and performance logs) as long as needed for incident resolution and debugging. Consider log lifecycle management automation, such as Amazon S3 Lifecycle configurations.

#### Risk Statement

Failure to retain security logs increases the risk of losing crucial historical data, hindering investigations, compliance audits, and the ability to identify and respond to security incidents that occurred beyond a limited timeframe.




#### Responsible Roles and Parties

* Maintainer:
  * System Developers
  * System Administrators
* Provider:
  * System Developers



#### By Components

* Log Storage: Maintainers retain logs for the required time period.



#### References

 * [MVSP 2.7: Logging](https://mvsp.dev/)
 * [IM8 Cloud Security (IaaS and PaaS): 1.9/S3](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 Cloud Security (IaaS and PaaS): 1.9/S9](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 Cloud Security (IaaS and PaaS): 1.9/S13](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 On-Premise IS (Non-S): 7.2/S6](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/On-Premise/Topics/Infrastructure-Security-(For-Non-S).aspx)

### LM-9: Security Monitoring and Alerting

* **Group:** [Logging and Monitoring](/catalog/lm)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Configure security monitoring to identify potential security violations or breaches and send automated alerts.

#### Control Recommendations

Enable Amazon GuardDuty, Microsoft Azure Security Center, or their equivalents.

#### Risk Statement

Without configuring security monitoring to identify potential security violations or breaches and send automated alerts, there's an increased risk of delayed or unnoticed security incidents, hindering timely response and mitigation efforts to protect the system from further compromise.




#### Responsible Roles and Parties

* Maintainer:
  * System Developers
  * System Administrators
* Provider:
  * System Developers



#### By Components

* Security Monitoring Service: Maintainers configure security monitoring and alerting.



#### References

 * [IM8 Cloud Security (IaaS and PaaS): 1.9/S3](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 Cloud Security (IaaS and PaaS): 1.9/S7](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 Cloud Security (IaaS and PaaS): 1.9/S10](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 Cloud Security (IaaS and PaaS): 1.9/S11](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 Cloud Security (IaaS and PaaS): 1.9/S13](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 On-Premise IS (Non-S): 7.2/S10](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/On-Premise/Topics/Infrastructure-Security-(For-Non-S).aspx)

### LM-10: Resource Usage Monitoring and Alerting

* **Group:** [Logging and Monitoring](/catalog/lm)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Configure resource usage monitoring to identify abnormal usage and send automated alerts.

#### Control Recommendations

Configure Amazon CloudWatch alarms, Azure Monitor alerts, or their equivalents to identify abnormal usage such as spike in usage, access to resources during expected hours, and excessive charges.

#### Risk Statement

Lack of resource usage monitoring with automated alerts increases the risk of overlooking abnormal usage patterns, potential resource abuse, and compromises in system performance, hindering the ability to proactively address issues and prevent service disruptions.




#### Responsible Roles and Parties

* Maintainer:
  * System Developers
  * System Administrators
* Provider:
  * System Developers



#### By Components

* Resource Usage Monitoring Service: Maintainers configure resource usage monitoring and alerting.



#### References

 * [IM8 Cloud Security (IaaS and PaaS): 1.9/S8](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)

### LM-11: Service Level Monitoring and Alerting

* **Group:** [Logging and Monitoring](/catalog/lm)
* **Profile:** [Low-Risk - Level 2](/profiles/low-risk/level-2), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Monitor, maintain and alert on service level objectives (SLOs) and indicators (SLIs) to ensure consistent service performance, availability and reliability.

#### Control Recommendations

Implement a comprehensive monitoring system that tracks key SLIs and evaluates them against defined SLOs. This will help in identifying potential service level breaches early and take proactive measures to maintain service quality. Examples include Cloudwatch metrics and alerts, Amazon Route 53 health checks, Azure Monitor Application Insights, or their equivalents.

#### Risk Statement

Without effective service level monitoring to identify potential application or service degradation and send automated alerts, there is a risk of failing to meet service availability standards, which could result in user dissatisfaction and reduced reliability.




#### Responsible Roles and Parties

* Maintainer:
  * System Developers
  * System Administrators
* Provider:
  * System Developers



#### By Components

* Availability Monitoring Service: Maintainers configure availability monitoring and alerting.



#### References

 * [IM8 Cloud ADS: 11.1/G3](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Application-Development-Security-(For-Cloud).aspx)

### LM-14: Web defacement monitoring and response

* **Group:** [Logging and Monitoring](/catalog/lm)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Plan for and implement measures to recover against web defacements.

#### Control Recommendations

Use GCSOC’s services for centralised monitoring for web defacements attacks on internet-facing systems.

#### Risk Statement

Leverage on GCSOC services to reduce duplication of effort and reduce inconsistent implementation.




#### Responsible Roles and Parties

* Maintainer:
  * System Developers
  * System Administrators
* Provider:
  * System Developers



#### By Components

* : Maintainers configure web defacement monitoring and response.



#### References

 * [IM8 Cloud Security (IaaS and PaaS): 1.9/S13](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 On-Premise IS (Non-S): 7.1/S5](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/On-Premise/Topics/Infrastructure-Security-(For-Non-S).aspx)

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

* Identity and Access Management Service: Administrators configure the identity and access management service to enforce the principle of least privilege.



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

* Identity and Access Management Service: Administrators configure the identity and access management service to require phishing-resistant MFA for remote developer, maintainer, or administrator access.



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

* Identity and Access Management Service: Administrators disable or remove inactive developer, maintainer and administrator accounts in the identity and access management service.



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

* Identity and Access Management Service: Administrators perform regular access reviews in the identity and access management service.



#### References

 * [MVSP 4.2: Logical access](https://mvsp.dev/)
 * [IM8 Cloud Security (IaaS and PaaS): 1.4/S13](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 On-Premise ADS (Non-S): 2.3/S1, 2.3/S6](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/On-Premise/Topics/Application-Development-Security-(For-Non-S).aspx)

### AC-5: Endpoint Device Hardening

* **Group:** [Access Control](/catalog/ac)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Require hardened endpoint devices for remote developer, maintainer, or administrator access.

#### Control Recommendations

Use Endpoint Management platfoms such as Security Suite for Engineering Endpoint Devices (SEED) to continuously check and enforce device security posture and deny access if the hardening requirements are not met.

#### Risk Statement

Without requiring hardened endpoint devices for remote access, there's an increased risk of compromised endpoints, potential malware infections, and security breaches, which could lead to unauthorised access and compromise the integrity of systems with developer, maintainer, or administrator access.




#### Responsible Roles and Parties

* Asset-administrator:
  * System Administrators



#### By Components

* Endpoint Device: Administrators enforce endpoint device hardening.
* Identity and Access Management Service: Administrators configure the identity and access management service to only grant remote developer, maintainer, or administrator access from a hardened endpoint device.



#### References

 * [IM8 Cloud Security (IaaS and PaaS): 1.4/S20a](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 On-Premise IS (Non-S): 1.3/S1, 4.7/S3](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/On-Premise/Topics/Infrastructure-Security-(For-Non-S).aspx)

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

* Endpoint Device: Administrators change default credentials in any component in the system.



#### References

 * [NIST SP 800-53 IA-5: Authenticator Management](https://doi.org/10.6028/NIST.SP.800-53r5)
 * [IM8 Cloud Security (IaaS and PaaS): 1.4/S1c](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 Cloud Security (IaaS and PaaS): 1.4/S2c](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 On-Premise ADS (Non-S): 2.2/S1d, 2.3/S5](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/On-Premise/Topics/Application-Development-Security-(For-Non-S).aspx)

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

### CS-1: Unique Base Container Image Tags

* **Group:** [Container Security](/catalog/cs)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Use unique base container image tags instead of rolling tags.

#### Control Recommendations

Avoid the `latest` tag or other common rolling tags for base images to minimise unintended changes during subsequent builds using the same instruction. A digest SHA can provide a unique identifier for the image if no tag is assigned during build time.

#### Risk Statement

Using unique base container image tags instead of rolling tags reduces the risk of unintentional updates, inconsistencies, and potential security vulnerabilities in containerised environments, ensuring a more stable and secure deployment process.




#### Responsible Roles and Parties

* Maintainer:
  * System Developers
* Provider:
  * System Developers



#### By Components

* Source Code: Developers use unique base image tags in the container image build instructions.



#### References

 * [SLSA Build L1: Provenance exists](https://slsa.dev)
 * [IM8 Cloud ADS: 12.1/G3](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Application-Development-Security-(For-Cloud).aspx)

### CS-2: Minimal Base Container Images

* **Group:** [Container Security](/catalog/cs)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Build container images with minimal base images.

#### Control Recommendations

Use minimal container images such as alpine, scratch, wolfi, and distroless images as the base image to reduce attack surface.

#### Risk Statement

Building container images with minimal base images reduces the attack surface, potential vulnerabilities, and resource overhead, minimising the risk of security exploits and enhancing the overall security posture of the containerised environment.




#### Responsible Roles and Parties

* Maintainer:
  * System Developers
* Provider:
  * System Developers



#### By Components

* Source Code: Developers use minimal base images in the container image build instructions.



#### References

 * [IM8 Cloud ADS: 12.1/G1](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Application-Development-Security-(For-Cloud).aspx)

### CS-3: Runtime Container Secrets

* **Group:** [Container Security](/catalog/cs)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Provide secrets and sensitive data to the container at runtime instead of image build time.

#### Control Recommendations

Ensure no secrets (e.g., TLS certificate keys, cloud provider credentials, SSH private keys, database passwords) are embedded in the container image by using dedicated features like Docker secrets or `podman-secret-create`.

#### Risk Statement

Providing secrets and sensitive data to the container at runtime instead of image build time reduces the risk of exposing sensitive information in the image and enhances security by ensuring that secrets are managed and updated independently, minimising the risk of unauthorised access or data compromise.




#### Responsible Roles and Parties

* Maintainer:
  * System Developers
* Provider:
  * System Developers



#### By Components

* Source Code: Developers exclude secrets in the container image build instructions.



#### References

 * [IM8 Cloud ADS: 2.2/S4](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Application-Development-Security-(For-Cloud).aspx)

### CS-4: Non-Privileged Container User

* **Group:** [Container Security](/catalog/cs)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Create a non-root user and set it as the default user in the container image build instructions.

#### Control Recommendations

Ensure the non-root user has the minimal set of permissions required to run the container.

#### Risk Statement

Failure to create a non-root user and set it as the default user in container image build instructions increases the risk of security vulnerabilities, as running containers with root privileges may lead to potential exploitation and compromise of the host system.




#### Responsible Roles and Parties

* Maintainer:
  * System Developers
* Provider:
  * System Developers



#### By Components

* Source Code: Developers set a non-root user as the default user in the container image build instructions.



#### References

 * [IM8 Cloud ADS: 12.2/S2](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Application-Development-Security-(For-Cloud).aspx)

### CS-5: Dockerfile Linting

* **Group:** [Container Security](/catalog/cs)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Lint Dockerfiles before building container images.

#### Control Recommendations

Use linters such as Hadolint to check the Dockerfile (or similar build file) instructions and flag any issues that contravene best practices. Ensure Dockerfile linting stage is run as part of the Continuous Integration (CI) pipelines.

#### Risk Statement

Without linting Dockerfiles before building container images, there's an increased risk of syntax errors, misconfigurations, and potential security vulnerabilities, compromising the reliability and security of the resulting containerised applications.




#### Responsible Roles and Parties

* Maintainer:
  * System Developers
* Provider:
  * System Developers



#### By Components

* Continuous Integration/Continuous Delivery Workflow: Developers implement a container image build instructions linting job in the CI/CD workflow.



#### References

 * [IM8 Cloud ADS: 12.1/G4](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Application-Development-Security-(For-Cloud).aspx)

### CS-7: CI/CD Container Image Scanning

* **Group:** [Container Security](/catalog/cs)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Set up a container image scanning job in the CI/CD pipeline that runs on each container image build.

#### Control Recommendations

Container image scanning tools (e.g., Trivy, Grype) scan the contents of a container image or filesystem for known vulnerabilities.

#### Risk Statement

Without setting up a container image scanning job in the CI/CD pipeline, there's an increased risk of deploying vulnerable images, as potential security vulnerabilities may go undetected, compromising the security and integrity of the containerised applications during deployment.




#### Responsible Roles and Parties

* Maintainer:
  * System Developers
* Provider:
  * System Developers



#### By Components

* Continuous Integration/Continuous Delivery Workflow: Developers implement a container image scanning job in the CI/CD workflow.



#### References

 * [IM8 Cloud ADS: 12.3/G2c](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Application-Development-Security-(For-Cloud).aspx)

### CS-8: Container Registry Image Scanning

* **Group:** [Container Security](/catalog/cs)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Scan container images in container registries (e.g., Amazon ECR) for known vulnerabilities.

#### Control Recommendations

Configure container registries to scan images automatically and continuously, as well as enable scanning of image on push. Block deployment of container images with HIGH CVE being detected during scan (e.g., using Amazon ECR with Security Hub).

#### Risk Statement

Failure to scan container images in container registries for known vulnerabilities increases the risk of deploying insecure images, potentially exposing the infrastructure to known exploits and compromising the security of the containerised applications during runtime.




#### Responsible Roles and Parties

* Maintainer:
  * System Administrators
  * System Developers
* Provider:
  * System Developers



#### By Components

* Container Image Registry: Maintainers configure the container registry to scan container images.



#### References

 * [IM8 Cloud ADS: 12.3/G2b](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Application-Development-Security-(For-Cloud).aspx)
 * [IM8 Cloud ADS: 12.3/G2c](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Application-Development-Security-(For-Cloud).aspx)

### CS-9: Private Container Image Registries

* **Group:** [Container Security](/catalog/cs)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Host built container images in private container registries.

#### Control Recommendations

Use only private container registries (e.g., Amazon ECR private registry) to host container images built by the organisation as images may contain proprietary code or sensitive information.

#### Risk Statement

Hosting built container images in private registries enhances security by reducing the exposure of sensitive images, minimising the risk of unauthorised access, and maintaining control over image distribution, ensuring a more secure and controlled container deployment process.




#### Responsible Roles and Parties

* Maintainer:
  * System Developers
* Provider:
  * System Developers



#### By Components

* Container Image Registry: Developers host container images in a private container image registry.

### CS-10: Container Orchestrator API Access Control

* **Group:** [Container Security](/catalog/cs)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Disable public access to Container Orchestrator API endpoints from the internet.

#### Control Recommendations

Restrict access to the Container Orchestrator API endpoints (such as the Kubernetes API Server) to specific address ranges or use CSP provided features such as disabling Endpoint public access and Private Clusters to disable public access.

#### Risk Statement

Failure to disable public access to Container Orchestrator API endpoints from the internet increases the risk of unauthorised access, potential exploitation, and security breaches, as exposing these endpoints publicly may lead to unauthorised control and compromise of the container infrastructure.




#### Responsible Roles and Parties

* Maintainer:
  * System Administrators
  * System Developers
* Provider:
  * System Developers



#### By Components

* Kubernetes Service: Maintainers configure the Kubernetes service to disable public access to the API.



#### References

 * [IM8 Cloud Security (IaaS and PaaS): 1.7/S21b](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)

### CS-11: Container Workload Segmentation

* **Group:** [Container Security](/catalog/cs)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Segregate container workloads to help contain attacks through isolation.

#### Control Recommendations

Create Kubernetes namespaces or similar container segmentation controls to isolate different workloads, services or projects.

#### Risk Statement

Without separating container workloads into namespaces, there's an increased risk of lateral movement and potential compromise, as attacks on one workload could impact others; utilising namespaces helps contain and isolate potential security incidents, enhancing overall cluster security.




#### Responsible Roles and Parties

* Maintainer:
  * System Developers
* Provider:
  * System Developers



#### By Components

* Kubernetes Service: Developers set namespaces for workloads in the Kubernetes service.

### PM-1: Cybersecurity Incident Management Plan

* **Group:** [Security Programme Management](/catalog/pm)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Develop, document, and disseminate an agency-level cybersecurity incident management plan to respond to cybersecurity incidents.

#### Control Recommendations

Refer to the Government Incident Reporting and Operations Centre (GIROC) [ICT and Data Incident Reporting Resources](https://gccprod.sharepoint.com/sites/GOVTECH-digitalgov/GIROC/SitePages/Useful-Resources.aspx) for an incident management plan and best practices template.

#### Risk Statement

Lack of a cybersecurity incident management plan increases the risk of ineffective response to cybersecurity incidents, hindering the ability to contain, mitigate, and recover from security breaches, potentially leading to extended downtime and data compromise.




#### Responsible Roles and Parties

* Asset-owner:
  * Agency



#### By Components

* Cybersecurity Incident Management Plan: The agency develops, documents, and disseminates a cybersecurity incident management plan.



#### References

 * [MVSP 1.7: Incident handling](https://mvsp.dev/)
 * [IM8 Cloud Security (IaaS and PaaS): 1.1/S3](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)

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

* System Security Plan: The agency develops, documents, and disseminates a system security plan.

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

### IS-1: Management Agents

* **Group:** [Infrastructure Security](/catalog/is)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Install CSP management agents on hosts to remotely and securely manage their configurations.

#### Control Recommendations

Most CSP compute instances preinstall management agents (e.g., AWS Systems Manager Agent, Azure Windows VM Agent) by default. If the image does not come with the preinstalled agent, install manually.

#### Risk Statement

Without installing management agents on hosts, there is an increased risk of manual misconfigurations, difficulty in maintaining consistent configurations, and potential security vulnerabilities due to reduced visibility and ability to manage hosts effectively.




#### Responsible Roles and Parties

* Maintainer:
  * System Administrators
  * System Developers
* Provider:
  * System Developers



#### By Components

* Compute Management Service: Maintainers install management agents on compute instances through the compute management service.



#### References

 * [IM8 Cloud Security (IaaS and PaaS): 1.1/G1](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 Cloud Security (IaaS and PaaS): 1.4/S21](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)

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

### IS-3: Restricted Administrator Privileges

* **Group:** [Infrastructure Security](/catalog/is)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Restrict administrator privileges by disabling remote login for the root/administrator user and removing sudo/administrators group access for other users.

#### Control Recommendations

Further reduce the attack surface by running common services such as the web server or database without root/administrator/system privileges.

#### Risk Statement

Without restricting administrator privileges, there is an increased risk of unauthorised access, privilege escalation, and potential security breaches, compromising the integrity and security of the system.




#### Responsible Roles and Parties

* Maintainer:
  * System Administrators
  * System Developers
* Provider:
  * System Developers



#### By Components

* Hosted Virtual Machine: Maintainers restrict administrator privileges in hosted virtual machines.



#### References

 * [IM8 Cloud Security (IaaS and PaaS): 1.6/S1d](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 Cloud Security (IaaS and PaaS): 1.6/S1e](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 On-Premise IS (Non-S): 1.2/S2a](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/On-Premise/Topics/Infrastructure-Security-(For-Non-S).aspx)

### IS-4: Least Functionality

* **Group:** [Infrastructure Security](/catalog/is)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Disable or remove unnecessary functions, system ports, protocols, software, and services on the host.

#### Control Recommendations

Follow the principle of least functionality to configure the host to carry out only its intended purpose. CSP node management services can provide an inventory of software and services (e.g., AWS Systems Manager Inventory). Vulnerability assessment scanners (e.g., AWS Inspector) can also identify software vulnerabilities and network exposure.

#### Risk Statement

Failure to disable or remove unnecessary functions, system ports, protocols, software, and services on the host increases the attack surface, potential vulnerabilities, and the risk of exploitation, compromising the overall security and performance of the system.




#### Responsible Roles and Parties

* Maintainer:
  * System Administrators
  * System Developers
* Provider:
  * System Developers



#### By Components

* Hosted Virtual Machine: Maintainers disable or remove unnecessary functions in hosted virtual machines.



#### References

 * [NIST SP 800-53 CM-7: Least Functionality](https://doi.org/10.6028/NIST.SP.800-53r5)
 * [IM8 Cloud Security (IaaS and PaaS): 1.4/S7](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 Cloud Security (IaaS and PaaS): 1.5/S4e](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 Cloud Security (IaaS and PaaS): 1.7/S1b](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 On-Premise IS (Non-S): 1.2/S2c](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/On-Premise/Topics/Infrastructure-Security-(For-Non-S).aspx)

### IS-5: Host System Hardening

* **Group:** [Infrastructure Security](/catalog/is)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Harden the host configuration in accordance with industry standards.

#### Control Recommendations

Select the appropriate benchmark for the host such as from the [NIST National Checklist Program](https://ncp.nist.gov/repository) or [CIS Benchmarks](https://www.cisecurity.org/cis-benchmarks). Automate the configuration process or use hardened images instead of manually configuring.

#### Risk Statement

Without hardening the operating system configuration according to industry standards, there's an increased risk of security vulnerabilities, unauthorised access, and potential exploitation, compromising the overall security posture and resilience of the operating system.




#### Responsible Roles and Parties

* Maintainer:
  * System Administrators
  * System Developers
* Provider:
  * System Developers



#### By Components

* Hosted Virtual Machine: Maintainers harden the operating systems of hosted virtual machines.



#### References

 * [IM8 Cloud Security (IaaS and PaaS): 1.6/G2](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 Cloud Security (IaaS and PaaS): 1.6/S2](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 On-Premise IS (Non-S): 1.2/S1](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/On-Premise/Topics/Infrastructure-Security-(For-Non-S).aspx)

### IS-6: Remote Administration

* **Group:** [Infrastructure Security](/catalog/is)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Use remote administration tools instead of direct SSH or RDP.

#### Control Recommendations

In production environments, use remote administration (e.g., AWS Systems Manager Session Manager, AWS Systems Manager Fleet Manager, GCC Privileged Identity Management) only for break glass scenarios where remote monitoring and automation is not available. Document and remediate gaps in monitoring and automation to minimise the need for remote administration. If SSH is still required and remote administration tools are not available, only use it within a private non-production environment such as an encrypted tunnel and authenticate with short-lived certificates.

#### Risk Statement

Using remote administration tools enhances security by providing controlled and audited access, reducing the risk of unauthorised activities, and improving overall management of privileged identities.




#### Responsible Roles and Parties

* Maintainer:
  * System Administrators
  * System Developers
* Provider:
  * System Developers



#### By Components

* Compute Management Service: Maintainers use remote administration tools provided by the compute management service.



#### References

 * [AWS SSB WKLD.06: Use Systems Manager instead of SSH or RDP](https://docs.aws.amazon.com/prescriptive-guidance/latest/aws-startup-security-baseline/)
 * [IM8 Cloud Security (IaaS and PaaS): 1.4/S21](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)

### IS-8: Endpoint Detection and Response (EDR)

* **Group:** [Infrastructure Security](/catalog/is)
* **Profile:** [Low-Risk - Level 2](/profiles/low-risk/level-2), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Monitor security threats on hosts with an EDR tool.

#### Control Recommendations

Implement EDR tools for all compute hosts. Security incident response should be planned and documented for the tool. EDR tools with built-in malware protection should be favoured to reduce additional agents.

#### Risk Statement

Failure to monitor security threats on hosts with an Endpoint Detection and Response (EDR) tool increases the risk of undetected advanced threats, compromises in host security, and delayed response to potential security incidents, highlighting the need for continuous monitoring and proactive threat detection.




#### Responsible Roles and Parties

* Maintainer:
  * System Administrators
  * System Developers
* Provider:
  * System Developers



#### By Components

* Hosted Virtual Machine: Maintainers implement Endpoint Detection and Response (EDR) tools on hosted virtual machines.



#### References

 * [IM8 Cloud Security (IaaS and PaaS): 1.6/G1a](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)

### IS-9: End-of-Support (EOS) Assets

* **Group:** [Infrastructure Security](/catalog/is)
* **Profile:** [Low-Risk - Level 1](/profiles/low-risk/level-1), [Sandbox - Level 2](/profiles/sandbox/level-2)

#### Control Statement

Ensure deployed [is-9_prm_1: software] assets have not reached end-of-support (EOS). Use of EOS assets will require risk acceptance by approved authority.

#### Control Recommendations

Identify, track and replace EOS assets in a timely manner. Regularly review assets to identify upcoming EOS timeframe and replace them ahead of EOS date.

#### Risk Statement

EOS assets can introduce security vulnerabilities as the assets are no longer provided with security fixes.




#### Responsible Roles and Parties

* Maintainer:
  * System Administrators
  * System Developers
* Provider:
  * System Developers



#### By Components

* Software Asset: Maintainers ensure end-of-support software assets are removed or replaced.



#### References

 * [IM8 On-Premise ADS (Non-S): 5.1/S8](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/On-Premise/Topics/Application-Development-Security-(For-Non-S).aspx)




