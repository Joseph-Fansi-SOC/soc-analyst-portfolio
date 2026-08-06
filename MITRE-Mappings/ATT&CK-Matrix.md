# 🛡️ MITRE ATT&CK Technique Reference

Common techniques observed during SOC investigations.

---

# Initial Access

## T1190 - Exploit Public-Facing Application

Examples:

- Web application compromise
- Vulnerable upload functionality

Observed in:

- WebStrike Lab

---

# Execution

## T1059 - Command and Scripting Interpreter

Examples:

- PowerShell
- Linux shell
- Command execution

---

## T1569.002 - Service Execution

Examples:

- PsExec
- Remote service creation

Observed in:

- PsExec Hunt Lab

---

# Persistence

## T1505.003 - Web Shell

Examples:

- Malicious PHP upload
- Server backdoor

Observed in:

- WebStrike Lab

---

# Defense Evasion

## T1574.002 - DLL Side-Loading

Examples:

- Malicious DLL loaded by trusted application

Observed in:

- 3CX Supply Chain Investigation

---

## T1497 - Virtualization/Sandbox Evasion

Examples:

- Anti-analysis checks

Observed in:

- 3CX Investigation

---

# Credential Access

## T1003 - OS Credential Dumping

Examples:

- LSASS dumping
- Credential extraction

---

# Discovery

## T1083 - File and Directory Discovery

Examples:

- File enumeration

---

# Lateral Movement

## T1021.002 - SMB/Windows Admin Shares

Examples:

- ADMIN$
- IPC$

Observed in:

- PsExec Hunt Lab

---

# Collection

## T1005 - Data from Local System

Examples:

- Local file collection

Observed in:

- Red Stealer Lab

---

# Command and Control

## T1071.001 - Web Protocols

Examples:

- HTTP/HTTPS communication

---

# Exfiltration

## T1041 - Exfiltration Over C2 Channel

Examples:

- Data transfer through attacker-controlled channel

Observed in:

- WebStrike Lab
