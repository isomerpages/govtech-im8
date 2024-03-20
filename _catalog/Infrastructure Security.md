---
title: Infrastructure Security
permalink: /catalog/is/
variant: markdown
description: ""
---
# Infrastructure Security

Controls to secure infrastructure that host applications, services, and data.

| Controls |
| ---- |
| [IS-1: Management Agents](#is-1) |
| [IS-2: Automated Patch Management](#is-2) |
| [IS-3: Restricted Administrator Privileges](#is-3) |
| [IS-4: Least Functionality](#is-4) |
| [IS-5: Host System Hardening](#is-5) |
| [IS-6: Remote Administration](#is-6) |
| [IS-7: Malware Protection](#is-7) |
| [IS-8: Endpoint Detection and Response (EDR)](#is-8) |
| [IS-9: End-of-Support (EOS) Assets](#is-9) |
| [IS-10: Synchronise time clocks](#is-10) |


<a id="is-1"></a>
## IS-1: Management Agents

### Control Statement

Install CSP management agents on hosts to remotely and securely manage their configurations.

### Control Recommendations

Most CSP compute instances preinstall management agents (e.g., AWS Systems Manager Agent, Azure Windows VM Agent) by default. If the image does not come with the preinstalled agent, install manually.

### Risk Statement

Without installing management agents on hosts, there is an increased risk of manual misconfigurations, difficulty in maintaining consistent configurations, and potential security vulnerabilities due to reduced visibility and ability to manage hosts effectively.



<a id="is-2"></a>
## IS-2: Automated Patch Management

### Control Statement

Automate patching of operating systems and applications.

### Control Recommendations

Apply patch baselines via the CSP node management service, unless the patch management process is automated as part of the build and deploy phase.

### Risk Statement

Failure to automate patching of operating systems and applications increases the risk of delayed or missed security updates, leaving systems vulnerable to known exploits and potential security breaches, compromising the overall security of the environment.



<a id="is-3"></a>
## IS-3: Restricted Administrator Privileges

### Control Statement

Restrict administrator privileges by disabling remote login for the root/administrator user and removing sudo/administrators group access for other users.

### Control Recommendations

Further reduce the attack surface by running common services such as the web server or database without root/administrator/system privileges.

### Risk Statement

Without restricting administrator privileges, there is an increased risk of unauthorised access, privilege escalation, and potential security breaches, compromising the integrity and security of the system.



<a id="is-4"></a>
## IS-4: Least Functionality

### Control Statement

Disable or remove unnecessary functions, system ports, protocols, software, and services on the host.

### Control Recommendations

Follow the principle of least functionality to configure the host to carry out only its intended purpose. CSP node management services can provide an inventory of software and services (e.g., AWS Systems Manager Inventory). Vulnerability assessment scanners (e.g., AWS Inspector) can also identify software vulnerabilities and network exposure.

### Risk Statement

Failure to disable or remove unnecessary functions, system ports, protocols, software, and services on the host increases the attack surface, potential vulnerabilities, and the risk of exploitation, compromising the overall security and performance of the system.



<a id="is-5"></a>
## IS-5: Host System Hardening

### Control Statement

Harden the host configuration in accordance with industry standards.

### Control Recommendations

Select the appropriate benchmark for the host such as from the [NIST National Checklist Program](https://ncp.nist.gov/repository) or [CIS Benchmarks](https://www.cisecurity.org/cis-benchmarks). Automate the configuration process or use hardened images instead of manually configuring.

### Risk Statement

Without hardening the operating system configuration according to industry standards, there's an increased risk of security vulnerabilities, unauthorised access, and potential exploitation, compromising the overall security posture and resilience of the operating system.



<a id="is-6"></a>
## IS-6: Remote Administration

### Control Statement

Use remote administration tools instead of direct SSH or RDP.

### Control Recommendations

In production environments, use remote administration (e.g., AWS Systems Manager Session Manager, AWS Systems Manager Fleet Manager, GCC Privileged Identity Management) only for break glass scenarios where remote monitoring and automation is not available. Document and remediate gaps in monitoring and automation to minimise the need for remote administration. If SSH is still required and remote administration tools are not available, only use it within a private non-production environment such as an encrypted tunnel and authenticate with short-lived certificates.

### Risk Statement

Using remote administration tools enhances security by providing controlled and audited access, reducing the risk of unauthorised activities, and improving overall management of privileged identities.



<a id="is-7"></a>
## IS-7: Malware Protection

### Control Statement

Detect and quarantine malware on hosts with anti-malware tools.

### Control Recommendations

Configure anti-malware tools for all compute hosts (e.g. AWS Guardduty Malware Protection, Azure Antimalware, Trend Micro CloudOne). These tools should be kept up-to-date with the latest malware signatures. Regular scans should be scheduled to detect and quarantine potential threats.

### Risk Statement

Without malware protection, there's an increased risk of undetected malicious activities, potential data breaches, and compromise of host systems, highlighting the importance of proactive measures to ensure the security and integrity of the environment.



<a id="is-8"></a>
## IS-8: Endpoint Detection and Response (EDR)

### Control Statement

Monitor security threats on hosts with an EDR tool.

### Control Recommendations

Implement EDR tools for all compute hosts. Security incident response should be planned and documented for the tool. EDR tools with built-in malware protection should be favoured to reduce additional agents.

### Risk Statement

Failure to monitor security threats on hosts with an Endpoint Detection and Response (EDR) tool increases the risk of undetected advanced threats, compromises in host security, and delayed response to potential security incidents, highlighting the need for continuous monitoring and proactive threat detection.



<a id="is-9"></a>
## IS-9: End-of-Support (EOS) Assets

### Control Statement

Ensure deployed {{ insert: param, is-9_prm_1 }} assets have not reached end-of-support (EOS). Use of EOS assets will require risk acceptance by approved authority.

### Control Recommendations

Identify, track and replace EOS assets in a timely manner. Regularly review assets to identify upcoming EOS timeframe and replace them ahead of EOS date.

### Risk Statement

EOS assets can introduce security vulnerabilities as the assets are no longer provided with security fixes.



<a id="is-10"></a>
## IS-10: Synchronise time clocks

### Control Statement

Synchronise internal clocks to a common reference time source.

### Control Recommendations

Use common time source such as Network Time Protocol.

### Risk Statement

Inconsistent time clocks will impede incident investigations.




