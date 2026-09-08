# windows

Windows offensive security research, vulnerability write-ups, and proof-of-concept code by
[@redroot97](https://github.com/redroot97).

> Everything here is published for defensive validation, detection engineering, and
> education. Use it only against systems you are explicitly authorized to test.

## Findings

| Finding | Class | Impact |
|---------|-------|--------|
| [CVE-2026-69267 — DiagTrack RPC NTLM Coercion → LPE](CVE-2026-69267-DiagTrack-NTLM-Coercion-LPE/) | NTLM coercion → RBCD → Kerberos S4U | Standard domain user → `NT AUTHORITY\SYSTEM` |
