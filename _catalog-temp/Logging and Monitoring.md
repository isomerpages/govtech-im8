---
title: Logging and Monitoring
permalink: /control-catalog/lm/
variant: markdown
description: ""
---
Controls to support detection and response to security and operations incidents.

| Controls |
| ---- |
| [LM-1: Separate Log Storage](#lm-1) |
| [LM-2: Tamper-Resistant Log Storage](#lm-2) |
| [LM-3: Network Flow Logging](#lm-3) |
| [LM-4: Cloud Management Event Logging](#lm-4) |
| [LM-5: Database Logging](#lm-5) |
| [LM-6: Access Logging](#lm-6) |
| [LM-7: Security Event Logging](#lm-7) |
| [LM-8: Security Log Retention](#lm-8) |
| [LM-9: Security Monitoring and Alerting](#lm-9) |
| [LM-10: Resource Usage Monitoring and Alerting](#lm-10) |
| [LM-11: Service Level Monitoring and Alerting](#lm-11) |
| [LM-12: Government Cyber Security Operations Centre (GCSOC)](#lm-12) |
| [LM-13: Database Activity Monitoring](#lm-13) |
| [LM-14: Web defacement monitoring and response](#lm-14) |
| [LM-15: Structured Log Formatting](#lm-15) |
| [LM-16: Key Signals Monitoring](#lm-16) |
| [LM-17: Software delivery performance monitoring](#lm-17) |


<a id="lm-1"></a>
## LM-1: Separate Log Storage

### Control Statement

Store logs in a repository that is part of a different system or system component than the system or component being audited.

### Control Recommendations

Send logs to the separate storage as soon as possible after the logged event. For cloud audit logs, store them in a separate service or account (such as AWS Organisation Cloudtrail in GCC). Sending logs to the Government Cyber Security Operations Centre (GCSOC) or the central Government Commercial Cloud (GCC) log bucket can also satisfy this control.

### Risk Statement

Storing logs in a repository separate from the audited system or component enhances security by reducing the risk of tampering, unauthorised access, and manipulation of audit trails, ensuring the integrity and reliability of log data for forensic analysis and compliance purposes.



<a id="lm-2"></a>
## LM-2: Tamper-Resistant Log Storage

### Control Statement

Protect logs from unauthorised access, modification, and deletion.

### Control Recommendations

Apply access control policies to logs based on the principle of least privilege. As far as possible, only read access should be granted. Logs sent to GCC Central Logs are tamper-resistant.

### Risk Statement

Without protection measures, logs are susceptible to unauthorised access, modification, or deletion, leading to the risk of tampering, loss of crucial audit information, and compromised forensic analysis capabilities during security incidents.



<a id="lm-3"></a>
## LM-3: Network Flow Logging

### Control Statement

Log network traffic going to and from network interfaces.

### Control Recommendations

Enable VPC Flow Logs for AWS or its equivalents.

### Risk Statement

Failing to log network traffic going to and from network interfaces increases the risk of overlooking suspicious activities, potential security breaches, and the inability to trace and investigate network-related incidents effectively.



<a id="lm-4"></a>
## LM-4: Cloud Management Event Logging

### Control Statement

Log management and audit events on cloud resources.

### Control Recommendations

Configure CloudTrail for AWS or its equivalents to log management and audit events such as changes to IAM policies and resources.

### Risk Statement

Neglecting to log and manage audit events on cloud resources increases the risk of undetected security incidents, compromises visibility into system activities, and hinders effective forensic analysis and compliance monitoring in cloud environments.



<a id="lm-5"></a>
## LM-5: Database Logging

### Control Statement

Log database audit events.

### Control Recommendations

Enable RDS logging for AWS or its equivalents.

### Risk Statement

Neglecting to log database audit events raises the risk of overlooking unauthorised activities, compromises in data security, and hinders the ability to track and investigate security incidents or compliance violations within the database environment.



<a id="lm-6"></a>
## LM-6: Access Logging

### Control Statement

Log access requests sent to web application firewalls, load balancers, proxies or web servers.

### Control Recommendations

Enable AWS WAF logging, Application Load Balancer logging, API Gateways, or their equivalents.

### Risk Statement

Failure to log access requests sent to web application firewalls, load balancers, proxies, or web servers increases the risk of overlooking potential security threats, unauthorised access attempts, and compromises visibility into the traffic that could lead to security incidents.



<a id="lm-7"></a>
## LM-7: Security Event Logging

### Control Statement

Log security events on hosts and other cloud resources.

### Control Recommendations

Security events include operating system security events, authentication and audit logs, and endpoint detection and response alerts.

### Risk Statement

Neglecting to log security events on hosts and other cloud resources increases the risk of undetected security incidents, compromises incident response capabilities, and hinders forensic analysis, limiting the ability to identify and mitigate potential threats.



<a id="lm-8"></a>
## LM-8: Security Log Retention

### Control Statement

Retain security logs for at least [lm-8_prm_1] day(s).

### Control Recommendations

Security logs include network flow logs, cloud management logs, access logs, database logs and host logs. Retain non-security logs (e.g. application, operations and performance logs) as long as needed for incident resolution and debugging. Consider log lifecycle management automation, such as Amazon S3 Lifecycle configurations.

### Risk Statement

Failure to retain security logs increases the risk of losing crucial historical data, hindering investigations, compliance audits, and the ability to identify and respond to security incidents that occurred beyond a limited timeframe.



#### Parameters

| ID | Type | Description |
| -- | ---- | ----------- |
| lm-8_prm_1 | time period (days) | The time period in days of log retention. |

<a id="lm-9"></a>
## LM-9: Security Monitoring and Alerting

### Control Statement

Configure security monitoring to identify potential security violations or breaches and send automated alerts.

### Control Recommendations

Enable Amazon GuardDuty, Microsoft Azure Security Center, or their equivalents.

### Risk Statement

Without configuring security monitoring to identify potential security violations or breaches and send automated alerts, there's an increased risk of delayed or unnoticed security incidents, hindering timely response and mitigation efforts to protect the system from further compromise.



<a id="lm-10"></a>
## LM-10: Resource Usage Monitoring and Alerting

### Control Statement

Configure resource usage monitoring to identify abnormal usage and send automated alerts.

### Control Recommendations

Configure Amazon CloudWatch alarms, Azure Monitor alerts, or their equivalents to identify abnormal usage such as spike in usage, access to resources during expected hours, and excessive charges.

### Risk Statement

Lack of resource usage monitoring with automated alerts increases the risk of overlooking abnormal usage patterns, potential resource abuse, and compromises in system performance, hindering the ability to proactively address issues and prevent service disruptions.



<a id="lm-11"></a>
## LM-11: Service Level Monitoring and Alerting

### Control Statement

Monitor, maintain and alert on service level objectives (SLOs) and indicators (SLIs) to ensure consistent service performance, availability and reliability.

### Control Recommendations

Implement a comprehensive monitoring system that tracks key SLIs and evaluates them against defined SLOs. This will help in identifying potential service level breaches early and take proactive measures to maintain service quality. Examples include Cloudwatch metrics and alerts, Amazon Route 53 health checks, Azure Monitor Application Insights, or their equivalents.

### Risk Statement

Without effective service level monitoring to identify potential application or service degradation and send automated alerts, there is a risk of failing to meet service availability standards, which could result in user dissatisfaction and reduced reliability.



<a id="lm-12"></a>
## LM-12: Government Cyber Security Operations Centre (GCSOC)

### Control Statement

Subscribe and send security logs to GCSOC for central threat monitoring.

### Control Recommendations

Logs that are sent to GCC Central Logs are forwarded to GCSOC.

### Risk Statement

Failure to subscribe and send security logs to the Government Cyber Security Operations Centre (GCSOC) impedes central threat monitoring, increasing the risk of delayed or unnoticed security incidents, hindering effective response, and compromising the overall cybersecurity posture.



<a id="lm-13"></a>
## LM-13: Database Activity Monitoring

### Control Statement

Monitor database activities for anomalous behaviour.

### Control Recommendations

Config RDS Activity Streams and logs with alerts or Database Activity Monitoring (DAM) tools to detect unusual authentication, reads or writes to a database.

### Risk Statement

Neglecting to monitor database activities for anomalous behaviour increases the risk of undetected security threats, unauthorised access, and compromises in data integrity, hindering the ability to identify and respond to potential database-related incidents.



<a id="lm-14"></a>
## LM-14: Web defacement monitoring and response

### Control Statement

Plan for and implement measures to recover against web defacements.

### Control Recommendations

Use GCSOC’s services for centralised monitoring for web defacements attacks on internet-facing systems.

### Risk Statement

Leverage on GCSOC services to reduce duplication of effort and reduce inconsistent implementation.



<a id="lm-15"></a>
## LM-15: Structured Log Formatting

### Control Statement

Publish logs in a consistent, structured format that aligns with industry standards for easy parsing and analysis.

### Control Recommendations

For security logs, implement or transform to OCSF (Open Cybersecurity Schema Framework), ECS (Elastic Common Schema) or similar schemas to standardize log formats for better threat detection and analysis. For operational logs, adopt OpenTelemetry or structured JSON formats to facilitate clear, structured, and efficient log analysis for system performance and diagnostics. Consistent log formatting aids in automated parsing and helps in integrating logs from various sources.

### Risk Statement

Inconsistent or unstructured log formatting can lead to difficulties in log analysis and monitoring, potentially resulting in missed critical events or delayed response to system anomalies.



<a id="lm-16"></a>
## LM-16: Key Signals Monitoring

### Control Statement

Monitor key user-facing signals to maintain robust service health and performance.

### Control Recommendations

Implement monitoring of key signals such as latency, traffic, errors, and saturation (the 4 Golden Signals). Regularly track and analyse these indicators for proactive issue detection and resolution. Use this data to identify trends and areas for system improvement, ensuring continuous enhancement in service quality and reliability.

### Risk Statement

Inadequate monitoring of key user-facing signals such as latency, traffic, errors, and saturation can lead to suboptimal service performance, adversely impacting user experience, system efficiency, and increasing the likelihood of system failures. This oversight can significantly detract from service reliability and user satisfaction.



<a id="lm-17"></a>
## LM-17: Software delivery performance monitoring

### Control Statement

Measure and analyse software delivery performance to optimise development velocity and operational efficiency.

### Control Recommendations

Implement tools and processes to track Deployment Frequency, Lead Time for Changes, Change Failure Rate, and Time to Restore Service (the DORA 4 Key metrics). Use these metrics as benchmarks to drive continuous improvement in the software development and deployment process, enhancing agility, reliability, and responsiveness to changes.

### Risk Statement

Failing to measure and improve the software delivery performance can lead to inefficient development processes, reduced software quality and longer recovery times.