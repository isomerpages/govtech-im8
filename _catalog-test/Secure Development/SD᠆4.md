---
title: SD᠆4
permalink: /catalog/sd/sd-4/
variant: markdown
description: ""
third_nav_title: Secure Development
---
# SD-4: Static Analysis

* **Group:** [Secure Development](/catalog/sd)

## Control Statement

Set up a static analysis job in the development CI/CD pipeline that runs on each merge request, and remediate or risk accept true positive vulnerability findings before merging into the production branch.

## Control Recommendations

Static analysis tools (such as SAST or IaC security scanners) check source code for common vulnerabilities and misconfigurations. By running static analysis tools earlier in the DevSecOps cycle, vulnerabilities can be detected and prevented from being deployed to production.

## Risk Statement

Without setting up static analysis in the CI/CD pipeline for each merge request and addressing true positive vulnerability findings, there is an increased risk of deploying insecure code to the production branch, potentially leading to security breaches and compromise of the overall system.



### References


 * [IM8 Cloud ADS: 6.4/S2](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Application-Development-Security-(For-Cloud).aspx)
 * [IM8 On-Premise ADS (Non-S): 4.1/S1](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/On-Premise/Topics/Application-Development-Security-(For-Non-S).aspx)