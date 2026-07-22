# Splunk and Detection Engineering

## Data sources used

- Windows Security Event Log
- Sysmon process, network, file and DNS events
- Microsoft 365 / Entra sign-in data
- Suricata `eve.json` (integration in progress)
- Network and endpoint security telemetry used in investigation exercises

## Detection use cases

| Use case | Primary telemetry | Relevant events / logic | ATT&CK context |
|---|---|---|---|
| Repeated failed logons | Windows Security | Event ID `4625`, user, host, source, logon type | Credential Access |
| Process execution | Sysmon | Event ID `1`, parent-child relationship, command line | T1059 |
| Network connections | Sysmon | Event ID `3`, process, destination and port | Command and Control |
| Suspicious DNS | Sysmon | Event ID `22`, queried domain and process | T1071.004 |
| PowerShell activity | Sysmon / Windows | Encoded commands, download patterns, unusual parents | T1059.001 |
| Scheduled-task persistence | Windows / Sysmon | Task creation and related process activity | T1053.005 |
| Overseas sign-in | Entra sign-ins | Geo-enrichment and non-Australian location filter | Valid Accounts |
| IDS signature alert | Suricata | Signature, category, severity, source/destination | Network detection |

## Example SPL patterns

These are portable starting points and may require field adjustments for the local sourcetype.

### Failed logons by user and source

```spl
index=windows EventCode=4625
| stats count min(_time) as first_seen max(_time) as last_seen by user, src_ip, host, Logon_Type
| where count >= 5
| convert ctime(first_seen) ctime(last_seen)
| sort - count
```

### Suspicious PowerShell command lines

```spl
index=windows (EventCode=1 OR EventCode=4688)
(Image="*\\powershell.exe" OR New_Process_Name="*\\powershell.exe")
(CommandLine="*-enc*" OR CommandLine="*EncodedCommand*" OR CommandLine="*DownloadString*" OR CommandLine="*Invoke-WebRequest*")
| table _time host user ParentImage Image CommandLine
```

### Suricata alerts

```spl
index=suricata event_type=alert
| stats count by alert.severity, alert.category, alert.signature, src_ip, dest_ip
| sort alert.severity - count
```

## Investigation workflow

1. Validate alert time, affected host/user and source data.
2. Determine whether activity was blocked, allowed or only observed.
3. Establish a timeline and pivot across identity, process, network and endpoint data.
4. Check for repetition, lateral movement, persistence and additional affected assets.
5. Map validated behavior to MITRE ATT&CK.
6. Record severity, impact, evidence and recommended response.
7. Tune detection logic only after preserving investigation evidence.

