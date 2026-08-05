# Indicators of Compromise (IOCs)

## File Hash

| Indicator | Value                                                              |
| --------- | ------------------------------------------------------------------ |
| SHA-256   | `59e1edf4d82fae4978e97512b0331b7eb21dd4b838b850ba46794d9c7a2c0983` |

---

## Malicious Files

| File                 | Description                                      |
| -------------------- | ------------------------------------------------ |
| `ffmpeg.dll`         | Malicious DLL executed through DLL side-loading  |
| `d3dcompiler_47.dll` | Secondary malicious DLL dropped by the installer |

---

## Malware Characteristics

* **Threat Category:** Trojan
* **Execution:** DLL Side-Loading
* **Encryption:** RC4
* **Sandbox Evasion:** VMware detection
* **Virtualization Evasion:** T1497

---

## Threat Attribution

**Associated Threat Actor:** Lazarus Group

---

## Summary

The compromised MSI installer deployed two malicious DLLs that abused DLL side-loading to execute within the legitimate 3CX Desktop Application. The malware decrypted its payload using RC4, executed in memory, and established communication with attacker-controlled infrastructure.

