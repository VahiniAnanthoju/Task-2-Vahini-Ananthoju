# 🖥️ Project 2: The Server Commander

> **Provisioning. Securing. Commanding.**

## 📋 Overview

A hands-on SysAdmin project where you act as a cloud infrastructure engineer to provision, configure, and serve a live web page from a virtual machine in the cloud.

---

## 🎯 Scenario

A startup is launching a new dynamic application and needs a dedicated server environment. They require full control over the Operating System (OS) to install custom software and security patches.

---

## 🚀 Mission

Act as a **SysAdmin** and provision a virtual server in the cloud by completing the following tasks:

- ☁️ Launch a **Virtual Machine (EC2/VM)** using Linux (Ubuntu / Amazon Linux)
- 🔐 Connect to the server securely using **SSH**
- 🌐 Install a **Web Server (Nginx)** via the command line
- 🏠 Host a custom **"Welcome to DecodeLabs"** webpage on the server

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|------|---------|
| **AWS EC2 / Azure Virtual Machines** | Cloud VM provisioning |
| **Terminal** | Command-line operations |
| **SSH** | Secure server connection |
| **Nginx** | Web server installation |
| **Linux (Ubuntu / Amazon Linux)** | Operating System |

---

## 📁 Project Structure

```
server-commander/
├── README.md
├── index.html          # Custom "Welcome to DecodeLabs" webpage
└── setup-notes.md      # Optional: commands and steps used
```

---

## 🧭 Step-by-Step Guide

### 1. Launch a VM
- Go to **AWS EC2** or **Azure Virtual Machines**
- Choose **Ubuntu 22.04 LTS** or **Amazon Linux 2**
- Select instance type (e.g., `t2.micro` for free tier)
- Configure Security Group to allow **port 22 (SSH)** and **port 80 (HTTP)**
- Launch and download your `.pem` key pair

### 2. Connect via SSH
```bash
ssh -i "decodelabs-key.pem" ubuntu@<your-public-ip>
```

### 3. Install Nginx
```bash
sudo apt update
sudo apt install nginx -y
sudo systemctl start nginx
sudo systemctl enable nginx
```

### 4. Host the Webpage
```bash
sudo nano /var/www/html/index.html
```

Paste your custom HTML content and save. Then visit:
```
http://13.206.255.225
```

---

## ✅ Completion Criteria

- [ ] VM successfully launched on AWS EC2 or Azure
- [ ] SSH connection established
- [ ] Nginx installed and running
- [ ] Custom "Welcome to DecodeLabs" page accessible via browser

---

## 👤 Author

**Vahini Ananthoju**  
GitHub: [@VahiniAnanthoju](https://github.com/VahiniAnanthoju)
