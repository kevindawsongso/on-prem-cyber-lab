# Cybersecurity Home Lab

## Overview
Welcome to my cybersecurity home lab repository! This lab is designed to enhance my skills and knowledge in cybersecurity, focusing on various tools and technologies. The lab includes multiple subnets and interfaces, IDS/IPS systems, and vulnerability scanning tools.

## Lab Components

### pfSense Firewall/Router
- **WAN:** 192.168.136.128/24 on em0
- **LAN:** 192.168.1.1/24 on em1
- **VICTIMNETWORK:** 192.168.2.1/24 on em2
- **SPLUNK:** 192.168.3.1/24 on em3
- **NESSUS:** 192.168.4.1/24 on em4
- **SURICATA:** 192.168.5.1/24 on em5
- **SPAN:** em6

### VMware Workstation VMnet Setup
- **VMnet1:** WAN
- **VMnet2:** Kali
- **VMnet3:** Victim Network
- **VMnet4:** Splunk
- **VMnet5:** Nessus
- **VMnet6:** Suricata
- **VMnet7:** Span Port

### Suricata IDS/IPS
- **Deployment:** Installed on a subnet with vulnerable computers.
- **Integration:** Logs are forwarded to Splunk using a Universal Forwarder for centralized monitoring.
- **Achievements:** Successfully detected and logged various types of network traffic and potential threats.

### Splunk
- **Role:** Centralized log management and analysis.
- **Data Sources:** Win event logs, Sysmon logs, Suricata logs, and Nessus scan results.
- **Configuration:** Logs forwarded from Suricata and Sysmon are ingested using a Splunk Universal Forwarder.

### Nessus Vulnerability Scanning
- **Deployment:** Installed to scan the Victim Network.
- **Targets:** One Windows 10 machine and a Metasploitable 2 instance.
- **Achievements:** Identified and reported vulnerabilities, providing a basis for further security measures.

## Firewall Rules
- **Suricata to Splunk:** Configured to allow traffic between Suricata and Splunk for log forwarding.

## Projects and Achievements

### Project: Suricata Deployment
- **Objective:** Deploy and configure Suricata for network traffic analysis and intrusion detection.
- **Setup:**
  - Installed Suricata on a designated subnet.
  - Configured Suricata rules and logging.
  - Integrated with Splunk for centralized log analysis.
- **Outcome:** Enhanced visibility into network traffic and improved detection capabilities.

### Project: Nessus Vulnerability Scanning
- **Objective:** Conduct regular vulnerability scans on the Victim Network.
- **Setup:**
  - Installed Nessus and configured scan policies.
  - Scheduled regular scans of Windows 10 and Metasploitable 2.
  - Integrated scan results with Splunk for comprehensive analysis.
- **Outcome:** Identified critical vulnerabilities and established a remediation process.

## Certifications
- Microsoft Certified: Azure Fundamentals
- ISC2 Certified in Cyber Security
- CompTIA Security+
- CompTIA A+
- CompTIA Network+

## Future Plans
- **Expand Network:** Add more machines and subnets to the lab.
- **Automate Remediation:** Develop scripts to automate vulnerability remediation.
- **Enhance Monitoring:** Integrate additional data sources and improve detection rules in Suricata and Splunk.

## Contact
Feel free to reach out if you have any questions or suggestions!

[Email](mailto:your-email@example.com) | [LinkedIn](https://www.linkedin.com/in/your-profile)
