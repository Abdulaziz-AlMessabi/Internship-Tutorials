# Network Design

## Overview
The EDU-SOC environment is planned to span **two campuses (Dubai & Abu Dhabi)**.  
Each campus having its own infrastructure, but both connected for centralized logging and SOC operations.

## Abu Dhabi Campus
- 1 Layer 7 Firewall 
- 2 Routers  
- 2 Layer 3 Switches  
- 5 VLANs  
- Malware Analysis Machine 
- 1 AD & DNS Server  
- DNS Server & a Centralized Domain Controller  
- SOC Lab + Attack Simulation Lab

## Dubai Campus
- 1 Routers  
- 1 Layer 2 Switch  
- 1 Firewall  
- 1 centralized Domain Controller  

## VLAN Structure
| VLAN | Purpose              | ID   | Notes                           |
|------|----------------------|------|---------------------------------|
| 201  | SOC Lab              | 201  | SOC analysts Machines and tools |
| 20   | Web Server DMZ       | 20   | Public-facing server zone       |
| 10   | Dell EMC Servers     | 10   | Security tools & storage        |
| 120  | Internal Services    | 120  | Web, DNS, Domain Controllers    |

## Future Traffic Flow
- Traffic path (simplified):  
  `Dubai Endpoint → R1 → FW1 → FW2 → R2 → Abudhabi Endpoint`  
- Logs forwarded centrally to SIEM for analysis.

## Diagram
