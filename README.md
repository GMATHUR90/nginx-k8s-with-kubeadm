# NGINX Kubernetes Deployment with Kubeadm

This repository contains YAML configuration files for deploying an NGINX server on a Kubernetes cluster set up using `kubeadm` on EC2 instances.

## Prerequisites

Before proceeding, make sure you have `kubeadm` installed on both the master and worker (slave) nodes. You can follow the installation guide here: [Kubeadm Installation Using Containerd](https://github.com/GMATHUR90/kubestarter/blob/main/Kubeadm_Installation_Using_Containerd.md).

## Setup Instructions

### Step 1: Deploy NGINX

To deploy NGINX, apply the `nginx-deployment.yaml` file on your Kubernetes cluster. This file creates a Deployment with two replicas of an NGINX pod.
