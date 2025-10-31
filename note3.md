## Introduction to CI/CD

### What is CI/CD?
CI/CD stands for Continuous Integration and Continuous Deployment. It is a core practice in modern software development that focuses on automatically building, testing, and deploying applications. The goal is to integrate code changes quickly and deploy them with minimal manual effort.

---

### Continuous Integration (CI)
Continuous Integration ensures that code changes are frequently merged and validated through automated pipelines.

- **Code Repository**  
  When a developer checks in code to a repository, it triggers an automated CI pipeline.

- **Pipeline Steps**  
  1. **Linting**  
     Linting checks code quality and syntax errors. Although some organizations skip this step, it is considered a best practice as it helps catch errors early.

  2. **Building**  
     This stage involves downloading required packages and compiling the application. Unit tests may also be included at this stage depending on the configuration.

  3. **Unit Testing**  
     Unit testing focuses on testing individual components of the application.  
     Mocking is commonly used to simulate external dependencies when testing functions that rely on external services.

  4. **SCA and SAST**  
     Software Composition Analysis (SCA) and Static Application Security Testing (SAST) are performed to ensure the application meets security standards and does not contain known vulnerabilities.

---

### Artifacts in CI
Artifacts are binary outputs generated during the build process.  
Depending on the technology stack, artifacts can be:
- JAR or WAR files  
- Executable files  
- Gems  
- Docker images  

These artifacts are essential for testing, deployment, and version control.

---

## Introduction to Containers and Docker

### Dockerization
Dockerization involves packaging applications into containers.  
A Docker image is a static artifact that contains the application along with its dependencies and can be deployed consistently across environments.

### Creating Docker Images
Docker images are created by starting from a base image and adding application specific layers on top.  
Each layer is cached, which improves build efficiency and reduces build time.

---

### Pushing Docker Images
Once created, Docker images are pushed to an artifact repository or container registry.  
This enables versioning, storage, and reuse of images across environments.

---

## Continuous Deployment (CD)

### Deployment Pipeline
The deployment pipeline begins by pulling artifacts from the artifact repository.  
This pipeline may run independently or as an extension of the CI pipeline.

### System Integration Testing (SIT)
System Integration Testing is the first environment where the complete application is deployed.  
It validates how the application interacts with other systems and services, focusing on end to end behavior rather than isolated components.

---

### Elastic and Public IPs in Deployment

**Public IPs**  
Public IP addresses are temporary and may change when an instance is stopped or restarted.

**Elastic IPs**  
Elastic IP addresses remain constant even if an instance is stopped or rebooted.  
They are useful for maintaining stable endpoints in production environments.

---

## Summary
- CI/CD automates code integration and deployment, reducing friction between development and operations teams.
- Docker and containerization enable portability, consistency, and lightweight execution of applications.
- Elastic IPs help maintain stable access points for applications that are frequently redeployed or restarted.

Implementing CI/CD pipelines along with Dockerization results in a robust and efficient software delivery process that improves productivity and software quality.
