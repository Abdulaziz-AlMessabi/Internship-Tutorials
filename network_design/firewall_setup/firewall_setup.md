# Firewall Setup

## Purpose
Firewalls were configured to enforce security and control interactions between VLANs, labs, and inter-campus links.  
Default policy = **Deny all**, then allow only required services.

## Firewall Policies
The following is an example of some of the policies that were configured

| Policy | Source VLAN | Destination VLAN | Service/Port   | Action | Justification |
|--------|-------------|------------------|----------------|--------|---------------|
| 1      | SOC Lab     | Dell Servers     | TCP 22, 443    | Allow  | Analysts need access to tools |
| 2      | SOC Lab     | Web DMZ          | TCP 80, 443    | Allow  | Analysts manage web server    |
| 3      | Any         | Any              | Any            | Deny   | Block all else (default)      |
