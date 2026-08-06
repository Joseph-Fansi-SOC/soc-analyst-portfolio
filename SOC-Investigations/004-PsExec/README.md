# PsExec Lateral Movement Investigation (Network Forensics / Lateral Movement)

## Executive Summary

This investigation analyzes a simulated lateral movement attack using **PsExec** through network traffic analysis.

Using a PCAP file and Wireshark, the investigation reconstructed the attack chain, identified the initial compromised host, discovered the targeted systems, extracted the compromised account, and identified the Windows administrative shares abused during the intrusion.

The investigation demonstrates practical SOC threat hunting skills using network evidence without relying on pre-generated alerts.

---

## Investigation Scenario

An Intrusion Detection System (IDS) detected suspicious lateral movement activity involving PsExec.

The objective was to investigate the network capture, identify the attacker's entry point, determine affected systems, and understand the techniques used to move through the environment.

---

## Investigation Objectives

* Identify the attacker's initial source IP.
* Determine the first compromised workstation.
* Identify compromised user credentials.
* Detect PsExec execution activity.
* Identify abused Windows administrative shares.
* Map attacker techniques to MITRE ATT&CK.
* Document detection opportunities.

---

## Investigation Environment

### Lab Setup

* VirtualBox SOC Lab
* Ubuntu 24.04 Analysis VM
* Wireshark
* CyberDefenders Blue Team Challenge

---

## Key Findings

| Finding              | Result         |
| -------------------- | -------------- |
| Initial Attacker IP  | `10.0.0.130`   |
| First Target Host    | `sales-pc`     |
| First Target IP      | `10.0.0.133`   |
| Compromised Username | `ssales`       |
| PsExec Service       | `PSEXESVC.exe` |
| Execution Share      | `ADMIN$`       |
| Communication Share  | `IPC$`         |
| Second Target Host   | `marketing-PC` |

---

## Attack Chain Reconstruction

```
Attacker
   |
   | SMB / NTLM Authentication
   |
10.0.0.130
   |
   | PsExec
   |
sales-pc
   |
   | Lateral Movement
   |
marketing-PC
```

---

## Detection Techniques Used

Wireshark filters:

```text
smb or smb2

tcp.port == 445

smb2 and frame contains "PSEXESVC"

ntlmssp.auth.username

smb2.cmd == 1
```

---

## Skills Demonstrated

* Network Forensics
* Threat Hunting
* PCAP Analysis
* SMB Investigation
* NTLM Authentication Analysis
* Lateral Movement Detection
* MITRE ATT&CK Mapping
* SOC Documentation

---

## Tools Used

* Wireshark
* VirtualBox
* Ubuntu SOC Lab
* CyberDefenders
* MITRE ATT&CK Framework

---

## Investigation Artifacts

| Document             | Description                          |
| -------------------- | ------------------------------------ |
| `PsExecHuntLab.pdf`  | Original investigation material      |
| `iocs.md`            | Network indicators and artifacts     |
| `mitre.md`           | ATT&CK technique mapping             |
| `timeline.md`        | Attack reconstruction timeline       |
| `lessons-learned.md` | Detection and defensive improvements |

---

## AI Assistance

AI was used to support documentation structure, improve investigation summaries, and organize technical findings.

All packet analysis, Wireshark investigation, filtering decisions, evidence interpretation, and conclusions were performed and verified by the analyst.

