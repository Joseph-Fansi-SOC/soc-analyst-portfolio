# Indicators of Compromise (IOCs)

## File Indicators

| Type     | Value                                                              | Description                                   |
| -------- | ------------------------------------------------------------------ | --------------------------------------------- |
| SHA-256  | `30E527E45F50D2BA82865C5679A6FA998EE0A1755361AB01673950810D071C85` | Malware sample analyzed in VirusTotal         |
| DLL      | `111bc461-1ca8-43c6-97ed-911e0e69fdf8.dll`                         | Malware filename observed on infected systems |
| DAT File | `solarmarker.dat`                                                  | File dropped in AppData folder                |

---

## Network Indicators

| Type      | Indicator     |
| --------- | ------------- |
| C2 Domain | `gogohid.com` |

---

## Malware Information

| Category                    | Value                |
| --------------------------- | -------------------- |
| Malware Family              | Yellow Cockatoo RAT  |
| Malware Type                | Remote Access Trojan |
| Compilation Time            | 2020-09-24 18:26     |
| First VirusTotal Submission | 2020-10-15 02:47     |

---

## Analyst Notes

The malware uses a randomly generated identifier stored in:

```
%USERPROFILE%\AppData\Roaming\solarmarker.dat
```

This artifact can assist defenders during endpoint hunting activities.

