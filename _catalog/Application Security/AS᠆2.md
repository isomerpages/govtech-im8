---
title: AS᠆2
permalink: /catalog/as/as-2/
variant: markdown
description: ""
third_nav_title: Application Security
---
# AS-2: Parametrised Interfaces

* **Group:** [Application Security](/catalog/as)

## Control Statement

Use parametrised interfaces for database queries or system commands.

## Control Recommendations

Parametrised interfaces such Object-Relational Mapping (ORM) libraries ensure that parameters used in database queries or system commands are properly sanitised and prevent injection attacks.

## Risk Statement

Failure to use parameterised interfaces increases the vulnerability to SQL injection or command injection attacks, posing a significant risk of unauthorised access, data manipulation, or even potential system compromise.



### References


 * [MVSP 2.5: Security libraries](https://mvsp.dev/)
 * [IM8 Cloud Security (IaaS and PaaS): 1.7/S8c](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 On-Premise ADS (Non-S): 1.1/S1c](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/On-Premise/Topics/Application-Development-Security-(For-Non-S).aspx)