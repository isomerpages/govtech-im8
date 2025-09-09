---
title: Cryptography, Encryption and Key Management
permalink: /cryptography-encryption-and-key-management/
variant: markdown
description: ""
third_nav_title: Cybersecurity
---
Controls to secure cryptographic protocols.

| Controls                                                                       |
| ------------------------------------------------------------------------------ |
| [CK-1: Cryptographic Key Establishment](#ck-1-cryptographic-key-establishment) |
| [CK-2: Cryptographic Key Rotation](#ck-2-cryptographic-key-rotation)           |
| [CK-3: Cryptographic Key Management](#ck-3-cryptographic-key-management)       |
| [CK-4: Cryptographic Key Storage](#ck-4-cryptographic-key-storage)             |

## CK-1: Cryptographic Key Establishment

**Group:** Cryptography, Encryption and Key Management

### Control Statement

Use industry-standard cryptographic key establishment schemes and key derivation methods.

### Control Recommendations

Refer to [SP 800-56A](https://doi.org/10.6028/NIST.SP.800-56Ar3), [SP 800-56B](https://doi.org/10.6028/NIST.SP.800-56Br2), and [SP 800-56C](https://doi.org/10.6028/NIST.SP.800-56Cr2) for updated industry-standard cryptographic key establishment schemes and key derivation methods. Cloud services such as AWS Key Management Service and Azure Key Vault can be used for generating and managing cryptographic keys.

### Risk Statement

Insecure cryptographic key establishment can lead to weak or broken encryption.

## CK-2: Cryptographic Key Rotation

**Group:** Cryptography, Encryption and Key Management

### Control Statement

Rotate cryptographic keys every [ insert: param, ck-2_prm_1 ] days.

### Control Recommendations

Cloud services such as AWS Key Management Service and Azure Key Vault enable automatic rotation of cryptographic keys.

### Risk Statement

Failing to rotate cryptographic keys increases the risk of broken encryption.

### Parameters

| ID         | Type                     | Description                                                      |
| ---------- | ------------------------ | ---------------------------------------------------------------- |
| ck-2_prm_1 | time period (days) (int) | The time period in days of cryptographic key rotation frequency. |

## CK-3: Cryptographic Key Management

**Group:** Cryptography, Encryption and Key Management

### Control Statement

Implement cryptographic key management processes to ensure cryptographic keys are well-managed and safeguarded throughout their lifecycle.

### Control Recommendations

Follow key management practices such as those described in NIST SP 800-57 or ISO/IEC 27017 to cover aspects including generation, registration, storage, distribution, installation, use, rotation, backup, recovery, revocation, suspension, and destruction of keys.

### Risk Statement

Inadequate key management increase the risk of unauthorised access, data breaches, and compromised cryptographic operations due to poorly managed or safeguarded cryptographic keys.

## CK-4: Cryptographic Key Storage

**Group:** Cryptography, Encryption and Key Management

### Control Statement

Securely store cryptographic keys and implement strict access controls based on the principle of least privilege.

### Control Recommendations

Use cloud services such as AWS Key Management Service and Azure Key Vault to securely store cryptographic keys with access controls.

### Risk Statement

Inadequate key storage and access controls can lead to unauthorised key access and potential data breaches.
