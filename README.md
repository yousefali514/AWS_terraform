# Cloud Infrastructure Automation with Terraform & AWS

A complete Infrastructure as Code (IaC) project that provisions and manages AWS cloud infrastructure using Terraform. The project demonstrates cloud automation, secure networking, CI/CD integration, and DevOps best practices.

---

## Project Overview

This project provisions a scalable AWS environment using Terraform.

Infrastructure includes:

- VPC
- Public & Private Subnets
- Internet Gateway
- Route Tables
- Security Groups
- IAM Roles
- EC2 Web Server
- S3 Backend
- DynamoDB State Locking

The entire infrastructure is deployed automatically through GitHub Actions.

---

## Architecture

```
                 GitHub Repository
                        │
                        ▼
                GitHub Actions
                        │
         terraform fmt / validate
                        │
                        ▼
                terraform plan
                        │
                        ▼
                terraform apply
                        │
                        ▼
               AWS Infrastructure

      ┌─────────────────────────────────┐
      │               VPC               │
      │                                 │
      │ Public Subnets                  │
      │    │                            │
      │    ▼                            │
      │ EC2 Web Server                  │
      │                                 │
      │ Private Subnets                 │
      │                                 │
      │ Security Groups                 │
      │ IAM Roles                       │
      │ Route Tables                    │
      │ Internet Gateway                │
      └─────────────────────────────────┘

               Terraform Backend

        S3 Bucket + DynamoDB Locking
```

---

## Features

- Infrastructure as Code
- AWS Automation
- Terraform Modules
- GitHub Actions CI/CD
- Remote Terraform State
- State Locking
- Secure IAM Roles
- Public & Private Networking
- Automated EC2 Deployment
- User Data Bootstrap Scripts

---

## Technologies

- Terraform
- AWS EC2
- AWS VPC
- AWS IAM
- AWS S3
- DynamoDB
- GitHub Actions
- Linux
- Bash
- Git

---

## Project Structure

```
terraform/
scripts/
docs/
architecture/
.github/
README.md
```

---

## CI/CD Workflow

The GitHub Actions pipeline performs:

1. Checkout repository
2. Terraform Init
3. Terraform Format Check
4. Terraform Validate
5. Terraform Plan
6. Terraform Apply
7. Verify Infrastructure

---

## AWS Resources

- VPC
- Public Subnets
- Private Subnets
- Internet Gateway
- Route Tables
- Security Groups
- IAM Roles
- EC2
- S3 Backend
- DynamoDB

---

## Getting Started

Clone the repository

```bash
git clone https://github.com/yousef-ali54554/terraform-aws-cloud-infrastructure.git

cd terraform-aws-cloud-infrastructure
```

Initialize Terraform

```bash
terraform init
```

Validate

```bash
terraform validate
```

Plan

```bash
terraform plan
```

Deploy

```bash
terraform apply
```

Destroy

```bash
terraform destroy
```

---

## Security Best Practices

- Least privilege IAM roles
- Private networking
- Restricted inbound access
- Remote encrypted Terraform state
- State locking with DynamoDB

---

## Future Improvements

- Deploy on Amazon EKS
- Auto Scaling Groups
- Application Load Balancer
- Route53
- ACM SSL Certificates
- RDS
- CloudWatch Monitoring
- Prometheus & Grafana
- Terraform Modules
- Terragrunt

---

## Screenshots

- GitHub Actions Workflow
- Terraform Apply
- AWS Console
- EC2
- VPC
- Security Groups

---

## Author

**Yousef Ali**

GitHub:
https://github.com/yousef-ali54554
