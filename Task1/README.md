# 🔍 Task 1: Network Port Scanning using Nmap

**Internship:** Elevate Labs Cybersecurity Internship  
**Date:** August 4, 2025  
**Task Objective:** Perform a TCP SYN scan using Nmap to identify open ports in the local network and assess exposed services and potential risks.

---

## 🛠️ Tools Used

- [Nmap](https://nmap.org/) (Network Mapper)
- Windows Command Prompt
- ipconfig (to find IP range)

---

## 📡 Network Setup

- **IPv4 Address:** 192.168.241.106  
- **Subnet Mask:** 255.255.255.0  
- **IP Range Scanned:** `192.168.241.0/24`  
- **Command Used:**
  ```bash
  nmap -sS 192.168.241.106 -oN scan_result.txt

---

## 📊 Scan Result Summary
| Port  | State | Service      |
|-------|-------|--------------|
| 80    | open  | HTTP         |
| 135   | open  | MSRPC        |
| 139   | open  | NetBIOS-SSN  |
| 445   | open  | Microsoft-DS |
| 3306  | open  | MySQL        |
| 5357  | open  | WSDAPI       |


📁 Output saved in: scan_result.txt

🔐 Security Risk Analysis
Port 3306 (MySQL): Might allow database attacks if not properly secured or firewalled.

Ports 139 & 445: SMB ports vulnerable to exploits like EternalBlue; should not be open on public networks.

Port 80 (HTTP): Unencrypted communication; HTTPS preferred for sensitive data.

Multiple open ports: Increase the network’s attack surface if not monitored.

📚 What I Learned
How to use Nmap to perform a TCP SYN scan.

How to identify my local IP and subnet mask.

Gained hands-on experience in interpreting port scan results.

Understood the importance of securing exposed services.

Learned how attackers could use this information for reconnaissance.

✅ Task Completion Checklist
 Installed and configured Nmap

 Identified local IP range

 Performed and saved a port scan

 Analyzed results

 Created README and documentation


📄 Supporting Files
scan_result.txt – Text file with scan result

screenshot_nmap_scan.png – Terminal screenshot

