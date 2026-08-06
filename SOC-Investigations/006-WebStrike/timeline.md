# Investigation Timeline

| Stage | Activity                                       |
| ----- | ---------------------------------------------- |
| 1     | IDS detected suspicious web server activity    |
| 2     | PCAP loaded into Wireshark                     |
| 3     | Attacker source identified: 117.11.88.124      |
| 4     | HTTP traffic analyzed                          |
| 5     | Malicious PHP upload discovered                |
| 6     | Web shell identified: image.jpg.php            |
| 7     | Reverse shell connection detected on port 8080 |
| 8     | Command execution observed                     |
| 9     | /etc/passwd file exfiltration confirmed        |

---

# Final Attack Path

```
Attacker
   |
   v
Web Upload Vulnerability
   |
   v
PHP Web Shell
   |
   v
Reverse Shell
   |
   v
Sensitive Data Theft
```

