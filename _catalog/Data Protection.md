---
title: Data Protection
permalink: /catalog/dp/
variant: markdown
description: ""
---
Controls to protect the data of a system.

| Controls |
| ---- |
| [DP-1: Data Residency](#dp-1) |
| [DP-2: Data at Rest Encryption](#dp-2) |
| [DP-3: Data in Transit Encryption](#dp-3) |
| [DP-4: Government on Commercial Cloud (GCC)](#dp-4) |
| [DP-5: Sanitisation](#dp-5) |
| [DP-6: Witness Sanitisation and Destruction of Storage Devices](#dp-6) |


<a id="dp-1"></a>
## DP-1: Data Residency

### Control Statement

Enforce data residency of primary data in Singapore.

### Control Recommendations

Use the Singapore region of cloud service providers for compute and storage of primary data, such as ap-southeast-1 for AWS.

### Risk Statement

Failure to enforce data residency of primary data in Singapore may lead to legal and regulatory compliance issues, privacy concerns, and potential unauthorised access or storage of sensitive data outside the jurisdiction, increasing the risk of legal consequences and data breaches.



<a id="dp-2"></a>
## DP-2: Data at Rest Encryption

### Control Statement

Encrypt data at rest.

### Control Recommendations

Many CSP services encrypt data at rest by default but this should be confirmed and validated depending on service usage.

### Risk Statement

Without encrypting data at rest, there's an increased risk of unauthorised access and data exposure in the event of physical theft, unauthorised access to storage media, or compromised security controls, compromising the confidentiality of stored information.



<a id="dp-3"></a>
## DP-3: Data in Transit Encryption

### Control Statement

Encrypt data in transit.

### Control Recommendations

While some CSP services transparently encrypt data in transit at the network layer, data at the application layer should be encrypted using protocols such as Transport Layer Security (TLS).

### Risk Statement

Failure to encrypt data in transit increases the risk of unauthorised interception and eavesdropping, potentially leading to data breaches, unauthorised access, and compromise of sensitive information during transmission.



<a id="dp-4"></a>
## DP-4: Government on Commercial Cloud (GCC)

### Control Statement

Host systems classified as CONFIDENTIAL (CLOUD-ELIGIBLE), RESTRICTED, OFFICIAL-CLOSED or OFFICIAL-OPEN on Commercial Cloud hosting environments in GCC.

### Control Recommendations

GCC allows oversight to be maintained at the Whole-of-Government level and implements several controls by default.

### Risk Statement

Hosting higher-sensitivity systems in Government on Commercial Cloud (GCC) ensures compliance with security classifications, reducing the risk of unauthorised access and maintaining data confidentiality according to government security standards.



<a id="dp-5"></a>
## DP-5: Sanitisation

### Control Statement

Sanitise all hardware that stores data at rest. Shred or incinerate data storage meant for retirement.

### Control Recommendations

Use industry standards such as
a) Peter Gutmann Secure Deletion;
b) Bruce Schneier Algorithm
c) US Department of Defence's Standards (DoD 5220.22-M).

### Risk Statement

Violating this control can expose government data to unauthorised users.



<a id="dp-6"></a>
## DP-6: Witness Sanitisation and Destruction of Storage Devices

### Control Statement

Witness the sanitisation and destruction process to ensure data is removed from storage.

### Control Recommendations

Establish a SOP to ensure sanitisation and destruction are witnessed by an agency staff.

### Risk Statement

Ensuring storage devices are sanitised or destroyed will eliminate the possibility of unauthorised or unintended data retention.




