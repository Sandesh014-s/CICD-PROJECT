# CICD-PROJECT 🚀

This project implements a **CI/CD Pipeline on AWS** using GitHub Actions and AWS services.  
It was developed as part of the AWS DevOps Engineer Demo Assignment.

---

## 📌 Project Overview

- Automates **build → test → deploy → rollback**.  
- Deploys a sample **web app** (Node.js/Python/React).  
- Uses **S3 + CloudFront** for hosting.  
- Ensures secure deployment using AWS IAM roles and Secrets Manager.

---

## 🏗️ Architecture Diagram

![Architecture](A_flowchart_in_the_image_depicts_the_architecture_.png)

**Flow:**  
1. Developer pushes code to GitHub.  
2. GitHub Actions triggers CI/CD pipeline.  
3. Pipeline builds & tests the app.  
4. App is deployed to **AWS S3** (frontend) or **EC2/ECS** (backend).  
5. CloudFront serves the app globally.  
6. Rollback is automated in case of failure.  

---

## ⚙️ Tech Stack Justification

- **GitHub Actions** → Easy CI/CD integration, event-driven workflows.  
- **AWS S3 + CloudFront** → Scalable, cost-effective web hosting.  
- **AWS IAM** → Secure roles & permissions.  
- **Terraform (IaC)** → Reproducible infra setup (VPC, S3, CloudFront).  
- **Node.js/Python (App)** → Lightweight demo web app.  

---

## 🚀 Deployment Steps

### Prerequisites
- AWS account (Free Tier)  
- GitHub repository with this project  
- IAM role with CodeDeploy/CI/CD permissions  

### Steps
1. **Clone the repo**
   ```bash
   git clone https://github.com/Sandesh014-s/CICD-PROJECT.git
   cd CICD-PROJECT
2. **Provision infrastructure with Terraform**
cd iac
terraform init
terraform apply

3. **Push code to GitHub → triggers pipeline automatically**

4.**Push code to GitHub → triggers pipeline automatically.** 
Install dependencies
Run tests
Build artifact
Deploy to AWS S3/EC2/ECS

5. **Access the app via CloudFront URL or EC2 public IP**
