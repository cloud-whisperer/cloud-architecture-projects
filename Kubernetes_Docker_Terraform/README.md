
# ☸️ Kubernetes-Docker-Terraform-MySQL-API

📝 *Local Containerized CRUD REST API Using Flask, MySQL, Docker, Kubernetes (Minikube), and Terraform (IaC)*

---

## 📸 Project Overview

**Part I — Docker & Flask API**  
![Part I](images/Part_I.jpg)

**Part II — Kubernetes & MySQL**  
![Part II](images/Part_II.jpg)

**Part III — Terraform & Infrastructure Automation**  
![Part III](images/Part_III.jpg)

---

## 📌 Project Description

This project demonstrates a **containerized application architecture** in which a Python-based Flask REST API performs CRUD operations against a MySQL relational database.

The application is initially deployed using Docker and subsequently orchestrated using **Kubernetes (Minikube)**, with infrastructure automation implemented using **Terraform (Infrastructure as Code)**.

The focus is on **containerization, microservices architecture, service discovery, persistent storage, health monitoring, secure configuration management, and infrastructure automation**.

Designed as a hands-on local lab without ongoing AWS infrastructure costs, this project reinforces **cloud-native application development, container orchestration, DevSecOps practices, and Infrastructure as Code (IaC)**.


---

## 🚀 Key Steps Simulated in This Project

- 🐍 Develop a Python Flask REST API supporting CRUD operations
- 🗄️ Integrate Flask with a MySQL relational database
- 🐳 Containerize the application using Docker
- 💾 Configure persistent database storage using Docker volumes
- ☸️ Load locally built Docker images into Minikube
- 📦 Deploy MySQL using Kubernetes Deployments and Pods
- 🔐 Manage database credentials using Kubernetes Secrets
- 🗂️ Configure application settings using Kubernetes ConfigMaps
- 🔌 Configure Kubernetes Services for internal service discovery
- 🌐 Deploy and expose the Flask API within Kubernetes
- 🩺 Configure Kubernetes readiness and liveness probes
- 📈 Scale application replicas using Kubernetes Deployments
- 🔧 Provision and manage infrastructure using Terraform
- 🧪 Validate API functionality, database connectivity, and persistence
- 🧹 Practice infrastructure cleanup and resource lifecycle management

---

## 🧱 Core Infrastructure

| Component | Description |
|---|---|
| 🐍 Flask | Python-based REST API supporting CRUD operations |
| 🗄️ MySQL | Relational database for persistent application data |
| 🐳 Docker | Containerization and image management |
| 💾 Docker Volumes | Persistent database storage |
| ☸️ Minikube | Local Kubernetes cluster |
| 📦 Kubernetes Pods | Run application and database containers |
| 🚀 Kubernetes Deployments | Manage replicas and application lifecycle |
| 🔌 Kubernetes Services | Stable networking and service discovery |
| 🔐 Kubernetes Secrets | Sensitive configuration and database credentials |
| 🗂️ Kubernetes ConfigMaps | Non-sensitive application configuration |
| 💿 PersistentVolumeClaims (PVCs) | Persistent storage requests |
| 🩺 Readiness & Liveness Probes | Application health monitoring |
| 🔧 Terraform | Infrastructure as Code and automation |
| 🖥️ PowerShell & VS Code | Local development and infrastructure management |

---

## 🧪 Testing & Validation

### ✅ Summary Table

| 🔢 Step | Goal | Tool / Location |
|---|---|---|
| 1️⃣ | Verify API availability | Flask `/ready` endpoint |
| 2️⃣ | Verify database connectivity | PyMySQL |
| 3️⃣ | Create a task | HTTP POST |
| 4️⃣ | Retrieve tasks | HTTP GET |
| 5️⃣ | Verify data persistence | MySQL / REST API |
| 6️⃣ | Load application image | Minikube |
| 7️⃣ | Deploy MySQL | Kubernetes Deployment |
| 8️⃣ | Configure persistent storage | Kubernetes PVC |
| 9️⃣ | Configure database networking | Kubernetes ClusterIP |
| 🔟 | Deploy Flask API | Kubernetes Deployment |
| 1️⃣1️⃣ | Verify API-to-MySQL connectivity | Kubernetes Pods / Services |
| 1️⃣2️⃣ | Validate application health | Readiness / Liveness Probes |
| 1️⃣3️⃣ | Test CRUD operations in Kubernetes | REST API endpoints |
| 1️⃣4️⃣ | Automate infrastructure provisioning | Terraform |

---

## 🧠 Behavior Confirmations

| 🔍 Verification Item | 📌 Status | 🧾 Evidence |
|---|---|---|
| Flask API runs locally | ✅ Confirmed | Docker container running |
| MySQL connectivity established | ✅ Confirmed | Successful PyMySQL connection |
| API readiness endpoint works | ✅ Confirmed | `/ready` returns `ready` |
| REST API creates tasks | ✅ Confirmed | HTTP POST returned task ID |
| REST API retrieves tasks | ✅ Confirmed | HTTP GET returned task |
| Docker API image built | ✅ Confirmed | `local-task-api:2.0` |
| Minikube image availability | ✅ Confirmed | Image verified in Minikube |
| Kubernetes MySQL Deployment | ⏳ In progress | Deployment and Pod validation |
| Kubernetes persistent storage | ⏳ Pending | PVC status `Bound` |
| Kubernetes API Deployment | ⏳ Pending | Pod status `Running` / `Ready` |
| Kubernetes service connectivity | ⏳ Pending | Internal API-to-MySQL communication |
| Kubernetes health probes | ⏳ Pending | Readiness and liveness validation |
| Terraform automation | ⏳ Planned | Local infrastructure provisioning |

---

## 🛡️ Security Controls & Design Principles

### 🔐 Security Implementation Objectives

- 🔒 **Credential Separation** — Store database credentials in Kubernetes Secrets
- 🗂️ **Configuration Separation** — Use ConfigMaps for non-sensitive application settings
- 🧱 **Service Isolation** — Keep MySQL accessible internally within the Kubernetes cluster
- 💾 **Persistent Data** — Separate database storage from container lifecycle
- 🩺 **Health Monitoring** — Configure readiness and liveness probes
- 🛡️ **Least Privilege** — Restrict permissions and resource access
- 🧾 **Infrastructure as Code** — Maintain reproducible and auditable infrastructure
- 🔍 **Observability** — Use Kubernetes logs, events, and resource status for troubleshooting
- 🚫 **Credential Protection** — Avoid hardcoding sensitive credentials in source code or container images

---

## 🎯 Security & Career Value

| Benefit | Description |
|---|---|
| 🐳 | Demonstrates containerization and image management |
| ☸️ | Develops practical Kubernetes orchestration experience |
| 🗄️ | Reinforces database architecture and persistence |
| 🔐 | Demonstrates secure configuration and secrets management |
| 🩺 | Shows understanding of application health and availability |
| 🔄 | Reinforces DevOps and deployment automation |
| 🏗️ | Demonstrates Terraform Infrastructure as Code |
| 🧠 | Develops cloud-native troubleshooting skills |
| 💼 | Aligns with Cloud Engineering, DevOps, Infrastructure, and Security roles |

---

## 🧹 Clean-Up Checklist

- 🛑 Stop or remove Kubernetes Deployments when no longer needed
- 🗑️ Delete Kubernetes Services and associated resources
- 🔐 Remove Kubernetes Secrets and ConfigMaps when appropriate
- 💾 Preserve or deliberately remove PersistentVolumeClaims and database data
- 🐳 Stop and remove Docker containers when no longer needed
- 🧼 Remove unused Docker images only after verifying they are no longer required
- ☸️ Stop Minikube when taking a break to reduce local resource consumption
- 🔧 Review Terraform-managed resources before executing `terraform destroy`
- ⚠️ Avoid deleting persistent database storage unless data loss is intentional

---

## 🎓 Learning Outcomes

- 🐍 Developed a **Python Flask REST API**
- 🗄️ Integrated a **MySQL relational database**
- 🐳 Containerized an application using **Docker**
- 💾 Implemented **persistent database storage**
- ☸️ Deployed applications using **Kubernetes Deployments and Pods**
- 🔌 Configured **Kubernetes Services and service discovery**
- 🔐 Applied **Secrets and ConfigMaps** for configuration management
- 🩺 Implemented **readiness and liveness probes**
- 🔧 Practiced **Terraform Infrastructure as Code**
- 🧠 Developed practical **cloud-native troubleshooting and DevOps skills**

---

*This project reflects real-world containerized application patterns commonly used in cloud and production environments, emphasizing security, persistence, orchestration, automation, and infrastructure integrity while remaining locally executable to minimize cloud costs.*
