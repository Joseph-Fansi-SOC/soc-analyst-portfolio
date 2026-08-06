# MITRE ATT&CK Mapping

| Tactic              | Technique                                     | ID        | Evidence                                  |
| ------------------- | --------------------------------------------- | --------- | ----------------------------------------- |
| Initial Access      | Exploitation for Client Execution             | T1203     | Vulnerable upload functionality exploited |
| Persistence         | Server Software Component: Web Shell          | T1505.003 | image.jpg.php deployed                    |
| Execution           | Command and Scripting Interpreter: Unix Shell | T1059.004 | Reverse shell commands executed           |
| Command and Control | Non-Application Layer Protocol                | T1095     | Reverse shell communication               |
| Exfiltration        | Exfiltration Over C2 Channel                  | T1041     | /etc/passwd transmitted                   |
| Discovery           | File and Directory Discovery                  | T1083     | System file enumeration                   |

---

# Technique Details

## T1505.003 — Web Shell

The attacker uploaded:

```
image.jpg.php
```

allowing remote command execution.

---

## T1059.004 — Unix Shell

The attacker executed shell commands through a reverse shell.

---

## T1041 — Exfiltration Over C2 Channel

Sensitive information was transmitted back to attacker infrastructure.

