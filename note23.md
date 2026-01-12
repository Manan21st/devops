# Revision Notes: Terraform and Infrastructure as Code

## Introduction to Terraform
Terraform is an open source Infrastructure as Code (IaC) tool that allows users to define, provision, and manage cloud infrastructure using code.  
It supports multiple cloud providers such as AWS, Azure, and Google Cloud, enabling consistent and repeatable infrastructure management.

---

## Key Characteristics

### Platform Agnostic
Terraform works across multiple cloud providers, allowing teams to manage heterogeneous environments using a single tool.

### Infrastructure as Code (IaC)
Infrastructure is defined using configuration files, enabling automation, consistency, and reduced manual errors.

---

## Terraform Lifecycle Commands

Terraform follows a structured workflow built around four primary commands.

### Terraform Init
- Initializes the working directory
- Downloads required providers and modules
- Locks provider versions to maintain compatibility

---

### Terraform Plan
- Compares the current infrastructure state with the desired configuration
- Generates an execution plan
- Allows previewing changes before applying them

---

### Terraform Apply
- Executes the changes defined in the plan
- Provisions or updates infrastructure to match the desired state
- Ensures controlled and predictable infrastructure changes

---

### Terraform Destroy
- Deletes all infrastructure resources defined in the Terraform configuration
- Useful for cleanup and cost control

---

## Advantages of Using Terraform

### Speed and Efficiency
Automates infrastructure provisioning, reducing setup time and operational overhead.

### Consistency
Ensures identical environments across deployments, eliminating configuration drift.

### Version Control
Terraform configuration files can be stored in Git, enabling:
- Change tracking
- Easy rollback
- Auditing of infrastructure changes

---

## Supporting Tools and Concepts

### Configuration Management Tools
Tools such as Ansible, Puppet, and Chef complement Terraform by managing software installation and configuration on provisioned infrastructure.

### Server Templating Tools
- **Vagrant** enables reproducible virtual environments
- **Docker** supports containerized application deployment

These tools work alongside Terraform to support modern DevOps workflows.

---

## Practical Demonstration

### Example Use Case: Creating an EC2 Instance
- Define infrastructure resources using `.tf` configuration files
- Specify cloud resources such as EC2 instances
- Execute:
  - `terraform init`
  - `terraform plan`
  - `terraform apply`
- Use Terraform state to track and manage resource changes

---

## Conclusion
Terraform is a powerful and essential tool for modern infrastructure management.  
Its Infrastructure as Code approach enables speed, consistency, and reliability while integrating seamlessly with DevOps and CI/CD practices.

Understanding Terraform commands, workflows, and supporting tools is critical for managing scalable and maintainable cloud infrastructure.
