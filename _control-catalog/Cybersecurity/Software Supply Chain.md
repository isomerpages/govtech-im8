---
title: Software Supply Chain
permalink: /control-catalog/cybersecurity/sc/
variant: markdown
description: ""
third_nav_title: Cybersecurity
---
Controls to prevent tampering and improve the integrity of the software supply chain.

| Controls                                                                                           |
| -------------------------------------------------------------------------------------------------- |
| [SC-1: Code Repository](#sc-1-code-repository)                                                     |
| [SC-2: Commit Signing](#sc-2-commit-signing)                                                       |
| [SC-3: Peer Review](#sc-3-peer-review)                                                             |
| [SC-4: Dependency Manifest Version Pinning](#sc-4-dependency-manifest-version-pinning)             |
| [SC-5: Build and Release Process](#sc-5-build-and-release-process)                                 |
| [SC-6: Dependency Installation during Deployment](#sc-6-dependency-installation-during-deployment) |
| [SC-7: Software Artefact Signing](#sc-7-software-artefact-signing)                                 |
| [SC-8: Software Artefact Signature Verification](#sc-8-software-artefact-signature-verification)   |
| [SC-9: Internal Code Collaboration and Sharing](#sc-9-internal-code-collaboration-and-sharing)     |

## SC-1: Code Repository

**Group:** Software Supply Chain

### Control Statement

Manage the codebase in a central code repository with version control.

### Control Recommendations

Use common internal platforms that provide Git repository services.

### Risk Statement

Absence of centralised code repository and version control increases the risk of code inconsistencies, loss of code history, and difficulties in collaboration, potentially leading to errors and security vulnerabilities.

## SC-2: Commit Signing

**Group:** Software Supply Chain

### Control Statement

Configure the code repository to reject unsigned commits.

### Control Recommendations

Use GitLab&#39;s push rules, GitHub&#39;s branch protection rules or similar code repository controls to reject unsigned commits on push.

### Risk Statement

Allowing unsigned commits in the code repository introduces the risk of unauthorised or malicious code changes, compromising the integrity and security of the software development process.

## SC-3: Peer Review

**Group:** Software Supply Chain

### Control Statement

Require peer review and approval by a designated reviewer before merging into the default branch.

### Control Recommendations

Use GitLab&#39;s protected branch and merge request settings, GitHub&#39;s branch protection settings or similar code repository controls to enforce this.

### Risk Statement

Without peer review and approval before merging, there is an increased risk of introducing undetected coding errors, security vulnerabilities, and maintaining codebase consistency may become challenging.

## SC-4: Dependency Manifest Version Pinning

**Group:** Software Supply Chain

### Control Statement

Pin direct and transitive dependency versions in the application&#39;s dependency manifest.

### Control Recommendations

Dependency manifests such as package-lock.json for npm and Pipfile.lock for pipenv allow you to pin dependency versions.

### Risk Statement

Failure to pin direct and transitive dependency versions in the application&#39;s manifest may lead to version drift, introducing compatibility issues, security vulnerabilities, and unpredictability in the software environment.

## SC-5: Build and Release Process

**Group:** Software Supply Chain

### Control Statement

Use a consistent build and release process that generates a record of how the release artefact was built and deployed.

### Control Recommendations

Consider automated build and deploy tools such as CI/CD Pipelines, Infrastructure as Code (IaC) and other scripts, which allow for signing and validation of build artefacts. If automation is not possible, develop and implement release management processes.

### Risk Statement

Inconsistent and unmanaged releases may lead to configuration drift, increased likelihood of errors, and unapproved changes to releases.

## SC-6: Dependency Installation during Deployment

**Group:** Software Supply Chain

### Control Statement

Only install pinned versions in the manifest when installing dependencies during deployment.

### Control Recommendations

Use package manager commands such as npm ci for npm and pipenv sync for pipenv that ensure only versions specified in the manifest are installed rather than the latest version.

### Risk Statement

Failure to install only pinned versions of dependencies during deployment increases the risk of introducing unforeseen changes, compatibility issues, and potential security vulnerabilities into the deployed environment.

## SC-7: Software Artefact Signing

**Group:** Software Supply Chain

### Control Statement

Sign software artefacts such as code and container images using a trusted source during build.

### Control Recommendations

Use tools or services like Cosign or AWS Signer to sign and verify code.

### Risk Statement

Unsigned code and container images pose a risk of tampering, impersonation, and the injection of malicious code during the build process, compromising the integrity and security of the deployed software.

## SC-8: Software Artefact Signature Verification

**Group:** Software Supply Chain

### Control Statement

Verify the signatures of code and artefacts before deployment or runtime.

### Control Recommendations

Implement a signature verification step such as a pipeline stage or Kubernetes Admission Controller.

### Risk Statement

Without verifying the signatures of code and artefacts before deployment or runtime, there&#39;s an increased risk of deploying tampered or malicious software, compromising the integrity and security of the system.

## SC-9: Internal Code Collaboration and Sharing

**Group:** Software Supply Chain

### Control Statement

Share source code internally to enhance code quality, accelerate innovation, and improve problem-solving efficiency.

### Control Recommendations

Adopt InnerSource practices for internal collaboration, utilising Git platforms to manage and share code repositories internally. Source code should be evaluated for suitability for InnerSourcing, such as the use of confidential algorithms or embedded sensitive data. The InnerSource guidelines published in the Singapore Government Developer Portal provide a useful framework for code sharing.

### Risk Statement

Restricting code repositories to closed source can result in duplicated efforts, hinder collaborative learning, and lead to missed bugs or vulnerabilities.