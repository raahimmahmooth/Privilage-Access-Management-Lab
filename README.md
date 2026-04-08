# 🔐 Privileged Access Management (PAM) Lab on Azure

I built and configured a complete **Privileged Access Management (PAM) lab environment** on Microsoft Azure using Senhasegura to simulate real-world enterprise security operations.

---

## 🎯 Objective

The goal of this project was to:

- Understand how organizations secure privileged accounts  
- Implement centralized credential management  
- Enforce controlled and monitored access to critical systems  
- Gain hands-on experience with PAM deployment in a cloud environment  

---

## 🏗️ Architecture Overview

This lab environment consists of:

- 🖥️ Linux VM (Target system)  
- 🪟 Windows VM (Target system)  
- 🔐 Senhasegura PAM Server  
- 🌐 Azure Virtual Network (VNet)  

---

## 🌐 Azure Networking Configuration

To ensure secure communication:

- Configured **Virtual Network (VNet)** and subnets  
- Implemented **VNet Peering**  
- Applied **Network Security Groups (NSGs)** to:
  - Allow required ports (SSH, RDP, WinRM)
  - Restrict unnecessary traffic  
- Verified connectivity using internal IP communication  

---

## ⚙️ PAM Implementation (Senhasegura)

Using Senhasegura PAM Core, I configured:

- Credential onboarding (Linux & Windows)  
- Secure password vaulting  
- Session proxy access (SSH, RDP)  
- Session monitoring and logging  
- Access control policies  

---

## 🔄 Password Management & Automation

- Configured **automatic password rotation**  
- Used:
  - Linux password change templates (sudo/root)  
  - Windows password change via WinRM  
- Implemented:
  - Execution plugins  
  - Change templates  

---

## 🧪 System Integration

### 🪟 Windows (WinRM)

- Enabled WinRM (port 5985)  
- Fixed issues related to:
  - Firewall rules  
  - Network profile (Public → Private)  
  - Listener configuration  
- Verified using:
  ```bash
  netstat -ano | findstr 5985
  curl http://<ip>:5985

  # 🔐 Privileged Access Management (PAM) Deployment & Troubleshooting Project

## 📖 Overview
This project demonstrates hands-on experience in deploying, configuring, and troubleshooting a **Privileged Access Management (PAM)** solution using **Senhasegura** in a cloud-based environment.

It focuses on secure access control, credential management, and real-world issue resolution across Linux, Windows, and containerized services.

---

## 🐧 Linux Configuration
- Configured **SSH-based access**
- Enabled **sudo automation** for password rotation
- Verified **non-interactive command execution**

---

## 🐳 Docker & Service Management
Managed Senhasegura services using Docker:

- `proxy-rdp`
- `proxy-terminal`
- `proxy-core`

### 🔧 Tasks Performed
- Created and modified **systemd service files**
- Troubleshot:
  - Container startup failures
  - Service dependency issues
  - Restart persistence after reboot

---

## 🛠️ Key Challenges & Fixes

### ❌ WinRM port not accessible after reboot  
✅ Enabled **PowerShell Remoting (PSRemoting)** and configured listeners  

### ❌ Password rotation failures in Linux  
✅ Fixed **sudo automation** and aligned templates  

### ❌ Proxy services failing (Docker/systemd)  
✅ Corrected **service configurations** and dependencies  

### ❌ Session not establishing  
✅ Debugged **proxy containers** and network communication  

---

## 🚀 Key Skills Gained

- 🔐 Privileged Access Management (PAM)
- ☁️ Azure Networking (VNet, NSG, Peering)
- 🪟 Windows Remote Management (WinRM)
- 🐧 Linux Administration & Sudo Automation
- 🐳 Docker & Service Troubleshooting
- 🔑 Secure Credential Management
- 🧠 Real-world Debugging & Incident Resolution

---

## 📌 Conclusion
This project provided practical exposure to deploying and managing a **real-world PAM solution** in a cloud environment.

It strengthened my understanding of how enterprises:

- Protect privileged accounts  
- Enforce secure access controls  
- Automate credential lifecycle management  

---

## 📎 Notes
- Environment included **Linux & Windows systems**
- Focused on **security, automation, and reliability**
- Emphasized **real-world troubleshooting scenarios**
