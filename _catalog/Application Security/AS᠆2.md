---
title: AS᠆2
permalink: /catalog/as/as-2/
variant: markdown
description: ""
third_nav_title: Application Security
---
# AS-10: HTTP Strict Transport Security (HSTS)

* **Group:** [Application Security](/catalog/as)

## Control Statement

Set HTTP Strict Transport Security (HSTS) response headers with a maximum age value of at least 1 year (31536000 seconds) to mitigate protocol downgrade attacks.

## Control Recommendations

Refer to the [OWASP Secure Headers Project](https://owasp.org/www-project-secure-headers) Best Practices for recommended header values.

## Risk Statement

Failure to implement HTTP Strict Transport Security (HSTS) with a sufficient maximum age may expose the system to protocol downgrade attacks, compromising the security of communication channels.



### References


 * [IM8 Cloud Security (IaaS and PaaS): 1.7/G4](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)