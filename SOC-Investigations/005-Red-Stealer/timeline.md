# Investigation Timeline

| Time/Event           | Activity                                                   |
| -------------------- | ---------------------------------------------------------- |
| 2023-10-06 04:41 UTC | Malware sample first submitted to VirusTotal               |
| Initial Detection    | Suspicious executable discovered on endpoint               |
| Phase 1              | SHA-256 hash analyzed using VirusTotal                     |
| Phase 2              | Malware classified as Trojan                               |
| Phase 3              | Behavior analysis performed using ANY.RUN                  |
| Phase 4              | C2 communication identified                                |
| Phase 5              | IOC enrichment performed using ThreatFox and MalwareBazaar |
| Phase 6              | MITRE ATT&CK techniques mapped                             |

---

# Attack Flow

```
Malicious Executable
        |
        v
RedLine / RecordStealer
        |
        +--> Local Data Collection
        |
        +--> Privilege Operations
        |
        +--> C2 Communication
        |
        v
77.91.124.55:19071
```

