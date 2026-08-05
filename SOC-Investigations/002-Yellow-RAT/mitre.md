# MITRE ATT&CK Mapping

| Tactic              | Technique                         | ID        | Evidence                                                 |
| ------------------- | --------------------------------- | --------- | -------------------------------------------------------- |
| Initial Access      | User Execution                    | T1204     | Malware execution required user interaction              |
| Execution           | Command and Scripting Interpreter | T1059     | RAT capability enables command execution                 |
| Defense Evasion     | Obfuscated/Compressed Files       | T1027     | Malware analysis required threat intelligence inspection |
| Credential Access   | Credentials from Web Browsers     | T1555.003 | Browser-related activity observed                        |
| Persistence         | Create or Modify System Process   | T1543     | RAT persistence behavior                                 |
| Command and Control | Application Layer Protocol        | T1071     | Communication with external C2 domain                    |
| Exfiltration        | Exfiltration Over C2 Channel      | T1041     | Malware capability for data transfer                     |

---

## Observed Techniques

### Command and Control

The malware communicates with attacker-controlled infrastructure:

```
gogohid.com
```

### Persistence

The malware stores artifacts in the user's AppData directory:

```
%USERPROFILE%\AppData\Roaming\
```

### Discovery and Collection

The RAT provides remote access capabilities that allow attackers to gather information from compromised systems.

