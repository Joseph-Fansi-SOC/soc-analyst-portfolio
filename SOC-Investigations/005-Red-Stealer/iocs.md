# Indicators of Compromise (IOCs)

## Malware Hash

| Type    | Value                                                              |
| ------- | ------------------------------------------------------------------ |
| SHA-256 | `248fcc901aff4e4b4c48c91e4d78a939bf681c9a1bc24addc3551b32768f907b` |

---

## Malware Information

| Indicator      | Value           |
| -------------- | --------------- |
| File Name      | WEXTRACT        |
| Malware Family | RedLine Stealer |
| Alias          | RECORDSTEALER   |
| Category       | Trojan          |

---

## Network Indicators

| Type             | Value          |
| ---------------- | -------------- |
| C2 IP            | `77.91.124.55` |
| Destination Port | `19071`        |
| Protocol         | TCP            |

---

## DNS Indicators

| Domain       | Purpose                                  |
| ------------ | ---------------------------------------- |
| facebook.com | DNS resolution observed during execution |

---

## Detection Intelligence

| Source        | Finding                             |
| ------------- | ----------------------------------- |
| MalwareBazaar | YARA rule: `detect_Redline_Stealer` |
| Author        | Varp0s                              |
| ThreatFox     | Alias: RECORDSTEALER                |

---

## Imported DLL

| DLL          | Purpose                                                         |
| ------------ | --------------------------------------------------------------- |
| ADVAPI32.dll | Windows API functions related to token and privilege operations |

