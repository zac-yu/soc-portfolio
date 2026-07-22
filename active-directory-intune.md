# Active Directory, Entra ID and Intune Lab

## Summary

Built a small-business identity and endpoint-management environment using Windows Server Active Directory, DNS, Microsoft Entra ID and Intune.

## Work completed

- Created and administered users, groups and organizational units in Active Directory.
- Joined Windows endpoints to the local domain and tested domain authentication.
- Configured the domain controller as the DNS server for domain endpoints.
- Migrated the lab from the previous bridged network to `10.10.10.0/24`.
- Updated the domain controller from its old address to `10.10.10.5`.
- Removed stale DNS information and verified `CyberLanding.com` resolves to the new address.
- Integrated on-premises identities with Microsoft Entra ID using Entra Connect.
- Troubleshot device synchronization and Hybrid Microsoft Entra Join.
- Configured automatic MDM enrollment through Group Policy.
- Enrolled a Windows test endpoint into Intune.
- Deployed Google Chrome as a managed application.
- Configured compliance policies, configuration profiles, Windows Update Rings, firewall policy and a Microsoft security baseline.
- Used Conditional Access in report-only mode to test policy impact safely.
- Tested remediation by disabling Windows Firewall, detecting noncompliance and restoring the required configuration.
- Investigated Intune error `65000` and identified unsupported virtualization-security settings in the VM.

## Validation criteria

- The endpoint resolves the AD domain through `10.10.10.5`.
- A domain user can log in to a domain-joined endpoint.
- The device appears in Entra ID and Intune with the expected join and management state.
- Assigned applications and policies reach the endpoint.
- Compliance state changes in response to a controlled configuration failure and remediation.

## Interview-ready summary

I built a Microsoft identity and endpoint-management lab that integrated on-premises Active Directory with Entra ID. I configured Hybrid Join and automatic Intune enrollment through Group Policy, deployed applications and security policies, and tested compliance remediation. During troubleshooting, I traced synchronization, DNS, device-registration and policy errors across the domain controller, Entra ID and the Windows endpoint.

