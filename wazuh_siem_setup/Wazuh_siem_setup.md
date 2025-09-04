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

