# Ubuntu Headless Infrastructure & AI-Driven Administration

## 📌 Overview
This repository contains the architectural documentation and implementation details of a multi-service Linux headless server (Ubuntu Server 25.04). It demonstrates the end-to-end deployment of core networking services, security hardening, external internet exposure, and the integration of a modern AI-based CLI assistant for system administration.

## ⚙️ Core Architecture & Services
The infrastructure was built from the ground up without a graphical interface (Headless), focusing entirely on CLI management and automation:
* **Core Daemons:** Configuration and status validation (`systemctl`) of **OpenSSH**, **Apache2** (HTTP Server), **Samba** (SMB/CIFS file sharing), and **MySQL** (Database).
* **Networking & External Access:** Strategic implementation of NAT rules, **Port Forwarding**, and dynamic DNS (**DDNS via No-IP**) to securely expose the internal server to the WAN.
* **Security Hardening:** Strict firewall management using **UFW** to restrict incoming traffic exclusively to necessary ports (22, 80, 137-139, 445).

## 🤖 NexoCli: AI-Assisted System Management
To push the boundaries of traditional system administration, this project integrates **NexoCli** (a fork of Google's `gemini-cli`). 
* The server was configured with Node.js environments to run LLM-based queries directly in the terminal.
* Custom context files (`.md` pushed via SFTP) were used to give the AI agent persistent awareness of the server's environment, allowing for natural language troubleshooting and intelligent log analysis.

## 📄 Architectural Whitepaper
The full technical report, including network diagrams, firewall rule validations, and AI CLI deployment steps, is available in this repository:
👉 **[View the full Infrastructure Architecture Report (PDF) here](./Infrastructure_Architecture_Report.pdf)**

## 🚀 Relevance for SRE / Cloud Engineering
A modern Site Reliability Engineer must understand the entire stack—from bare-metal OS networking and firewall rules to advanced tooling. This project proves a holistic understanding of how traffic flows from the public internet into a secure internal service, and showcases an innovative approach to reducing operational *toil* using AI.

*Tech Stack: Ubuntu Server 25.04, UFW, Apache2, MySQL, Samba, DDNS, Node.js, NexoCli (LLM/GenAI), SSH/SFTP.*
