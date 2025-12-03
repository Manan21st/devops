# Introduction to Kubernetes YAML Structure

In Kubernetes, most YAML configuration files follow a common structure made up of four essential components.

---

## Core Components of a Kubernetes YAML

### API Version
Specifies the API version being used.  
Kubernetes APIs are versioned to maintain backward compatibility while introducing new features.

### Kind
Defines the type of Kubernetes object being created, such as:
- Pod
- ReplicaSet
- Deployment

### Metadata
Contains information about the object, such as its name and labels.  
The name field is usually mandatory.

### Spec
Describes the desired state of the object.  
The structure of `spec` varies depending on the object type, such as Pod or ReplicaSet.

---

## Understanding Pods

A pod is the smallest deployable unit in Kubernetes.  
It consists of one or more containers that share resources and are both co located and co scheduled.

If a container inside a pod crashes, Kubernetes automatically replaces it without manual intervention.  
This behavior ensures application resilience and high availability.

---

## YAML Syntax Basics

Kubernetes YAML uses three primary data structures:

### Key Value Pair
Defined using: `key: value`


### Map
A nested structure consisting of key value pairs.  
Maps can contain lists or other maps.

---

## ReplicaSets Explained

### Purpose of ReplicaSets
A ReplicaSet ensures that a specified number of pod replicas are running at all times.

If a pod crashes or a node becomes unavailable, the ReplicaSet automatically creates new pods on available nodes to maintain the desired count.

---

### Structure of a ReplicaSet YAML

A ReplicaSet YAML file typically includes:
- `kind` set to `ReplicaSet`
- A `replicas` field specifying how many pod instances should run
- A `selector` that matches the labels of the pods it manages
- A pod template defining the pod configuration

Labels are used to group and manage pods collectively, similar to tags in cloud platforms.

---

## Internal Working and Processes

### Kubernetes Component Interaction

**Kubelet**  
Runs on worker nodes and manages the lifecycle of pods.  
It also reports node and pod status to the API server.

**API Server**  
Handles authentication, authorization, and validation of requests.  
It communicates with etcd to store and retrieve cluster state.

**Controllers**  
Continuously monitor the cluster state and generate events to maintain the desired configuration.

**Scheduler**  
Assigns pods to worker nodes based on resource availability and scheduling constraints.

---

## Pod Lifecycle and Recovery

Kubernetes continuously compares the desired state with the current state of the cluster.  
If a mismatch is detected, such as a pod failure, the controller instructs the API server to initiate corrective actions, like creating a new pod.

This ensures self healing and consistency across the cluster.

---

## Practical kubectl Commands

Some commonly used `kubectl` commands include: 

`kubectl apply -f <file>`
Creates or updates Kubernetes resources.

`kubectl delete -f <file>`
Deletes Kubernetes resources.

`kubectl get <resource>`
Lists Kubernetes resources such as pods or ReplicaSets.

---

## Summary
These notes cover the fundamentals of Kubernetes YAML structure, pods, and ReplicaSets.  
Understanding these core concepts is essential for effectively managing and scaling applications in a Kubernetes environment.







