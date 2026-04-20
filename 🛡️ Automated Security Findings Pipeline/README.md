# 🛡️ Automated Security Findings Pipeline

🔐 *A DevSecOps pipeline that used pre-deployment and post-scan analysis to transform infrastructure security findings into structured, actionable security events*

---

## 📌 Project Description

This project implemented a **cloud-native security data processing pipeline** designed to ingest and process **Infrastructure-as-Code (IaC) scan results** from multiple security tools and transform them into **standardised, audit-ready security events**.

The pipeline incorporated both **preventative scanning (Checkov)** and **post-scan analysis (tfsec)** to ensure misconfigurations were identified **before and after deployment stages**. Raw outputs were normalised into structured JSON records, enabling **consistent security visibility**, **compliance tracking**, and **integration with downstream cloud services**.

**Built within a Windows-based PowerShell environment, the solution emphasized:**
<br>- Shift-left security
<br>- Data transformation
<br>- Network automation
<br>- Secure cloud ingestion<br>
<br>The components used in this project reflected real-world DevSecOps best practices and demonstrated hands-on experience with:
<br>- **Multi-tool security orchestration
<br>- CLI workflows
<br>- Cloud storage integration**
<br>The workflow reinforced a strong focus on **data integrity and observability**.

---

## 🚀 Key Steps Simulated in This Project

- 🛡️ **Scanned IaC configurations (pre-deployment)** using Checkov  
- 🔍 **Performed static security analysis (post-scan)** using tfsec
- 🔄 **Parsed and extracted security findings** from scan results in JSON
- 🧠 **Normalised security data** using `jq` transformations  
- 🧩 **Mapped findings into structured security events** (rule_id, severity, status)  
- 📦 **Aggregated multi-tool findings into a unified format**  
- ☁️ **Uploaded processed results to cloud storage (S3)**  
- 🔐 **Validated secure API interactions** via AWS CLI  
- 📡 **Enabled downstream consumption** for analytics and compliance systems  

---

## 🧱 Core Components

| Component | Description |
|----------|-------------|
| 🛡️ Checkov Scanner | Performed pre-deployment IaC security checks (shift-left validation) |
| 🛡️ tfsec Scanner | Performed Terraform static analysis for misconfigurations |
| 🧠 jq Transformation Engine | Normalised and restructured raw security findings |
| 🔄 PowerShell CLI Layer | Orchestrated scanning, transformation, and metwork automation |
| 📄 Cleaned JSON Output | Stored structured, normalized security events |
| ☁️ Amazon S3 Bucket | Stored and processed security artifacts for persistence |
| 🔐 AWS CLI | Authenticated upload and interactions with S3 |
| 📡 S3 API Endpoint | Enabled secure ingestion and storage of security data |

---

## 🧪 Testing & Validation

### ✅ Summary Table

| 🔢 Step | Goal | Tool / Command |
|-------|------|----------------|
| 1️⃣ | Completed pre-deployment security scan | `checkov -d . --output json` |
| 2️⃣ | Generated Terraform findings | `tfsec --format json` |
| 3️⃣ | Validated raw JSON structure | `jq . tfsec_output.json` |
| 4️⃣ | Transformed & normalised data | `jq '[.results[] | {...}]'` |
| 5️⃣ | Validated cleaned JSON output | `ConvertFrom-Json` |
| 6️⃣ | Uploaded to cloud storage | `aws s3 cp cleaned.json` |

---

### 🧠 Behavior Confirmations

| 🔍 Verification Item | 📌 Status | 🧾 Evidence |
|---------------------|-----------|-------------|
| Pre-deployment misconfigurations detected | ✅ | Checkov scan results |
| Security findings generated correctly | ✅ | tfsec JSON output |
| Data transformation executed successfully | ✅ | jq structured output |
| JSON integrity validated | ✅ | PowerShell parsing success |
| File uploaded to S3 | ✅ | AWS CLI upload confirmation |
| Secure API interaction established | ✅ | HTTPS PUT (200 OK response) |

---

## 🛡️ Security Awareness & Design Principles

### 🔐 What Was Implemented

- 🛡️ **Shift-left security validation** using Checkov before deployment  
- ✅ Structured **security event normalization** for consistency  
- 🔐 Network automation using AWs SDK (boto3) 
- 🧾 Strong emphasis on **log integrity, centralised visibility, and actionable threat detection &nbsp;&nbsp;signals  
- 🧠 Clear mapping of raw findings → actionable security records  
- 🧩 Modular pipeline architecture aligned with **DevSecOps best practices**  

---

## 🎯 Learning Outcomes

- 🛡️ Built a **multi-stage DevSecOps security pipeline (pre + post scan)**  
- 🔄 Practiced **JSON transformation and normalization using jq**  
- 🧠 Learned to **correlate findings across multiple security tools**  
- ☁️ Integrated **local tooling with AWS cloud services**  
- 🔐 Reinforced **secure data handling and audit readiness**  
- 📊 Enabled **security observability through structured outputs**  

---

*This project reflects real-world DevSecOps patterns by combining preventative and detective security controls, transforming raw scan data into structured, cloud-ingested intelligence for scalable monitoring and compliance workflows.*
