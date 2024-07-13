# VMware-based Cybersecurity Lab

This repository contains details and findings from my VMware-based cybersecurity lab, which includes various tools and configurations for reconnaissance, vulnerability scanning, intrusion detection, and security monitoring.

## Objective

Deploy and configure a comprehensive cybersecurity lab to simulate, detect, and analyze malicious activities.

## Lab Components

- **Kali Linux**: Used for reconnaissance and penetration testing.
- **pfSense**: Provides network segmentation and firewall functionalities.
- **Splunk**: Used as a Security Information and Event Management (SIEM) system.
- **Suricata**: Functions as an Intrusion Detection System (IDS) and Intrusion Prevention System (IPS).
- **Nessus**: Used for vulnerability scanning.


# Latest Findings 7.12.24

### Nmap Scan Report (7.7.24)

The following are the results of an Nmap scan performed on the Victim Network (192.168.2.0/24). The scan was executed to discover open ports and services running on the network.

#### Scan Command
nmap -sV -p0-65535 -oN /home/kali/Desktop/nmap_scan_results.txt 192.168.2.1/24


#### Results
* 192.168.2.1: Ports: 53 (domain), 80 (http), 443 (ssl/http) Services: Unbound, nginx

* 192.168.2.2 (DESKTOP-6NM36N8.home.arpa): Ports: 135 (msrpc), 139 (netbios-ssn), 445 (microsoft-ds?), 5040 (unknown), and various high ports for msrpc.
Services: Microsoft Windows RPC, Microsoft Windows netbios-ssn

* 192.168.2.3: Ports: 21 (ftp), 22 (ssh), 23 (telnet), 25 (smtp), 53 (domain), 80 (http), 111 (rpcbind), 139 (netbios-ssn), 445 (netbios-ssn), 512 (exec), 513 (login), 514 (shell), 1099 (java-rmi), 1524 (bindshell), 2049 (nfs), 2121 (ccproxy-ftp?), 3306 (mysql), 3632 (distccd), 5432 (postgresql), 5900 (vnc), 6000 (X11), 6667 (irc), 6697 (irc), 8009 (ajp13), 8180 (http), 8787 (drb), various RPC ports.
Services: vsftpd, OpenSSH, Linux telnetd, Postfix smtpd, ISC BIND, Apache httpd, Samba smbd, netkit-rsh rexecd, Netkit rshd, MySQL, PostgreSQL, VNC, UnrealIRCd, Apache Tomcat, Ruby DRb, distccd

### Nessus PCI Scan Report (1.7.24)
A PCI scan was performed using Nessus, and the following vulnerabilities were identified along with their suggested remediations:

### Suggested Remediations
#### ISC BIND 9.x < 9.11.22, 9.12.x < 9.16.6, 9.17.x < 9.17.4 DoS:

* Action: Upgrade to BIND 9.11.22, 9.16.6, 9.17.4 or later.
* Vulnerabilities: 3
* Hosts: 1

#### phpMyAdmin prior to 4.8.6 SQLi vulnerability (PMASA-2019-3):
* Action: Upgrade to phpMyAdmin version 4.8.6 or later. Alternatively, apply the patches referenced in the vendor advisories.
* Vulnerabilities: 2
* Hosts: 1

#### Samba Badlock Vulnerability:
* Action: Upgrade to Samba version 4.2.11 / 4.3.8 / 4.4.2 or later.
* Vulnerabilities: 1
* Hosts: 1
#### TWiki 'rev' Parameter Arbitrary Command Execution:
* Action: Apply the appropriate hotfix referenced in the vendor advisory.
* Vulnerabilities: 0
* Hosts: 1


## Lab Configuration

### Network Setup

- **VMnet1**: WAN - 192.168.136.128/24
- **VMnet2**: Kali - 192.168.2.1/24
- **VMnet3**: Victim Network - 192.168.2.0/24
- **VMnet4**: Splunk - 192.168.3.0/24
- **VMnet5**: Nessus - 192.168.4.0/24
- **VMnet6**: Suricata - 192.168.5.0/24
- **VMnet7**: Span Port - Promiscuous mode for traffic monitoring

### Interfaces

- **WAN**: 192.168.136.128/24
- **LAN**: 192.168.1.1/24
- **Victim Network**: 192.168.2.1/24
- **Splunk**: 192.168.3.1/24
- **Nessus**: 192.168.4.1/24
- **Suricata**: 192.168.5.1/24

## Setup and Objectives

### Objective 1: Perform Reconnaissance

- **Tool**: Kali Linux
- **Setup**: 
  - Deployed on VMnet2.
  - Configured to access all networks within the lab.
- **Outcome**: Successfully performed NMAP scans and Metasploit exploits on the victim network.

### Objective 2: Network Segmentation

- **Tool**: pfSense
- **Setup**: 
  - Configured network segmentation with subnets and firewall rules.
  - Enabled traffic filtering and monitoring.
- **Outcome**: Enhanced network security through effective segmentation and firewall configurations.

### Objective 3: Intrusion Detection and Prevention

- **Tool**: Suricata
- **Setup**: 
  - Deployed on VMnet6.
  - Configured to monitor network traffic and generate alerts.
- **Outcome**: Successfully detected and prevented malicious activities.

### Objective 4: Security Monitoring and Analysis

- **Tool**: Splunk
- **Setup**: 
  - Deployed on VMnet4.
  - Configured to collect and analyze logs from various sources, including Suricata and Nessus.
- **Outcome**: Centralized logging and enhanced visibility into network activities.

### Objective 5: Vulnerability Scanning

- **Tool**: Nessus
- **Setup**: 
  - Deployed on VMnet5.
  - Conducted regular vulnerability scans on the victim network.
- **Outcome**: Identified and remediated critical vulnerabilities.
