---
title: SD᠆6
permalink: /catalog/sd/sd-6/
variant: markdown
description: ""
third_nav_title: Secure Development
---
# SD-6: Secret Detection Scanning

* **Group:** [Secure Development](/catalog/sd)

## Control Statement

Set up a secret detection alert or job in the development CI/CD pipeline that runs on each commit and remediate true positives within [sd-6_prm_1] day(s).

## Control Recommendations

Ensure that the exposed secret is revoked and purged from the Git history.

## Risk Statement

Without setting up secret detection alerts or jobs in the development CI/CD pipeline and addressing true positive findings promptly, there&#39;s an increased risk of exposing sensitive information, potential unauthorized access, and compromised security.



### Parameters

| ID | Type | Description |
| -- | ---- | ----------- |
| sd-6_prm_1 | time period (days) | Number of days within which to remediate a secret detection true positive. |

### References


 * [IM8 Cloud Security (IaaS and PaaS): 1.7/S8f](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 Cloud ADS: 1.1/S1f](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Application-Development-Security-(For-Cloud).aspx)
 * [IM8 Cloud ADS: 6.4/G1b](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Application-Development-Security-(For-Cloud).aspx)