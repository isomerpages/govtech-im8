---
title: CS᠆6
permalink: /catalog/cs/cs-6/
variant: markdown
description: ""
third_nav_title: Container Security
---
# CS-6: Read-Only Container Root Filesystem

* **Group:** [Container Security](/catalog/cs)

## Control Statement

Configure the container filesystem to be read-only.

## Control Recommendations

Use security policies (e.g., `readonlyRootFilesystem` for Kubernetes) to prevent any direct writes to the container&#39;s root filesystem during runtime and ensure immutable infrastructure. Do not directly apply patches or alter running containers as the containers are ephemeral and patches will disappear upon redeploy. Apply patches by rebuilding and redeploying container images.

## Risk Statement

Failure to configure the container filesystem as read-only increases the risk of unauthorised modifications, potential tampering, and compromise of containerised applications, as attackers may exploit write access to alter the container&#39;s state and integrity.