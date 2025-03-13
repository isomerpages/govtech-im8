---
title: Software Supply Chain
permalink: /control-catalog/sc/
variant: markdown
description: ""
third_nav_title: Cybersecurity
---
Controls to prevent tampering and improve the integrity of the software supply chain.

| Controls |
| ---- |
| [SC-1: Code Repository](#sc-1) |
| [SC-2: Commit Signing](#sc-2) |
| [SC-3: Peer Review](#sc-3) |
| [SC-4: Dependency Manifest Version Pinning](#sc-4) |
| [SC-5: Build and Release Process](#sc-5) |
| [SC-6: Dependency Installation during Deployment](#sc-6) |
| [SC-7: Software Artefact Signing](#sc-7) |
| [SC-8: Software Artefact Signature Verification](#sc-8) |
| [SC-9: Internal Code Collaboration and Sharing](#sc-9) |


<a id="sc-1"></a>
## SC-1: Code Repository

### Control Statement

Manage the codebase in a central code repository with version control.

### Control Recommendations

Use common platforms such as SHIP-HATS 2.0 GitLab or equivalents.

### Risk Statement

Absence of centralised code repository and version control increases the risk of code inconsistencies, loss of code history, and difficulties in collaboration, potentially leading to errors and security vulnerabilities.



<a id="sc-2"></a>
## SC-2: Commit Signing

### Control Statement

Configure the code repository to reject unsigned commits.

### Control Recommendations

Use GitLab's push rules, GitHub's branch protection rules or similar code repository controls to reject unsigned commits on push.

### Risk Statement

Allowing unsigned commits in the code repository introduces the risk of unauthorised or malicious code changes, compromising the integrity and security of the software development process.



<a id="sc-3"></a>
## SC-3: Peer Review

### Control Statement

Require peer review and approval by a designated reviewer before merging into the default branch.

### Control Recommendations

Use GitLab's protected branch and merge request settings, GitHub's branch protection settings or similar code repository controls to enforce this.

### Risk Statement

Without peer review and approval before merging, there is an increased risk of introducing undetected coding errors, security vulnerabilities, and maintaining codebase consistency may become challenging.



<a id="sc-4"></a>
## SC-4: Dependency Manifest Version Pinning

### Control Statement

Pin direct and transitive dependency versions in the application's dependency manifest.

### Control Recommendations

Dependency manifests such as package-lock.json for npm and Pipfile.lock for pipenv allow you to pin dependency versions.

### Risk Statement

Failure to pin direct and transitive dependency versions in the application's manifest may lead to version drift, introducing compatibility issues, security vulnerabilities, and unpredictability in the software environment.



<a id="sc-5"></a>
## SC-5: Build and Release Process

### Control Statement

Use a consistent build and release process that generates a record of how the release artefact was built and deployed.

### Control Recommendations

Consider automated build and deploy tools such as CI/CD Pipelines, Infrastructure as Code (IaC) and other scripts, which allow for signing and validation of build artefacts. If automation is not possible, develop and implement release management processes.

### Risk Statement

Inconsistent and unmanaged releases may lead to configuration drift, increased likelihood of errors, and unapproved changes to releases.



<a id="sc-6"></a>
## SC-6: Dependency Installation during Deployment

### Control Statement

Only install pinned versions in the manifest when installing dependencies during deployment.

### Control Recommendations

Use package manager commands such as npm ci for npm and pipenv sync for pipenv that ensure only versions specified in the manifest are installed rather than the latest version.

### Risk Statement

Failure to install only pinned versions of dependencies during deployment increases the risk of introducing unforeseen changes, compatibility issues, and potential security vulnerabilities into the deployed environment.



<a id="sc-7"></a>
## SC-7: Software Artefact Signing

### Control Statement

Sign software artefacts such as code and container images using a trusted source during build.

### Control Recommendations

Use tools or services like Cosign or AWS Signer to sign and verify code.

### Risk Statement

Unsigned code and container images pose a risk of tampering, impersonation, and the injection of malicious code during the build process, compromising the integrity and security of the deployed software.



<a id="sc-8"></a>
## SC-8: Software Artefact Signature Verification

### Control Statement

Verify the signatures of code and artefacts before deployment or runtime.

### Control Recommendations

Implement a signature verification step such as a pipeline stage or Kubernetes Admission Controller.

### Risk Statement

Without verifying the signatures of code and artefacts before deployment or runtime, there's an increased risk of deploying tampered or malicious software, compromising the integrity and security of the system.



<a id="sc-9"></a>
## SC-9: Internal Code Collaboration and Sharing

### Control Statement

Share source code within Government to enhance code quality, accelerate innovation, and improve problem-solving efficiency.

### Control Recommendations

Adopt Innersource practices for internal collaboration, utilizing platforms like SHIP-HATS GitLab to manage and share code repositories in Government. Source code should be evaluated for suitability for innersourcing, such as the use of confidential algorithms or embedded sensitive data. The Innersource guidelines published in Developers Portal provide a useful framework for code sharing.

### Risk Statement

Restricting code repositories to closed source can result in duplicated efforts, hinder collaborative learning, and lead to missed bugs or vulnerabilities.