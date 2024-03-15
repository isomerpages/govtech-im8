---
title: AS 3
permalink: /catalog/as/as-3/
variant: markdown
description: ""
third_nav_title: Application Security
---
# AS-3: Output Sanitisation

* **Group:** [Application Security](/catalog/as)

## Control Statement

Sanitise all application outputs that will be used to render a HTML document.

## Control Recommendations

Any application outputs that are returned to the requester and used to render a HTML document can lead to cross-site scripting (XSS) attacks if they contain special characters that change the rendering of the HTML document by the browser.

## Risk Statement

Lack of sanitisation for application outputs used in rendering HTML documents exposes the system to the risk of cross-site scripting (XSS) attacks, allowing malicious code execution in users&#39; browsers.



### References


 * [MVSP 2.5: Security libraries](https://mvsp.dev/)
 * [IM8 Cloud Security (IaaS and PaaS): 1.7/S8e](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 On-Premise ADS (Non-S): 1.1/S1e,k,l](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/On-Premise/Topics/Application-Development-Security-(For-Non-S).aspx)