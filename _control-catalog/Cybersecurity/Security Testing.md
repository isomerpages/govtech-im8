---
title: Security Testing
permalink: /control-catalog/st/
variant: markdown
description: ""
third_nav_title: Cybersecurity
---

Controls to validate the security of a system via internal and external testing.

| Controls                                                                                           |
| -------------------------------------------------------------------------------------------------- |
| [ST-1: Vulnerability Assessment](#st-1-vulnerability-assessment)                                   |
| [ST-2: Cloud Security Posture Management](#st-2-cloud-security-posture-management)                 |
| [ST-3: Public Vulnerability Disclosure Programme](#st-3-public-vulnerability-disclosure-programme) |
| [ST-4: Security Testing Programme](#st-4-security-testing-programme)                               |
| [ST-5: Vulnerability Management](#st-5-vulnerability-management)                                   |

## ST-1: Vulnerability Assessment

**Group:** Security Testing

### Control Statement

Run regular [ insert: param, st-1_prm_1 ] vulnerability assessment scans for eligible hosts at least every [ insert: param, st-1_prm_2 ] day(s).

### Control Recommendations

Select agent-based or network-based scans as necessary. Implement authenticated scans where possible for greater coverage. Use scanners such as Amazon Inspector or Microsoft Defender for Cloud for continuous scanning of cloud systems. For on-premises systems or systems that require periodic scans, subscribe to Vulnerability Management System (VMS). For SaaS, refer to past vulnerability scanning reports done by the SaaS provider, if any.

### Risk Statement

Without regular vulnerability assessment scans, hosts remain exposed to undetected security vulnerabilities or misconfigurations, increasing the risk of exploitation and unauthorised access to critical systems.

### Parameters

| ID         | Type                     | Description                                                 |
| ---------- | ------------------------ | ----------------------------------------------------------- |
| st-1_prm_1 | type (str)               | The type of vulnerability assessment scanning.              |
| st-1_prm_2 | time period (days) (int) | The time period in days for vulnerability assessment scans. |

### References

- [IM8 Cloud Security (IaaS and PaaS): 1.8/S1](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)

## ST-2: Cloud Security Posture Management

**Group:** Security Testing

### Control Statement

Set up cloud security posture management that performs continuous configuration scans on cloud assets.

### Control Recommendations

Use cloud security posture management tools such as CloudSCAPE, AWS Security Hub, and Datadog Cloud Security Posture Management.

### Risk Statement

Lack of continuous configuration scans through cloud security posture management increases the risk of misconfigurations in cloud assets, leading to security vulnerabilities, data breaches, and unauthorised access.

### References

- [IM8 Cloud Security (IaaS and PaaS): 1.1/S6](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)

## ST-3: Public Vulnerability Disclosure Programme

**Group:** Security Testing

### Control Statement

Establish a public reporting channel for disclosing vulnerabilities in public-facing systems via [ insert: param, st-3_prm_1 ].

### Control Recommendations

Use the [security.txt standard](https://securitytxt.org) or add a link to the vulnerability reporting channel on all pages, such as in the footer.

### Risk Statement

Lack of a reporting channel for vulnerabilities increases the risk of undetected and unmitigated vulnerabilities.

### Parameters

| ID         | Type       | Description                                         |
| ---------- | ---------- | --------------------------------------------------- |
| st-3_prm_1 | type (str) | The type of public vulnerability reporting channel. |

### References

- [MVSP 1.1: Vulnerability reports](https://mvsp.dev/)
- [IM8 On-Premise ADS (Non-S): 5.1/S4]()
- [NIST SP 800-53 RA-5(11): Public Disclosure Program](https://doi.org/10.6028/NIST.SP.800-53r5)
- [Cloud Controls Matrix TVM-09: Vulnerability Management Reporting](https://cloudsecurityalliance.org/artifacts/cloud-controls-matrix-v4)

## ST-4: Security Testing Programme

**Group:** Security Testing

### Control Statement

Conduct and document a [ insert: param, st-4_prm_1 ] by internal teams or independent external parties every [ insert: param, st-4_prm_2 ] day(s).

### Control Recommendations

Refer to the [WOG Security Testing Guidelines](https://docs.developer.tech.gov.sg/docs/security-testing-guidelines/) for recommendations on the conduct of security testing engagements. For systems that are permitted to use Government Bug Bounty Programmeme as an alternative, obtain a passing rating based on the Agency Readiness Scorecard. For SaaS, refer to past penetration testing reports done by the SaaS provider, if any.

### Risk Statement

Without undergoing security testing, there's an increased risk of undetected security weaknesses, leaving the application susceptible to exploitation, data breaches, and unauthorised access.

### Parameters

| ID         | Type                     | Description                                               |
| ---------- | ------------------------ | --------------------------------------------------------- |
| st-4_prm_1 | type (str)               | The type of security testing programme.                   |
| st-4_prm_2 | time period (days) (int) | The time period in days of penetration testing frequency. |

### References

- [MVSP 1.4: External testing](https://mvsp.dev/)
- [IM8 Cloud Security (IaaS and PaaS): 1.8/S1](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
- [IM8 On-Premise ADS (Non-S): 4.1/S1]()
- [WOG Security Testing Guidelines](https://docs.developer.tech.gov.sg/docs/security-testing-guidelines/)

## ST-5: Vulnerability Management

**Group:** Security Testing

### Control Statement

Triage, prioritise and then remediate or risk accept vulnerabilities that materially impact security within the following timeframe based on severity:

- Critical: [ insert: param, st-5_prm_1 ] day(s)
- High: [ insert: param, st-5_prm_2 ] day(s)
- Medium: [ insert: param, st-5_prm_3 ] day(s)
- Low: [ insert: param, st-5_prm_4 ] day(s)

### Control Recommendations

Vulnerabilities that materially impact security include vulnerabilities that have a high likelihood of exploitability, or are known to be exploited. Refer to resources such as the [Known Exploited Vulnerabilities Catalog](https://www.cisa.gov/known-exploited-vulnerabilities-catalog) to prioritise vulnerabilities that should be remediated. Seek approval from the appropriate approving authority for risk acceptance. Document the actions taken.

### Risk Statement

Failure to promptly remediate vulnerabilities increases the risk of potential exploits, security breaches, and prolonged exposure to known vulnerabilities in the system.

### Parameters

| ID         | Type                     | Description                                                                          |
| ---------- | ------------------------ | ------------------------------------------------------------------------------------ |
| st-5_prm_1 | time period (days) (int) | The time period in days to remediate or risk accept critical vulnerability findings. |
| st-5_prm_2 | time period (days) (int) | The time period in days to remediate or risk accept high vulnerability findings.     |
| st-5_prm_3 | time period (days) (int) | The time period in days to remediate or risk accept medium vulnerability findings.   |
| st-5_prm_4 | time period (days) (int) | The time period in days to remediate or risk accept low vulnerability findings.      |

### References

- [MVSP 3.4: Time to fix vulnerabilities](https://mvsp.dev/)
- [IM8 Cloud Security (IaaS and PaaS): 1.8/S3](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
- [IM8 Cloud Security (IaaS and PaaS): 1.8/S4](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
- [IM8 On-Premise ADS (Non-S): 5.1/S3]()
