
# 🌐 Linux Network Health Check

🧪 *A Beginner Bash Utility for Validating Network Connectivity, DNS Health, and Local Port Exposure*

---

## 📌 Project Description

This project demonstrates a **modular Bash-based network diagnostic tool** designed to perform **core Linux network health checks** commonly used in enterprise and security-focused environments.

The script provides a menu-driven interface to validate **internet connectivity**, **DNS resolution**, and **local listening ports**, with additional logic to identify **commonly risky services** exposed on a host. Emphasis is placed on **script structure, process handling, and terminal usability**, rather than advanced tooling.

Designed as a hands-on learning project, it showcases **practical Bash scripting fundamentals**, Linux networking concepts, and foundational security awareness—making it well-suited for early-career cloud, systems, and security roles.

Part I<br>
![Alt Text](800x500_1.jpg)

---

## 🚀 Key Steps Simulated in This Project

- 🔌 **Check external network connectivity** using ICMP (`ping`)
- 🧭 **Validate DNS resolution** using system name services
- 🔍 **Enumerate listening ports** and active services
- ⚠️ **Identify commonly risky open ports** (e.g., SSH, database services)
- 🧩 **Structure logic into reusable Bash functions**
- 🧭 **Present a menu-driven CLI interface** for user interaction
- ⏳ **Provide visual feedback** using spinners and ASCII banners
- 🎨 **Enhance terminal UX** with ANSI colors and icons

---

## 🧱 Core Components

| Component | Description |
|---------|-------------|
| 🐚 Bash Script | Modular shell script implementing all checks |
| 🔌 ICMP Check | Tests external reachability via `ping` |
| 🧭 DNS Check | Validates name resolution using `getent` |
| 🔍 Port Enumeration | Lists active listening ports via `ss` |
| ⚠️ Risk Logic | Flags commonly abused or sensitive ports |
| ⏳ Spinner | Displays progress during background tasks |
| 🎨 Terminal UX | ANSI colors, icons, and ASCII section headers |

---

## 🧪 Testing & Validation

### ✅ Summary Table (Mit Ikons)

| 🔢 Step | Goal | Tool / Command |
|-------|------|----------------|
| 1️⃣ | Verify internet reachability | `ping 9.9.9.9` |
| 2️⃣ | Confirm DNS resolution | `getent hosts` |
| 3️⃣ | List active listening ports | `ss -tulpn` |
| 4️⃣ | Detect risky exposed ports | Port comparison logic |
| 5️⃣ | Validate script flow & UX | Menu + spinner output |

---

### 🧠 Behavior Confirmations

| 🔍 Verification Item | 📌 Status | 🧾 Evidence |
|---------------------|-----------|-------------|
| Connectivity test executes correctly | ✅ | ICMP success/failure output |
| DNS resolution validated | ✅ | Host lookup response |
| Listening ports enumerated | ✅ | `ss` output displayed |
| Risky ports identified accurately | ✅ | Ports listed only when open |
| Spinner reflects background execution | ✅ | PID-based spinner behavior |

---

## 🛡️ Security Awareness & Design Principles

### 🔐 What Was Implemented

- ✅ Awareness of **common high-risk ports** (SSH, database, legacy services)
- 🧠 Separation of **logic into functions** for clarity and maintainability
- 🧾 No hardcoded credentials or secrets
- 🧩 Modular sourcing (`functions.sh`) reflecting real-world script design
- 🎯 Clear output to avoid ambiguous security findings

---

### 🎯 Security & Career Value

| Benefit | Description |
|-------|-------------|
| 🛡️ | Reinforces baseline host security awareness |
| 🧠 | Builds confidence with Linux networking tools |
| 🔧 | Demonstrates clean Bash scripting practices |
| ⏳ | Introduces background jobs and PID handling |
| 💼 | Strong foundational project for sysadmin & security paths |

---

## 🧹 Clean-Up Checklist

- 🧼 Exit script cleanly via menu option
- 📺 Clear terminal output after execution (optional)
- 🧩 Remove sourced functions if used in shared environments

---

## 🎯 Learning Outcomes

- 🐚 Built **modular Bash scripts** using functions and sourcing
- 🔌 Practiced **core Linux network diagnostics**
- 🔍 Learned how services expose ports on a system
- ⏳ Implemented **background execution with spinners**
- 🎨 Improved **terminal user experience** using ANSI styling

---

*This project reflects foundational network and scripting patterns commonly encountered in Linux administration and security environments, serving as a solid stepping stone toward more advanced automation and DevSecOps tooling.*
