# Virtual Enterprise Network Lab (Cybersecurity-Focused)

## Project Overview

This project simulates a full-stack enterprise network inside a virtual lab environment. It includes a pfSense firewall, a Windows Server 2022 domain controller with DHCP, DNS, and Active Directory services, a Windows 10 domain-joined client, and a Kali Linux attacker machine. The goal is to showcase core IT and cybersecurity concepts such as domain authentication, internal network segmentation, and penetration testing in a safe and controlled setup.

## Network Diagram

The following diagram represents the logical layout of the network used in this lab.

![Network Diagram](screenshots/network_diagram.png)

## Lab Components

pfSense Firewall
- Serves as the primary router and firewall for the lab
- NAT and firewall rules for controlling internal/external traffic
- Optional IDS/IPS (Snort or Suricata)

Windows Server 2022
- Promoted to Domain Controller (mydomain.local)
- Active Directory Domain Services (AD DS)
- DNS and DHCP roles
- File sharing with NTFS and Share permissions
- Group Policy for user/device restrictions

Windows 10 Client
- Joined to the Active Directory domain
- Receives IP via DHCP from Windows Server
- Subject to GPO restrictions
- Able to access domain resources and shared folders

Kali Linux
- Used for penetration testing and internal reconnaissance
- Tools used: rpcclient, Kerbrute, Nmap, smbclient, and others
- Demonstrates lateral movement and domain enumeration techniques

## Tools and Technologies

- VirtualBox (hypervisor)
- pfSense firewall
- Windows Server 2022
- Windows 10 Pro
- Kali Linux
- Wireshark
- Kerbrute
- rpcclient
- smbclient
- Group Policy Editor
- Event Viewer

## Skills Demonstrated

- Network design and subnetting
- pfSense configuration and firewall rule management
- DHCP and DNS role configuration
- Active Directory domain setup
- Group Policy creation and deployment
- Domain client joining and access control
- File sharing with NTFS and Share permissions
- Basic penetration testing and enumeration
- Use of terminal tools and scripting in Kali Linux
- Traffic analysis using Wireshark

## Folder Structure

/ (root)
│
├── README.md
├── /screenshots
│   ├── network_diagram.png
│   └── other_screenshots_here.png
├── /configs
│   ├── pfsense_rules.txt
│   ├── dns_scope.txt
│   └── gpo_settings.md
├── /docs
│   ├── setup_notes.md
│   └── troubleshooting_log.md

## Lab Host Machine Specifications

This lab was built and tested using the following hardware:

- CPU: AMD Ryzen 5 7500F
- GPU: AMD RX 7800 XT
- RAM: 32 GB DDR5
- Storage: 2 TB NVMe SSD
- Host OS: Windows 11
- Virtualization Software: Oracle VirtualBox

## Notes

- All screenshots and configurations are based on a real, working home lab running on a Ryzen 5 desktop with VirtualBox.
- This lab was built to support job applications in IT support, networking, and cybersecurity roles.
- Project is actively being expanded with more advanced features like IDS/IPS and vulnerability scanning.
