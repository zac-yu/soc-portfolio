# Project Status

Last updated: 22 July 2026

## Validated capabilities

- Windows Server provides AD DS and DNS at `10.10.10.5`.
- The `CyberLanding.com` lab domain resolves to `10.10.10.5`.
- Domain endpoints can reach the domain controller and authenticate with domain accounts.
- The lab uses an isolated `10.10.10.0/24` VMware network.
- Ubuntu/Suricata provides the planned gateway at `10.10.10.1`.
- Suricata captures traffic on `ens34` and generates alerts.
- Custom Suricata SID `1000001` successfully detected ICMP test traffic.
- Splunk Server is reachable at `10.10.10.20`; Splunk Web uses TCP `8000`.
- Ubuntu can ping the Splunk server.
- The forwarder destination has been corrected from an obsolete IP to `10.10.10.20:9997`.

## Immediate validation tasks

- [ ] Confirm the Admin Device does not duplicate `10.10.10.20`.
- [ ] Confirm Splunk is listening for forwarders on TCP `9997`.
- [ ] Confirm `10.10.10.20:9997` appears under **Active forwards** on Ubuntu.
- [ ] Add `local.rules` to the Suricata `rule-files` section.
- [ ] Confirm the custom detection appears in `eve.json`.
- [ ] Ingest `eve.json` into a dedicated Splunk index or sourcetype.
- [ ] Build and screenshot the first Suricata Splunk dashboard.

## Roadmap

### Phase 1 — Stable infrastructure

- Validate IP addressing, DNS, routing and NAT.
- Confirm domain authentication after network migration.
- Record a clean network diagram and asset inventory.

### Phase 2 — Centralized telemetry

- Ingest Windows Security and Sysmon logs.
- Ingest Suricata `eve.json`.
- Normalize hostnames, sourcetypes and timestamps.
- Verify data freshness and source coverage.

### Phase 3 — Detection engineering

- Failed-logon/brute-force detection.
- Encoded PowerShell and suspicious process detection.
- Suspicious DNS query detection.
- Suricata high-severity alert detection.
- Scheduled-task persistence detection.

### Phase 4 — Investigation and response

- Execute a safe Atomic Red Team/PowerShell scenario.
- Build a timeline across endpoint, network and SIEM evidence.
- Map activity to MITRE ATT&CK.
- Write an incident report and containment plan.

### Phase 5 — Vulnerability management

- Add Nessus Essentials or another lab-appropriate scanner.
- Scan intentionally vulnerable targets.
- Prioritize findings by severity, exploitability and asset impact.
- Validate remediation with a rescan.

