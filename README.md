# Ubuntu Headless Infrastructure & AI-Driven Administration

## 📌 Overview
This repository contains the architectural documentation and implementation details of a multi-service Linux headless server (Ubuntu Server 25.04). It was developed as a **collaborative team project** to demonstrate the integration of core networking services, security hardening, external internet exposure, and an AI-based CLI assistant.

## 👥 Team & Roles
This project was divided into two main engineering pillars to simulate a real-world DevOps/SRE environment:

### 🛠️ Infrastructure, Networking & Security (My Contribution - Rodolfo Coelho)
I was responsible for provisioning the platform, securing the perimeter, and ensuring reliable external access:
* **Core OS & Daemons:** Configuration and status validation (`systemctl`) of the headless environment, **OpenSSH**, **Apache2**, **Samba**, and **MySQL**.
* **Networking & External Access:** Strategic implementation of NAT rules, **Port Forwarding**, and dynamic DNS (**DDNS via No-IP**) to securely expose the internal server to the WAN.
* **Security Hardening:** Strict firewall management using **UFW** to restrict incoming traffic exclusively to necessary ports (22, 80, 137-139, 445).

### 🤖 AI Integration & LLM Training (Co-Author - Nuno Salvação)
My colleague focused on the software and artificial intelligence layer:
* **NexoCli Implementation:** Deploying and configuring a fork of Google's `gemini-cli` within the Node.js environment.
* **Context Training:** Customizing the LLM context files (`.md`) to give the AI agent persistent awareness of the server's environment for system administration troubleshooting.

## 📄 Architectural Whitepaper
The full technical report, including network diagrams, firewall rule validations, and AI CLI deployment steps, is available in this repository:
👉 **[View the full Infrastructure Architecture Report (PDF) here](./Infrastructure_Architecture_Report.pdf)**

## 🚀 Relevance for SRE / Cloud Engineering
A core aspect of Site Reliability Engineering is building robust platforms that enable developers and data scientists to deploy their tools securely. This project proves my ability to collaborate in a cross-functional team, taking full ownership of the network flow—from the public internet into a secure internal firewall—providing a highly available foundation for an AI application to run.

*Tech Stack: Ubuntu Server 25.04, UFW, Apache2, MySQL, Samba, DDNS, Node.js, NexoCli (LLM/GenAI), SSH/SFTP.*
