# 📝 Django Notes App: Docker, Jenkins & Kubernetes

![Django](https://img.shields.io/badge/Django-092E20?style=flat-square&logo=django&logoColor=white) ![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=white) ![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white) ![Jenkins](https://img.shields.io/badge/Jenkins-D24939?style=flat-square&logo=jenkins&logoColor=white) ![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)

A Django + React notes app, **containerized**, delivered through a **Jenkins CI/CD pipeline** and deployed to **Kubernetes**.

> Application code is based on [LondheShubham153/django-notes-app](https://github.com/LondheShubham153/django-notes-app). My focus here is the DevOps side: containerization, pipeline and Kubernetes deployment.

## 🔄 CI/CD pipeline (Jenkinsfile)

```
Clone Code → Build and Test → Push to Docker Hub → Deploy
```

## ☸️ Kubernetes (`k8s/`)

| File | Resource |
|---|---|
| `namespace.yml` | Dedicated namespace |
| `deployment.yml` | App Deployment (image from Docker Hub) |
| `service.yml` | ClusterIP Service on port 8000 |

## 🚀 Run locally

```bash
docker build -t notes-app .
docker run -d -p 8000:8000 notes-app:latest
# or
docker compose up -d
```

## 🚀 Deploy to Kubernetes

```bash
kubectl apply -f k8s/namespace.yml
kubectl apply -f k8s/
kubectl port-forward svc/<service-name> 8000:8000 -n <namespace>
```

---

## 👤 Author

**Abdur Rehman** · DevSecOps Engineer · Founder of [ARTechOps](https://artechops.com)

[LinkedIn](https://www.linkedin.com/in/muhamad-abdur-rehman-81777b366/) · [GitHub](https://github.com/abdur-rehman-tech) · [artechops.com](https://artechops.com)
