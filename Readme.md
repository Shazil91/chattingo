# 🚀 Chattingo - Production-Ready DevOps Deployment (Full Stack Chat App)

## 📌 Overview

**Chattingo** is a full-stack real-time chat application that I transformed into a **production-ready, cloud-deployable system** using modern DevOps practices.

This project demonstrates my ability to:

* Containerize applications using Docker
* Orchestrate services with Docker Compose & Kubernetes
* Automate deployments using GitHub Actions (CI/CD)
* Deploy scalable applications on cloud infrastructure (AWS EC2 / VPS)

---

## 🧠 Key DevOps Highlights

✅ Multi-stage Docker builds for optimized images
✅ Microservices architecture (Frontend + Backend + Database)
✅ CI/CD pipeline using GitHub Actions
✅ Kubernetes deployment with autoscaling
✅ Nginx reverse proxy configuration
✅ Infrastructure as Code (K8s YAML manifests)
✅ Production-grade deployment strategy

---

## 🏗️ Architecture

```
             ┌──────────────┐
             │   Frontend   │  (React + Nginx)
             └──────┬───────┘
                    │
                    ▼
             ┌──────────────┐
             │   Backend    │  (Spring Boot)
             └──────┬───────┘
                    │
                    ▼
             ┌──────────────┐
             │   MySQL DB   │
             └──────────────┘
```

### 🔄 Communication

* REST APIs for standard communication
* WebSockets for real-time messaging

---

## ⚙️ Tech Stack

### 🖥️ Application

* Frontend: React, Tailwind CSS
* Backend: Spring Boot (Java)
* Database: MySQL
* Real-time: WebSocket (STOMP)

### ⚙️ DevOps & Cloud

* Docker & Docker Compose
* Kubernetes (Deployments, Services, HPA, VPA)
* GitHub Actions (CI/CD)
* Nginx (Reverse Proxy)
* AWS EC2 / VPS Deployment

---

## 🐳 Docker Implementation

### 🔹 Backend (Multi-stage)

* Maven build stage
* JAR packaging
* Lightweight JRE runtime

### 🔹 Frontend (Multi-stage)

* Node build stage
* Static build optimization
* Nginx serving layer

### 🔹 Run Locally

```bash
docker-compose up --build
```

---

## ☸️ Kubernetes Deployment

All Kubernetes manifests are available in the `k8s/` directory:

### Resources Implemented:

* Deployments (Frontend, Backend, MySQL)
* Services (ClusterIP / NodePort)
* Ingress (Routing)
* HPA (Horizontal Pod Autoscaler)
* VPA (Vertical Pod Autoscaler)
* Persistent Volume Claim (MySQL storage)

### Apply Deployment

```bash
kubectl apply -f k8s/
```

---

## 🔄 CI/CD Pipeline (GitHub Actions)

Automated pipeline triggered on push to `main` branch.

### Pipeline Stages:

1. ✅ Code Checkout
2. ✅ Build Docker Images
3. ✅ Push to Container Registry
4. ✅ SSH into Server
5. ✅ Pull Latest Images
6. ✅ Deploy using Docker Compose

### Example Workflow File:

```
.github/workflows/main.yaml
```

---

## ☁️ Deployment

### 🔹 Environment

* Cloud: AWS EC2 / VPS
* OS: Ubuntu
* Container Runtime: Docker

### 🔹 Steps

1. Launch EC2 instance
2. Install Docker & Docker Compose
3. Configure SSH access
4. Setup GitHub Secrets:

   * `EC2_HOST`
   * `EC2_USER`
   * `EC2_SSH_KEY`
5. Push code → Auto deployment triggered 🚀

---

## 🌐 Features

* 🔐 JWT Authentication
* 💬 Real-time chat (WebSockets)
* 👥 Group messaging
* 📱 Responsive UI
* ⚡ Scalable backend services

---

## 📊 Project Structure

```
chattingo/
├── backend/
├── frontend/
├── docker-compose.yaml
├── k8s/
│   ├── deployments
│   ├── services
│   ├── ingress
│   └── autoscaling
└── .github/workflows/
```

---


---

## 💼 What This Project Demonstrates

This project highlights my ability to:

* Design and deploy scalable systems
* Implement CI/CD pipelines
* Work with containerization & orchestration tools
* Automate infrastructure and deployments
* Follow production-level DevOps practices

---

## 🚀 Future Improvements

* Helm charts for Kubernetes deployment
* Monitoring (Prometheus + Grafana)
* Logging (ELK stack)
* Blue-Green / Canary deployments
* Terraform for infrastructure provisioning

---

## 👨‍💻 Author

**Shazil Ali**

* GitHub: https://github.com/Shazil91

---

## ⭐ Final Note

This project is part of my journey to becoming a **DevOps Engineer**, focusing on real-world deployment, automation, and scalability.

If you like this project, feel free to ⭐ the repository!
