---
title: LM᠆1
permalink: /catalog/lm/lm-1/
variant: markdown
description: ""
third_nav_title: Logging and Monitoring
---
# LM-1: Separate Log Storage

* **Group:** [Logging and Monitoring](/catalog/lm)

## Control Statement

Store logs in a repository that is part of a different system or system component than the system or component being audited.

## Control Recommendations

Send logs to the separate storage as soon as possible after the logged event. For cloud audit logs, store them in a separate service or account (such as AWS Organisation Cloudtrail in GCC). Sending logs to the Government Cyber Security Operations Centre (GCSOC) or the central Government Commercial Cloud (GCC) log bucket can also satisfy this control.

## Risk Statement

Storing logs in a repository separate from the audited system or component enhances security by reducing the risk of tampering, unauthorised access, and manipulation of audit trails, ensuring the integrity and reliability of log data for forensic analysis and compliance purposes.



### References


 * [MVSP 2.7: Logging](https://mvsp.dev/)
 * [NIST SP 800-53 AU-9(2): Store on Separate Physical Systems or Components](https://doi.org/10.6028/NIST.SP.800-53r5)
 * [IM8 On-Premise IS (Non-S): 7.2/S8](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/On-Premise/Topics/Infrastructure-Security-(For-Non-S).aspx)