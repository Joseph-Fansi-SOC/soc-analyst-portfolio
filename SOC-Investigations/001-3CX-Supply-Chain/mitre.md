# MITRE ATT&CK Mapping

| Tactic               | Technique                      | ID    |
| -------------------- | ------------------------------ | ----- |
| Persistence          | DLL Side-Loading               | T1574 |
| Privilege Escalation | DLL Side-Loading               | T1574 |
| Defense Evasion      | Virtualization/Sandbox Evasion | T1497 |
| Discovery            | System Information Discovery   | T1082 |

---

## Key Techniques Observed

### T1574 – DLL Side-Loading

The legitimate 3CX application loaded a malicious `ffmpeg.dll`, allowing attacker-controlled code to execute within a trusted process.

### T1497 – Virtualization/Sandbox Evasion

The malware checked whether it was running inside a VMware virtual machine before continuing execution.

### T1082 – System Information Discovery

The malware gathered host information before contacting command-and-control infrastructure.

