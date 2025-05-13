---
title: Secure Development
permalink: /control-catalog/sd/
variant: markdown
description: ""
third_nav_title: Cybersecurity
---
Controls to secure the development pipeline and perform source code quality assurance.

| Controls                                                                                             |
| ---------------------------------------------------------------------------------------------------- |
| [SD-1: Push Protection for Secrets](#sd-1-push-protection-for-secrets)                               |
| [SD-2: Default Branch Push Permissions](#sd-2-default-branch-push-permissions)                       |
| [SD-3: Continuous Integration (CI) Tests](#sd-3-continuous-integration-ci-tests)                     |
| [SD-4: Static Analysis](#sd-4-static-analysis)                                                       |
| [SD-5: Dependency Scanning](#sd-5-dependency-scanning)                                               |
| [SD-6: Secret Detection](#sd-6-secret-detection)                                                     |
| [SD-7: CI Environment Variable Secrets Management](#sd-7-ci-environment-variable-secrets-management) |
| [SD-8: Deployment Environment Segregation](#sd-8-deployment-environment-segregation)                 |

## SD-1: Push Protection for Secrets

**Group:** Secure Development

### Control Statement

Configure the code repository to prevent secrets from being pushed to the repository.

### Control Recommendations

Use GitLab's push rules or GitHub's push protection to reject secrets on push.

### Risk Statement

Failure to configure the code repository to prevent secrets from being pushed introduces the risk of inadvertent exposure, unauthorised access, and potential misuse of sensitive information, compromising the security of the codebase and associated systems.

### References

- [IM8 Cloud ADS: 6.4/G1]()

## SD-2: Default Branch Push Permissions

**Group:** Secure Development

### Control Statement

Configure the code repository to prevent pushes (including force pushes) to the default branch.

### Control Recommendations

Use GitLab's protected branch and merge request settings or GitHub's branch protection settings to enforce this.

### Risk Statement

Without configuring the code repository to prevent pushes, including force pushes, to the default branch, there's an increased risk of unintentional or malicious changes, potential loss of code history, and compromised version control, impacting the integrity and reliability of the software development process.

## SD-3: Continuous Integration (CI) Tests

**Group:** Secure Development

### Control Statement

Require Continuous Integration (CI) tests to pass before merging into the default branch.

### Control Recommendations

Use GitLab's protected branch and merge request settings or GitHub's branch protection settings to enforce this.

### Risk Statement

Failing to require passing Continuous Integration (CI) tests before merging into the default branch increases the risk of introducing faulty code, potential regressions, and compromise of code quality.

## SD-4: Static Analysis

**Group:** Secure Development

### Control Statement

Set up a static analysis job in the [ insert: param, sd-4_prm_1 ], and remediate or risk accept true positive vulnerability findings before deploying to production.

### Control Recommendations

Static analysis tools (such as SAST or IaC security scanners) check source code for common vulnerabilities and misconfigurations. By running static analysis tools earlier in the DevSecOps cycle, vulnerabilities can be detected and prevented from being deployed to production.

### Risk Statement

Without setting up static analysis in the CI/CD pipeline for each merge request and addressing true positive vulnerability findings, there is an increased risk of deploying insecure code to the production branch, potentially leading to security breaches and compromise of the overall system.

### Parameters

| ID         | Type           | Description                                |
| ---------- | -------------- | ------------------------------------------ |
| sd-4_prm_1 | location (str) | The location where static analysis occurs. |

### References

- [IM8 Cloud ADS: 6.4/S2]()
- [IM8 On-Premise ADS (Non-S): 4.1/S1]()

## SD-5: Dependency Scanning

**Group:** Secure Development

### Control Statement

Schedule a scan at least every [ insert: param, sd-5_prm_1 ] day(s) in the [ insert: param, sd-5_prm_2 ] to identify the use of vulnerable software libraries.

### Control Recommendations

Dependency scanning checks the source code for dependencies with known vulnerabilities. By running scans regularly using bots or software composition analysis (SCA) tools, vulnerabilities arising from outdated dependencies can be quickly detected and patched. Software composition analysis can be performed using tools such as Gitlab, Nexus IQ, or their equivalent, with output in a common SBOM format such as SPDX or CycloneDX.

### Risk Statement

Failing to schedule regular dependency scanning to identify vulnerable software libraries and address findings in a timely manner increases the risk of deploying applications with known vulnerabilities, potentially exposing the system to security exploits and compromise.

### Parameters

| ID         | Type                     | Description                                               |
| ---------- | ------------------------ | --------------------------------------------------------- |
| sd-5_prm_1 | time period (days) (int) | The time period in days of dependency scanning frequency. |
| sd-5_prm_2 | location (str)           | The location where dependency scanning occurs.            |

### References

- [MVSP 2.6: Dependency Patching](https://mvsp.dev/)
- [IM8 Cloud Security (IaaS and PaaS): 1.7/S8i](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
- [IM8 Cloud ADS: 8.1/S2]()
- [IM8 Cloud ADS: 6.1/S1c]()
- [IM8 On-Premise ADS (Non-S): 1.1/S1i]()

## SD-6: Secret Detection

**Group:** Secure Development

### Control Statement

Set up secret detection in the [ insert: param, sd-6_prm_1 ] and remediate true positives within [ insert: param, sd-6_prm_2 ] day(s).

### Control Recommendations

Ensure that the exposed secret is revoked and purged from the Git history.

### Risk Statement

Without setting up secret detection and addressing true positive findings promptly, there's an increased risk of exposing sensitive information, potential unauthorised access, and compromised security.

### Parameters

| ID         | Type                     | Description                                                                |
| ---------- | ------------------------ | -------------------------------------------------------------------------- |
| sd-6_prm_1 | location (str)           | The location where secret detection occurs.                                |
| sd-6_prm_2 | time period (days) (int) | Number of days within which to remediate a secret detection true positive. |

### References

- [IM8 Cloud Security (IaaS and PaaS): 1.7/S8f](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
- [IM8 Cloud ADS: 1.1/S1f]()
- [IM8 Cloud ADS: 6.4/G1b]()
- [IM8 On-Premise ADS (Non-S): 6.4/G1]()

## SD-7: CI Environment Variable Secrets Management

**Group:** Secure Development

### Control Statement

Protect environment variable secrets used in CI jobs by limiting them to protected pipelines and masking them in job logs.

### Control Recommendations

Use GitLab's CI/CD variable security settings or GitHub's encrypted secrets with the add-mask workflow command.

### Risk Statement

Failing to protect environment variable secrets in CI jobs by limiting them to protected pipelines and masking them in job logs increases the risk of unauthorized access and exposure of sensitive information.

## SD-8: Deployment Environment Segregation

**Group:** Secure Development

### Control Statement

Segregate production and non-production environments including applications, services, data, secrets, roles, and networks.

### Control Recommendations

Achieve segregation using separate Government on Commercial Cloud (GCC) accounts for environments such as production, development, test, and staging. Account segregation enhances security by limiting exposure, simplifies resource and cost management, maintains configuration integrity, facilitates compliance and auditing and streamlines operational tasks. Deploy and operate environments as similarly as possible to enhance debugging and time-to-market.

### Risk Statement

Failure to segregate production and non-production environments increases the risk of unauthorized access, data leaks, and denial of service attacks, as compromises in non-production environments may lead to cascading impacts on production systems.

### References

- [MVSP 4.2: Logical access](https://mvsp.dev/)
- [IM8 Cloud Security (IaaS and PaaS): 1.4/S9](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)