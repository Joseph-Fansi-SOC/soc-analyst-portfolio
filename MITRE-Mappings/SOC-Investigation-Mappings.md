# 🔎 SOC Investigation MITRE Mappings

Mapping of completed investigations to MITRE ATT&CK techniques.

---

# 001 - 3CX Supply Chain

## Techniques

| Technique | Description |
|-|-|
| T1574.002 | DLL Side-Loading |
| T1497 | Virtualization/Sandbox Evasion |
| T1059 | Command Execution |
| T1071.001 | Web Protocols |

Evidence:

- Malicious ffmpeg.dll
- d3dcompiler_47.dll
- RC4 encrypted payload
- C2 communication

---

# 002 - Yellow RAT

## Techniques

| Technique | Description |
|-|-|
| T1059 | Command Execution |
| T1071 | Application Layer Protocol |
| T1105 | Ingress Tool Transfer |

Evidence:

- RAT execution
- C2 infrastructure
- Malware persistence

---

# 004 - PsExec Hunt

## Techniques

| Technique | Description |
|-|-|
| T1021.002 | SMB/Windows Admin Shares |
| T1569.002 | Service Execution |
| T1078 | Valid Accounts |

Evidence:

- PSEXESVC.exe
- ADMIN$
- IPC$

---

# 005 - Red Stealer

## Techniques

| Technique | Description |
|-|-|
| T1005 | Data from Local System |
| T1134 | Access Token Manipulation |

Evidence:

- ADVAPI32.dll usage
- Information theft behavior

---

# 006 - WebStrike

## Techniques

| Technique | Description |
|-|-|
| T1505.003 | Web Shell |
| T1059.004 | Unix Shell |
| T1041 | Exfiltration Over C2 Channel |

Evidence:

- image.jpg.php upload
- Reverse shell
- /etc/passwd exfiltration

---

# Purpose

This mapping supports:

- Detection development
- Threat hunting
- Incident response
- Security reporting
