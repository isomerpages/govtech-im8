---
title: SD᠆7
permalink: /catalog/sd/sd-7/
variant: markdown
description: ""
third_nav_title: Secure Development
---
# SD-7: CI Environment Variable Secrets Management

* **Group:** [Secure Development](/catalog/sd)

## Control Statement

Protect environment variable secrets used in CI jobs by limiting them to protected pipelines and masking them in job logs.

## Control Recommendations

Use GitLab&#39;s CI/CD variable security settings or GitHub&#39;s encrypted secrets with the add-mask workflow command.

## Risk Statement

Failing to protect environment variable secrets in CI jobs by limiting them to protected pipelines and masking them in job logs increases the risk of unauthorized access and exposure of sensitive information.
