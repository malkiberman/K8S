# ☸️ Kubernetes Microservices Orchestration

This repository demonstrates a complete cloud-native infrastructure setup using **Kubernetes**. It features a multi-tier voting application architecture, showcasing container orchestration, service discovery, and persistent storage management.

## 🏗️ Architecture Overview
The system is composed of several interconnected microservices:
- **Voting UI:** Frontend where users cast their votes.
- **Result UI:** Dashboard to view real-time voting results.
- **Worker Service:** Logic layer that processes votes and moves them to the database.
- **Redis:** In-memory message broker for fast vote queuing.
- **PostgreSQL:** Persistent database for storing final results.

## 🛠️ Infrastructure Features
- **Deployments:** Managed scaling and self-healing for all services.
- **Services:** Internal and external load balancing using ClusterIP and NodePort.
- **Ingress:** Configured routing for external traffic management.
- **Persistence:** Implementation of **PersistentVolumeClaims (PVC)** for database durability.
- **Security:** Usage of **Secrets** and **ConfigMaps** for sensitive environment variables.

## 🚀 Deployment Instructions
To deploy the entire stack on your cluster:

1. **Apply configurations:**
   ```bash
   kubectl apply -f voting-app-config.yaml
   kubectl apply -f voting-app-secret.yaml
