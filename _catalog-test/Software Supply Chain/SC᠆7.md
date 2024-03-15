---
title: SC᠆7
permalink: /catalog/sc/sc-7/
variant: markdown
description: ""
third_nav_title: Software Supply Chain
---
# SC-7: Dependency Installation during Deployment

* **Group:** [Software Supply Chain](/catalog/sc)

## Control Statement

When installing dependencies during deployment, only install pinned versions in the manifest.

## Control Recommendations

Use package manager commands such as npm ci for npm and pipenv sync for pipenv that ensure only versions specified in the manifest are installed rather than the latest version.

## Risk Statement

Failure to install only pinned versions of dependencies during deployment increases the risk of introducing unforeseen changes, compatibility issues, and potential security vulnerabilities into the deployed environment.



### References


 * [SLSA Build L1: Provenance exists](https://slsa.dev)