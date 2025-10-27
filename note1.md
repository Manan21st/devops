# Introduction to Microservices

## What are Microservices?
Microservices are an architectural style where an application is built as a collection of small, loosely coupled services.  
Each service focuses on a specific business capability and communicates using lightweight protocols, typically over HTTP.

Unlike monolithic architectures, where the entire application is deployed as a single unit, microservices break the application into independent and autonomous services that can be developed, deployed, and scaled separately.

---

## Benefits of Microservices

### Scalability
Individual services can be scaled independently based on demand, leading to more efficient use of resources.

### Flexibility in Technology Stack
Each microservice can be developed using a different programming language, framework, or database, allowing teams to choose the most suitable tools.

### Independent Deployment
Microservices can be deployed independently without affecting the entire system, enabling faster releases and reduced downtime.

---

## Key Concepts in Microservices

### REST API Communication
Microservices communicate with each other using REST APIs that rely on HTTP or HTTPS.  
This ensures interoperability between services regardless of the programming languages used.

### Statelessness
Microservices are designed to be stateless, meaning they do not store session data internally.  
All state is maintained in external data stores, making services easier to scale and replicate.

### Externalized Logging
Since microservices are distributed systems, logging must be externalized to track system behavior even if individual services fail.  
Common tools used for log aggregation and analysis include:
- Fluentd  
- ELK Stack  
- Splunk  

### Load Balancing and DNS

**Load Balancer**  
A load balancer distributes incoming network traffic across multiple service instances to improve reliability and availability.

**DNS (Domain Name System)**  
DNS converts human readable domain names into IP addresses, making service discovery easier in distributed environments.

---

## Introduction to DevOps

### Importance of DevOps
DevOps integrates software development and IT operations.  
The main objective is to reduce the software development lifecycle while maintaining high software quality.

### Continuous Integration and Continuous Deployment (CI/CD)

**Continuous Integration (CI)**  
CI involves frequently merging code changes into a shared repository where automated tests are executed.

**Continuous Deployment (CD)**  
CD automates the deployment of code changes to production environments, ensuring faster and more reliable releases.

A complete CI/CD pipeline with tool based examples was discussed during the class.

---

## Upcoming Topics and Expectations
Upcoming sessions will focus on Docker and Kubernetes, which are essential for containerization and orchestration in DevOps.

Assignments and active class participation will be part of the evaluation process, with emphasis on practical learning.

---

## Class Dynamics and Participation
- Students are encouraged to submit daily notes on GitHub to maintain learning consistency.
- Hands on sessions will follow theoretical lectures to strengthen conceptual understanding through practice.

---

## Summary
Microservices and DevOps together enable the development of scalable, reliable, and efficient applications.  
Understanding these concepts is essential for building modern distributed systems.
