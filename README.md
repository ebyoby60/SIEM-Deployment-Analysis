 SIEM-Deployment-Analysis
SIEM Environment Deployment & Risk Analysis 

 Project Overview
This project demonstrates the deployment of a Security Information and Event Management (SIEM) stack using Elasticsearch and Kibana on an Ubuntu server. The environment is designed to ingest and analyze security telemetry from a Cowrie Honeypot, mapping attacker activity to industry-standard frameworks.

Technical Stack
Operating Systems: Ubuntu 24.04 (SIEM Node), Kali Linux (Attacker Node)
Tools: ELK Stack (Elasticsearch, Kibana), Cowrie, UFW, VMware Workstation
Frameworks: NIST RMF, MITRE ATT&CK

🚀 Key Features & Implementation
Centralized Logging: Configured Elasticsearch as the primary data store for security events.
Remote Monitoring: Modified `kibana.yml` to bind to `0.0.0.0`, enabling cross-VM access from Kali Linux.
Network Security: Implemented firewall rules via `UFW` to secure ports 5601 and 9200.
Resource Optimization: Managed high-load environments (89% RAM utilization) using Linux service management (`systemctl`, `daemon-reload`).

 🛡️ Cybersecurity Analysis
 MITRE ATT&CK Mapping
The honeypot environment is specifically tuned to detect:
T1110 (Brute Force): Identifying credential stuffing on SSH services.
T1021 (Remote Services): Monitoring for unauthorized lateral movement attempts.

 AI Risk Management
This project incorporates research into securing AI agents against:
Prompt Injection: Mitigated via input sanitization and instruction isolation.
Data Poisoning: Addressed through model provenance and strict access controls.

 📉 Troubleshooting & Resolution
During deployment, the system encountered **Hardware Resource Exhaustion (CPU Soft Lockup)**. 
Diagnosis: Identified 89.2% RAM usage via terminal monitoring.
Resolution: Applied the NIST Risk Management Framework (RMF) to document the incident, optimize service start-sequences, and implement swap-space tuning to maintain system availability.

 📁 Repository Structure
```text
├── config/             # kibana.yml and firewall scripts
├── logs/               # Sample Cowrie event logs
└── report/             # Full technical documentation (PDF)
Author: Mbakpobe Adaeze

Cybersecurity Analyst & Technology Risk Professional
