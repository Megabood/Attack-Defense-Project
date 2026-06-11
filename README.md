# Attack-Defense-Project
Created by: Adam Snyder & Kyle Questad College: Grand Canyon University Project Type: Self-Paced

***

## Full PDF Here: https://mygcuedu6961-my.sharepoint.com/:w:/g/personal/asnyder51_my_gcu_edu/IQA7Xf39tUhLQaR44CR_dySJAfTlrpuMd_dvXYbGXl56rtU?e=eeS2dO 

## Also uploaded to this repo!

***

## 🌐 Network Topology

This project features a custom‑built virtualized network designed to emulate a realistic enterprise environment. The lab consists of multiple virtual machines connected through a private LAN (`192.168.100.0/24`) using bridged adapters for internal communication and NAT for internet access.

Each VM plays a distinct role in the ecosystem:

| Hostname | OS | IP Address | Role |
|-----------|----|-------------|------|
| **KaliATTACK** | Kali Linux | 192.168.100.20 | Attacker VM |
| **UbuSIEM** | Ubuntu Desktop | 192.168.100.11 | Wazuh SIEM |
| **snortubuntu1** | Ubuntu Server | 192.168.100.30 | Snort IDS Server |
| **KaliAgent1** | Kali Linux | 192.168.100.10 | Agent / Victim |
| **WindowsAgent** | Windows 10 | 192.168.100.12 | Agent / Victim |

---

## 🛡️ Defense Summary

The blue team engineered a multi‑layered defensive architecture integrating **Wazuh**, **Snort**, and **Suricata** to simulate enterprise‑grade monitoring and detection.

- **Wazuh SIEM** served as the central hub for log aggregation, correlation, and real‑time alerting.  
- **Snort & Suricata IDS** provided network‑based threat detection using signature‑based analysis.  
- A custom **Snort ruleset** was developed to align with the lab’s traffic patterns, improving alert clarity and relevance.  

This setup enabled seamless visibility across host and network layers, ensuring efficient detection and response to simulated attacks.

---

## ⚔️ Attack Summary

The red team conducted a series of offensive operations targeting the **KaliAgent1** victim machine (`192.168.100.10`), all of which were successfully detected and logged by the defensive stack.

Key attack phases included:

- **Reconnaissance:** Nmap SYN scan and OS fingerprinting revealed open FTP (21), SSH (22), and HTTP (80) services.  
- **Brute Force:** Hydra attacks against SSH and FTP using the *rockyou* wordlist tested credential resilience.  
- **Denial of Service:** A SYN flood via *hping3* simulated service disruption with over 343,000 packets sent.  
- **Man‑in‑the‑Middle:** ARP spoofing using *arpspoof* intercepted traffic between victim and gateway.  
- **Vulnerability Scanning:** *Nikto* identified Apache misconfigurations, missing headers, and XSS exposure.  

All malicious activities were captured by **Snort 3** and **Suricata**, then correlated within **Wazuh**, confirming a fully functional detection pipeline.

---

## 🧰 Tools & Technologies


| Category | Tool | Purpose |
|-----------|------|----------|
| **Operating Systems** | Kali Linux, Ubuntu Desktop, Ubuntu Server, Windows 10 | Diverse OS environment for realistic enterprise simulation |
| **SIEM** | Wazuh | Centralized log aggregation, correlation, and alerting |
| **IDS/IPS** | Snort 3, Suricata | Network-based intrusion detection and traffic analysis |
| **Attack Tools** | Nmap, Hydra, hping3, arpspoof, Nikto | Reconnaissance, brute force, DoS, MITM, and vulnerability scanning |
| **Networking** | VirtualBox, NAT & Bridged Adapters | LAN communication and internet access |
| **Custom Rules** | Snort Ruleset | Tailored detection for lab-specific traffic patterns |
| **Visualization** | Wazuh Dashboard | Real-time event monitoring and alert correlation |


---

## 🚀 Project Impact

This lab provides hands‑on experience with **real‑world cybersecurity tools**, bridging offensive and defensive operations. It demonstrates:

- Practical understanding of SIEM and IDS integration  
- Incident detection and response workflows  
- Custom rule creation and alert optimization  
- Realistic attack simulation and forensic analysis  

This project stands as a strong portfolio piece — showcasing technical depth, problem‑solving ability, and a comprehensive grasp of enterprise security architecture.

---
