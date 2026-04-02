# Building the Foundation: AWS EC2, Secure Shell (SSH), and Server Observability

## 📌 Overview
As part of my journey to become a Cloud & DevOps Engineer, I am documenting my progression from manual server management to full infrastructure automation. This module covers the foundational steps of provisioning cloud compute resources, securing access, and implementing basic server observability.

## 🛠️ Tech Stack & Tools
* **Cloud Provider:** Amazon Web Services (AWS)
* **Compute:** EC2 (Elastic Compute Cloud)
* **Security:** Key Pairs (Asymmetric Encryption), Security Groups
* **Terminal:** Git Bash / Linux CLI
* **Observability:** Nginx/Apache Access & Error Logs

--------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 🚀 Key Milestones Achieved

### 1. Compute Provisioning (AWS EC2)
Instead of relying on local hardware, I provisioned virtual servers in the cloud. 
* Launched an **Ubuntu Linux** EC2 instance.
* Configured the **Security Group** (Firewall) to allow **Inbound HTTP (Port 80)** traffic for web access, while strictly locking down **SSH (Port 22)** to my specific IP address based on the Principle of Least Privilege.

### 2. Secure Authentication (SSH)
Security is the first step in DevOps. I bypassed traditional password authentication by implementing **Public Key Infrastructure (PKI)**.
* Utilized a `.pem` Private Key file to establish a secure connection.
* Applied strict Linux file permissions (`chmod 400 key.pem`) to ensure the private key remained read-only to the owner, preventing unauthorized access and terminal warnings.
* Connected to the remote server using the **Secure Shell (SSH)** protocol via Git Bash.

### 3. Observability & Troubleshooting (Log Analysis)
A system engineer doesn't guess; they read the logs. I navigated the Linux file system to monitor real-time server traffic and diagnose issues.
* **Access Logs:** Monitored `/var/log/nginx/access.log` (or Apache equivalent) to track incoming HTTP requests, client IP addresses, and response status codes (e.g., 200 OK, 404 Not Found).
* **Error Logs:** Investigated `/var/log/nginx/error.log` to identify broken configurations or missing files, establishing a proactive troubleshooting mindset.

--------------------------------------------------------------------------------------------------------------------------------------------------------------------


## 🧠 The "Productive Lazy" Takeaway
While launching servers manually via the AWS Console is a necessary learning step, doing it repeatedly is inefficient. 

By understanding the underlying mechanics of SSH, Security Groups, and Log Paths, I am now prepared for the next phase: **Infrastructure as Code (IaC)**. The ultimate goal is to codify these exact steps using **Terraform** and **Bash Scripting** so this entire architecture can be deployed in seconds without human intervention.

> *"If you have to do it twice, automate it."*

--------------------------------------------------------------------------------------------------------------------------------------------------------------------
**Author:** Pranit Patil  
**Role:** Aspiring Cloud & DevOps Engineer  
**Location:** Pune, India
