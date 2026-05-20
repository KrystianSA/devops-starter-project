# PostgreSQL Deployment on Kubernetes

## Tools Used
* Minikube
* Docker Desktop
* Visual Studio Code
* kubectl
  
## Deployment Steps
1. Created project folder and PostgreSQL YAML manifest file.
2. Started local Kubernetes cluster using Minikube:
minikube start
3. Applied Kubernetes manifests:
kubectl apply -f postgres.yaml
4. Verified deployed resources:
kubectl get namespaces
kubectl get pods -n postgres
kubectl get pvc -n postgres
kubectl get svc -n postgres

## Security Decisions

PersistentVolumeClaim (PVC)
- Used PersistentVolumeClaim to ensure PostgreSQL data persists even after pod restart or
recreation.

Kubernetes Secret
- Used Kubernetes Secret to avoid storing database credentials directly in the deployment
configuration.

Backup Storage
- Created a dedicated PersistentVolumeClaim for storing PostgreSQL backup files.
Automated Backups
- Implemented Kubernetes CronJob to automate scheduled PostgreSQL backups using
pg_dump.

Health Checks
- Configured readinessProbe and livenessProbe to improve application reliability and automatic
recovery.
