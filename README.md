# SOC-Analyst-Wazuh-Home-Lab
SOC Analyst Home Lab using Wazuh SIEM, Windows Server 2022, Kali Linux, MITRE ATT&amp;CK, and real-world security event investigations.
Windows VM

↓

Wazuh
      

Windows Agent failed to start.

Symptoms

Service stopped immediately.

Investigation

Reviewed ossec.log

Verified Windows Services

Checked configuration

Found incorrect manager IP

Root Cause

Manager configured as

0.0.0.0

Resolution

Updated ossec.conf

Restarted Wazuh

Verified communication

Result

Agent connected successfully.

Linux Administration

Windows Server

PowerShell

VirtualBox

Networking

TCP/IP

Log Analysis

Threat Detection

SIEM

MITRE ATT&CK

Incident Response

Troubleshooting

Endpoint Security

Blue Team Operations
