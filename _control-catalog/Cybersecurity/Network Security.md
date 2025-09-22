---
title: Network Security
permalink: /control-catalog/cybersecurity/ns/
variant: markdown
description: ""
third_nav_title: Cybersecurity
---
Controls to secure the network boundaries of a system.

| Controls                                                                                                                                        |
| ----------------------------------------------------------------------------------------------------------------------------------------------- |
| [NS-1: Network and System Component Segmentation](#ns-1-network-and-system-component-segmentation)                                              |
| [NS-2: Access Restrictions on CSP Resources Outside Virtual Network](#ns-2-access-restrictions-on-csp-resources-outside-virtual-network)        |
| [NS-3: Deny by Default - Allow by Exception](#ns-3-deny-by-default-allow-by-exception)                                                          |
| [NS-4: Inter-Private Network Connectivity](#ns-4-inter-private-network-connectivity)                                                            |
| [NS-5: Network and Application Layer Filtering](#ns-5-network-and-application-layer-filtering)                                                  |
| [NS-6: Valid and Trusted SSL/TLS Certificates](#ns-6-valid-and-trusted-ssltls-certificates)                                                     |
| [NS-7: Secure Inter-Service Communication](#ns-7-secure-inter-service-communication)                                                            |
| [NS-8: Secure Cloud and On-Premises Connectivity](#ns-8-secure-cloud-and-on-premises-connectivity)                                              |
| [NS-9: Intrusion Prevention System (IPS)/Intrusion Detection System (IDS)](#ns-9-intrusion-prevention-system-ipsintrusion-detection-system-ids) |
| [NS-10: Private Network Connectivity](#ns-10-private-network-connectivity)                                                                      |
| [NS-11: Alerts on Firewall Configuration Changes](#ns-11-alerts-on-firewall-configuration-changes)                                              |

## NS-1: Network and System Component Segmentation

**Group:** Network Security

### Control Statement

Segment and isolate system components into separate physical and logical networks or environments based on their security requirements and risk levels.

### Control Recommendations

Deploy security controls such as firewalls, security groups, and API gateways to establish and maintain segmentation. In cloud environments, implement a tiered network architecture where internet-facing services are restricted to designated public segments, while sensitive backend systems remain in private segments with controlled outbound access. Consider micro-segmentation for granular control based on workload sensitivity.

### Risk Statement

Failure to segregate private and public resources within distinct subnets in a virtual network increases the risk of unauthorised access to sensitive data, as private resources may be exposed to the public internet, compromising the overall security of the infrastructure.

## NS-2: Access Restrictions on CSP Resources Outside Virtual Network

**Group:** Network Security

### Control Statement

Restrict access to CSP resources outside of a virtual network (e.g., Lambda, DynamoDb, API Gateways, S3, CloudFront) using access controls or application layer authorisation.

### Control Recommendations

Apply access restrictions appropriate to the resource type. Access through interface VPC endpoints is only required if the client is hosted in a private subnet. For example:

- Restrict access to DynamoDB with IAM policies.

- Restrict access to API Gateway with Lambda authorizers or authorisation middlewares at the application layer. If the API Gateway is exposed to private subnets, create a private API.

- Restrict access to S3 Buckets with IAM policies and block public access from the internet.

### Risk Statement

Lack of access restrictions raises the risk of unauthorised access, data exposure, and potential misuse of critical services, compromising the overall security posture.

## NS-3: Deny by Default - Allow by Exception

**Group:** Network Security

### Control Statement

Deny network communications traffic by default and allow network communications traffic by exception at managed interfaces.

### Control Recommendations

Configure network access control lists and security groups to deny all traffic by default. Only allow traffic to and from specific hosts and ports by exception. For egress traffic to the internet, consider whitelisting domains at the application layer or DNS resolver rather than just hosts or ports at the transport layer.

### Risk Statement

Without network access controls, there&#39;s an increased risk of unauthorised or malicious network access, leading to potential security breaches and compromise of system integrity.

## NS-4: Inter-Private Network Connectivity

**Group:** Network Security

### Control Statement

Route network traffic between private networks without going through the internet.

### Control Recommendations

Use CSP Private endpoint services (e.g., AWS PrivateLink with VPC endpoints) when you want to allow one or more consumer VPCs unidirectional access to a specific service or set of instances in the service provider VPC. Otherwise, use VPC peering and Transit Gateway when you want to enable layer-3 IP connectivity between VPCs. Refer to the [Multi-VPC AWS Network Infrastructure Whitepaper](https://docs.aws.amazon.com/whitepapers/latest/building-scalable-secure-multi-vpc-network-infrastructure/vpc-to-vpc-connectivity.html) for further guidance.

### Risk Statement

When routing through the internet, there&#39;s an increased risk of man-in-the-middle and spoofing attacks. Allowing bidirectional access between networks without fine-grained access controls increases the risk of unauthorised access, potential data exfiltration, and compromise of network security compared to unidirectional access to specific resources.

## NS-5: Network and Application Layer Filtering

**Group:** Network Security

### Control Statement

Filter direct traffic from the internet to protect against network and application layer attacks.

### Control Recommendations

Deploy the following mechanisms as appropriate for the system and network architecture:

- Web Application Firewall

- Distributed Denial of Service Protection (e.g., AWS Shield)

- Content Delivery Network (e.g., CloudFront)

### Risk Statement

Lack of filtering for direct traffic from the internet exposes the system to the risk of network and application layer attacks, increasing the likelihood of unauthorised access, denial-of-service incidents, and compromise of sensitive data.

## NS-6: Valid and Trusted SSL/TLS Certificates

**Group:** Network Security

### Control Statement

Ensure that deployed SSL/TLS certificates are:

- signed by a trusted root Certificate Authority;
- match the domain name of the service they are issued for;
- not expired; and
- not revoked.

### Control Recommendations

Configure a certificate manager that auto-renews certificates and sends alerts before expiry (e.g., AWS Certificate Manager). Otherwise, automate these functions separately.

### Risk Statement

Using invalid SSL/TLS certificates introduces the risk of compromised encryption, man-in-the-middle attacks, and potential unauthorised access to sensitive information.

## NS-7: Secure Inter-Service Communication

**Group:** Network Security

### Control Statement

Ensure communications between services are secure by making them authenticated, authorised and encrypted.

### Control Recommendations

Design and build inter-service communications (e.g., databases, microservices) to be authenticated, authorised and encrypted (e.g., via API gateways, proxies, private endpoint services, message queues, or service meshes). It is recommended to log communication (such as access logs, transaction logs or payloads) between services for detection, monitoring and investigation of incidents.

### Risk Statement

Failure to ensure secure communications between services increases the risk of unauthorised access, data breaches, and potential manipulation of sensitive information during transit.

## NS-8: Secure Cloud and On-Premises Connectivity

**Group:** Network Security

### Control Statement

Route network traffic between on-premises systems and cloud systems through a secure intermediary.

### Control Recommendations

Design and build secure communications to or from on-premises systems through a managed interface with boundary protection mechanisms rather than direct connectivity (e.g. via API gateways, application proxies or private endpoint services).

### Risk Statement

Insecure connectivity between cloud and on-premises environments can lead to data breaches, unauthorised access, and compromise of both cloud and on-premises resources.

## NS-9: Intrusion Prevention System (IPS)/Intrusion Detection System (IDS)

**Group:** Network Security

### Control Statement

Set up and configure an Intrusion Prevention System (IPS)/Intrusion Detection System (IDS) in the network.

### Control Recommendations

Configure network or host IPS/IDS to detect malicious traffic to/from public or untrusted networks.

### Risk Statement

Absence of network or host IPS or IDS in the network increases the likelihood of undetected intrusions, putting sensitive data and system integrity at risk.

## NS-10: Private Network Connectivity

**Group:** Network Security

### Control Statement

Implement strong access controls, encryption, and logging for remote developer, maintainer, or administrator access to private network resources.

### Control Recommendations

Use strong authentication and MFA. Layered security mechanisms and controls include:

- Inspect traffic from gateway to private network;

- Terminate all remote access connections in a dedicated network segment within the network and restrict access to only systems and services allowed by the organisation;

- Implement strong encryption for remote access into internal networks;

- Only allow authorised devices to remotely access internal networks;

- Ensure that remote access connections are not perpetual and re-authenticate remote connections to the VPN gateway on a periodic basis (such as every four hours);

- Set the maximum number of consecutive failed authentication attempts before account lockout for remote access to internal networks; and

- Make sure that split tunnelling is not implemented.

### Risk Statement

Weak private network security may expose the network to malicious activities, jeopardising the confidentiality, integrity, and availability of critical resources.

## NS-11: Alerts on Firewall Configuration Changes

**Group:** Network Security

### Control Statement

Generate alerts to inform appointed administrators on changes to firewall rules, including the enabling or disabling of rules.

### Control Recommendations

Implement real time alerts to inform administrators of creation, deletion, modification, enabling and disabling of firewall rules. Also alert administrators when unusual or sudden spike/drop in utilisation of firewall&#39;s system resources.

### Risk Statement

Any unintended changes to firewall rules can significantly lower the perimeter defence of a network.