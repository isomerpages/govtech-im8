---
title: CS᠆1
permalink: /catalog/cs/cs-1/
variant: markdown
description: ""
third_nav_title: Container Security
---
# CS-1: Unique Base Container Image Tags

* **Group:** [Container Security](/catalog/cs)

## Control Statement

Use unique base container image tags instead of rolling tags.

## Control Recommendations

Avoid the `latest` tag or other common rolling tags for base images to minimise unintended changes during subsequent builds using the same instruction. A digest SHA can provide a unique identifier for the image if no tag is assigned during build time.

## Risk Statement

Using unique base container image tags instead of rolling tags reduces the risk of unintentional updates, inconsistencies, and potential security vulnerabilities in containerised environments, ensuring a more stable and secure deployment process.



### References


 * [SLSA Build L1: Provenance exists](https://slsa.dev)
 * [IM8 Cloud ADS: 12.1/G3](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Application-Development-Security-(For-Cloud).aspx)