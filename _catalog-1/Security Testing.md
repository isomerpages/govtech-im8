---
title: Security Testing
permalink: /security-testing/
variant: markdown
description: ""
---
Controls to validate the security of a system via internal and external testing.

| Controls |
| ---- |
| [ST-1: Vulnerability Assessment](#st-1) |
| [ST-2: Cloud Security Posture Management](#st-2) |
| [ST-3: Vulnerability Disclosure Programme](#st-3) |
| [ST-4: Penetration Testing](#st-4) |
| [ST-5: Vulnerability Management](#st-5) |


<a id="st-1"></a>
## ST-1: Vulnerability Assessment

### Control Statement

Run [st-1_prm_1] vulnerability assessment scans for eligible hosts.

### Control Recommendations

Select agent-based or network-based scans as necessary. Use scanners such as Amazon Inspector that support continuous scanning. Use authenticated scans for greater coverage.

### Risk Statement

Without regular vulnerability assessment scans, hosts remain exposed to undetected security vulnerabilities, increasing the risk of exploitation and unauthorised access to critical systems.



#### Parameters

| ID | Type | Description |
| -- | ---- | ----------- |
| st-1_prm_1 | type | The time period of vulnerability assessment scanning. |

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
## ST-4: Penetration Testing

### Control Statement

Conduct and document a penetration test by internal teams or independent external parties every [st-4_prm_1] day(s).

### Control Recommendations

A white-box penetration test should be performed to effectively test the application.

### Risk Statement

Without conducting and documenting penetration tests, there's an increased risk of undetected security weaknesses, leaving the application susceptible to exploitation, data breaches, and unauthorised access.



#### Parameters

| ID | Type | Description |
| -- | ---- | ----------- |
| st-4_prm_1 | time period (days) | The time period in days of penetration testing frequency. |

<a id="st-5"></a>
## ST-5: Vulnerability Management

### Control Statement

Triage and then remediate or risk accept all true positive vulnerability findings discovered through security testing within the following timeframe based on severity:
 * Critical: [st-5_prm_1] day(s)
 * High: [st-5_prm_2] day(s)
 * Medium: [st-5_prm_3] day(s)
 * Low: [st-5_prm_4] day(s)


### Control Recommendations

Seek approval from the appropriate approving authority for risk acceptance.

### Risk Statement

Failure to promptly remediate vulnerabilities increases the risk of potential exploits, security breaches, and prolonged exposure to known vulnerabilities in the system.



#### Parameters

| ID | Type | Description |
| -- | ---- | ----------- |
| st-5_prm_1 | time period (days) | The time period in days to remediate or risk accept critical vulnerability findings. |
| st-5_prm_2 | time period (days) | The time period in days to remediate or risk accept high vulnerability findings. |
| st-5_prm_3 | time period (days) | The time period in days to remediate or risk accept medium vulnerability findings. |
| st-5_prm_4 | time period (days) | The time period in days to remediate or risk accept low vulnerability findings. |


