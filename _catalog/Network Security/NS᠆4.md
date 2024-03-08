---
title: NS᠆4
permalink: /catalog/ns/ns-4/
variant: markdown
description: ""
third_nav_title: Network Security
---
# NS-4: Inter-Private Network Connectivity

* **Group:** [Network Security](/catalog/ns)

## Control Statement

Route network traffic between private networks without going through the internet.

## Control Recommendations

Use CSP Private endpoint services (e.g., AWS PrivateLink with VPC endpoints) when you want to allow one or more consumer VPCs unidirectional access to a specific service or set of instances in the service provider VPC. Otherwise, use VPC peering and Transit Gateway when you want to enable layer-3 IP connectivity between VPCs. Refer to the [Multi-VPC AWS Network Infrastructure Whitepaper](https://docs.aws.amazon.com/whitepapers/latest/building-scalable-secure-multi-vpc-network-infrastructure/vpc-to-vpc-connectivity.html) for further guidance.

## Risk Statement

When routing through the internet, there&#39;s an increased risk of man-in-the-middle and spoofing attacks. Allowing bidirectional access between networks without fine-grained access controls increases the risk of unauthorized access, potential data exfiltration, and compromise of network security compared to unidirectional access to specific resources.



### References


 * [IM8 Cloud Security (IaaS and PaaS): 1.5/S7](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 Cloud Security (IaaS and PaaS): 1.5/S4](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)