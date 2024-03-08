---
title: IS᠆6
permalink: /catalog/is/is-6/
variant: markdown
description: ""
third_nav_title: Infrastructure Security
---
# IS-6: Remote Administration

* **Group:** [Infrastructure Security](/catalog/is)

## Control Statement

Use remote administration tools instead of direct SSH or RDP.

## Control Recommendations

In production environments, use remote administration (e.g., AWS Systems Manager Session Manager, AWS Systems Manager Fleet Manager, GCC Privileged Identity Management) only for break glass scenarios where remote monitoring and automation is not available. Document and remediate gaps in monitoring and automation to minimise the need for remote administration. If SSH is still required and remote administration tools are not available, only use it within a private non-production environment such as an encrypted tunnel and authenticate with short-lived certificates.

## Risk Statement

Using remote administration tools enhances security by providing controlled and audited access, reducing the risk of unauthorised activities, and improving overall management of privileged identities.



### References


 * [AWS SSB WKLD.06: Use Systems Manager instead of SSH or RDP](https://docs.aws.amazon.com/prescriptive-guidance/latest/aws-startup-security-baseline/)
 * [IM8 Cloud Security (IaaS and PaaS): 1.4/S21](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)