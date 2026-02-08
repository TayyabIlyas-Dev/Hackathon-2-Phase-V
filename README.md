# 🧠 Hackathon II – Phase V  
## **Evolution of Todo: Advanced Cloud Deployment**

Phase V evolves the **Todo AI Chatbot** to **advanced cloud deployment** with **production-grade Kubernetes**, distributed architecture, and event-driven features.  

All implementation is **spec-driven via Claude Code + Spec-Kit Plus**.  

---

## 🎯 Phase V Goals

1. **Advanced Features (Part A)**  
   - Implement all **Advanced Level features**: Recurring Tasks, Due Dates & Reminders  
   - Implement **Intermediate Level features**: Priorities, Tags, Search, Filter, Sort  
   - Add **event-driven architecture** using Kafka  
   - Integrate **Dapr** for distributed runtime: Pub/Sub, State, Bindings (cron), Secrets, Service Invocation  

2. **Local Deployment (Part B)**  
   - Deploy to **Minikube**  
   - Run full **Dapr stack** locally  
   - Use Helm charts from Phase IV  

3. **Cloud Deployment (Part C)**  
   - Deploy to **Azure AKS / Google GKE / Oracle Cloud**  
   - Deploy **Dapr** fully on cloud cluster  
   - Kafka via **Redpanda Cloud** or alternative Pub/Sub with Dapr  
   - Set up **CI/CD pipeline** using GitHub Actions  
   - Configure **monitoring and logging**  

---

## 🛠️ Technology Stack

| Component        | Technology |
|-----------------|------------|
| Containerization | Docker + Helm Charts |
| Orchestration    | Kubernetes (Minikube locally, AKS/GKE cloud) |
| Distributed Runtime | Dapr (Pub/Sub, State, Bindings, Service Invocation) |
| Event Bus        | Kafka (Confluent/Redpanda Cloud) |
| CI/CD            | GitHub Actions |
| Monitoring/Logging | Cloud-native tools / Dapr metrics |
| Application      | Phase III Todo AI Chatbot |

---

## 🌐 Local Deployment Steps (Minikube)

```bash
# Start Minikube cluster
minikube start

# Deploy Helm charts (Phase IV)
helm install todo-frontend ./helm/frontend
helm install todo-backend ./helm/backend

# Deploy Dapr
dapr init --kubernetes
