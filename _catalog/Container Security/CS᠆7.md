---
title: CS᠆7
permalink: /catalog/cs/cs-7/
variant: markdown
description: ""
third_nav_title: Container Security
---
# CS-7: CI/CD Container Image Scanning

* **Group:** [Container Security](/catalog/cs)

## Control Statement

Set up a container image scanning job in the CI/CD pipeline that runs on each container image build.

## Control Recommendations

Container image scanning tools (e.g., Trivy, Grype) scan the contents of a container image or filesystem for known vulnerabilities.

## Risk Statement

Without setting up a container image scanning job in the CI/CD pipeline, there&#39;s an increased risk of deploying vulnerable images, as potential security vulnerabilities may go undetected, compromising the security and integrity of the containerised applications during deployment.



### References


 * [IM8 Cloud ADS: 12.3/G2c](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Application-Development-Security-(For-Cloud).aspx)