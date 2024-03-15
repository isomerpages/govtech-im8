---
title: CS᠆5
permalink: /catalog/cs/cs-5/
variant: markdown
description: ""
third_nav_title: Container Security
---
# CS-5: Dockerfile Linting

* **Group:** [Container Security](/catalog/cs)

## Control Statement

Lint Dockerfiles before building container images.

## Control Recommendations

Use linters such as Hadolint to check the Dockerfile (or similar build file) instructions and flag any issues that contravene best practices. Ensure Dockerfile linting stage is run as part of the Continuous Integration (CI) pipelines.

## Risk Statement

Without linting Dockerfiles before building container images, there&#39;s an increased risk of syntax errors, misconfigurations, and potential security vulnerabilities, compromising the reliability and security of the resulting containerised applications.



### References


 * [IM8 Cloud ADS: 12.1/G4](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Application-Development-Security-(For-Cloud).aspx)