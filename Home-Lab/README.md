## Home Lab — Personal SOC Environment
Built: April 2026

A personal SOC environment built from beginner to advanced
level, used to practise real-world threat detection, log
analysis and incident response.

---

## Documents

### 1. SOC Lab Architecture — Beginner to Advanced
📄 MyhomeSOCLab_Project_ArchitectureFinal.pdf
Three-level SOC lab built on VirtualBox:
- Beginner: Flat network — Kali attacker → Windows victim → Wazuh SIEM
- Intermediate: Host-only adapter, Sysmon log forwarding
- Advanced: Enterprise-style network with pfSense firewall,
  network segmentation, full SOC stack

### 2. Advanced SOC Lab — Description & Analysis
📄 DescriptionAdvanced_SOC_Lab.pdf
Critical analysis of the advanced lab including:
- Proper network segmentation (4 subnets)
- Full SOC stack: Security Onion, Wazuh, Splunk,
  Wireshark, Zeek, Nmap, Sysmon
- Gaps identified and improvement roadmap
- Design maturity assessment: 8/10

### 3. Splunk Project — Malware Simulation & Network Investigation
📄 My_home_SOC_Lab_Splunk_Project_1.pdf
Complete attack simulation and defensive investigation:
- Malware generated using Metasploit Framework
- Detection using Wireshark, Splunk, Brim and Sysmon
- Incident response triggered by real misconfiguration
- IOC investigation and threat containment

### 4. Wazuh SOC Lab — Setup & Configuration
📄 SOC_Lab_with_Wazuh.pdf
Complete Wazuh SIEM deployment:
- VirtualBox lab with Kali, Windows 11, Ubuntu
- Wazuh 4.12 + Sysmon installation
- Agent configuration and log ingestion
- Vulnerability detected: CVE-2023-47359

### 5. Security Incident Report — CVE-2023-47359/47360
📄 Wazuh_CVE_Investigation_Testing-Report.pdf
Real incident report written in SOC format:
- Wazuh alert triage and investigation
- MITRE ATT&CK mapping: T1204
- CVSS Score: 7.5 (High)
- VLC Media Player vulnerability — investigated and remediated

### 6. Wireshark Installation Guide — Ubuntu 24.04
📄 How_to_Install_Wireshark_on_Ubuntu_24.pdf
Step-by-step installation guide:
- Two installation methods documented
- Troubleshooting permission errors
- Live packet capture screenshots included

---

## Real-World Cases
📸 Investigation_of_friends_PC_with_my_labWazuh.jfif
📸 Investigation_of_friends_PC_with_my_Wireshark.jfif

Friend reported suspected spoofing, memory overflow
and high CPU/fan activity. Investigated using Wazuh
and Wireshark. Found 13 vulnerabilities including
1 Critical and 4 High severity CVEs.

---

## Tools used
- Wazuh 4.12 — SIEM/XDR
- Splunk — log correlation
- Wireshark 4.6.4 — packet analysis
- Security Onion — IDS/IPS
- Sysmon — endpoint telemetry
- Metasploit Framework — attack simulation
- Brim — PCAP investigation
- pfSense — firewall
- VirtualBox — virtualisation
- Kali Linux — attack simulation
- Ubuntu 24.04 — log server

---

## April 2026 Projects
See april2026-projects.md for full project list
and real-world case details.

## Screenshots
See screenshots/ folder for live evidence from
Wazuh and Wireshark investigations.

