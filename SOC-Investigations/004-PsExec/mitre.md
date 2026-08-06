# MITRE ATT&CK Mapping

| Tactic            | Technique                          | ID        | Evidence                                    |
| ----------------- | ---------------------------------- | --------- | ------------------------------------------- |
| Execution         | System Services: Service Execution | T1569.002 | PsExec created and executed PSEXESVC.exe    |
| Lateral Movement  | SMB/Windows Admin Shares           | T1021.002 | ADMIN$ and IPC$ shares used                 |
| Lateral Movement  | Lateral Tool Transfer              | T1570     | PsExec transferred executable components    |
| Credential Access | Valid Accounts                     | T1078     | Compromised username `ssales` used          |
| Discovery         | File and Directory Discovery       | T1083     | Remote system activity observed             |
| Defense Evasion   | Masquerading                       | T1036     | Legitimate Windows service mechanism abused |

---

## Key Techniques Observed

### T1021.002 — SMB/Windows Admin Shares

The attacker used SMB communication and Windows administrative shares to move between systems.

### T1569.002 — Service Execution

PsExec created the service:

```
PSEXESVC.exe
```

to execute commands remotely.

### T1078 — Valid Accounts

The attacker authenticated using:

```
ssales
```

indicating possible credential compromise.

