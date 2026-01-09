# CI/CD with Kubernetes Deployment Overview

## Introduction
This class focused on deploying applications into a Kubernetes cluster, with special emphasis on Continuous Integration (CI) and Continuous Deployment (CD).  
These practices are core components of modern DevOps environments.

---

## Continuous Integration (CI) and Continuous Deployment (CD)

### Continuous Integration (CI)
Continuous Integration involves automating the integration of code changes from multiple contributors into a single shared codebase.

Key objectives include:
- Frequent code merges
- Automated testing
- Ensuring the main branch remains in a deployable state

---

### Continuous Deployment (CD)
Continuous Deployment extends automation beyond CI to production deployments.

Key aspects include:
- Automated deployment pipelines
- Infrastructure configuration
- Deploying application updates with minimal or zero downtime

---

## Setting Up a Kubernetes Environment

### Creating a Virtual Machine
- A minimum of a single node Kubernetes cluster is required.
- Tools such as **VirtualBox** and **Vagrant** can be used to create virtual machines.
- Vagrant scripts automate the setup of virtual environments with required configurations.

Vagrant simplifies setup by allowing users to reuse predefined scripts rather than configuring everything manually.

---

### Deploying on Kubernetes
- Ensure Kubernetes is pre-installed on the virtual machine.
- Using an existing Amazon Machine Image (AMI) with Kubernetes pre-installed can significantly reduce setup time.

---

## GitHub Actions and Custom Runners

### GitHub Actions
GitHub Actions enables automation of CI/CD workflows directly within a repository.

It supports:
- Building code
- Running tests
- Packaging artifacts
- Releasing and deploying applications

---

### Custom Runners
Instead of GitHub-hosted runners, self-hosted runners can be configured.

Key points:
- Linux systems are commonly preferred
- The runner machine is registered with GitHub
- Workflows can be executed on this custom infrastructure

#### Configuration Steps
- Use `config.sh` to register the runner
- Assign labels and apply appropriate security settings

---

## Project Demonstration and Teamwork
- Teams worked on projects that implemented CI/CD pipelines using GitHub Actions and related tools.
- Each team presented their project implementation.
- Although projects were collaborative, individual understanding and contributions were evaluated during presentations.

---

## Testing and Quality Assurance
A structured testing strategy was emphasized, including:
- System Integration Testing (SIT)
- Performance Testing
- Security Testing

Testing stages are often automated to reduce human error and ensure consistent coverage.

---

## Practical Considerations
- CI and CD are usually implemented as separate processes to maintain clear separation of concerns.
- Deployment pipelines often require customization based on application requirements and hosting infrastructure.

---

## Conclusion
This session covered the end to end CI/CD process involving Kubernetes setup and deployment strategies.  
Understanding CI, CD, Kubernetes environments, and automation tools is essential for building scalable and reliable modern applications.
