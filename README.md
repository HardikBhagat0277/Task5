# Task5
Build a Kubernetes Cluster Locally with Minikub

## 📌 Objective
Deploy and manage an application on Kubernetes using **Minikube**.

---

## 🛠 Tools Used
- Minikube
- kubectl
- Docker (as driver for Minikube)

---

## ⚡ Steps

### 1️⃣ Install Minikube & Start Cluster
```bash
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
sudo install minikube-linux-amd64 /usr/local/bin/minikube
sudo snap install kubectl --classic
minikube start --driver=docker
kubectl get nodes

## COMMANDS TO APPLY AND CHECK ##

**for deployment.yml

kubectl apply -f deployment.yaml
kubectl get pods

**for service.yml

kubectl apply -f service.yaml
kubectl get svc
minikube service myapp-service

**To Scale deployment

kubectl scale deployment myapp-deployment --replicas=4
kubectl get pods



