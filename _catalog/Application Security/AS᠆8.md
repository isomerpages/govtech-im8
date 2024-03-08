---
title: AS᠆8
permalink: /catalog/as-8/
variant: markdown
description: ""
third_nav_title: Application Security
---
# AS-8: Application Secrets Management

* **Group:** [Application Security](/catalog/as)

## Control Statement

Encrypt and store application secrets in a secret management solution with appropriate access controls and do not hard-code secrets in source code.

## Control Recommendations

Secret management solutions include cloud solutions like AWS Secrets Manager and Azure Key Vault as well as cloud-agnostic solutions like HashiCorp Vault and CyberArk Conjur.

## Risk Statement

Exposure of sensitive information and unauthorised access to system credentials may occur if application secrets are stored without encryption or if hard-coded in source code.



### References


 * [IM8 Cloud Security (IaaS and PaaS): 1.7/S11](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 On-Premise ADS (Non-S): 1.1/S1f, 2.2/S4, 3.1/S1 and 3.1/S4](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/On-Premise/Topics/Application-Development-Security-(For-Non-S).aspx)