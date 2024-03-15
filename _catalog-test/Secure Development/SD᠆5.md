---
title: SD᠆5
permalink: /catalog/sd/sd-5/
variant: markdown
description: ""
third_nav_title: Secure Development
---
# SD-5: Dependency Scanning

* **Group:** [Secure Development](/catalog/sd)

## Control Statement

Schedule a scan at least every [sd-5_prm_1] day(s) in the CI/CD pipeline and/or repository to identify the use of vulnerable software libraries.

## Control Recommendations

Dependency scanning checks the source code for dependencies with known vulnerabilities. By running scans regularly using bots or software composition analysis (SCA) tools, vulnerabilities arising from outdated dependencies can be quickly detected and patched. Triage and prioritise vulnerabilities against Common Vulnerability Scoring System (CVSS), Known Exploited Vulnerabilities (KEV) Catalog, Vulnerability Exploitability eXchange (VEX) and other sources.

## Risk Statement

Failing to schedule regular scans in the CI/CD pipeline to identify vulnerable software libraries and address findings in a timely manner increases the risk of deploying applications with known vulnerabilities, potentially exposing the system to security exploits and compromise.



### Parameters

| ID | Type | Description |
| -- | ---- | ----------- |
| sd-5_prm_1 | time period (days) | The time period in days of dependency scanning frequency. |

### References


 * [MVSP 2.6: Dependency Patching](https://mvsp.dev/)
 * [IM8 Cloud Security (IaaS and PaaS): 1.7/S8i](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 Cloud ADS: 8.1/S2](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Application-Development-Security-(For-Cloud).aspx)