# Azure DevOps App Deployment

This project demonstrates a real-world DevOps workflow for deploying a resources to Microsoft Azure using Infrastructure as Code and CI/CD pipelines.

## 🚀 What this project does
- Builds and tests a Python application
- Containerizes the app using Docker
- Deploys infrastructure on Azure using Terraform
- Automates the deployment with GitHub Actions

## 🧱 Architecture
- GitHub Actions → CI/CD pipeline
- Docker → application containerization
- Terraform → Azure infrastructure provisioning
- Azure → hosting environment

## 🧰 Tech Stack
- Microsoft Azure
- Terraform (Infrastructure as Code)
- Docker
- GitHub Actions (CI/CD)
- Python

## ⚙️ CI/CD Pipeline
Pipeline is triggered on every push:
1. Checkout repository
2. Setup Python environment
3. Run validation/tests
4. Build Docker image
5. (Future) Push image to Azure Container Registry
6. (Future) Deploy to Azure

## 🔐 Security considerations
- Infrastructure managed via code (Terraform)
- Secrets should be stored in GitHub Secrets / Azure Key Vault

## 📌 Status
Project in progress – extending with full Azure deployment and monitoring
