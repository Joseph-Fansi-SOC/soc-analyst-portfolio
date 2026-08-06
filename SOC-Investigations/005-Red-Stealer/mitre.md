# MITRE ATT&CK Mapping

| Tactic               | Technique                    | ID    | Evidence                                            |
| -------------------- | ---------------------------- | ----- | --------------------------------------------------- |
| Collection           | Data from Local System       | T1005 | Malware collects local system information           |
| Privilege Escalation | Access Token Manipulation    | T1134 | ADVAPI32.dll usage associated with token operations |
| Command and Control  | Application Layer Protocol   | T1071 | Malware communicates with external infrastructure   |
| Discovery            | System Information Discovery | T1082 | Collects host information                           |
| Collection           | Automated Collection         | T1119 | Collects targeted data automatically                |

---

# Technique Analysis

## T1005 — Data from Local System

The malware collects information stored locally before possible exfiltration.

---

## T1134 — Access Token Manipulation

ADVAPI32.dll was identified as an imported Windows library associated with privilege and security token operations.

---

## C2 Communication

The malware communicates with:

```
77.91.124.55:19071
```

indicating external command and control activity.

