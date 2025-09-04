# Troubleshooting and Lessons Learned

## Common Issues

### Network-Related
- **VM Connectivity Issues:** Some VMs had no internet access even though the host machine did. Root cause: wrong port group/VLAN configuration in ESXi.  
- **VLAN Misconfiguration:** Incorrect IDs or mismatched trunk/access settings dropped traffic.  
- **Firewall Rule Errors:** Wrong source/destination VLAN assignments blocked traffic.  
- **Inter-Campus Confusion:** Lack of physical network line resulted in communication.  
- **Switch Port Setup:** Needed clarity on when to use access vs trunk ports.

### SIEM/EDR/NDR
- **SIEM Logs Missing:** Caused by missing forwarding rules or syslog misconfiguration.  
- **EDR Agents Not Reporting:** Due to install/connectivity issues.  

### Lab Operations
- **Student Engagement:** Long lectures lost attention; SOC simulations worked better.  
- **Topology Complexity:** Early static designs had to be redone for more realistic security dynamics.

---

## Lessons Learned
- Proper VLAN planning is critical — one misconfig can isolate key servers.  
- Centralized logging in SIEM greatly improves detection and response.  
- Inline IPS is valuable before the firewall; IDS provides visibility inside.  
- Open-source IPS can be adopted for cost-effective coverage.  
- Clear log forwarding design prevents inter-campus confusion.  
- Hands-on firewall policy design reinforced balancing security with usability.  
- Simulation exercises (CALDERA-style) kept students engaged and validated SOC processes.  
- Designing an EDU-SOC is not only about tools — it’s about creating a **learning environment** for real-world skills.
