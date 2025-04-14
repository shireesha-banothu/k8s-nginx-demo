# Kubernetes Task 5: Nginx on Minikube# Kubernetes Cluster with Minikube

## Overview

This project demonstrates how to deploy a simple application in a Kubernetes cluster locally using Minikube. The application is a basic echoserver running in Kubernetes with Docker and kubectl tools.

---

## Prerequisites

To complete this task, you’ll need the following tools installed:

- **Minikube**: For creating a local Kubernetes cluster.
- **kubectl**: Kubernetes command-line tool.
- **Docker**: For building container images and interacting with containers.

### Installation

#### 1. Install Minikube:
Follow the installation steps [here](https://minikube.sigs.k8s.io/docs/).

#### 2. Install kubectl:
Follow the installation steps [here](https://kubernetes.io/docs/tasks/tools/install-kubectl/).

#### 3. Install Docker:
Follow the installation steps [here](https://docs.docker.com/get-docker/).

---

## Setup and Running the Application

### 1. Start Minikube Cluster

```bash
minikube start
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
kubectl get pods
kubectl get svc
kubectl scale deployment nginx-deployment --replicas=3
kubectl describe pod <pod-name>
