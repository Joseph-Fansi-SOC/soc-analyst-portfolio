# 🧠 Detection Engineering Notes

## Purpose

This document tracks detection engineering concepts, methodologies, and improvements developed during SOC training.

---

# Detection Lifecycle

## 1. Threat Intelligence

Sources:

- CyberDefenders investigations
- MITRE ATT&CK
- VirusTotal
- MalwareBazaar
- ThreatFox

Goal:

Understand attacker behavior before creating detections.

---

# 2. Data Sources

Common telemetry:

## Endpoint

- Windows Event Logs
- Sysmon
- Wazuh agents

## Network

- PCAP
- Firewall logs
- IDS alerts

## Authentication

- Login events
- Privilege changes
- Remote access

---

# 3. Detection Examples

## PowerShell Abuse

MITRE:

```
T1059.001 - PowerShell
```

Detection idea:

Detect encoded or suspicious PowerShell execution.

---

## PsExec Lateral Movement

MITRE:

```
T1569.002 - Service Execution
T1021.002 - SMB/Windows Admin Shares
```

Detection idea:

Detect:

- PSEXESVC.exe creation
- ADMIN$ access
- Remote service creation

---

## Web Shell Activity

MITRE:

```
T1505.003 - Web Shell
```

Detection idea:

Detect:

- Suspicious PHP uploads
- Unexpected server-side scripts
- Reverse shell behavior

---

# Future Development

Planned additions:

- Sigma detection rules
- Splunk correlation searches
- Wazuh custom rules
- MITRE ATT&CK coverage mapping
