<img width="960" height="540" alt="image" src="https://github.com/user-attachments/assets/e0f6ce75-73ee-4ea9-8bfe-741ecf0d042f" /># 🚀 Kubernetes Deployment & Auto-Scaling of a Containerized Application

## 📌 Project Overview

This project demonstrates deployment of a full-stack containerized application on Kubernetes using Minikube.

The application consists of:

- Frontend (React)
- Backend (Node.js)
- MongoDB Database

---

## ⚙️ Features Implemented

- Kubernetes Deployments
- ReplicaSets
- Services (ClusterIP / NodePort / LoadBalancer)
- Horizontal Pod Autoscaler (HPA)
- Rolling Updates
- Rollback
- Self-Healing Pods
- Monitoring & Logging

---

## 🏗️ Architecture

Frontend (React)
→ Frontend Service
→ Backend Service (ClusterIP)
→ Backend Pods (Node.js)
→ MongoDB Service
→ MongoDB Pod

---

## 🛠️ Technologies Used

- Docker
- Kubernetes
- Minikube
- kubectl
- React
- Node.js
- MongoDB

---

## 📁 Project Structure

Kubernetes-Deployment-Project/
├── frontend/
│   ├── Dockerfile
│   ├── package.json
│   └── src/
│
├── backend/
│   ├── Dockerfile
│   ├── package.json
│   └── server.js
│
├── k8s/
│   ├── frontend-deployment.yaml
│   ├── backend-deployment.yaml
│   ├── database-deployment.yaml
│   ├── services.yaml
│   ├── hpa.yaml
│   ├── configmap.yaml
│   └── secret.yaml
│
└── README.md

---

🚀 Deployment Steps
1. Start Minikube

A Kubernetes cluster is initialized using Minikube to create a local development environment.

2. Build Docker Images

Docker images are created for both the frontend (React) and backend (Node.js) applications.

3. Push Images to DockerHub

The built Docker images are pushed to DockerHub so they can be pulled by Kubernetes.

4. Deploy to Kubernetes

All Kubernetes configuration files (Deployments, Services, etc.) are applied to deploy the application.

5. Verify Deployment

Pods, Deployments, and Services are checked to ensure everything is running correctly.

6. Access the Application

The frontend service is exposed, and the application is accessed through a browser using the service URL.

💡 Simple flow

Minikube start
   ↓
Docker build
   ↓
Docker push
   ↓
kubectl apply
   ↓
Pods running
   ↓
App access


📈 Auto Scaling (HPA)
kubectl apply -f hpa.yaml
kubectl get hpa

🔄 Rolling Update
kubectl set image deployment/backend backend=ashu72/backend:v2
kubectl rollout status deployment/backend

↩️ Rollback
kubectl rollout undo deployment/backend

🛡️ Self Healing
kubectl delete pod <pod-name>
kubectl get pods -w

📊 Monitoring & Logs
kubectl logs -l app=frontend
kubectl top pods

🎯 Project Outcomes
Kubernetes Deployments
ReplicaSets
Services
Horizontal Pod Autoscaler
Rolling Updates
Rollback
Self-Healing
Monitoring & Logging
React Frontend Deployment
Node.js Backend Deployment
MongoDB Deployment

👨‍💻 Author

Ashu Chamle
DevOps & Cloud Project
