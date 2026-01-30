# EAASBank-Internet-IntranetArchetectureProject

# Project Overview
This project establishes a robust and secure communication infrastructure for EAAS Bank, a financial institution operating across four major cities in Pakistan: Karachi, Lahore, Islamabad, and Rawalpindi. The architecture combines Local Area Networks (LAN) for branch-level operations and Wide Area Network (WAN) links for inter-city connectivity, ensuring high-speed data sharing and secure access to banking services.

# Network Topology & Design
1. The network is built using a redundant ring topology in each city, featuring five routers connected via serial links to ensure high availability.
2. Staff LANs: Four routers in each city are dedicated to staff segments, connecting end devices (PCs, laptops) through switches.
3. Server VLAN: A fifth router in each city is reserved for a dedicated Server VLAN.
4. Central Backbone: All four city networks are integrated through a central redistributed CORE router that serves as the backbone for the entire corporate network.

# Technical Specifications
1. Routing Protocols
The project demonstrates a multi-protocol environment with redistribution to ensure seamless communication between different regions:
Karachi: Static Routing.
Lahore: RIPv2.
Islamabad: EIGRP (AS 50).
Rawalpindi: OSPF.

2. Network Services
The server infrastructure hosts several critical banking services:
Web Servers: For banking applications.
DNS: For domain resolution.
FTP: For secure file transfers.
SMTP: For email communication.
DHCP: Automated IP assignment for end devices across all branches.

3. Security Measures
Extended ACLs: Implemented to control and filter traffic between segments.
NAT (Network Address Translation): Configured for secure internet/external access.
Port Security: Applied at the switch level to prevent unauthorized device access.

4. IP Addressing Scheme
The project utilizes a diverse IP scheme spanning Class A, B, and C addresses to efficiently manage the various subnets across the four cities.
