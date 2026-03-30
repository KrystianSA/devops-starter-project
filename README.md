# DevOps Starter Project

![CI](https://github.com/KrystianSA/devops-starter-project/actions/workflows/ci.yml/badge.svg)

This project demonstrates a practical DevOps workflow including CI/CD, containerization, and Infrastructure as Code.

---

## 🚀 Features

- CI/CD pipeline using GitHub Actions triggered on each commit  
- Multi-stage pipeline: build → test → Docker build → run  
- Docker image build integrated into CI pipeline  
- Infrastructure provisioning using Terraform (Azure)  

---

## 🧰 Tech Stack

- GitHub Actions (CI/CD)
- Docker (containerization)
- Terraform (Infrastructure as Code)
- Microsoft Azure
- Python

---

## ⚙️ CI/CD Pipeline

The pipeline is automatically triggered on each push and performs:

1. Checkout code  
2. Setup Python environment  
3. Build step  
4. Run basic validation tests  
5. Build Docker image  
6. Run application  

---

## 🐳 Docker

Application is containerized using Docker.

Build locally:
```bash
docker build -t devops-app .
