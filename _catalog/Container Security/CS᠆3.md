---
title: CS᠆3
permalink: /catalog/cs/cs-3/
variant: markdown
description: ""
third_nav_title: Container Security
---
# CS-3: Runtime Container Secrets

* **Group:** [Container Security](/catalog/cs)

## Control Statement

Provide secrets and sensitive data to the container at runtime instead of image build time.

## Control Recommendations

Ensure no secrets (e.g., TLS certificate keys, cloud provider credentials, SSH private keys, database passwords) are embedded in the container image by using dedicated features like Docker secrets or `podman-secret-create`.

## Risk Statement

Providing secrets and sensitive data to the container at runtime instead of image build time reduces the risk of exposing sensitive information in the image and enhances security by ensuring that secrets are managed and updated independently, minimising the risk of unauthorised access or data compromise.



### References


 * [IM8 Cloud ADS: 2.2/S4](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Application-Development-Security-(For-Cloud).aspx)