# NGINX Kubernetes Deployment with Kubeadm

This repository contains YAML configuration files for deploying an NGINX server on a Kubernetes cluster set up using `kubeadm` on EC2 instances.

## Prerequisites

Before proceeding, make sure you have `kubeadm` installed on both the master and worker (slave) nodes. You can follow the installation guide here: [Kubeadm Installation Using Containerd](https://github.com/GMATHUR90/kubestarter/blob/main/Kubeadm_Installation_Using_Containerd.md).

## Setup Instructions

### Step 1: Create a Namespace for NGINX

Start by creating a dedicated namespace for the NGINX deployment.

1. Run the following command to create a namespace named `nginx`:
```bash
   kubectl create namespace nginx
```
2. Verify that the namespace has been created:
```bash
   kubectl get namespaces
```
### Step 2: Create an NGINX Pod in the Namespace
With the namespace created, deploy an NGINX Pod.

**1. Create a file named [`pod.yaml`](https://github.com/GMATHUR90/nginx-k8s-with-kubeadm/blob/main/pod.yaml)**

**2. Apply the Pod configuration in the nginx namespace:**
```bash
kubectl apply -f pod.yml -n nginx
```
**3. Verify that the Pod is running in the nginx namespace:**
```bash
kubectl get pods -n nginx
```

### Step 3: Create an NGINX Deployment in the Namespace

**1. Create a file named ['deployment.yaml'](https://github.com/GMATHUR90/nginx-k8s-with-kubeadm/blob/main/deployment.yaml)**

**2. Apply the Deployment configuration in the nginx namespace:**
```bash
kubectl apply -f deployment.yml --namespace nginx
```
**3. Verify that the Deployment and replicas are running:**
```bash
kubectl get deployments -n nginx
kubectl get pods -n nginx
```


