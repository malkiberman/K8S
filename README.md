# ☸️ Kubernetes Microservices Orchestration

This repository demonstrates a complete cloud-native infrastructure setup using **Kubernetes**. It features a multi-tier voting application architecture, showcasing container orchestration, service discovery, and persistent storage management.

---

## 🏗️ Architecture Overview

The system is composed of several interconnected microservices:

- **Voting UI** – Frontend where users cast their votes  
- **Result UI** – Dashboard to view real-time voting results  
- **Worker Service** – Logic layer that processes votes and moves them to the database  
- **Redis** – In-memory message broker for fast vote queuing  
- **PostgreSQL** – Persistent database for storing final results  

---

## 🛠️ Infrastructure Features

### Deployments

Managed scaling and self-healing for all services.

### Services

Internal and external load balancing using **ClusterIP** and **NodePort**.

### Ingress

Configured routing for external traffic management.

### Persistence

Implementation of **PersistentVolumeClaims (PVC)** for database durability.

### Security

Usage of **Secrets** and **ConfigMaps** for sensitive environment variables.

---

## 🚀 Deployment Instructions

### 1. Apply configurations

```bash
kubectl apply -f voting-app-config.yaml
kubectl apply -f voting-app-secret.yaml
```

### 2. Deploy services and databases

```bash
kubectl apply -f postgres-deployment.yaml
kubectl apply -f redis-deployment.yaml
```

### 3. Deploy the application layers

```bash
kubectl apply -f vote-deployment.yaml
kubectl apply -f result-deployment.yaml
kubectl apply -f worker-deployment.yaml
```

---

## 🧠 Skills Demonstrated

- Cloud-native architecture design  
- Container orchestration with Kubernetes  
- Microservices communication  
- YAML configuration  
- Infrastructure as Code (IaC)  

---

## 📌 Technologies Used

- Kubernetes  
- Docker  
- Redis  
- PostgreSQL  
- YAML  
- Microservices Architecture  
- DevOps Practices  

---
