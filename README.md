# fastapi-gke-terraform-cicd
A production-ready FastAPI microservice deployed to GKE using Terraform and CI/CD on GCP.

# FastAPI GKE Terraform CI/CD

Deploy a production-ready Python FastAPI app on Google Cloud using:
- ✅ Kubernetes (GKE)
- ✅ Terraform (IaC)
- ✅ Docker
- ✅ CI/CD (Cloud Build or GitHub Actions)

---

## 📌 Features

- 🌐 FastAPI microservice
- ☁️ Google Kubernetes Engine (GKE)
- 🛠️ Infrastructure managed via Terraform
- 🐳 Docker-based deployment
- 🔁 Auto-deploy via CI/CD
- 🛡️ Secure access with GCP IAM
- 💾 Optional: Cloud SQL + Secret Manager

---

## 📂 Folder Structure

- `app/` - FastAPI application code
- `terraform/` - GKE infrastructure defined in Terraform
- `k8s/` - Kubernetes manifests for deploying the app
- `cicd/` - CI/CD pipeline setup (Cloud Build / GitHub Actions)

---

## 🚀 Quickstart

```bash
# Authenticate with GCP
gcloud auth login
gcloud config set project <your-project-id>

# Deploy infrastructure
cd terraform
terraform init
terraform apply

# Configure kubectl
gcloud container clusters get-credentials fastapi-gke-cluster --zone=us-central1-a

# Deploy the FastAPI app
kubectl apply -f ../k8s/

