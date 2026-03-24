# Secure Network Design for Corporate Merger

## Overview
Two companies operating in the insurance and financial services industries required a secure merged network infrastructure. One organization had significant access control gaps, outdated hardware, and no dedicated cybersecurity personnel. The other had devices running end of life operating systems, open vulnerable ports, and an outdated firewall. This project involved assessing both networks, identifying security risks, and designing a unified secure network topology that addressed all vulnerabilities while staying within budget.

## The Problem
A combined review of both networks using Zenmap and OpenVAS scanning tools revealed critical security risks across both organizations including:

- Open remote desktop ports exposing the network to unauthorized access
- Servers, workstations, and laptops running end of life operating systems (Windows 10 and Windows Server 2012)
- Obsolete routers and firewalls with no vendor support or security updates
- All employees granted full system access with no role based restrictions
- Password changes not enforced across the organization
- Former employee accounts still active on the network
- Message signing disabled on network devices

## Compliance Frameworks
- HIPAA (Health Insurance Portability and Accountability Act)
- GLBA (Gramm Leach Bliley Act)

## Tools and Technologies
- Zenmap (Network Scanning)
- OpenVAS (Vulnerability Scanning)
- Microsoft Visio (Network Topology Diagram)
- Kali Linux
- Cisco 4331 Routers with built in firewall and VPN
- Cisco Catalyst 2960X 48 Port Switches
- Windows Server 2022
- Windows 10 with BitLocker and Windows Defender
- Role Based Access Control (RBAC)
- Demilitarized Zones (DMZ)

## What Was Implemented

### Network Assessment
- Conducted vulnerability scans on both networks using Zenmap and OpenVAS from Kali Linux machines
- Identified and documented 8 risks in the first organization and 5 risks in the second
- Mapped all devices to their corresponding OSI and TCP/IP layers

### Network Topology Design
- Designed a merged network topology in Microsoft Visio incorporating all remediation efforts
- Implemented DMZs using firewalls at network entry points to segment internal and external traffic
- Applied defense in depth and least privilege as core design principles
- Closed vulnerable open ports (135, 139, 88 through 93)
- Replaced open remote desktop ports with VPN access

### Hardware Upgrades
- Replaced outdated Cisco 2811 and OPNsense routers with Cisco 4331 Routers at both locations, eliminating the need for third party firewall and VPN services
- Upgraded all switches to Cisco Catalyst 2960X 48 Port Switches with SSH, HTTPS, and ACL support
- Retained existing Cat5e cabling to stay within budget without compromising performance

### Software and OS Upgrades
- Upgraded all servers to Windows Server 2022 to ensure continued Microsoft support and compliance
- Upgraded all workstations and laptops to Windows 10, enabling BitLocker Drive Encryption and Windows Defender Antivirus
- Enabled message signing on all applicable devices

### Access Control
- Implemented RBAC to enforce least privilege across both organizations
- Enforced periodic password changes
- Established a policy for immediate removal of accounts upon employee termination


## Full Project Report
[View Full Report (PDF)](./SecureNetworkDesign.pdf)
