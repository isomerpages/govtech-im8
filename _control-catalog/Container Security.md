---
title: Container Security
permalink: /control-catalog/cs/
variant: markdown
description: ""
---
Controls to secure container building, distribution, and deployment.

| Controls |
| ---- |
| [CS-1: Unique Base Container Image Tags](#cs-1) |
| [CS-2: Minimal Base Container Images](#cs-2) |
| [CS-3: Runtime Container Secrets](#cs-3) |
| [CS-4: Non-Privileged Container User](#cs-4) |
| [CS-5: Dockerfile Linting](#cs-5) |
| [CS-6: Read-Only Container Root Filesystem](#cs-6) |
| [CS-7: Container Image Scanning](#cs-7) |
| [CS-8: Private Container Image Registries](#cs-8) |
| [CS-9: Container Orchestrator API Access Control](#cs-9) |
| [CS-10: Container Workload Segmentation](#cs-10) |
| [CS-11: Container Runtime Security](#cs-11) |


<a id="cs-1"></a>
## CS-1: Unique Base Container Image Tags

### Control Statement

Use unique base container image tags instead of rolling tags.

### Control Recommendations

Avoid the `latest` tag or other common rolling tags for base images to minimise unintended changes during subsequent builds using the same instruction. A digest SHA can provide a unique identifier for the image if no tag is assigned during build time.

### Risk Statement

Using unique base container image tags instead of rolling tags reduces the risk of unintentional updates, inconsistencies, and potential security vulnerabilities in containerised environments, ensuring a more stable and secure deployment process.



<a id="cs-2"></a>
## CS-2: Minimal Base Container Images

### Control Statement

Build container images with minimal base images.

### Control Recommendations

Use minimal container images such as alpine, scratch, wolfi, and distroless images as the base image to reduce attack surface.

### Risk Statement

Building container images with minimal base images reduces the attack surface, potential vulnerabilities, and resource overhead, minimising the risk of security exploits and enhancing the overall security posture of the containerised environment.



<a id="cs-3"></a>
## CS-3: Runtime Container Secrets

### Control Statement

Provide secrets and sensitive data to the container at runtime instead of image build time.

### Control Recommendations

Ensure no secrets (e.g., TLS certificate keys, cloud provider credentials, SSH private keys, database passwords) are embedded in the container image by using dedicated features like Docker secrets or `podman-secret-create`.

### Risk Statement

Providing secrets and sensitive data to the container at runtime instead of image build time reduces the risk of exposing sensitive information in the image and enhances security by ensuring that secrets are managed and updated independently, minimising the risk of unauthorised access or data compromise.



<a id="cs-4"></a>
## CS-4: Non-Privileged Container User

### Control Statement

Create a non-root user and set it as the default user in the container image build instructions.

### Control Recommendations

Ensure the non-root user has the minimal set of permissions required to run the container.

### Risk Statement

Failure to create a non-root user and set it as the default user in container image build instructions increases the risk of security vulnerabilities, as running containers with root privileges may lead to potential exploitation and compromise of the host system.



<a id="cs-5"></a>
## CS-5: Dockerfile Linting

### Control Statement

Lint Dockerfiles before building container images.

### Control Recommendations

Use linters such as Hadolint to check the Dockerfile (or similar build file) instructions and flag any issues that contravene best practices. Ensure Dockerfile linting stage is run as part of the Continuous Integration (CI) pipelines.

### Risk Statement

Without linting Dockerfiles before building container images, there's an increased risk of syntax errors, misconfigurations, and potential security vulnerabilities, compromising the reliability and security of the resulting containerised applications.



<a id="cs-6"></a>
## CS-6: Read-Only Container Root Filesystem

### Control Statement

Configure the container filesystem to be read-only.

### Control Recommendations

Use security policies (e.g., `readonlyRootFilesystem` for Kubernetes) to prevent any direct writes to the container's root filesystem during runtime and ensure immutable infrastructure. Do not directly apply patches or alter running containers as the containers are ephemeral and patches will disappear upon redeploy. Apply patches by rebuilding and redeploying container images.

### Risk Statement

Failure to configure the container filesystem as read-only increases the risk of unauthorised modifications, potential tampering, and compromise of containerised applications, as attackers may exploit write access to alter the container's state and integrity.



<a id="cs-7"></a>
## CS-7: Container Image Scanning

### Control Statement

Scan container images in the [cs-7_prm_1] for known vulnerabilities.

### Control Recommendations

Container image scanning tools (e.g., Amazon Inspector, Trivy, Grype) scan the contents of a container image for known vulnerabilities. Configure scans to run automatically and continuously, as well as enable scanning of image on push. Block deployment of container images with HIGH CVE being detected during scan (e.g., using Amazon ECR with Security Hub).

### Risk Statement

Failure to scan container images increases the risk of deploying insecure images, potentially exposing the infrastructure to known exploits and compromising the security of the containerised applications during runtime.



#### Parameters

| ID | Type | Description |
| -- | ---- | ----------- |
| cs-7_prm_1 | location | The location where container image scanning occurs. |

<a id="cs-8"></a>
## CS-8: Private Container Image Registries

### Control Statement

Host built container images in private container registries.

### Control Recommendations

Use only private container registries (e.g., Amazon ECR private registry) to host container images built by the organisation as images may contain proprietary code or sensitive information.

### Risk Statement

Hosting built container images in private registries enhances security by reducing the exposure of sensitive images, minimising the risk of unauthorised access, and maintaining control over image distribution, ensuring a more secure and controlled container deployment process.



<a id="cs-9"></a>
## CS-9: Container Orchestrator API Access Control

### Control Statement

Disable public access to Container Orchestrator API endpoints from the internet.

### Control Recommendations

Restrict access to the Container Orchestrator API endpoints (such as the Kubernetes API Server) to specific address ranges or use CSP provided features such as disabling Endpoint public access and Private Clusters to disable public access.

### Risk Statement

Failure to disable public access to Container Orchestrator API endpoints from the internet increases the risk of unauthorised access, potential exploitation, and security breaches, as exposing these endpoints publicly may lead to unauthorised control and compromise of the container infrastructure.



<a id="cs-10"></a>
## CS-10: Container Workload Segmentation

### Control Statement

Segregate container workloads to help contain attacks through isolation.

### Control Recommendations

Create Kubernetes namespaces or similar container segmentation controls to isolate different workloads, services or projects.

### Risk Statement

Without separating container workloads into namespaces, there's an increased risk of lateral movement and potential compromise.



<a id="cs-11"></a>
## CS-11: Container Runtime Security

### Control Statement

Detect and remediate changes to running containers with container runtime protection tools.

### Control Recommendations

Runtime protection tools, such as AWS EKS Protection, Microsoft Defender for Containers, or Falco, monitor threats and changes to running containers. Vulnerable container instances should be isolated for investigation and replaced with rebuilt and patched images. To avoid persistence if patches do not exist, the container instance should be replaced frequently with an un-compromised image until a patch released. These tools replace Malware Protection (IS-7) and EDR (IS-8) in container environments.

### Risk Statement

Failure to detect and remediate changes to running containers using container runtime protection tools increases the risk of unnoticed compromises, potential exploitation, and unauthorised alterations to containerised applications, compromising the security and integrity of the runtime environment.




