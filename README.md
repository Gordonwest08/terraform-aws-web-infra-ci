# Terraform AWS Web Infrastructure with CI/CD

> Modular, multi-environment Terraform project for deploying a web application on AWS  
> Fully integrated with **GitHub Actions CI/CD** for automated Terraform plan and review.

---

## 🔹 Project Overview

This repository demonstrates **Terraform best practices** and **automated CI/CD**:

- **Modular Terraform** design for reusable components
- **Multi-environment setup** (`dev`, `prod`) with isolated state
- **CI pipeline using GitHub Actions**:
  - Automatically runs `terraform fmt`, `validate`, and `plan` on Pull Requests
  - Plan output can be posted as PR comments for review
- Remote backend with **S3 + DynamoDB** for state management
- Infrastructure includes:
  - EC2 instances managed by Auto Scaling Groups
  - Application Load Balancer (ALB)
  - Security Groups for EC2 and ALB
  - IAM roles for EC2 with SSM access
  - CloudWatch dashboard for metrics

---

## ⚡ Key CI/CD Features

- **PR-based CI**: every Pull Request triggers a Terraform plan  
- **Plan Output in PR**: reviewers can see what Terraform will do before merging  
- **Environment Safety**: `dev` and `prod` have separate Terraform states  
- **Automated Checks**:
  - `terraform fmt` → ensures code style
  - `terraform validate` → ensures config is correct
  - `terraform plan` → previews infrastructure changes

> ✅ This ensures **safe, automated, and reviewable infrastructure changes**.

---

## 🏗️ Project Structure


