---
title: Third Party Management
permalink: /third-party-management/
variant: markdown
description: ""
---
Controls to govern the shared responsibility between organisations and a third party.

| Controls |
| ---- |
| [TP-1: Software as a Service (SaaS) Service Level Agreement](#tp-1) |
| [TP-4: Attestation Report Review](#tp-4) |
| [TP-6: Supplier Assessments and Reviews](#tp-6) |


<a id="tp-1"></a>
## TP-1: Software as a Service (SaaS) Service Level Agreement

### Control Statement

Obtain a service level agreement with the SaaS provider.

### Control Recommendations

Ensure that the service level agreement covers uptime, response times, downtime notifications, support avenues (such as email/phone support), support content (such as logs related to access control, incident report, SOC 2 Type 2 report) and it is regularly checked for compliance.

### Risk Statement

Without a service level agreement the availability of the Software as a Service (SaaS) system may be poorly maintained by the provider.



<a id="tp-4"></a>
## TP-4: Attestation Report Review

### Control Statement

Review the [tp-4_prm_1] attestation report every [tp-4_prm_2] day(s) and ensure that outstanding exceptions or findings are remediated.

### Control Recommendations

The scope of the attestation report should minimally cover the risk assessment, risk mitigation, logical and physical access controls, system operations and change management and should be perfomed by an independent third party.

### Risk Statement

Without reviewing the certification audit report by an independent third party may pose security and compliance risks as there is no independent verification that the system meets industry standards relating to data management and security controls, which potentially lead to data breaches and reputational damage.



#### Parameters

| ID | Type | Description |
| -- | ---- | ----------- |
| tp-4_prm_1 | audit | The audit type. |
| tp-4_prm_2 | time period (days) | The time period in days for report review. |

<a id="tp-6"></a>
## TP-6: Supplier Assessments and Reviews

### Control Statement

Seek an assessment by [tp-6_prm_1] on the risks associated with suppliers or contractors, including the processing and storage of data.

### Control Recommendations

Submit SaaS usage via the [Request for SaaS FormSG](https://go.gov.sg/requestforsaas) and the assessment outcome will be provided within 3 working days.

### Risk Statement

Failure to assess suppliers may introduce supply chain risks associated with data residency and jurisdiction.



#### Parameters

| ID | Type | Description |
| -- | ---- | ----------- |
| tp-6_prm_1 | Assessing party | The party conducting the assessment. |


