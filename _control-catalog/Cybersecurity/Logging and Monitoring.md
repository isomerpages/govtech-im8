---
title: Logging and Monitoring
permalink: /control-catalog/cybersecurity/lm/
variant: markdown
description: ""
third_nav_title: Cybersecurity
---
Controls to support detection and response to security and operations incidents.

| Controls                                                                                                           |
| ------------------------------------------------------------------------------------------------------------------ |
| [LM-1: Separate Log Storage](#lm-1-separate-log-storage)                                                           |
| [LM-2: Tamper-Resistant Log Storage](#lm-2-tamper-resistant-log-storage)                                           |
| [LM-3: Network Flow Logging](#lm-3-network-flow-logging)                                                           |
| [LM-4: Audit Logging](#lm-4-audit-logging)                                                                         |
| [LM-5: Database Logging](#lm-5-database-logging)                                                                   |
| [LM-6: Access Logging](#lm-6-access-logging)                                                                       |
| [LM-7: Host Security Event Logging](#lm-7-host-security-event-logging)                                             |
| [LM-8: Security Log Retention](#lm-8-security-log-retention)                                                       |
| [LM-9: Security Monitoring and Alerting](#lm-9-security-monitoring-and-alerting)                                   |
| [LM-10: Resource Usage Monitoring and Alerting](#lm-10-resource-usage-monitoring-and-alerting)                     |
| [LM-11: Service Level Monitoring and Alerting](#lm-11-service-level-monitoring-and-alerting)                       |
| [LM-12: Central Security Log Management and Monitoring](#lm-12-central-security-log-management-and-monitoring)     |
| [LM-13: Anomalous Database Activity Monitoring](#lm-13-anomalous-database-activity-monitoring)                     |
| [LM-14: Web Defacement Monitoring](#lm-14-web-defacement-monitoring)                                               |
| [LM-15: Structured Log Formatting](#lm-15-structured-log-formatting)                                               |
| [LM-16: Key Signals Monitoring](#lm-16-key-signals-monitoring)                                                     |
| [LM-17: Software delivery performance monitoring](#lm-17-software-delivery-performance-monitoring)                 |
| [LM-19: Log Sanitisation](#lm-19-log-sanitisation)                                                                 |
| [LM-21: Detection Updates](#lm-21-detection-updates)                                                               |

## LM-1: Separate Log Storage

**Group:** Logging and Monitoring

### Control Statement

Store logs in a different system or system component than the system component that generated the logs.

### Control Recommendations

Do not store logs only in the same system component that generated it. For example, an application server on EC2 or ECS should send logs to a separate storage such as an S3 bucket as soon as possible after the logged event instead of only storing it on the server. For cloud audit logs, store them in a separate system or account.

### Risk Statement

Storing logs in a repository separate from the system component reduces the risk of tampering, unauthorised access, and manipulation of logs if the system component is compromised.

## LM-2: Tamper-Resistant Log Storage

**Group:** Logging and Monitoring

### Control Statement

Protect logs from unauthorised access, modification, and deletion.

### Control Recommendations

Apply access control policies to logs based on the principle of least privilege. As far as possible, only read access should be granted. Logs sent to GCC Central Logs are tamper-resistant.

### Risk Statement

Without protection measures, logs are susceptible to unauthorised access, modification, or deletion, leading to the risk of tampering, loss of crucial audit information, and compromised forensic analysis capabilities during security incidents.

## LM-3: Network Flow Logging

**Group:** Logging and Monitoring

### Control Statement

Log network traffic going to and from network interfaces.

### Control Recommendations

Enable VPC Flow Logs for AWS or its equivalents.

### Risk Statement

Failing to log network traffic going to and from network interfaces increases the risk of overlooking suspicious activities, potential security breaches, and the inability to trace and investigate network-related incidents effectively.

## LM-4: Audit Logging

**Group:** Logging and Monitoring

### Control Statement

Log management and audit events.

### Control Recommendations

For cloud, configure CloudTrail for AWS or its equivalents to log management and audit events such as changes to accounts, access, IAM policies and resources. For SaaS and COTS, enable audit logging features.

### Risk Statement

Neglecting to log and manage audit events increases the risk of undetected security incidents, compromises visibility into system activities, and hinders effective forensic analysis and compliance monitoring.

## LM-5: Database Logging

**Group:** Logging and Monitoring

### Control Statement

Log database audit events.

### Control Recommendations

Enable RDS logging for AWS or its equivalents.

### Risk Statement

Neglecting to log database audit events raises the risk of overlooking unauthorised activities, compromises in data security, and hinders the ability to track and investigate security incidents or compliance violations within the database environment.

## LM-6: Access Logging

**Group:** Logging and Monitoring

### Control Statement

Log access requests sent to web application firewalls, load balancers, proxies or web servers.

### Control Recommendations

Enable AWS WAF logging, Application Load Balancer logging, API Gateways, or their equivalents.

### Risk Statement

Failure to log access requests sent to web application firewalls, load balancers, proxies, or web servers increases the risk of overlooking potential security threats, unauthorised access attempts, and compromises visibility into the traffic that could lead to security incidents.

## LM-7: Host Security Event Logging

**Group:** Logging and Monitoring

### Control Statement

Log security events on hosts.

### Control Recommendations

Host security events include operating system security events, authentication, and endpoint detection and response alerts, configuration changes, and account and access rights changes.

### Risk Statement

Neglecting to log security events on hosts increases the risk of undetected security incidents, compromises incident response capabilities, and hinders forensic analysis, limiting the ability to identify and mitigate potential threats.

## LM-8: Security Log Retention

**Group:** Logging and Monitoring

### Control Statement

Retain security logs for at least [ insert: param, lm-8_prm_1 ] day(s).

### Control Recommendations

Security logs include network flow logs, cloud management logs, access logs, database logs and host logs. Retain non-security logs (e.g. application, operations and performance logs) as long as needed for incident resolution and debugging. Consider log lifecycle management automation, such as Amazon S3 Lifecycle configurations.

### Risk Statement

Failure to retain security logs increases the risk of losing crucial historical data, hindering investigations, compliance audits, and the ability to identify and respond to security incidents that occurred beyond a limited timeframe.

### Parameters

| ID         | Type                     | Description                               |
| ---------- | ------------------------ | ----------------------------------------- |
| lm-8_prm_1 | time period (days) (int) | The time period in days of log retention. |

## LM-9: Security Monitoring and Alerting

**Group:** Logging and Monitoring

### Control Statement

Configure security monitoring to identify potential security violations or breaches and send automated alerts, and respond to them accordingly.

### Control Recommendations

Enable Amazon GuardDuty, Microsoft Azure Security Center, or their equivalents.

### Risk Statement

Without configuring security monitoring to identify potential security violations or breaches and send automated alerts, there&#39;s an increased risk of delayed or unnoticed security incidents, hindering timely response and mitigation efforts to protect the system from further compromise.

## LM-10: Resource Usage Monitoring and Alerting

**Group:** Logging and Monitoring

### Control Statement

Configure resource usage monitoring to identify abnormal usage and send automated alerts.

### Control Recommendations

Configure Amazon CloudWatch alarms, Azure Monitor alerts, or their equivalents to identify abnormal usage such as spike in usage, access to resources during unexpected hours, and excessive charges.

### Risk Statement

Lack of resource usage monitoring with automated alerts increases the risk of overlooking abnormal usage patterns, potential resource abuse, and compromises in system performance, hindering the ability to proactively address issues and prevent service disruptions.

## LM-11: Service Level Monitoring and Alerting

**Group:** Logging and Monitoring

### Control Statement

Monitor, maintain and alert on service level objectives (SLOs) and indicators (SLIs) to ensure consistent service performance, availability and reliability.

### Control Recommendations

Implement a comprehensive monitoring system that tracks key SLIs and evaluates them against defined SLOs. This will help in identifying potential service level breaches early and take proactive measures to maintain service quality. Examples include CloudWatch metrics and alerts, Amazon Route 53 health checks, Azure Monitor Application Insights, or their equivalents.

### Risk Statement

Without effective service level monitoring to identify potential application or service degradation and send automated alerts, there is a risk of failing to meet service availability standards, which could result in user dissatisfaction and reduced reliability.

## LM-12: Central Security Log Management and Monitoring

**Group:** Logging and Monitoring

### Control Statement

Centralise security log management and monitoring with [ insert: param, lm-12_prm_1 ].

### Control Recommendations

Tenants on Government Commercial Cloud (GCC) already have Cloud Service Provider (CSP) tenant security logs stored centrally and available for forwarding to Government Cyber Security Operations Centre (GCSOC). Contact GCSOC for subscription and additional services.

### Risk Statement

Lack of central security log management and monitoring increases the risk of delayed or unnoticed security incidents, hindering effective response, and compromising the overall cybersecurity posture.

### Parameters

| ID          | Type          | Description                                                 |
| ----------- | ------------- | ----------------------------------------------------------- |
| lm-12_prm_1 | service (str) | The central security log management and monitoring service. |

## LM-13: Anomalous Database Activity Monitoring

**Group:** Logging and Monitoring

### Control Statement

Monitor database activities for anomalous activity.

### Control Recommendations

Configure database activity monitoring tools, such as RDS Activity Streams or similar mechanisms, to detect and alert on unusual authentication attempts, abnormal read or write operations, or other anomalous database activity.

### Risk Statement

Neglecting to monitor database activities for anomalous behaviour increases the risk of undetected security threats, unauthorised access, and compromises in data integrity, hindering the ability to identify and respond to potential database-related incidents.

## LM-14: Web Defacement Monitoring

**Group:** Logging and Monitoring

### Control Statement

Plan for and implement measures to detect and recover from web defacements.

### Control Recommendations

Visual monitoring tools enable detection of web defacements of internet-facing systems.

### Risk Statement

Failure to detect and respond to web defacement promptly will lead to prolonged disruption to services.

## LM-15: Structured Log Formatting

**Group:** Logging and Monitoring

### Control Statement

Publish logs in a consistent, structured format that aligns with industry standards for easy parsing and analysis.

### Control Recommendations

For security logs, implement or transform to OCSF (Open Cybersecurity Schema Framework), ECS (Elastic Common Schema) or similar schemas to standardise log formats for better threat detection and analysis. For operational logs, adopt OpenTelemetry or structured JSON formats to facilitate clear, structured, and efficient log analysis for system performance and diagnostics. Consistent log formatting aids in automated parsing and helps in integrating logs from various sources.

### Risk Statement

Inconsistent or unstructured log formatting can lead to difficulties in log analysis and monitoring, potentially resulting in missed critical events or delayed response to system anomalies.

## LM-16: Key Signals Monitoring

**Group:** Logging and Monitoring

### Control Statement

Monitor key user-facing signals to maintain robust service health and performance.

### Control Recommendations

Implement monitoring of key signals such as latency, traffic, errors, and saturation (the 4 Golden Signals). Regularly track and analyse these indicators for proactive issue detection and resolution. Use this data to identify trends and areas for system improvement, ensuring continuous enhancement in service quality and reliability.

### Risk Statement

Inadequate monitoring of key user-facing signals such as latency, traffic, errors, and saturation can lead to suboptimal service performance, adversely impacting user experience, system efficiency, and increasing the likelihood of system failures. This oversight can significantly detract from service reliability and user satisfaction.

## LM-17: Software delivery performance monitoring

**Group:** Logging and Monitoring

### Control Statement

Measure and analyse software delivery performance to optimise development velocity and operational efficiency.

### Control Recommendations

Implement tools and processes to track Deployment Frequency, Lead Time for Changes, Change Failure Rate, and Time to Restore Service (the DORA 4 Key metrics). Use these metrics as benchmarks to drive continuous improvement in the software development and deployment process, enhancing agility, reliability, and responsiveness to changes.

### Risk Statement

Failing to measure and improve the software delivery performance can lead to inefficient development processes, reduced software quality and longer recovery times.

## LM-19: Log Sanitisation

**Group:** Logging and Monitoring

### Control Statement

Sanitise logs to protect classified and sensitive data before it is recorded in any logging system or shared to any third party.

### Control Recommendations

Identify types of classified and sensitive data that may appear in logs. When logging, consider using sanitisation techniques like masking or tokenisation. This ensures that sensitive information — such as PII, credentials, API keys, and payment details — are not stored in plaintext during log collection.

### Risk Statement

Failing to sanitise logs increases the risk of unauthorised exposure or misuse of sensitive information and other confidential data. This exposure could lead to privacy breaches, financial losses, compliance violations and damage to national reputation.

## LM-21: Detection Updates

**Group:** Logging and Monitoring

### Control Statement

Update detections for malware and indicators of compromise at least every [ insert: param, lm-21_prm_1 ] day(s).

### Control Recommendations

Implement automation to monitor the rollout of detection updates and ensure conformance.

### Risk Statement

Outdated detection rules increase the risk of undetected compromises.

### Parameters

| ID          | Type                     | Description                                             |
| ----------- | ------------------------ | ------------------------------------------------------- |
| lm-21_prm_1 | time period (days) (int) | The time period in days for detection update frequency. |