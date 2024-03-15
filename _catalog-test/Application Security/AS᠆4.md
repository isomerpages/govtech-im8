---
title: AS᠆4
permalink: /catalog/as/as-4/
variant: markdown
description: ""
third_nav_title: Application Security
---
# AS-4: Authentication Mechanism Rate-Limiting

* **Group:** [Application Security](/catalog/as)

## Control Statement

Apply rate-limiting on all authentication mechanisms to deter brute-force attacks.

## Control Recommendations

Consider rate-limiting to a maximum of 3 consecutive failed authentication attempts within 15 minutes. Time delays between log-on attempts reduce the risk of successful brute-forcing attacks. Bot mitigation tools such as CAPTCHA can further reduce this risk.

## Risk Statement

Without rate-limiting, there&#39;s an increased risk of unauthorised access as attackers may exploit weak credentials through repeated login attempts.



### References


 * [MVSP 2.4: Password policy](https://mvsp.dev/)
 * [IM8 Cloud ADS: 2.2/S1j, 2.2/S5b](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Application-Development-Security-(For-Cloud).aspx)