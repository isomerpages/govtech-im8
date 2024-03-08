---
title: CS᠆8
permalink: /catalog/cs/cs-8/
variant: markdown
description: ""
third_nav_title: Container Security
---
# CS-8: Container Registry Image Scanning

* **Group:** [Container Security](/catalog/cs)

## Control Statement

Scan container images in container registries (e.g., Amazon ECR) for known vulnerabilities.

## Control Recommendations

Configure container registries to scan images automatically and continuously, as well as enable scanning of image on push. Block deployment of container images with HIGH CVE being detected during scan (e.g., using Amazon ECR with Security Hub).

## Risk Statement

Failure to scan container images in container registries for known vulnerabilities increases the risk of deploying insecure images, potentially exposing the infrastructure to known exploits and compromising the security of the containerised applications during runtime.



### References


 * [IM8 Cloud ADS: 12.3/G2b](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Application-Development-Security-(For-Cloud).aspx)
 * [IM8 Cloud ADS: 12.3/G2c](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Application-Development-Security-(For-Cloud).aspx)