# Lab28-HSRP-Ipsec-VPN-OSPF-Practice
This project demonstrates a 3-tier network architecture that includes redundancy, dynamic routing, and secure site-to-site communication. The lab is designed for educational purposes, allowing hands-on practice with L2/L3 switches, routers, HSRP, OSPF, and IPsec VPN.

Architecture
Sites

Site 1: Core and Access Layer switches with VLANs for IT (VLAN 10) and HR (VLAN 20).

Site 2: Core and Access Layer switches with VLANs for IT (VLAN 30) and HR (VLAN 40).

Routers: Connect the sites, enable OSPF routing, and establish an IPsec VPN between the sites.

Devices

L2 Switches: Provide access ports for PCs and trunk ports to Core switches.

L3 Core Switches: Enable VLAN interfaces, HSRP virtual IPs, inter-VLAN routing, and OSPF.

Routers: Handle site-to-site VPN, OSPF routing, and redundancy through HSRP.

Key Features
High Availability (HSRP)

HSRP configured on VLAN interfaces on the L3 Core switches.

Provides default gateway redundancy for PCs.

Active/standby priorities set to ensure smooth failover.

Dynamic Routing (OSPF)

OSPF used to propagate routes across VLANs and between sites.

Ensures fast convergence in case of link failure.

All routers and L3 switches participate in OSPF Area 0.

Secure Site-to-Site Communication (IPsec VPN)

IPsec VPN tunnel between Router 1 (Site 1) and Router 3 (Site 2).

Encrypts traffic between VLANs across sites.

Access-lists define the traffic allowed through the VPN.

IP Addressing

VLAN 10 (IT) & VLAN 20 (HR) in Site 1: 10.10.10.0/24 and 20.20.20.0/24.

VLAN 30 (IT) & VLAN 40 (HR) in Site 2: 90.90.90.0/24 and 100.100.100.0/24.

HSRP virtual IPs used as default gateways for all PCs.

Router inter-site links: 50.50.50.0/24, 60.60.60.0/24, 70.70.70.0/24, 80.80.80.0/24.

PCs Configuration

Default gateway points to HSRP virtual IP.

Allows transparent communication even if the primary Core switch fails.

Site-to-site communication enabled through IPsec VPN.

Lab Objectives

Configure VLANs, trunk ports, and access ports on L2 switches.

Configure L3 VLAN interfaces with HSRP for redundancy.

Configure OSPF on routers and L3 switches for dynamic routing.

Configure site-to-site IPsec VPN for encrypted communication between sites.

Test connectivity between PCs and across sites.

Verify HSRP failover and OSPF routing convergence.
