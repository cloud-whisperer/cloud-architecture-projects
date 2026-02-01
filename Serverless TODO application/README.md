# 🧭 Serverless-DynamoDB-Todo-App

📝 *Secure Serverless CRUD Application Using AWS Lambda, DynamoDB, and Terraform (IaC)*

Part I<br>  
![Alt Text](800x500_1.jpg)  
<br><br>Part II<br>  
![Alt Text](800x500_2.jpg)

---

## 📌 Project Description

This project demonstrates a **secure, serverless application architecture** where a Python-based AWS Lambda function performs CRUD operations against a DynamoDB table, fully provisioned using **Terraform Infrastructure as Code**.

The focus is on **event-driven design**, **least-privilege IAM**, **modular Terraform**, and **automated data lifecycle management** using DynamoDB **Time to Live (TTL)**. The infrastructure is structured to support **CI/CD pipelines**, drift detection, and future security automation.

Designed as a hands-on lab to showcase **cloud-native application development**, **secure AWS service integration**, and **DevSecOps-ready infrastructure patterns**, making it well-suited for AWS Developer (DVA-C02), Solutions Architect, and Cloud Security roles.

---

## 🚀 Key Steps Simulated in This Project

- 🗃 **Provision DynamoDB table** with partition key and TTL enabled  
- 🐍 **Deploy Python AWS Lambda function** for CRUD logic  
- 🌐 **Expose Lambda via API Gateway** for HTTP access  
- 🛡️ **Create IAM role & policies** using least-privilege principles  
- 🔐 **Pass DynamoDB access securely** via IAM (no hardcoded credentials)  
- 🔄 **Structure Terraform modules** for CI/CD compatibility  
- 🧪 **Validate data lifecycle behavior** via DynamoDB TTL expiration  
- 🧹 **Safely destroy infrastructure** using Terraform  

---

## 🧱 Core Infrastructure (Provisioned)

| Component | Description |
|---------|-------------|
| 🐍 AWS Lambda | Python-based serverless function handling CRUD operations |
| 🗃 DynamoDB | Fully managed NoSQL database with TTL enabled |
| 🌐 API Gateway | REST API fronting the Lambda function |
| 🛡️ AWS IAM | Custom roles & policies enforcing least privilege |
| 🔧 Terraform | Modular Infrastructure as Code for reproducible deployments |
| 📊 CloudWatch Logs | Centralized logging for Lambda execution |

---

## 🧪 Testing & Validation

### ✅ Summary Table (Mit Ikons)

| 🔢 Step | Goal | Tool / Location |
|-------|------|----------------|
| 1️⃣ | Invoke Lambda via API | API Gateway endpoint |
| 2️⃣ | Create To-Do item | HTTP POST request |
| 3️⃣ | Retrieve item | HTTP GET request |
| 4️⃣ | Update item | HTTP PUT request |
| 5️⃣ | Verify TTL expiration | DynamoDB console / CLI |

---

### 🧠 Behavior Confirmations

| 🔍 Verification Item | 📌 Status | 🧾 Evidence |
|--------------------|-----------|-------------|
| Lambda executes with IAM role | ✅ | IAM role attached |
| No hardcoded AWS credentials | ✅ | IAM-only access |
| DynamoDB CRUD operations succeed | ✅ | Items visible in table |
| TTL attribute configured | ✅ | TTL status enabled |
| Expired items auto-deleted | ✅ | Item removed after expiry |

---

## 🛡️ Security Controls & Design Principles

### 🔐 What Was Implemented

- ✅ **IAM Role per Service** (Lambda-specific role)  
- 🔒 **Least-Privilege Policies** (DynamoDB + CloudWatch only)  
- 🧾 **No Secrets in Code or State**  
- 🧠 **Infrastructure as Code for auditability**  
- 🕒 **Automated data expiration using DynamoDB TTL**  

---

### 🎯 Security & Career Value

| Benefit | Description |
|-------|-------------|
| 🛡️ | Demonstrates least-privilege IAM in AWS |
| 🧠 | Shows understanding of serverless security boundaries |
| 🔄 | CI/CD-ready Terraform module design |
| 📊 | Exposure to audit-friendly logging patterns |
| 💼 | Directly aligned with DVA-C02 & DevSecOps roles |

---

## 🧹 Clean-Up Checklist

- 🧼 Delete DynamoDB table  
- 🗑️ Remove Lambda function  
- 🌐 Delete API Gateway resources  
- 🛡️ Remove IAM roles and policies  
- 📉 Destroy Terraform-managed infrastructure  

---

## 🎯 Learning Outcomes

- 🐍 Built a **serverless Python application** on AWS  
- 🗃 Implemented **DynamoDB CRUD operations + TTL**  
- 🛡️ Applied **least-privilege IAM design**  
- 🔧 Structured **modular Terraform for CI/CD**  
- 🧠 Reinforced **event-driven, cloud-native architecture concepts**

---

*This project reflects real-world serverless application patterns commonly used in production AWS environments, with a strong emphasis on security, automation, and infrastructure integrity.*

