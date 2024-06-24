# Comprehensive Enterprise Network Implementation

This project involved configuring a comprehensive network setup, demonstrating advanced networking concepts and technologies across multiple offices. The configuration included VLANs, Layer-2 and Layer-3 EtherChannels, HSRP, RSTP, IP addressing, routing protocols, network services, and security features.

## Part 1: VLANs and Layer-2 EtherChannel

In Office A and Office B, Layer-2 EtherChannels were configured using both Cisco-proprietary and open standard protocols respectively. Trunk links were established between Access and Distribution switches, with specific VLANs allowed on each trunk. VTPv2 was set up to propagate VLAN configurations across switches, and access ports were configured for PCs, phones, and other devices, ensuring that appropriate VLANs were used. Trunk links were also manually set to disable DTP, and native VLANs were set to unused VLAN 1000 for security.

## Part 2: IP Addresses, Layer-3 EtherChannel, HSRP

IP addressing was meticulously planned and implemented across all interfaces, including dynamic IP configurations for external interfaces and static IPs for internal connections. Layer-3 EtherChannels were configured between core switches with Cisco-proprietary protocols, and HSRPv2 was set up for redundancy across various subnets, ensuring high availability and reliability for management, PCs, phones, Wi-Fi, and server subnets. Specific HSRP priorities and preemption were configured to align with network design.

## Part 3: Rapid Spanning Tree Protocol (RSTP)

RSTP was enabled on all Access and Distribution switches, with the root bridge for each VLAN aligning with the HSRP active router. PortFast and BPDU Guard were configured on ports connected to end hosts to optimize network convergence and enhance security.

## Part 4: Static and Dynamic Routing

OSPF was implemented on routers and switches to enable dynamic routing across the network. Process ID 1 and Area 0 were used, with specific configurations to ensure OSPF was enabled on all relevant interfaces. Static default routes were configured on R1 for internet connectivity, with failover mechanisms in place.

## Part 5: Network Services

A suite of network services was configured to support the network infrastructure:

- **DHCP:** Pools were created on R1 for different subnets, excluding the first ten usable addresses to reserve them for static assignments.
- **DNS:** Entries were configured on SRV1 for domain name resolution.
- **NTP:** R1 was configured as an NTP server, and other devices were set to synchronize time with it.
- **SNMP:** Community strings were configured for network management.
- **Syslog:** Logging was set up to send messages to SRV1 and reserve buffer space on devices.
- **FTP:** Used to update IOS versions on routers.
- **SSH:** Configured for secure remote access with restricted access control.
- **NAT:** Static and dynamic NAT configurations were implemented for internet access.

## Part 6: Security Features

Extended ACLs were configured to control traffic between Office A and Office B. Port security was enabled on access ports to limit the number of MAC addresses and block invalid traffic. DHCP snooping and Dynamic ARP Inspection (DAI) were configured on Access switches to prevent DHCP and ARP spoofing attacks.

## Part 7: IPv6 Configuration

IPv6 routing was enabled on key devices, with IPv6 addresses configured on relevant interfaces using both static and EUI-64 addressing. Default static routes were set up on R1 for IPv6 internet connectivity.

## Part 8: Wireless Configuration

The Wireless LAN Controller (WLC1) was accessed and configured via its GUI. Dynamic interfaces and WLANs were set up with appropriate IP addressing and security settings, including WPA2 with AES encryption and pre-shared keys.

---

This project showcases a robust implementation of various networking technologies, highlighting the ability to design, configure, and manage a complex network infrastructure. The configurations ensure high availability, security, and efficient management of network resources, providing a solid foundation for enterprise network environments.


## Topology:

![Screenshot 2024-06-24 182726](https://github.com/pnsudhanva/Advanced-Enterprise-Network/assets/14261453/4b0ce720-ab5b-4dc4-aece-369cd662162a)
