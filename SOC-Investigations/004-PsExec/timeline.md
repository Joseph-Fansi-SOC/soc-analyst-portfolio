# Investigation Timeline

| Step | Activity                                                          |
| ---- | ----------------------------------------------------------------- |
| 1    | IDS alert generated for suspicious lateral movement.              |
| 2    | PCAP file imported into Wireshark.                                |
| 3    | SMB traffic analyzed to identify attacker source.                 |
| 4    | Initial attacker IP identified: `10.0.0.130`.                     |
| 5    | First target identified: `sales-pc`.                              |
| 6    | NTLM authentication analyzed and compromised username identified. |
| 7    | PsExec execution detected through `PSEXESVC.exe`.                 |
| 8    | ADMIN$ share identified as execution path.                        |
| 9    | IPC$ share identified as communication channel.                   |
| 10   | Additional lateral movement identified toward `marketing-PC`.     |

---

## Final Attack Path

```
10.0.0.130
     |
     v
sales-pc
     |
     v
marketing-PC
```

