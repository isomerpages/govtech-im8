---
title: Security Testing
permalink: /control-catalog/st/
variant: markdown
description: ""
third_nav_title: Cybersecurity
---
Controls to validate the security of a system via internal and external testing.

| Controls |
| ---- |
| [ST-1: Vulnerability Assessment](#st-1) |
| [ST-2: Cloud Security Posture Management](#st-2) |
| [ST-3: Vulnerability Disclosure Programme](#st-3) |
| [ST-4: Security Testing Program](#st-4) |
| [ST-5: Vulnerability Management](#st-5) |


<a id="st-1"></a>
## ST-1: Vulnerability Assessment

### Control Statement

Run regular [st-1_prm_1] vulnerability assessment scans for eligible hosts.

### Control Recommendations

Select agent-based or network-based scans as necessary. Implement authenticated scans where possible for greater coverage. Use scanners such as Amazon Inspector or Microsoft Defender for Cloud for continuous scanning of cloud systems. For on-premises systems or systems that require periodic scans, subscribe to Vulnerability Management System (VMS).

### Risk Statement

Without regular vulnerability assessment scans, hosts remain exposed to undetected security vulnerabilities or misconfigurations, increasing the risk of exploitation and unauthorised access to critical systems.



#### Parameters

| ID | Type | Description |
| -- | ---- | ----------- |
| st-1_prm_1 | type | The type of vulnerability assessment scanning. |

<a id="st-2"></a>
## ST-2: Cloud Security Posture Management

### Control Statement

Set up cloud security posture management that performs continuous configuration scans on cloud assets.

### Control Recommendations

Use cloud security posture management tools such as CloudSCAPE, AWS Security Hub, and Datadog Cloud Security Posture Management.

### Risk Statement

Lack of continuous configuration scans through cloud security posture management increases the risk of misconfigurations in cloud assets, leading to security vulnerabilities, data breaches, and unauthorised access.



<a id="st-3"></a>
## ST-3: Vulnerability Disclosure Programme

### Control Statement

Display a way to responsibly disclose vulnerabilities via the Government Vulnerability Disclosure Programme.

### Control Recommendations

Add a link to https://go.gov.sg/report-vulnerability on all pages, such as in the footer.

### Risk Statement

Publicly disclosing vulnerabilities without following a responsible disclosure process increases the risk of malicious exploitation; responsible disclosure via the Government Vulnerability Disclosure Programme ensures a coordinated and secure approach to addressing vulnerabilities.



<a id="st-4"></a>
## ST-4: Security Testing Program

### Control Statement

Conduct and document a [st-4_prm_1] by internal teams or independent external parties every [st-4_prm_2] day(s).

### Control Recommendations

Refer to the [WOG Security Testing Guidelines](https://docs.developer.tech.gov.sg/docs/security-testing-guidelines/) for recommendations on the conduct of security testing engagements. For systems that are permitted to use Government Bug Bounty Program as an alternative, obtain a passing rating based on the Agency Readiness Scorecard. For SaaS, refer to past penetration testing reports done by the SaaS provider, if any.

### Risk Statement

Without undergoing security testing, there's an increased risk of undetected security weaknesses, leaving the application susceptible to exploitation, data breaches, and unauthorised access.



#### Parameters

| ID | Type | Description |
| -- | ---- | ----------- |
| st-4_prm_1 | type of security testing program | The type of security testing program. |
| st-4_prm_2 | time period (days) | The time period in days of penetration testing frequency. |

<a id="st-5"></a>
## ST-5: Vulnerability Management

### Control Statement

Triage, prioritise and then remediate or risk accept vulnerabilities that materially impact security within the following timeframe based on severity:
 * Critical: [st-5_prm_1] day(s)
 * High: [st-5_prm_2] day(s)
 * Medium: [st-5_prm_3] day(s)
 * Low: [st-5_prm_4] day(s)


### Control Recommendations

Vulnerabilities that materially impact security include vulnerabilities that have a high likelihood of exploitability, or are known to be exploited. Refer to resources such as the [Known Exploited Vulnerabilities Catalog](https://www.cisa.gov/known-exploited-vulnerabilities-catalog) to prioritise vulnerabilities that should be remediated. Seek approval from the appropriate approving authority for risk acceptance.

### Risk Statement

Failure to promptly remediate vulnerabilities increases the risk of potential exploits, security breaches, and prolonged exposure to known vulnerabilities in the system.



#### Parameters

| ID | Type | Description |
| -- | ---- | ----------- |
| st-5_prm_1 | time period (days) | The time period in days to remediate or risk accept critical vulnerability findings. |
| st-5_prm_2 | time period (days) | The time period in days to remediate or risk accept high vulnerability findings. |
| st-5_prm_3 | time period (days) | The time period in days to remediate or risk accept medium vulnerability findings. |
| st-5_prm_4 | time period (days) | The time period in days to remediate or risk accept low vulnerability findings. |