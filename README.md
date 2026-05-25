# 🛡️ Advanced Enterprise Threat Hunting and Malware Analysis Platform

---

## 📖 Overview

This project demonstrates an enterprise-style threat hunting and malware analysis platform using VMware Workstation Pro, Windows 11 Enterprise, Red Hat Enterprise Linux (RHEL 10.2), Splunk Enterprise, Sysmon, Microsoft Defender, Splunk Universal Forwarder, MalwareBazaar, Wireshark, PowerShell, NGINX, Cloudflare SSL, VS Code, WSL, Suricata, YARA, VirusTotal, and MITRE ATT&CK.

The environment simulates a real-world Security Operations Center (SOC) by combining isolated malware analysis, SIEM monitoring, endpoint telemetry collection, detection engineering, incident response, network intrusion detection, malware remediation validation, forensic investigation, and endpoint recovery testing.

The platform safely executes and analyzes malware inside an isolated VMware Host-Only network while collecting endpoint telemetry and security events through Sysmon, Suricata, and Splunk Enterprise dashboards.

The project demonstrates practical enterprise cybersecurity skills including:

- 🔥 Threat Hunting
- 🧪 Malware Analysis
- 📊 SIEM Engineering
- 🛡️ Detection Engineering
- 🧠 SOC Operations
- 🚨 Incident Response
- 🖥️ Endpoint Detection and Response (EDR)
- 🎯 MITRE ATT&CK Mapping
- 📡 Security Monitoring
- 📑 Windows Event Investigation
- 🌐 Network Intrusion Detection
- 📈 Security Dashboard Development
- 🔍 Log Analysis
- 📋 Threat Intelligence Analysis

---

## 🚀 Security Features

- 🔒 Isolated Malware Analysis Lab
- 🖥️ Sysmon Endpoint Telemetry
- 📊 SIEM Monitoring
- ⚙️ Process Creation Monitoring
- 🔑 Authentication Monitoring
- 🎯 MITRE ATT&CK Mapping
- 🚨 Threat Hunting Dashboards
- 🛡️ Microsoft Defender Detection Validation
- 🧹 Malware Remediation Validation
- 🧪 Dynamic Malware Analysis
- 📦 Static Malware Analysis
- 🔍 Incident Response Workflow
- ✅ Endpoint Recovery Validation
- 🌐 Network Traffic Monitoring
- 📡 Splunk Log Forwarding
- 🔥 LOLBins Detection
- 🧠 PowerShell Threat Hunting
- 📈 Security Event Correlation
- 🚫 Malware Containment Validation
- 🛠️ Registry Persistence Detection
- 📋 Threat Intelligence Analysis
- 🔐 Secure HTTPS Splunk Deployment
- 📑 Windows Security Event Monitoring
- ⚡ Real-Time Threat Detection
- 🔎 Malware Behavioral Analysis
- 📡 Endpoint Visibility Collection
- 🛡️ Suricata IDS Monitoring
- 🌐 Command-and-Control (C2) Detection
- 🧬 Threat Correlation Analysis
- 📊 Security Dashboard Visualization
- 🧪 Malware Sandbox Testing
- 📂 IOC Analysis
- 🔥 Detection Engineering Workflows
- 🧠 SOC Investigation Procedures

---

## 🏗️ Architecture Diagram

![Threat Hunting Architecture](screenshots/architecture/Threat-Hunting-Architecture.png)

---

## 🧱 Repository Structure

```text
docs/
├── deployment-guide.md
├── incident-report.md
├── lessons-learned.md
├── mitigations.md
├── malware-analysis-report.md
├── threat-hunting-report.md
├── architecture-explanation.md
├── forensic-analysis.md
├── static-analysis.md
├── dynamic-analysis.md
├── soc-workflow.md
├── detection-engineering.md

splunk/
├── dashboards/
├── detection-rules/
│   ├── powershell-detection.spl
│   ├── failed-logons.spl
│   ├── successful-logons.spl
│   ├── process-creation-monitoring.spl
│   ├── encoded-powershell-detection.spl
│   ├── registry-persistence-detection.spl
│   ├── process-injection-detection.spl
│   ├── suspicious-services.spl
│   ├── certutil-detection.spl
│   ├── rundll32-detection.spl
│   ├── mimikatz-detection.spl
│   ├── suricata-c2-alerts.spl
│   ├── network-connections.spl
│   └── mitre-attack-mapping.spl
├── saved-searches/
├── threat-hunting-queries/
├── alerts/
├── reports/
├── correlation-searches/

configs/
├── sysmon/
├── splunk/
├── nginx/
├── windows/
├── firewall/
├── cloudflare/
├── suricata/

screenshots/
├── architecture/
├── dashboards/
├── detections/
├── malware-analysis/
├── sysmon/
├── splunk/
├── incident-response/
├── wireshark/
├── powershell/
├── suricata/
├── vmware/
├── windows/
├── rhel/

reports/
├── static-analysis/
├── dynamic-analysis/
├── malware-remediation/
├── forensic-analysis/
├── indicators-of-compromise/
├── network-analysis/
├── memory-analysis/
├── incident-response/

scripts/
├── powershell/
├── bash/
├── splunk/

README.md
```

---

## 🖥️ Technologies Used

| Technology | Purpose |
|---|---|
| VMware Workstation Pro | Virtualization Platform |
| Windows 11 Enterprise | Malware Analysis Endpoint |
| RHEL 10.2 | Splunk SIEM Server |
| Splunk Enterprise | Security Monitoring |
| Sysmon | Endpoint Telemetry Collection |
| Microsoft Defender | Malware Detection |
| Splunk Universal Forwarder | Log Collection |
| MalwareBazaar | Malware Sample Repository |
| MITRE ATT&CK | Threat Mapping |
| NGINX | Reverse Proxy |
| Cloudflare SSL | HTTPS Security |
| PowerShell | Administrative Automation |
| Wireshark | Network Packet Analysis |
| VS Code | Configuration and Development |
| WSL | Linux Development Environment |
| Suricata | Intrusion Detection System |
| Sysinternals Suite | Windows Monitoring |
| PEStudio | Static Malware Analysis |
| Detect It Easy (DIE) | Malware Identification |
| VirusTotal | Threat Intelligence |
| YARA | Malware Signature Detection |

---

## 🔍 Threat Hunting Capabilities

- 📡 Endpoint Telemetry Collection
- 🔥 Real-Time Security Monitoring
- 🧠 Behavioral Malware Analysis
- 📈 SIEM Dashboard Visualization
- 🛠️ PowerShell Activity Monitoring
- 🚨 LOLBins Detection
- 🧬 MITRE ATT&CK Correlation
- 🌐 Network Connection Analysis
- 🔐 Windows Authentication Monitoring
- 🧹 Malware Cleanup Validation
- 📋 IOC Detection and Analysis
- ⚡ Process Injection Detection
- 🧪 Malware Sandbox Testing
- 📊 Threat Visualization Dashboards
- 🔎 Registry Persistence Monitoring
- 🧾 Event Log Investigation
- 🛡️ Security Event Correlation
- 📡 Command and Control (C2) Detection
- 🔥 Suspicious PowerShell Monitoring
- 🧠 Threat Intelligence Correlation
- 🌐 Suricata IDS Alert Monitoring
- 📦 Malware Hash Analysis
- 🚫 Network Intrusion Detection
- 🔥 Detection Engineering Validation
- 📊 SOC Investigation Workflow

---

## 🧪 Malware Analysis Workflow

### 📦 Static Malware Analysis

The static analysis phase examines malware samples without executing them.

#### 📋 Static Analysis Activities

- File Hash Analysis
- PE Header Inspection
- Strings Extraction
- YARA Rule Scanning
- VirusTotal Analysis
- Entropy Analysis
- Embedded URL Discovery
- Registry Artifact Identification
- Import Table Analysis
- DLL Dependency Inspection
- File Signature Validation

#### 🛠️ Static Analysis Tools

- PEStudio
- Detect It Easy (DIE)
- Strings
- VirusTotal
- YARA
- HashCalc

---

### 🧪 Dynamic Malware Analysis

The dynamic analysis phase safely executes malware inside the isolated VMware environment.

#### 📋 Dynamic Analysis Activities

- Process Monitoring
- Registry Monitoring
- Network Traffic Analysis
- Persistence Detection
- PowerShell Monitoring
- LOLBins Detection
- Credential Access Detection
- File System Monitoring
- Memory Analysis
- Process Injection Detection
- Service Creation Detection
- C2 Communication Detection
- Suricata IDS Alert Monitoring

#### 🛠️ Dynamic Analysis Tools

- Sysmon
- Splunk Enterprise
- Wireshark
- Process Explorer
- Process Monitor
- TCPView
- Windows Defender
- Suricata

---

## 📊 Detection Engineering

This project includes enterprise-style Splunk detection rules designed to identify suspicious endpoint activity, malware execution, PowerShell abuse, persistence mechanisms, authentication anomalies, LOLBins activity, and command-and-control communications.

Detection rules were mapped against MITRE ATT&CK techniques to simulate real-world SOC detection engineering workflows.

---

## 📊 Splunk Dashboards

### 📈 Security Monitoring Panels

- Failed Logons Monitoring
- Successful Logons Monitoring
- Privileged Logons Monitoring
- Process Creation Monitoring
- LOLBins Detection
- Live Threat Timeline
- Top Process Activity
- MITRE ATT&CK Mapping
- Failed Login Timeline
- PowerShell Monitoring
- Registry Persistence Detection
- Network Activity Monitoring
- Malware Execution Timeline
- Suricata IDS Alerts
- C2 Traffic Detection
- IOC Investigation Dashboard
- Detection Engineering Dashboard

---

## 🛠️ Splunk Detection Queries

### 🔍 Process Creation Monitoring

```spl
index=windows EventCode=4688
| table _time host Account_Name New_Process_Name Command_Line Parent_Process_Name
| sort -_time
```

---

### 🎯 MITRE ATT&CK PowerShell Detection

```spl
index=* powershell
| eval MITRE_Technique="T1059.001 - PowerShell"
| stats count by MITRE_Technique host source sourcetype
```

---

### 📊 Top Process Activity

```spl
index=windows EventCode=4688
| top limit=10 New_Process_Name
```

---

### 🚨 Failed Logons Detection

```spl
index=windows EventCode=4625
| stats count as "Failed Logins"
```

---

### ✅ Successful Logons Detection

```spl
index=windows EventCode=4624
| stats count as "Successful Logins"
```

---

### 🛠️ Registry Persistence Detection

```spl
index=sysmon EventCode=13
| table _time host TargetObject Details
```

---

### 🧠 Encoded PowerShell Detection

```spl
index=sysmon powershell.exe "*EncodedCommand*"
| table _time host CommandLine
```

---

### 🌐 Suricata IDS Alerts

```spl
index=suricata
| stats count by alert.signature src_ip dest_ip
```

---

## 🧬 MITRE ATT&CK Techniques

| Technique ID | Technique Name |
|---|---|
| T1059.001 | PowerShell |
| T1218 | Signed Binary Proxy Execution |
| T1055 | Process Injection |
| T1027 | Obfuscated Files or Information |
| T1547.001 | Registry Run Keys |
| T1105 | Ingress Tool Transfer |
| T1082 | System Information Discovery |
| T1016 | Network Discovery |
| T1057 | Process Discovery |
| T1049 | System Network Connections Discovery |
| T1071 | Application Layer Protocol |
| T1102 | Web Service Communication |

---

## 🔥 Malware Detection Workflow

1. 📥 Download malware samples from MalwareBazaar
2. 🔄 Transfer malware into isolated VMware environment
3. 🧪 Execute malware sample safely
4. 📡 Collect telemetry using Sysmon
5. 📊 Forward logs into Splunk Enterprise
6. 🌐 Monitor network activity with Suricata
7. 🔍 Analyze suspicious process behavior
8. 🧠 Monitor PowerShell execution
9. 🌐 Investigate network connections
10. 🎯 Correlate activity with MITRE ATT&CK
11. 🛠️ Detect persistence mechanisms
12. 🚫 Contain malware activity
13. 🧹 Validate remediation procedures
14. ♻️ Restore clean VMware snapshot
15. ✅ Verify endpoint recovery

---

## 🛡️ Security Operations Center (SOC) Workflow

1. 🔍 Alert Detection
2. 📊 Threat Analysis
3. 🚨 IOC Investigation
4. 🧠 Threat Validation
5. 🌐 Network Traffic Investigation
6. 🖥️ Endpoint Investigation
7. 🚫 Threat Containment
8. 🧹 Malware Eradication
9. ♻️ Endpoint Recovery
10. ✅ Validation and Reporting
11. 📘 Lessons Learned

---

## 🚨 Incident Response Workflow

### 📋 Incident Response Stages

1. 🔍 Detection
2. 📊 Analysis
3. 🚫 Containment
4. 🧹 Eradication
5. ♻️ Recovery
6. ✅ Validation
7. 📘 Lessons Learned

---

## 🧹 Malware Remediation Procedures

- Terminate Malicious Processes
- Remove Persistence Mechanisms
- Block Malicious IP Addresses
- Quarantine Malware Samples
- Restore Clean Snapshots
- Validate Endpoint Integrity
- Verify Splunk Telemetry
- Confirm Registry Cleanup
- Validate Network Isolation
- Remove Temporary Artifacts
- Re-enable Security Protections
- Validate Suricata IDS Monitoring

---

## 📁 Screenshots Included

The repository contains screenshots for:

- VMware Configuration
- Windows 11 Enterprise Setup
- RHEL 10.2 Configuration
- Splunk Enterprise Dashboards
- Sysmon Event Logs
- Malware Execution
- PowerShell Activity
- Threat Hunting Queries
- MITRE ATT&CK Dashboards
- LOLBins Detection
- Incident Response Workflow
- Malware Containment
- Endpoint Recovery
- Wireshark Packet Captures
- Registry Persistence Detection
- Suricata IDS Alerts
- Detection Engineering Workflows
- VS Code Configurations

---

## 🧠 Key Learning Outcomes

- Built an enterprise-grade threat hunting environment
- Performed live malware analysis safely
- Implemented SIEM monitoring with Splunk Enterprise
- Configured Sysmon advanced telemetry collection
- Integrated Suricata IDS monitoring
- Developed custom detection engineering rules
- Mapped malware behavior to MITRE ATT&CK
- Investigated malicious PowerShell activity
- Detected LOLBins abuse techniques
- Conducted malware remediation validation
- Performed endpoint recovery procedures
- Practiced real-world SOC investigation workflows
- Analyzed Windows Security Events
- Investigated endpoint telemetry
- Monitored malware persistence mechanisms
- Created enterprise security dashboards
- Investigated malicious network traffic

---

## 📌 Project Highlights

- 🛡️ Enterprise Security Monitoring
- 🧪 Live Malware Analysis
- 📊 SIEM Dashboard Development
- 🔥 Threat Hunting Investigations
- 🧬 MITRE ATT&CK Correlation
- 🚨 Incident Response Simulation
- 🧹 Malware Cleanup Validation
- ♻️ Endpoint Recovery Testing
- 🔍 PowerShell Threat Detection
- 🌐 Network Traffic Analysis
- 📡 Endpoint Telemetry Collection
- ⚡ Real-Time Security Monitoring
- 🔐 Secure Splunk HTTPS Deployment
- 🛡️ Suricata IDS Integration
- 📋 Threat Intelligence Analysis
- 🔥 Detection Engineering Workflows
- 🧠 SOC Investigation Procedures

---

## ⚠️ Security Notice

This project is intended for educational cybersecurity research and threat hunting training purposes only.

### 🚫 Do NOT Upload

- Live Malware Samples
- Private Keys
- Credentials
- API Keys
- Cloudflare Certificates
- Sensitive Logs
- Personal Information

### ✅ Recommended Safe Content

- Sanitized Screenshots
- Redacted Logs
- IOC Reports
- Sample Hashes
- Detection Screenshots
- Redacted Configurations

---

## 📚 References

## 🖥️ VMware Workstation Pro

VMware Workstation Pro Documentation:  
https://docs.vmware.com/en/VMware-Workstation-Pro/index.html

Purpose:  
Used to create isolated virtual machines for malware analysis and threat hunting.

---

## 🪟 Windows 11 Enterprise

Microsoft Windows Documentation:  
https://learn.microsoft.com/en-us/windows/

Purpose:  
Used as the enterprise endpoint for malware execution and telemetry collection.

---

## 🐧 Red Hat Enterprise Linux (RHEL)

RHEL Documentation:  
https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/

Purpose:  
Used as the SIEM server platform hosting Splunk Enterprise and Suricata.

---

## 📊 Splunk Enterprise

Splunk Documentation:  
https://docs.splunk.com/Documentation/Splunk

Purpose:  
Used for centralized SIEM monitoring and threat hunting.

---

## 📡 Splunk Universal Forwarder

Splunk Forwarder Documentation:  
https://docs.splunk.com/Documentation/Forwarder

Purpose:  
Used to forward Windows and Sysmon logs into Splunk Enterprise.

---

## 🖥️ Sysmon

Sysmon Documentation:  
https://learn.microsoft.com/en-us/sysinternals/downloads/sysmon

Purpose:  
Used to capture advanced endpoint telemetry and process monitoring.

---

## ⚔️ SwiftOnSecurity Sysmon Config

GitHub Repository:  
https://github.com/SwiftOnSecurity/sysmon-config

Purpose:  
Provides advanced Sysmon configuration rules for malware detection.

---

## 🛡️ Microsoft Defender

Microsoft Defender Documentation:  
https://learn.microsoft.com/en-us/microsoft-365/security/defender/

Purpose:  
Used to validate malware detection and remediation procedures.

---

## ☁️ MalwareBazaar

MalwareBazaar:  
https://bazaar.abuse.ch/

Purpose:  
Used to download malware samples for analysis.

---

## 🎯 MITRE ATT&CK

MITRE ATT&CK Framework:  
https://attack.mitre.org/

Purpose:  
Used to map attacker tactics and techniques.

---

## 🌐 NGINX

NGINX Documentation:  
https://nginx.org/en/docs/

Purpose:  
Used as a secure reverse proxy for Splunk Enterprise.

---

## 🔒 Cloudflare SSL/TLS

Cloudflare Documentation:  
https://developers.cloudflare.com/ssl/

Purpose:  
Used to configure HTTPS encryption.

---

## 🌐 Wireshark

Wireshark Documentation:  
https://www.wireshark.org/docs/

Purpose:  
Used for packet capture and network traffic analysis.

---

## ⚡ PowerShell

PowerShell Documentation:  
https://learn.microsoft.com/en-us/powershell/

Purpose:  
Used for scripting, automation, and malware analysis.

---

## 💻 Visual Studio Code (VS Code)

VS Code Documentation:  
https://code.visualstudio.com/docs

Purpose:  
Used for editing configurations, scripts, dashboards, and Markdown documentation.

---

## 🛡️ Suricata

Suricata Documentation:  
https://docs.suricata.io/

Purpose:  
Used as an IDS/IPS platform for detecting suspicious network traffic and malware communications.

---

## 📈 Splunk Security Essentials

Splunkbase:  
https://splunkbase.splunk.com/app/3435

Purpose:  
Provides security dashboards and MITRE ATT&CK detections.

---

## 🧬 Splunk Add-on for Sysmon

Splunkbase:  
https://splunkbase.splunk.com/app/1914/

Purpose:  
Used to normalize Sysmon logs for Splunk analysis.

---

## 🪟 Splunk Add-on for Microsoft Windows

Splunkbase:  
https://splunkbase.splunk.com/app/742/

Purpose:  
Used to ingest and parse Windows Event Logs.

---

## 🔥 LOLBAS Project

LOLBAS Documentation:  
https://lolbas-project.github.io/

Purpose:  
Used for identifying Living Off the Land Binaries (LOLBins).

---

## 📦 PEStudio

PEStudio Documentation:  
https://www.winitor.com/

Purpose:  
Used for static malware analysis.

---

## 🧪 Detect It Easy (DIE)

GitHub Repository:  
https://github.com/horsicq/Detect-It-Easy

Purpose:  
Used to identify packers and malware signatures.

---

## 🧾 YARA

YARA Documentation:  
https://yara.readthedocs.io/

Purpose:  
Used to create malware detection rules.

---

## 📊 VirusTotal

VirusTotal Documentation:  
https://docs.virustotal.com/

Purpose:  
Used for malware intelligence and hash reputation analysis.

---

# 👨‍💻 Author

James Banday

- LinkedIn: https://www.linkedin.com/in/james-allen-morta-banday-62a391128/
- GitHub: https://github.com/jbanday808/Enterprise-Threat-Hunting/tree/main

---

# 📄 License

This project is intended for educational, cybersecurity research, and threat hunting training purposes only.

---
