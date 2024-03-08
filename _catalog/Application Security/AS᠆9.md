---
title: AS᠆9
permalink: /catalog/as/as-9/
variant: markdown
description: ""
third_nav_title: Application Security
---
# AS-9: Content Security Policy (CSP)

* **Group:** [Application Security](/catalog/as)

## Control Statement

Set minimally permissive CSP response headers to mitigate cross-site scripting attacks.

## Control Recommendations

Utilise the relevant fetch directives such as `default-src`, `script-src`, `style-src`, `connect-src`, `img-src`, `media-src` and `object-src` to prevent loading of scripts from malicious sources. Refer to the [OWASP Secure Headers Project](https://owasp.org/www-project-secure-headers) Best Practices for recommended header values.

## Risk Statement

Without minimally permissive Content Security Policy (CSP) headers, the risk of cross-site scripting attacks, leading to unauthorised script execution and potential data theft, is increased.



### References


 * [MVSP 2.3: Security Headers](https://mvsp.dev/)
 * [IM8 Cloud Security (IaaS and PaaS): 1.7/G7](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)