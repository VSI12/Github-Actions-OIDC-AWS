# Using OIDC to connect Github Actions to AWS.

This project demonstrates how to use OIDC to connect to AWS in order to enable deployments using Github Aactions.  It includes building and deploying a Dockerized Flask backend to Amazon ECR using a fully automated CI/CD pipeline.

##  Tech Stack

- **Flask** – Python backend application
- **Docker** – Containerize the application
- **Amazon ECR** – Store Docker images
- **GitHub Actions** – CI/CD pipeline
- **OIDC** – Secure GitHub → AWS access

##  Project Overview

### CI/CD Flow
1. Code pushed to `main` triggers GitHub Actions.
2. GitHub authenticates to AWS using OIDC.
3. Docker image is built and pushed to Amazon ECR.

##  GitHub Secrets You Need

| Name               | Purpose                                  |
|--------------------|-------------------------------------------|
| `AWS_ROLE_ARN`     | IAM role GitHub assumes via OIDC         |
| `ECR_REGISTRY`     | AWS ECR registry (e.g., `123...amazonaws.com`) |
| `ECR_URL`          | Full ECR image URI (e.g., `.../flask-app`)     |

---


