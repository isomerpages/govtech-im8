---
title: Human Resource
permalink: /control-catalog/cybersecurity/hr/
variant: markdown
description: ""
third_nav_title: Cybersecurity
---
Controls for human resources.

| Controls                                                                       |
| ------------------------------------------------------------------------------ |
| [HR-1: Security Awareness Training](#hr-1-security-awareness-training)         |
| [HR-2: Security Screening of Employees](#hr-2-security-screening-of-employees) |
| [HR-3: Employee Termination Process](#hr-3-employee-termination-process)       |

## HR-1: Security Awareness Training

**Group:** Human Resource

### Control Statement

Conduct security awareness training for all employees that operate and manage the system every [ insert: param, hr-1_prm_1 ] months.

### Control Recommendations

Develop a comprehensive security awareness training that covers:
(a) Relevant laws, regulations, codes of practice, policies, standards, guidelines and procedures
(b) Phishing and social engineering awareness
(c) Incident reporting procedures
(d) Secure handling of sensitive information

Utilise other methods such as posters, emails to provide regular and timely communication covering cybersecurity awareness messages and prevailing threats, impacts and mitigations.

### Risk Statement

Inadequate or infrequent security awareness programs increase the likelihood of successful social engineering attacks or data breaches and non-compliance due to human error or negligence.

### Parameters

| ID         | Type                       | Description                                                             |
| ---------- | -------------------------- | ----------------------------------------------------------------------- |
| hr-1_prm_1 | time period (months) (int) | The frequency at which security awareness training should be conducted. |

## HR-2: Security Screening of Employees

**Group:** Human Resource

### Control Statement

Conduct security screening of employees that operate and manage the system, during their hiring phase.

### Control Recommendations

Consider engaging reputable 3rd party screening companies to conduct background checks before extending employment offers.

### Risk Statement

Inadequate screening may lead to the hiring of individuals with criminal histories, falsified credentials or conflicts of interest. This potentially leads to insider threats, causing damage to the organisation.

## HR-3: Employee Termination Process

**Group:** Human Resource

### Control Statement

Develop and document a process for the secure termination of employees.

### Control Recommendations

The employee termination process should include:

1. Deprovisioning accounts promptly before terminating employees to reduce opportunity for damage
2. Conducting exit interviews to ensure understanding of ongoing confidentiality obligations
3. Ensuring all issued equipment is returned and inventoried
4. Secure disposal of employee&#39;s data and removal of access rights
5. Notification to relevant stakeholders about the employee&#39;s departure and changes to contact points

### Risk Statement

Inadequate employment termination processes can lead to unauthorised access to sensitive information due to either disgruntled employees retaining access or attackers exploiting non-disabled accounts.