# Kubernetes Revision Notes

This set of revision notes consolidates the key concepts covered in the Kubernetes class.  
The goal is to provide a clear and comprehensive recap of core Kubernetes components and their roles.

---

## 1. Introduction to Kubernetes
Kubernetes is an open source platform designed to automate the deployment, scaling, and operation of containerized applications.  
It enables efficient management of applications running across a cluster of machines.

---

## 2. Pods
A Pod is the fundamental building block of Kubernetes.  
It represents a running process in a cluster and can contain one or more containers.

All containers within a Pod share the same network namespace, including IP address and port space. This allows them to communicate locally as if they were running on the same machine.

### Key Characteristics of Pods
- **Co located**  
  All containers in a Pod are scheduled on the same node and start together.

- **Shared Networking**  
  Containers within a Pod share a single IP address and port range.

### Analogy
A Pod is like a house that contains one or more rooms.  
The address is assigned to the house, not to the individual rooms.

---

## 3. Replica Sets
A ReplicaSet ensures that a specified number of Pod replicas are running at all times.  
If a Pod fails, the ReplicaSet automatically creates a replacement to maintain continuity.

### Characteristics
- Supports scaling out and scaling in
- Even with a single Pod, using a ReplicaSet is recommended for fault tolerance, as Kubernetes automatically recreates failed Pods

---

## 4. Deployments
Deployments provide declarative management for Pods and ReplicaSets.  
They define how applications should be deployed and updated.

### Features
- **Scale Management**  
  Applications can be scaled up or down easily.

- **Updates and Rollbacks**  
  Supports rolling updates and quick rollbacks.

Internally, a Deployment manages ReplicaSets, which in turn manage Pods.

---

## 5. Services
Services provide a stable network endpoint for accessing Pods.  
They expose applications running on a set of Pods as a network service.

### Types of Services

#### ClusterIP
- Exposes the Service on an internal cluster IP
- Accessible only within the cluster

#### NodePort
- Exposes the Service on each node’s IP at a static port
- Automatically creates a ClusterIP Service

### Important Concepts
- **Service Discovery**  
  Services locate Pods using labels.

- **Load Balancing**  
  Traffic is evenly distributed across all Pods in the Service.

### Analogy
A Service is like attendants at a movie theater.  
Visitors can approach any attendant, and their request is handled without needing a specific counter.

---

## 6. Load Balancers
Load balancers distribute incoming traffic across multiple targets such as Pods.

- **Internal Load Balancer**  
  Distributes traffic within the cluster.

- **External Load Balancer**  
  Handles traffic coming from outside the cluster to Kubernetes services.

---

## 7. YAML Files in Kubernetes
Kubernetes resources are defined using YAML configuration files.  
A typical YAML file includes the following components:

- **API Version**  
  Specifies which Kubernetes API version to use.

- **Kind**  
  Defines the type of resource, such as Deployment or Service.

- **Metadata**  
  Contains identifying information like name and namespace.

- **Spec**  
  Defines the desired behavior and configuration of the resource.

---

## Summary
Understanding Pods, ReplicaSets, Deployments, Services, Load Balancers, and YAML configuration files forms the foundation of Kubernetes.  
These components work together to enable efficient deployment, scaling, and management of containerized applications.
