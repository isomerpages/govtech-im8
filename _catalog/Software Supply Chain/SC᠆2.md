---
title: SC᠆2
permalink: /catalog/sc/sc-2/
variant: markdown
description: ""
third_nav_title: Software Supply Chain
---
# SC-2: Commit Signing

* **Group:** [Software Supply Chain](/catalog/sc)

## Control Statement

Configure the code repository to reject unsigned commits.

## Control Recommendations

Use GitLab&#39;s push rules, GitHub&#39;s branch protection rules or similar code repository controls to reject unsigned commits on push.

## Risk Statement

Allowing unsigned commits in the code repository introduces the risk of unauthorised or malicious code changes, compromising the integrity and security of the software development process.