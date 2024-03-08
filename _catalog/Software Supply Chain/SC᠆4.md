---
title: SC᠆4
permalink: /catalog/sc/sc-4/
variant: markdown
description: ""
third_nav_title: Software Supply Chain
---
# SC-4: Dependency Manifest Version Pinning

* **Group:** [Software Supply Chain](/catalog/sc)

## Control Statement

Pin direct and transitive dependency versions in the application&#39;s dependency manifest.

## Control Recommendations

Dependency manifests such as package-lock.json for npm and Pipfile.lock for pipenv allow you to pin dependency versions.

## Risk Statement

Failure to pin direct and transitive dependency versions in the application&#39;s manifest may lead to version drift, introducing compatibility issues, security vulnerabilities, and unpredictability in the software environment.



### References


 * [SLSA Build L1: Provenance exists](https://slsa.dev)
 * [IM8 Cloud ADS: 8.1/G4](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Application-Development-Security-(For-Cloud).aspx)