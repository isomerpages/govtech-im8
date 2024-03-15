---
title: AS᠆5
permalink: /catalog/as-5/
variant: markdown
description: ""
third_nav_title: Application Security
---
# AS-5: Password Requirements

* **Group:** [Application Security](/catalog/as)

## Control Statement

Where SSO or passwordless is not supported, verify that user-defined passwords are at least [as-5_prm_1] characters in length and [as-5_prm_2].

## Control Recommendations

Latest NIST [SP 800-63B](https://doi.org/10.6028/NIST.SP.800-63b) guidelines found that password length is a primary factor in determining the strength of a password while composition and complexity rules provide marginal security benefits.

## Risk Statement

Short or commonly used passwords increase the vulnerability to unauthorised access, potentially leading to compromised accounts and unauthorised activities on the system.



### Parameters

| ID | Type | Description |
| -- | ---- | ----------- |
| as-5_prm_1 | number of characters | The minimum length of a password. |
| as-5_prm_2 | policy | The password policy. |

### References


 * [MVSP 2.4: Password policy](https://mvsp.dev/)
 * [NIST SP 800-53 IA-5(1): Password-based Authentication](https://doi.org/10.6028/NIST.SP.800-53r5)
 * [IM8 Cloud Security (IaaS and PaaS): 1.4/S1a](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 Cloud Security (IaaS and PaaS): 1.4/S2a](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 On-Premise ADS (Non-S): 2.2/S1](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/On-Premise/Topics/Application-Development-Security-(For-Non-S).aspx)