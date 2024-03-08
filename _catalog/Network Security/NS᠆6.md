---
title: NS᠆6
permalink: /catalog/ns/ns-6/
variant: markdown
description: ""
third_nav_title: Network Security
---
# NS-6: Valid and Trusted SSL/TLS Certificates

* **Group:** [Network Security](/catalog/ns)

## Control Statement

Ensure that deployed SSL/TLS certificates are:
 * signed by a trusted root Certificate Authority;
 * match the domain name of the service they are issued for;
 * not expired; and
 * not revoked.


## Control Recommendations

Configure a certificate manager that auto-renews certificates and sends alerts at least [ns-6_prm_1] day(s) before expiry (e.g., AWS Certificate Manager). Otherwise, automate these functions separately.

## Risk Statement

Using invalid SSL/TLS certificates introduces the risk of compromised encryption, man-in-the-middle attacks, and potential unauthorised access to sensitive information.



### Parameters

| ID | Type | Description |
| -- | ---- | ----------- |
| ns-6_prm_1 | time period (days) | The time period in days before certificate expiry. |

### References


 * [IM8 Cloud Security (IaaS and PaaS): 1.5/S8](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)