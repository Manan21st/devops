# Kubernetes Horizontal Pod Autoscaler (HPA)

## Introduction
This session focused on understanding and implementing the Kubernetes Horizontal Pod Autoscaler (HPA).  
HPA enables automatic scaling of pod replicas based on observed CPU utilization or other supported metrics.

---

## What is HPA?
HPA stands for **Horizontal Pod Autoscaler**.  
It is a Kubernetes resource that automatically adjusts the number of pod replicas in a Deployment, ReplicaSet, or StatefulSet.

### Automatic Scaling
- Pods scale up automatically when load increases
- Pods scale down when load decreases
- Ensures efficient resource usage and high availability

---

## Analogy Used
The concept of HPA was explained using a real world work scenario:

### Horizontal Scaling
When workload increases and existing manpower is insufficient, more people are added to share the load.  
Similarly, HPA increases the number of pods when system load rises.

---

## Setting Up Kubernetes for HPA

### Prerequisites

#### Kubernetes Installation
A functional Kubernetes cluster is required, commonly set up using `kubeadm`.

#### Metrics Server
The Metrics Server is a critical component for HPA.  
It collects CPU and memory metrics and exposes them via the Kubernetes API.

Without a running Metrics Server, HPA cannot function.

---

## Kubernetes Commands Discussed

### Core Kubernetes Tools
- **kubeadm**  
  Used to initialize and manage Kubernetes clusters.

- **kubectl**  
  Command line tool to interact with Kubernetes clusters.

- **kubelet**  
  Node level agent responsible for managing pods and containers.

---

### Important kubectl Commands

#### Apply Configuration
`kubectl apply -f <file.yaml>`
Used to deploy configurations such as the Metrics Server.

---

#### Manual Scaling
`kubectl scale --replicas=<number> <resource_type>/<resource_name>`
Manually adjusts the number of pod replicas.

---

#### Resource Monitoring
`kubectl top`
Displays CPU and memory usage for nodes and pods.  
Requires Metrics Server to be running.

---

## Deploying HPA

### Steps to Deploy HPA

1. **Create a Deployment**  
   Define and apply a Deployment for the application.

2. **Deploy Metrics Server**  
   Required to collect CPU and memory metrics.

3. **Configure HPA**  
   Create an HPA resource defining scaling rules.

An example configuration may specify:
- Scale when CPU usage exceeds 50%
- Minimum replicas: 1
- Maximum replicas: 10

---

## Real Time Monitoring
The instructor demonstrated real time scaling by simulating increased load.  
As CPU usage crossed defined thresholds, Kubernetes automatically created new pods.

---

## Advanced Concepts

### Resource Requests and Limits

- **Requests**  
  Minimum guaranteed CPU and memory for a pod.

- **Limits**  
  Maximum CPU and memory a pod can consume.

Proper configuration of requests and limits is essential for accurate HPA behavior.

---

### HPA Configuration Details
- Minimum number of replicas
- Maximum number of replicas
- Resource thresholds such as CPU utilization percentage

---

## Actions and Troubleshooting

### Monitoring Commands
- `kubectl get pods`
- `kubectl get nodes`

Used to observe system and scaling behavior.

---

### Error Handling
A common issue discussed was HPA failing due to missing metrics.  
This reinforced the importance of ensuring the Metrics Server is properly deployed and running.

---

## Summary
The Horizontal Pod Autoscaler is a powerful Kubernetes feature that enables automatic horizontal scaling of applications.  
Understanding metrics collection, resource configuration, and HPA behavior is essential for building scalable and resilient Kubernetes workloads.
