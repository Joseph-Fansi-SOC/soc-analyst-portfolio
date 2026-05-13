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

---

## Tools used
- Wazuh — SIEM/XDR
- Splunk — log correlation
- Wireshark — packet analysis
- Security Onion — IDS/IPS
- Sysmon — endpoint telemetry
- pfSense — firewall
- VirtualBox — virtualisation
- Kali Linux — attack simulation
- Ubuntu — log server

---

## Lab projects
See april2026-projects.md for full project details
including real-world cases investigated.

---

## Screenshots
See screenshots/ folder for Wazuh vulnerability
assessment and Wireshark packet capture evidence.
