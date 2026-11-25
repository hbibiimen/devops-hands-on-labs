# Kubernetes Hands-on Lab

## Project Overview

Personal DevOps project focused on container orchestration
using Kubernetes and Nginx.

## Environment

- Killercoda Kubernetes Playground
- Ubuntu Linux
- Kubernetes
- kubectl
- containerd
- Nginx Alpine
- YAML
- GitHub

## Architecture

- 1 Control Plane
- 1 Worker Node
- 1 Deployment
- 1 ReplicaSet
- 3 Nginx Pods
- 1 ClusterIP Service
- 1 NodePort Service

## Skills Practiced

- Kubernetes cluster management
- Pod creation and management
- Deployments and ReplicaSets
- Horizontal scaling from 3 to 5 replicas
- Self-healing and automatic Pod replacement
- ClusterIP and NodePort networking
- Labels and Selectors
- Declarative configuration using YAML

## Project Files

- deployment.yaml
- service-clusterip.yaml
- service-nodeport.yaml

## Deployment

```bash
kubectl apply -f deployment.yaml
kubectl apply -f service-clusterip.yaml
kubectl apply -f service-nodeport.yaml
```

## Verification

```bash
kubectl get nodes
kubectl get deployments
kubectl get replicasets
kubectl get pods -o wide
kubectl get services
kubectl get pods --show-labels
```

## Scaling

```bash
kubectl scale deployment nginx-deployment --replicas=5
```

## Test Results

- Kubernetes nodes: Ready
- Deployment: 3/3 replicas available
- Pods: Running
- Horizontal scaling: Successful
- Self-healing: Successful
- ClusterIP HTTP test: 200 OK
- NodePort HTTP test: 200 OK
- YAML deployment: Successful

## Conclusion

This hands-on project demonstrates practical knowledge
of Kubernetes orchestration, application deployment,
service networking, scaling and self-healing.
