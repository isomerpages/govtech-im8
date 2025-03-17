---
title: Data Protection
permalink: /control-catalog/dp/
variant: markdown
description: ""
third_nav_title: Cybersecurity
---

Controls to protect the data of a system.

| Controls                                                                                                                       |
| ------------------------------------------------------------------------------------------------------------------------------ |
| [DP-1: Data Residency](#dp-1-data-residency)                                                                                   |
| [DP-2: Data at Rest Encryption](#dp-2-data-at-rest-encryption)                                                                 |
| [DP-3: Data in Transit Encryption](#dp-3-data-in-transit-encryption)                                                           |
| [DP-4: Government on Commercial Cloud (GCC)](#dp-4-government-on-commercial-cloud-gcc)                                         |
| [DP-5: Sanitisation](#dp-5-sanitisation)                                                                                       |
| [DP-6: Witness Sanitisation and Destruction of Storage Devices](#dp-6-witness-sanitisation-and-destruction-of-storage-devices) |
| [DP-7: Data Loss Prevention](#dp-7-data-loss-prevention)                                                                       |

## DP-1: Data Residency

**Group:** Data Protection

### Control Statement

Enforce data residency of primary data in [ insert: param, dp-1_prm_1 ].

### Control Recommendations

Use the appropriate region of cloud service providers for storage of data, such as ap-southeast-1 for Singapore in AWS. Primary data excludes transient data such as data-in-transit or temporary caches which may briefly pass through or be temporarily stored in other locations as part of normal system operations.

### Risk Statement

Failure to enforce data residency of primary data in the appropriate country may lead to legal and regulatory compliance issues, privacy concerns, and potential unauthorised access or storage of sensitive data outside the jurisdiction, increasing the risk of legal consequences and data breaches.

### Parameters

| ID         | Type          | Description                              |
| ---------- | ------------- | ---------------------------------------- |
| dp-1_prm_1 | country (str) | The country the primary data resides in. |

### References

- [MVSP 1.6: Compliance](https://mvsp.dev/)
- [IM8 Cloud Security (IaaS and PaaS): 1.3/S3](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
- [IM8 On-Premise IS (Non-S): 1.1/S1a]()
- [IM8 Cloud SaaS Security: 1.1/S4]()

## DP-2: Data at Rest Encryption

**Group:** Data Protection

### Control Statement

Encrypt data at rest.

### Control Recommendations

Many CSP services encrypt data at rest by default but this should be confirmed and validated depending on service usage.

### Risk Statement

Without encrypting data at rest, there's an increased risk of unauthorised access and data exposure in the event of physical theft, unauthorised access to storage media, or compromised security controls, compromising the confidentiality of stored information.

### References

- [MVSP 2.8: Encryption](https://mvsp.dev/)
- [IM8 Cloud Security (IaaS and PaaS): 1.3/S2a](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
- [IM8 On-Premise ADS (Non-S): 1.1/S1h]()
- [NIST FIPS 140-3](https://csrc.nist.gov/pubs/fips/140-3/final)

## DP-3: Data in Transit Encryption

**Group:** Data Protection

### Control Statement

Encrypt data in transit.

### Control Recommendations

While some CSP services transparently encrypt data in transit at the network layer, data at the application layer should be encrypted using protocols such as Transport Layer Security (TLS) and Secure Socket Layer (SSL).

### Risk Statement

Failure to encrypt data in transit increases the risk of unauthorised interception and eavesdropping, potentially leading to data breaches, unauthorised access, and compromise of sensitive information during transmission.

### References

- [MVSP 2.8: Encryption](https://mvsp.dev/)
- [IM8 Cloud Security (IaaS and PaaS): 1.3/S2b](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
- [IM8 On-Premise ADS (Non-S): 3.1/S3]()
- [NIST FIPS 140-3](https://csrc.nist.gov/pubs/fips/140-3/final)

## DP-4: Government on Commercial Cloud (GCC)

**Group:** Data Protection

### Control Statement

Host systems classified as CONFIDENTIAL (CLOUD-ELIGIBLE), RESTRICTED, or OFFICIAL-CLOSED on Commercial Cloud hosting environments in GCC.

### Control Recommendations

GCC allows oversight to be maintained at the Whole-of-Government level and implements several controls by default.

### Risk Statement

Hosting higher-sensitivity systems in Government on Commercial Cloud (GCC) ensures compliance with security classifications, reducing the risk of unauthorised access and maintaining data confidentiality according to government security standards.

### References

- [MVSP 1.6: Compliance](https://mvsp.dev/)
- [IM8 Cloud Security (IaaS and PaaS): 1.1/S4](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)

## DP-5: Sanitisation

**Group:** Data Protection

### Control Statement

Sanitise all hardware that stores data at rest. Shred or incinerate data storage meant for retirement.

### Control Recommendations

Use industry standards such as
a) Peter Gutmann Secure Deletion;
b) Bruce Schneier Algorithm
c) US Department of Defence's Standards (DoD 5220.22-M).

### Risk Statement

Violating this control can expose government data to unauthorised users.

### References

- [IM8 On-Premise IS (Non-S): 3.3/S1]()

## DP-6: Witness Sanitisation and Destruction of Storage Devices

**Group:** Data Protection

### Control Statement

Witness the sanitisation and destruction process to ensure data is removed from storage.

### Control Recommendations

Establish a SOP to ensure sanitisation and destruction are witnessed by an agency staff.

### Risk Statement

Ensuring storage devices are sanitised or destroyed will eliminate the possibility of unauthorised or unintended data retention.

### References

- [IM8 On-Premise IS (Non-S): 3.3/S1]()

## DP-7: Data Loss Prevention

**Group:** Data Protection

### Control Statement

Implement data loss prevention mechanisms that monitor data flows, detect sensitive data transfers, and block unauthorised sharing of sensitive data.

### Control Recommendations

Where possible, use built-in solutions such as Microsoft Purview or Google Workspace data loss prevention rules. Regularly review and update data loss prevention policies to adapt to evolving threats and organisational needs.

### Risk Statement

Failure to implement data loss prevention measures increases the risk of unauthorized data exfiltration, accidental data leaks, and data breaches, compromising sensitive information and organizational integrity.

### References

- [CIS Critical Security Controls v8 3.13: Deploy a Data Loss Prevention Solution](https://www.cisecurity.org/controls/v8)
