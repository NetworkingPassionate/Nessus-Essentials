# Nessus-Essentials
<img width="1710" height="424" alt="image" src="https://github.com/user-attachments/assets/7f945f3e-472c-490b-8599-fee091ea08b7" />


# 🔍 Nessus Essentials Lab – Vulnerability Scanning Sandbox

This project demonstrates a basic vulnerability scan using Nessus Essentials against a consented localhost environment (127.0.0.1), showcasing how vulnerability assessment tools identify configuration issues, legacy protocols, and outdated software.
## 🛠️ Scan Environment
- Target: Local Windows test system (loopback interface only)
- Tool Used: Nessus Essentials (Tenable)
- Scan Type: Host Discovery and Vulnerability Assessment
- Plugins: Default enabled plugins (with TCP/UDP checks)


  
## 📌 Lab Objectives (Pre-Scan Phase)

- Set up and configure Nessus Essentials in a Windows/Linux VM
- Review scanning policies, targets, and credentialed scan options
- Define scope and ethical usage boundaries for vulnerability scans
- Prepare documentation templates for scan reports, remediation tracking, and lab notes


## 📄 Sample Findings (Redacted)

| Severity   | Description                               | CVE Reference     |
|------------|-------------------------------------------|-------------------|
| 🔴 Critical | SMBv1 protocol detected (disabled by default) | CVE-2017-0144     |
| 🟠 High     | OpenSSH version out-of-date                  | CVE-2018-15473     |
| 🔵 Info     | ICMP timestamp responses enabled             | —                 |

All identifiers (hostnames, paths, usernames, MACs) have been sanitized.

<img width="1905" height="759" alt="image" src="https://github.com/user-attachments/assets/a6632e09-d8c3-42f1-b2c3-da523e8ae9c8" />


## 🧪 Vulnerability Description

We have a critical vulnerability displayed, so why don't we go ahead and tackle that issue: <b/>

When SMB signing is **not required**, SMB packets lack integrity verification, allowing attackers to intercept or modify traffic between hosts. Disabling this vulnerability is critical to prevent **man-in-the-middle** and **relay attacks** in SMB-based file sharing environments. This exposure is flagged by tools like **Nessus**, **OpenVAS**, and **Microsoft Defender**.


### Remedial Actions
Our critical vulnerability, **“SMB Signing Not Required”**, requires our attention. 


## 🔧 Fix Applied (Windows Home Edition)

On my Windows 11 Home-Edition, I decided to use Powershell to try and solve the problem; 

### ➤ PowerShell Commands
```powershell
Set-SmbClientConfiguration -RequireSecuritySignature $true
Set-SmbServerConfiguration -RequireSecuritySignature $true
```

## 📘 Purpose & Takeaways
- ✅ Practice responsible use of vulnerability scanners in controlled environments
- ✅ Review and apply recommended patches and configuration hardening
- ✅ Capture and document findings for portfolio and interview prep





## 🛡️ Ethical Disclaimer

This lab is for **educational purposes only** and operates on non-production, consented systems. No scanning of public IPs or unauthorized networks will be conducted. All demonstrations prioritize responsible security practices.


