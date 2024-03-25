---
title: Secure Development
permalink: /catalog/sd/
variant: markdown
description: ""
---
Controls to secure the development pipeline and perform source code quality assurance.

| Controls |
| ---- |
| [SD-1: Push Protection for Secrets](#sd-1) |
| [SD-2: Default Branch Push Permissions](#sd-2) |
| [SD-3: Continuous Integration (CI) Tests](#sd-3) |
| [SD-4: Static Analysis](#sd-4) |
| [SD-5: Dependency Scanning](#sd-5) |
| [SD-6: Secret Detection Scanning](#sd-6) |
| [SD-7: CI Environment Variable Secrets Management](#sd-7) |
| [SD-8: Deployment Environment Segregation](#sd-8) |


<a id="sd-1"></a>
## SD-1: Push Protection for Secrets

### Control Statement

Configure the code repository to prevent secrets from being pushed to the repository.

### Control Recommendations

Use GitLab's push rules or GitHub's push protection to reject secrets on push.

### Risk Statement

Failure to configure the code repository to prevent secrets from being pushed introduces the risk of inadvertent exposure, unauthorised access, and potential misuse of sensitive information, compromising the security of the codebase and associated systems.



<a id="sd-2"></a>
## SD-2: Default Branch Push Permissions

### Control Statement

Configure the code repository to prevent pushes (including force pushes) to the default branch.

### Control Recommendations

Use GitLab's protected branch and merge request settings or GitHub's branch protection settings to enforce this.

### Risk Statement

Without configuring the code repository to prevent pushes, including force pushes, to the default branch, there's an increased risk of unintentional or malicious changes, potential loss of code history, and compromised version control, impacting the integrity and reliability of the software development process.



<a id="sd-3"></a>
## SD-3: Continuous Integration (CI) Tests

### Control Statement

Require Continuous Integration (CI) tests to pass before merging into the default branch.

### Control Recommendations

Use GitLab's protected branch and merge request settings or GitHub's branch protection settings to enforce this.

### Risk Statement

Failing to require passing Continuous Integration (CI) tests before merging into the default branch increases the risk of introducing faulty code, potential regressions, and compromise of code quality.



<a id="sd-4"></a>
## SD-4: Static Analysis

### Control Statement

Set up a static analysis job in the development CI/CD pipeline that runs on each merge request, and remediate or risk accept true positive vulnerability findings before merging into the production branch.

### Control Recommendations

Static analysis tools (such as SAST or IaC security scanners) check source code for common vulnerabilities and misconfigurations. By running static analysis tools earlier in the DevSecOps cycle, vulnerabilities can be detected and prevented from being deployed to production.

### Risk Statement

Without setting up static analysis in the CI/CD pipeline for each merge request and addressing true positive vulnerability findings, there is an increased risk of deploying insecure code to the production branch, potentially leading to security breaches and compromise of the overall system.



<a id="sd-5"></a>
## SD-5: Dependency Scanning

### Control Statement

Schedule a scan at least every [sd-5_prm_1] day(s) in the CI/CD pipeline and/or repository to identify the use of vulnerable software libraries.

### Control Recommendations

Dependency scanning checks the source code for dependencies with known vulnerabilities. By running scans regularly using bots or software composition analysis (SCA) tools, vulnerabilities arising from outdated dependencies can be quickly detected and patched. Triage and prioritise vulnerabilities against Common Vulnerability Scoring System (CVSS), Known Exploited Vulnerabilities (KEV) Catalog, Vulnerability Exploitability eXchange (VEX) and other sources.

### Risk Statement

Failing to schedule regular scans in the CI/CD pipeline to identify vulnerable software libraries and address findings in a timely manner increases the risk of deploying applications with known vulnerabilities, potentially exposing the system to security exploits and compromise.



#### Parameters

| ID | Type | Description |
| -- | ---- | ----------- |
| sd-5_prm_1 | time period (days) | The time period in days of dependency scanning frequency. |

<a id="sd-6"></a>
## SD-6: Secret Detection Scanning

### Control Statement

Set up a secret detection alert or job in the development CI/CD pipeline that runs on each commit and remediate true positives within [sd-6_prm_1] day(s).

### Control Recommendations

Ensure that the exposed secret is revoked and purged from the Git history.

### Risk Statement

Without setting up secret detection alerts or jobs in the development CI/CD pipeline and addressing true positive findings promptly, there's an increased risk of exposing sensitive information, potential unauthorized access, and compromised security.



#### Parameters

| ID | Type | Description |
| -- | ---- | ----------- |
| sd-6_prm_1 | time period (days) | Number of days within which to remediate a secret detection true positive. |

<a id="sd-7"></a>
## SD-7: CI Environment Variable Secrets Management

### Control Statement

Protect environment variable secrets used in CI jobs by limiting them to protected pipelines and masking them in job logs.

### Control Recommendations

Use GitLab's CI/CD variable security settings or GitHub's encrypted secrets with the add-mask workflow command.

### Risk Statement

Failing to protect environment variable secrets in CI jobs by limiting them to protected pipelines and masking them in job logs increases the risk of unauthorized access and exposure of sensitive information.



<a id="sd-8"></a>
## SD-8: Deployment Environment Segregation

### Control Statement

Segregate production and non-production environments including applications, services, data, secrets, roles, and networks.

### Control Recommendations

Achieve segregation using separate Government on Commercial Cloud (GCC) accounts for environments such as production, development, test, and staging. Account segregation enhances security by limiting exposure, simplifies resource and cost management, maintains configuration integrity, facilitates compliance and auditing and streamlines operational tasks. Deploy and operate environments as similarly as possible to enhance debugging and time-to-market.

### Risk Statement

Failure to segregate production and non-production environments increases the risk of unauthorized access, data leaks, and denial of service attacks, as compromises in non-production environments may lead to cascading impacts on production systems.




