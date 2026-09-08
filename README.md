# windows

A collection of Windows security research POCs targeting local privilege escalation and Active Directory trust boundaries. Each finding has a dedicated folder with a README covering the vulnerability, how to build, run, reproduce, and clean up.

## POCs

| POC | Path | Target | Privs |
| --- | --- | --- | --- |
| DiagTrack RPC NTLM Coercion (CVE-2026-69267) | [CVE-2026-69267-DiagTrack-NTLM-Coercion-LPE/](CVE-2026-69267-DiagTrack-NTLM-Coercion-LPE/) | Coerces the SYSTEM DiagTrack service into NTLM auth, relays it to the DC over LDAPS, and abuses RBCD + Kerberos S4U to reach NT AUTHORITY\SYSTEM. | standard domain user |

## Building

The POC is a single self-contained C# file with no external dependencies. Compile with the in-box .NET Framework compiler present on every Windows install:

```cmd
%WINDIR%\Microsoft.NET\Framework64\v4.0.30319\csc.exe /nologo /platform:anycpu /out:dt.exe poc\DiagTrackExploit.cs
```

No Visual Studio project, no dependencies. Per-finding build notes live in each folder's README.

## Repository layout

```
windows/
|-- README.md
`-- CVE-2026-69267-DiagTrack-NTLM-Coercion-LPE/
    |-- README.md
    |-- EXPLANATION.md
    |-- REPRODUCE.md
    `-- poc/
        `-- DiagTrackExploit.cs
```

## Author

[@redroot97](https://github.com/redroot97) - offensive security engineer.

## Disclaimer

For authorized security research and red team engagements only.
