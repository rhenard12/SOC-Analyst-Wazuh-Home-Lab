# 🛡️ SOC Analyst Home Lab – Wazuh SIEM Deployment & Troubleshooting

> A hands-on Security Operations Center (SOC) home lab built using Wazuh SIEM, Windows Server, Ubuntu Linux, and Oracle VirtualBox to simulate enterprise endpoint monitoring, agent deployment, and incident investigation.

![Status](https://img.shields.io/badge/Status-In%20Progress-blue)
![Platform](https://img.shields.io/badge/Platform-Windows%20Server%202025-blue)
![SIEM](https://img.shields.io/badge/SIEM-Wazuh-green)
![Virtualization](https://img.shields.io/badge/VirtualBox-Lab-orange)
![License](https://img.shields.io/badge/License-MIT-yellow)

---

# 📖 Overview

This project documents my journey of building a Security Operations Center (SOC) home lab using **Wazuh SIEM**.

The objective of this lab is to gain practical experience deploying security monitoring infrastructure, connecting Windows endpoints, investigating deployment issues, analyzing logs, and troubleshooting agent communication.

Rather than only documenting successful installations, this repository demonstrates the complete troubleshooting process that a SOC Analyst performs during real-world deployments.

---

# 🎯 Objectives

- Deploy Wazuh SIEM
- Configure Windows Server endpoint
- Install and register Wazuh Agent
- Monitor endpoint activity
- Investigate service failures
- Analyze logs
- Troubleshoot configuration issues
- Document findings using professional SOC methodology

---

# 🖥️ Lab Environment

| Component | Technology |
|-----------|------------|
| SIEM | Wazuh 4.x |
| Server | Ubuntu Linux |
| Endpoint | Windows Server 2025 |
| Virtualization | Oracle VirtualBox |
| Shell | Windows PowerShell |
| Logs | Windows Event Logs |
| Monitoring | Wazuh Agent |


---

# 🔧 Skills Demonstrated

- SIEM Deployment
- Windows Server Administration
- Linux Administration
- PowerShell
- VirtualBox
- Endpoint Monitoring
- Log Analysis
- Windows Services
- Troubleshooting
- Security Monitoring
- Blue Team Operations
- Incident Investigation

---

# 📷 Deployment Process

## Step 1 – Access Wazuh Dashboard

- Verified Wazuh dashboard accessibility
- Reviewed security modules
- Confirmed dashboard health

---

## Step 2 – Deploy Windows Agent

- Generated deployment package
- Copied PowerShell installation command
- Installed Windows Agent

---

## Step 3 – Register Endpoint

Successfully authenticated the Windows endpoint with the Wazuh Manager.

Example output:

```
INFO: Requesting a key from server
INFO: Waiting for server reply
INFO: Valid key received
```

---

## Step 4 – Troubleshooting

During deployment the Windows service failed to start.

Observed message:

```
The Wazuh service could not be started.
```

This required additional investigation.

---

# 🔍 Investigation

The following troubleshooting steps were performed:

- Verified Windows Service status
- Reviewed PowerShell output
- Checked Wazuh installation
- Examined ossec.log
- Opened ossec.conf
- Verified server configuration
- Confirmed agent authentication

---

# 🚨 Root Cause

The Wazuh Agent configuration contained an invalid server address.

```
<address>0.0.0.0</address>
```

The agent log reported:

```
ERROR: Invalid server address found: '0.0.0.0'
```

---

# 🛠️ Resolution

- Identified incorrect manager address
- Updated configuration
- Restarted Wazuh service
- Verified communication with manager

---

# 📁 Repository Structure

```
SOC-Analyst-Wazuh-Home-Lab
│
├── README.md
├── Incident_Report.md
├── Troubleshooting.md
├── MITRE_Attack.md
├── screenshots
└── architecture
```

---

# 📚 MITRE ATT&CK Mapping

| Tactic | Technique |
|---------|-----------|
| Discovery | T1082 – System Information Discovery |
| Execution | T1059 – Command and Scripting Interpreter |
| Defense Evasion | T1562 – Impair Defenses |
| Command and Control | T1071 – Application Layer Protocol |

---

# 📖 Lessons Learned

This project strengthened my understanding of:

- SIEM deployment
- Endpoint monitoring
- Windows services
- Agent authentication
- Log analysis
- Troubleshooting enterprise software
- Security documentation

---

# 🚀 Future Improvements

- Install Sysmon
- Create custom Wazuh detection rules
- Simulate brute-force attacks
- Perform Nmap scans
- Integrate VirusTotal
- Generate alerts
- Create incident response playbooks
- Build dashboards for threat hunting

---

# 👨‍💻 About Me

I am transitioning into Cybersecurity with a focus on SOC Analyst and Blue Team operations.

This repository is part of my cybersecurity portfolio documenting hands-on projects involving:

- Wazuh
- Active Directory
- Windows Server
- Linux
- VirtualBox
- PowerShell
- Network Security
- Incident Response



