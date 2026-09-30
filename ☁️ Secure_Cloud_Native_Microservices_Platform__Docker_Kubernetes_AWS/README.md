# ☁️ Secure Cloud-Native Microservices Platform

🧪 *A Hands-On Cloud-Native Project Demonstrating Containerization, Kubernetes Orchestration, Service Resilience, and AWS Deployment Patterns*

---

## 📌 Project Description

This project demonstrates a **containerized microservices architecture** designed to explore practical cloud-native infrastructure, Kubernetes orchestration, application resilience, and AWS deployment patterns.

The project begins with a Python/Flask backend packaged into a Docker image and deployed locally using **Minikube/Kubernetes**. The architecture is progressively extended to demonstrate Kubernetes Deployments, Services, health checks, self-healing, horizontal scaling, and eventually AWS services such as **Amazon ECR and Amazon EKS**.

Rather than focusing solely on application development, the project emphasizes the **infrastructure and operational characteristics surrounding a cloud-native workload**—including container lifecycle management, service availability, orchestration, health monitoring, scalability, and secure cloud deployment.

The project is designed as a practical learning environment for **cloud infrastructure, systems administration, DevOps, DevSecOps, and cloud security**.

---

## 🚀 Key Steps Implemented / Planned

- 🐍 **Develop Flask backend** with health and application endpoints
- 📦 **Manage Python dependencies** using `requirements.txt`
- 🐳 **Containerize the application** using Docker
- 🏷️ **Version Docker images** using explicit image tags
- ☸️ **Deploy containers to Kubernetes** using Minikube
- 🧩 **Create Kubernetes Deployments** for application workloads
- 🔌 **Expose workloads through Kubernetes Services**
- ❤️ **Implement liveness and readiness health checks**
- 🔄 **Demonstrate Kubernetes self-healing** through Pod replacement
- 📈 **Scale application workloads** using Kubernetes replicas
- ⚖️ **Implement Horizontal Pod Autoscaling (HPA)**
- 🖥️ **Introduce a frontend microservice**
- ☁️ **Publish container images to Amazon ECR**
- ☸️ **Deploy the workload to Amazon EKS**
- ⚖️ **Explore AWS load balancing and service exposure**
- 🔐 **Integrate AWS IAM and Secrets Manager**
- 📊 **Explore CloudWatch-based monitoring and observability**

---

## 🧱 Core Components

| Component | Description |
|---------|-------------|
| 🐍 Flask | Lightweight Python backend application |
| 📄 `requirements.txt` | Defines Python application dependencies |
| 🐳 Docker | Packages the application and dependencies into a portable image |
| 🏷️ Docker Tags | Provides explicit image versioning such as `dva-backend:1.0` |
| ☸️ Kubernetes | Container orchestration platform |
| 🧪 Minikube | Local Kubernetes development environment |
| 🚀 Deployment | Manages desired Pod replicas and application lifecycle |
| 🔌 Service | Provides stable network access to Kubernetes Pods |
| ❤️ Health Probes | Supports Kubernetes readiness and liveness decisions |
| 🔄 Self-Healing | Demonstrates automatic replacement of failed Pods |
| 📈 Scaling | Demonstrates horizontal workload scaling |
| ⚖️ HPA | Automatically adjusts Pod replicas based on resource utilization |
| 📦 Amazon ECR | AWS container image registry |
| ☁️ Amazon EKS | Managed Kubernetes service |
| 🔐 IAM | AWS identity and access management |
| 🔑 Secrets Manager | Secure application secret management |
| 📊 CloudWatch | AWS monitoring and observability |

---

## 🧪 Testing & Validation

### ✅ Summary Table

| 🔢 Step | Goal | Tool / Command |
|-------|------|----------------|
| 1️⃣ | Validate Flask application syntax | `python -m py_compile app.py` |
| 2️⃣ | Verify local Flask health endpoint | `Invoke-RestMethod http://localhost:5000/health` |
| 3️⃣ | Build Docker image | `docker build -t dva-backend:1.0 .` |
| 4️⃣ | Verify Docker image | `docker images` |
| 5️⃣ | Run application inside Docker | `docker run -p 5000:5000 dva-backend:1.0` |
| 6️⃣ | Test containerized application | `Invoke-WebRequest ... -UseBasicParsing` |
| 7️⃣ | Load image into Minikube | `minikube image load dva-backend:1.0` |
| 8️⃣ | Deploy application to Kubernetes | `kubectl apply -f ...` |
| 9️⃣ | Verify Kubernetes Pods | `kubectl get pods` |
| 🔟 | Verify Kubernetes Service | `kubectl get services` |
| 1️⃣1️⃣ | Test application through Service | `kubectl port-forward ...` |
| 1️⃣2️⃣ | Test self-healing | `kubectl delete pod ...` |
| 1️⃣3️⃣ | Scale workload | `kubectl scale deployment ...` |
| 1️⃣4️⃣ | Monitor resource utilization | `kubectl top pods` |
| 1️⃣5️⃣ | Configure HPA | `kubectl autoscale deployment ...` |

---

## 🧪 Behavior Confirmations

| 🔍 Verification Item | 📌 Status | 🧾 Evidence |
|---------------------|-----------|-------------|
| Flask application starts successfully | ✅ | Application startup output |
| `/health` endpoint responds | ✅ | HTTP `200` response |
| Docker image builds successfully | ✅ | `docker build` completion |
| Flask dependencies installed inside image | ✅ | Docker build output |
| Container starts successfully | 🔄 | Docker runtime validation |
| Kubernetes Deployment creates Pods | 🔄 | `kubectl get pods` |
| Kubernetes Service exposes backend | 🔄 | Service/port-forward testing |
| Failed Pod is automatically replaced | 🔄 | Pod deletion/recreation |
| Application scales horizontally | 🔄 | Replica count validation |
| HPA adjusts workload replicas | 🔄 | HPA metrics/output |
| Image deployed through Amazon ECR | 🔄 | AWS deployment validation |
| Workload deployed to Amazon EKS | 🔄 | EKS cluster validation |

> 🔄 **Status:** Items marked as 🔄 represent planned or progressive stages of the project and will be updated as they are implemented.

---

## 🛡️ Security & Infrastructure Design Principles

### 🔐 Security Considerations

- 🔒 Avoid hardcoding application secrets into source code
- 🔑 Use appropriate secret-management mechanisms for sensitive configuration
- 🧩 Apply least-privilege IAM principles when integrating AWS services
- 📦 Treat container images as deployable infrastructure artifacts
- 🔍 Validate application and infrastructure configuration before deployment
- 🛡️ Separate application, container, and infrastructure concerns
- 🧾 Maintain reproducible infrastructure and deployment configuration
- 📊 Incorporate monitoring and operational visibility into cloud deployments

---

## 🏗️ Architecture Evolution

### Phase I — Local Application

```text
🐍 Flask Application
        │
        ▼
🖥️ Windows / Python
        │
        ▼
🧪 Local Testing
```
---

### Phase II - Containerisation
<br>

```text
🐍 Flask<br> 
      │
      ▼
<br> 📄 requirements.txt <br> 
      │
      ▼
<br> 🐳 Dockerfile <br>
      │
      ▼
<br> 📦 dva-backend:1.0 <br>
      │
      ▼
<br> 🐳 Docker Container <br>
```

