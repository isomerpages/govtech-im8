---
title: NS᠆3
permalink: /catalog/ns/ns-3/
variant: markdown
description: ""
third_nav_title: Network Security
---
# NS-3: Deny by Default – Allow by Exception

* **Group:** [Network Security](/catalog/ns)

## Control Statement

Deny network communications traffic by default and allow network communications traffic by exception at managed interfaces.

## Control Recommendations

Configure network access control lists and security groups to deny all traffic by default. Only allow traffic to and from specific hosts and ports by exception. For egress traffic to the internet, consider whitelisting domains at the application layer or DNS resolver rather than just hosts or ports at the transport layer.

## Risk Statement

Without network access controls, there&#39;s an increased risk of unauthorised or malicious network access, leading to potential security breaches and compromise of system integrity.



### References


 * [NIST SP 800-53 SC-7(5): Deny by Default – Allow by Exception](https://doi.org/10.6028/NIST.SP.800-53r5)
 * [IM8 Cloud Security (IaaS and PaaS): 1.5/S3](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 Cloud Security (IaaS and PaaS): 1.5/S5](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 Cloud Security (IaaS and PaaS): 1.6/S1h](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 Cloud Security (IaaS and PaaS): 1.7/S23b](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 On-Premise IS (Non-S): 4.2/S1b](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/On-Premise/Topics/Infrastructure-Security-(For-Non-S).aspx)
 * [IM8 On-Premise AAS (Non-S): 2.2/S1](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/On-Premise/Topics/Application-Architecture-Security-(For-Non-S).aspx)