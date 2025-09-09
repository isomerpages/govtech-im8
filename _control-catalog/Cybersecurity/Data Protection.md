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
| [DP-4: Central Cloud Tenant Management](#dp-4-central-cloud-tenant-management)                                                 |
| [DP-5: Sanitisation](#dp-5-sanitisation)                                                                                       |
| [DP-6: Witness Sanitisation and Destruction of Storage Devices](#dp-6-witness-sanitisation-and-destruction-of-storage-devices) |

## DP-1: Data Residency

**Group:** Data Protection

### Control Statement

Enforce data residency of [ insert: param, dp-1_prm_2 ] data in [ insert: param, dp-1_prm_1 ].

### Control Recommendations

Data residency in Singapore must be enforced for [ insert: param, dp-1_prm_2 ] data.

### Risk Statement

Failure to enforce data residency in the appropriate country may lead to legal and regulatory compliance issues, privacy concerns, and potential unauthorised access or storage of sensitive data outside the jurisdiction, increasing the risk of legal consequences and data breaches.

### Parameters

| ID         | Type          | Description                                                |
| ---------- | ------------- | ---------------------------------------------------------- |
| dp-1_prm_1 | country (str) | The country the data resides in.                           |
| dp-1_prm_2 | type (str)    | The type of data that should have enforced data residency. |

## DP-2: Data at Rest Encryption

**Group:** Data Protection

### Control Statement

Encrypt data at rest.

### Control Recommendations

Many CSP services encrypt data at rest by default but this should be confirmed and validated depending on service usage.

### Risk Statement

Without encrypting data at rest, there&#39;s an increased risk of unauthorised access and data exposure in the event of physical theft, unauthorised access to storage media, or compromised security controls, compromising the confidentiality of stored information.

## DP-3: Data in Transit Encryption

**Group:** Data Protection

### Control Statement

Encrypt data in transit.

### Control Recommendations

While some CSP services transparently encrypt data in transit at the network layer, data at the application layer should be encrypted using protocols such as Transport Layer Security (TLS) and Secure Socket Layer (SSL).

### Risk Statement

Failure to encrypt data in transit increases the risk of unauthorised interception and eavesdropping, potentially leading to data breaches, unauthorised access, and compromise of sensitive information during transmission.

## DP-4: Central Cloud Tenant Management

**Group:** Data Protection

### Control Statement

Implement a centralised cloud tenant management structure for [ insert: param, dp-4_prm_1 ] using [ insert: param, dp-4_prm_2 ].

### Control Recommendations

Consider services like AWS Organizations, GCP Organizations, or Azure Management Groups for centralised management. Implement appropriate landing zone frameworks. Establish consistent policies and guardrails across all accounts or projects. Centralise logging and monitoring for comprehensive visibility. Use tagging strategies for resource organisation.

### Risk Statement

Lack of centralised cloud tenant management can lead to inconsistent security policies, reduced visibility, and increased difficulty in managing and securing cloud resources across the organisation.

### Parameters

| ID         | Type          | Description                                   |
| ---------- | ------------- | --------------------------------------------- |
| dp-4_prm_1 | systems (str) | The systems to be hosted on a central tenant. |
| dp-4_prm_2 | system (str)  | The central tenant management structure.      |

## DP-5: Sanitisation

**Group:** Data Protection

### Control Statement

Sanitise all hardware that stores data at rest. Shred or incinerate data storage meant for retirement.

### Control Recommendations

Use industry standards such as
a) Peter Gutmann Secure Deletion;
b) Bruce Schneier Algorithm
c) US Department of Defence&#39;s Standards (DoD 5220.22-M).

### Risk Statement

Violating this control can expose government data to unauthorised users.

## DP-6: Witness Sanitisation and Destruction of Storage Devices

**Group:** Data Protection

### Control Statement

Witness the sanitisation and destruction process to ensure data is removed from storage.

### Control Recommendations

Establish a SOP to ensure sanitisation and destruction are witnessed by an agency staff.

### Risk Statement

Ensuring storage devices are sanitised or destroyed will eliminate the possibility of unauthorised or unintended data retention.

