# gns3-mpls-cybersecurity-lab
GNS3 lab implementing a Cisco IP/MPLS backbone, VRF CYBER, VLAN segmentation, HSRP redundancy, AAA/RADIUS, Zabbix monitoring, and a secured DMZ with Cisco ASA firewalls.
# GNS3 IP/MPLS Cybersecurity Lab

A network engineering and cybersecurity lab built with GNS3 and Cisco IOS devices to explore MPLS VPNs, network segmentation, redundancy, access control, monitoring, and DMZ security.

## Project Overview

This project demonstrates the design and configuration of a simulated service-provider IP/MPLS backbone connected to a dedicated cybersecurity environment.

### Objectives

- Build an IP/MPLS backbone using OSPF and LDP.
- Configure VRF-based network isolation and MP-BGP VPNv4.
- Implement VLAN segmentation and inter-VLAN routing.
- Improve gateway availability using HSRP.
- Explore AAA/RADIUS authentication and access-control policies.
- Configure network monitoring, logging, and time synchronization.
- Design a DMZ protected by Cisco ASA firewalls.

## Technologies

- **Network simulation:** GNS3
- **Routing:** OSPF, MP-BGP
- **MPLS:** LDP, MPLS VPN
- **Segmentation:** VRF, VLAN, ACL
- **Redundancy:** HSRP, firewall failover
- **Security:** AAA/RADIUS, Cisco ASA
- **Monitoring:** Zabbix, SNMPv3, Syslog, NTP
- **Network testing:** Connectivity checks, routing-table inspection, and service verification

## Main Components

| Component | Purpose |
|---|---|
| IP/MPLS backbone | Connects network sites using MPLS |
| VRF CYBER | Separates the cybersecurity routing environment |
| OSPF | Provides internal routing between backbone routers |
| LDP | Distributes MPLS labels |
| MP-BGP VPNv4 | Exchanges VPN routing information |
| VLANs and ACLs | Segment networks and control traffic |
| HSRP | Provides default-gateway redundancy |
| AAA/RADIUS | Centralizes network-device authentication |
| Zabbix and SNMPv3 | Supports infrastructure monitoring |
| DMZ and Cisco ASA | Isolates and protects exposed services |

## Validation and Testing

The following checks can be used to validate a deployment, depending on the device configuration:

- `show ip route` — inspect the IP routing table.
- `show ip ospf neighbor` — verify OSPF adjacencies.
- `show mpls ldp neighbor` — inspect LDP neighbors.
- `show mpls forwarding-table` — inspect MPLS label forwarding.
- `show ip bgp vpnv4 all summary` — inspect VPNv4 BGP peers.
- `show standby brief` — verify HSRP state.
- `show access-lists` — inspect ACL rules and counters.

Commands vary by Cisco IOS version and device role. Run each command on the appropriate device and record actual results before claiming successful validation.

## Repository Structure

```text
gns3-mpls-cybersecurity-lab/
├── README.md
├── .gitignore
├── docs/
│   └── technical-report.pdf
└── configs/
    └── README.md
```

## Lab Requirements

- GNS3
- Compatible Cisco IOS images that you are authorized to use
- Appropriate router, switch, and firewall templates
- Sufficient system resources for the simulated topology

The topology and commands may require adaptation to the IOS images and GNS3 appliances available in your environment.

## Security Notice

This repository is intended for educational and authorized lab use. Before publishing configurations, remove passwords, shared secrets, private keys, public IP addresses that should remain confidential, and other sensitive information. Use placeholder values in examples.

Cisco software images and other licensed vendor files are not included.

## Project Context

Academic project: Backbone IP/MPLS – NGN  
Academic year: 2025–2026

## Authors

- Med Aziz Salem
- Laith Sahli
- Farouk Bessouda
