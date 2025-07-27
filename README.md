# Nessus-Essentials


# 🔍 Nessus Essentials Lab – Vulnerability Scanning Sandbox

This project demonstrates a basic vulnerability scan using Nessus Essentials against a consented localhost environment (127.0.0.1), showcasing how vulnerability assessment tools identify configuration issues, legacy protocols, and outdated software.
## 🛠️ Scan Environment
- Target: Local Windows test system (loopback interface only)
- Tool Used: Nessus Essentials (Tenable)
- Scan Type: Host Discovery and Vulnerability Assessment
- Plugins: Default enabled plugins (with TCP/UDP checks)
  
## 📄 Sample Findings (Redacted)
| Severity | Description | CVE Reference | 
| 🔴 Critical | SMBv1 protocol detected (disabled by default) | CVE-2017-0144 | 
| 🟠 High | OpenSSH version out-of-date | CVE-2018-15473 | 
| 🔵 Info | ICMP timestamp responses enabled | — | 


All identifiers (hostnames, paths, usernames, MACs) have been sanitized.
📘 Purpose & Takeaways
- ✅ Practice responsible use of vulnerability scanners in controlled environments
- ✅ Review and apply recommended patches and configuration hardening
- ✅ Capture and document findings for portfolio and interview prep
⚠️ Disclaimer
This scan was conducted on a consented test system for educational purposes only. No private or external assets were scanned, and all sensitive data has been redacted.




## 📌 Lab Objectives (Pre-Scan Phase)

- Set up and configure Nessus Essentials in a Windows/Linux VM
- Review scanning policies, targets, and credentialed scan options
- Define scope and ethical usage boundaries for vulnerability scans
- Prepare documentation templates for scan reports, remediation tracking, and lab notes

## 🛡️ Ethical Disclaimer

This lab is for **educational purposes only** and operates on non-production, consented systems. No scanning of public IPs or unauthorized networks will be conducted. All demonstrations prioritize responsible security practices.


