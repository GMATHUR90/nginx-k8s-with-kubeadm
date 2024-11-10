# Kubernetes Commands Cheat Sheet

This document contains commonly used `kubectl` commands for managing Kubernetes namespaces, pods, deployments, and services.

---

### 1. Create a Namespace
To create a new namespace:
```bash
kubectl apply -f namespace <namespace_name>
```

### 2. Apply Pod Configuration in a Namespace
To apply a pod configuration file to a specific namespace:

```bash
kubectl apply -f pod.yaml -n <namespace_name>
```

### 3. Get All Pods in a Namespace
List all pods in a specific namespace:

```bash
kubectl get pods -n <namespace_name>
```

### 4. Get Detailed Information of Pods in a Namespace
List all pods with additional details like node, IP, etc., in a specific namespace:

```bash
kubectl get pods -o wide -n <namespace_name>
```

### 5. Describe Pods in a Namespace

```bash
kubectl describe pods -n <namespace_name>
```

### 6. Apply Deployment Configuration in a Namespace
To apply a deployment configuration file to a specific namespace:

```bash
kubectl apply -f deployment.yaml -n <namespace_name>
```

### 7. Get Deployment in a Namespace
List all deployments in a specific namespace:

```bash
kubectl get deployment -n <namespace_name>
```

### 8. Describe Deployment in a Namespace
Display detailed information about a specific deployment in a namespace:

```bash
kubectl describe deployment -n <namespace_name>
```
### 9. Scale a Deployment in a Namespace
Scale the number of replicas in a specific deployment:

```bash
kubectl scale deployment nginx-deployment --replicas=5 -n <namespace_name>
```

### 10. Apply Service Configuration in a Namespace
To apply a service configuration file to a specific namespace:

```bash
kubectl apply -f service.yaml -n <namespace_name>
```

### 11. Get Services in a Namespace
List all services in a specific namespace:

```bash
kubectl get service -n <namespace_name>
```

#### Note: Replace <namespace_name> with the actual namespace name where the resources are managed.







