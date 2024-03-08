---
title: CS᠆4
permalink: /catalog/cs/cs-4/
variant: markdown
description: ""
third_nav_title: Container Security
---
# CS-4: Non-Privileged Container User

* **Group:** [Container Security](/catalog/cs)

## Control Statement

Create a non-root user and set it as the default user in the container image build instructions.

## Control Recommendations

Ensure the non-root user has the minimal set of permissions required to run the container.

## Risk Statement

Failure to create a non-root user and set it as the default user in container image build instructions increases the risk of security vulnerabilities, as running containers with root privileges may lead to potential exploitation and compromise of the host system.



### References


 * [IM8 Cloud ADS: 12.2/S2](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Application-Development-Security-(For-Cloud).aspx)