## Overview
Wazuh was deployed as the central SIEM with plans of replacing it with IBM QRadar to aggregate logs from all devices:
- Firewalls  
- Windows Servers (Domain Controllers)  
- Web Servers (DMZ)  
- EDR and NDR tools  

## Log Sources
| Source              | Protocol   | Notes                          |
|---------------------|-----------|-------------------------------|
| Fortinet Firewalls  | Syslog    | Forwarded security events      |
| Windows DC          | WinCollect| AD events and authentication   |
| Kaspersky EDR       | API       | Endpoint alerts                |
| ExtraHop NDR        | Syslog    | Network detections             |

## Benefits
- **Central Visibility**: All logs in one place  
- **Correlation**: Detect multi-stage attacks  
- **Incident Response**: Faster triage for analysts  

## Example Log Forwarding Snippet
<localfile>
  <log_format>eventchannel</log_format>
  <location>Microsoft-Windows-Sysmon/Operational</location>
</localfile>





# EDR Deployment (Wazuh/Kapersky EDR)

## Overview
Endpoints across the SOC environment were protected with Wazuh EDR with future plans to incorporate Kapersky EDR's.  
This provided visibility into malware, exploits, and suspicious behavior.

## Key Features
- Real-time detection of endpoint attacks  
- Alerts forwarded to SIEM  
- Coverage for student lab machines and servers  

## Deployment Notes
- Agents had to be installed on each endpoint  
- Connectivity issues sometimes caused reporting delays  
- Integration with SIEM worked through API + syslog  

## Example Use Case
- Student machine infected in red team exercise  
- EDR detected suspicious process execution  
- Alert correlated in SIEM with firewall traffic  
