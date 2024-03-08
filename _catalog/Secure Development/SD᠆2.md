---
title: SD᠆2
permalink: /catalog/sd/sd-2/
variant: markdown
description: ""
third_nav_title: Secure Development
---
# SD-2: Default Branch Push Permissions

* **Group:** [Secure Development](/catalog/sd)

## Control Statement

Configure the code repository to prevent pushes (including force pushes) to the default branch.

## Control Recommendations

Use GitLab&#39;s protected branch and merge request settings or GitHub&#39;s branch protection settings to enforce this.

## Risk Statement

Without configuring the code repository to prevent pushes, including force pushes, to the default branch, there&#39;s an increased risk of unintentional or malicious changes, potential loss of code history, and compromised version control, impacting the integrity and reliability of the software development process.