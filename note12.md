# Kubernetes Class Overview

These notes summarize a class on Kubernetes concepts, with a strong focus on understanding cluster architecture through practical demonstrations and hands on setup.

---

## Introduction to Kubernetes Nodes

The instructor demonstrated setting up a Kubernetes cluster using three machines:
- One machine was configured as the **master node**
- Two machines were configured as **worker nodes**

### Node Roles
- **Master Node**  
  Responsible for control plane operations such as scheduling, cluster state management, and decision making.

- **Worker Nodes**  
  Execute application workloads assigned by the master node.

---

## Setting Up the Master Node

Preliminary installations were completed before the class session.  
A shell script was used to install the required components and convert a machine into a master node.

The setup process involved:
- Switching to superuser mode using: `sudo su`
- Initializing the Kubernetes control plane using: `kubeadm init`

This process downloads and configures essential Kubernetes components such as:
- API server
- etcd
- Controller manager
- Scheduler

These components are deployed using predefined Kubernetes YAML manifests.

---

## Understanding Pods

### What is a Pod?
A pod is the smallest deployable unit in Kubernetes.  
It can contain one or more containers that run together on the same node.

### Key Characteristics
- **Co located**  
Containers in a pod share the same network namespace and storage resources.

- **Co scheduled**  
All containers in a pod are scheduled together on the same worker node.

---

## Architecture Overview

### Control Plane and Data Plane

**Control Plane**  
Includes the following components:
- API server  
- etcd, a distributed key value store for cluster state  
- Controller manager  
- Scheduler  

**Data Plane**  
Runs on worker nodes and is responsible for executing application workloads.

---

## API Server and kubectl

`kubectl` is the command line tool used to interact with a Kubernetes cluster.  
It communicates with the API server using REST based communication.

The API server performs:
- Authentication  
- Authorization  
- Request validation  

After validation, data is stored or retrieved from etcd.

---

## Hands On Deployment

### Creating and Managing Pods
The instructor demonstrated how to create and manage pods using `kubectl` commands.

Important commands discussed included: `kubectl get pods`
This command is used to monitor pod status and verify successful deployments.

---

## Namespaces in Kubernetes

Namespaces are used to logically isolate and organize resources within a Kubernetes cluster.

Default namespaces include:
- `default`
- `kube-system`
- Other system specific namespaces

Namespaces help manage resources and improve security in large clusters.

---

## Network Configuration

### CoreDNS and Network Plugins
CoreDNS is responsible for internal DNS resolution within the Kubernetes cluster.

For CoreDNS to function correctly, a network plugin must be installed.  
An example discussed in class was **Weave**.

The discussion also highlighted that pod scheduling depends on available CPU and RAM resources on worker nodes.

---

## Conclusion

The class concluded by emphasizing the importance of understanding Kubernetes architecture and pod management.  
Although Kubernetes is complex, mastering these fundamentals is essential for deploying and managing modern microservices based applications.

These notes provide a solid foundation for revision.  
Exploring additional `kubectl` commands and experimenting with personal cluster setups is strongly encouraged for deeper understanding.



