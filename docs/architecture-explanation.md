# 🛡️ Enterprise Threat Hunting Platform Deployment Guide

---

## 📖 Overview

This deployment guide explains how to build and deploy the Advanced Enterprise Threat Hunting and Malware Analysis Platform using VMware Workstation Pro, Windows 11 Enterprise, Red Hat Enterprise Linux (RHEL 10.2), Splunk Enterprise, Sysmon, Microsoft Defender, Splunk Universal Forwarder, Suricata, Wireshark, VS Code, and WSL.

The environment simulates a real-world Security Operations Center (SOC) by collecting endpoint telemetry, monitoring malicious activity, analyzing malware behavior, and validating incident response procedures.

---

## 🏗️ Deployment Architecture

### 🖥️ Windows 11 Enterprise VM

Purpose:

- Malware Analysis Endpoint
- Sysmon Telemetry Collection
- Microsoft Defender Monitoring
- PowerShell Threat Hunting
- Windows Event Monitoring

---

### 🐧 RHEL 10.2 VM

Purpose:

- Splunk Enterprise SIEM Server
- Log Collection Platform
- Suricata IDS Monitoring
- Threat Correlation Engine
- Dashboard Visualization

---

### 🌐 VMware Host-Only Network

Purpose:

- Isolated Malware Analysis Environment
- Prevents External Internet Exposure
- Simulates Internal Enterprise Network
- Allows Safe Malware Execution

---

## 📋 Deployment Requirements

| Requirement | Purpose |
|---|---|
| VMware Workstation Pro | Virtualization Platform |
| Windows 11 Enterprise ISO | Malware Analysis VM |
| RHEL 10.2 ISO | Splunk Server VM |
| Splunk Enterprise | SIEM Platform |
| Sysmon | Endpoint Telemetry |
| Splunk Universal Forwarder | Log Forwarding |
| Suricata | Intrusion Detection |
| Wireshark | Packet Analysis |
| VS Code | Configuration Editing |
| WSL | Linux Development Environment |

---

## 🚀 Deployment Workflow

1. Install VMware Workstation Pro
2. Create Windows 11 Enterprise VM
3. Create RHEL 10.2 VM
4. Configure VMware Host-Only Network
5. Install Splunk Enterprise
6. Install Sysmon
7. Install Splunk Universal Forwarder
8. Configure Log Forwarding
9. Install Suricata IDS
10. Configure Splunk Dashboards
11. Create Detection Rules
12. Perform Malware Analysis
13. Validate Threat Detection
14. Document Findings
15. Restore Clean Snapshots

---

## 🖥️ Step 1 — Install VMware Workstation Pro

### Command Overview

### Command

```bash
VMware Workstation Pro Installer
```

---

### Explanation

- VMware Workstation Pro creates isolated virtual machines.
- Supports malware sandbox environments.
- Allows secure SOC simulation testing.

---

### Summary

This installs the virtualization platform used for the enterprise threat hunting lab.

---

## 🪟 Step 2 — Create Windows 11 Enterprise VM

### Recommended Configuration

| Setting | Value |
|---|---|
| CPU | 4 vCPUs |
| Memory | 8 GB RAM |
| Disk | 100 GB |
| Network | Host-Only |
| OS | Windows 11 Enterprise |

---

### Purpose

- Malware Analysis Endpoint
- Sysmon Telemetry Collection
- PowerShell Threat Hunting
- Windows Event Monitoring

---

## 🐧 Step 3 — Create RHEL 10.2 VM

### Recommended Configuration

| Setting | Value |
|---|---|
| CPU | 4 vCPUs |
| Memory | 8 GB RAM |
| Disk | 100 GB |
| Network | Host-Only |
| OS | RHEL 10.2 |

---

### Purpose

- Splunk Enterprise SIEM
- Suricata IDS Monitoring
- Dashboard Visualization
- Threat Correlation

---

## 🌐 Step 4 — Configure VMware Host-Only Network

### Purpose

- Prevents malware from reaching the internet
- Isolates malware traffic
- Simulates internal enterprise network

---

### Recommended Configuration

| Network Setting | Value |
|---|---|
| Network Type | Host-Only |
| DHCP | Enabled |
| Internet Access | Disabled |

---

## 💻 Step 5 — Install VS Code

### Command Overview

### Command

```bash
code .
```

---

### Explanation

- `code`: Opens Visual Studio Code.
- `.`: Opens the current folder.

---

### Summary

This opens the enterprise threat hunting project inside VS Code.

---

## 🐧 Step 6 — Install WSL

### Command Overview

### Command

```powershell
wsl --install
```

---

### Explanation

- `wsl`: Windows Subsystem for Linux.
- `--install`: Installs WSL and Ubuntu.

---

### Summary

This installs the Linux development environment used inside VS Code.

---

## 📊 Step 7 — Install Splunk Enterprise

### Command Overview

### Command

```bash
sudo rpm -ivh splunk-*.rpm
```

---

### Explanation

- `sudo`: Runs the command as administrator.
- `rpm -ivh`: Installs RPM packages.
- `splunk-*.rpm`: Splunk Enterprise installer.

---

### Summary

This installs Splunk Enterprise on the RHEL SIEM server.

---

## ▶️ Step 8 — Start Splunk Enterprise

### Command Overview

### Command

```bash
sudo /opt/splunk/bin/splunk start --accept-license
```

---

### Explanation

- `sudo`: Runs as administrator.
- `/opt/splunk/bin/splunk`: Splunk executable.
- `start`: Starts Splunk services.
- `--accept-license`: Accepts the Splunk license.

---

### Summary

This starts the Splunk Enterprise SIEM platform.

---

## 🖥️ Step 9 — Install Sysmon

### Command Overview

### Command

```powershell
sysmon64.exe -accepteula -i sysmonconfig-export.xml
```

---

### Explanation

- `sysmon64.exe`: Sysmon installer.
- `-accepteula`: Accepts Sysmon license agreement.
- `-i`: Installs Sysmon configuration.
- `sysmonconfig-export.xml`: Sysmon configuration file.

---

### Summary

This installs Sysmon endpoint telemetry collection.

---

## 📡 Step 10 — Install Splunk Universal Forwarder

### Purpose

- Collect Windows Event Logs
- Forward Sysmon Telemetry
- Send Defender Alerts to Splunk

---

## ⚙️ Step 11 — Configure Splunk Forwarding

### Example inputs.conf

```ini
[WinEventLog://Application]
disabled = 0
index = windows

[WinEventLog://Security]
disabled = 0
index = windows

[WinEventLog://System]
disabled = 0
index = windows

[WinEventLog://Microsoft-Windows-Sysmon/Operational]
disabled = 0
renderXml = true
index = sysmon
```

---

## 🛡️ Step 12 — Install Suricata IDS

### Command Overview

### Command

```bash
sudo dnf install suricata -y
```

---

### Explanation

- `sudo`: Runs as administrator.
- `dnf install`: Installs software packages.
- `suricata`: Intrusion Detection System.
- `-y`: Automatically confirms installation.

---

### Summary

This installs Suricata IDS for network threat monitoring.

---

## ▶️ Step 13 — Start Suricata

### Command Overview

### Command

```bash
sudo systemctl enable --now suricata
```

---

### Explanation

- `systemctl`: Manages Linux services.
- `enable`: Starts service at boot.
- `--now`: Starts service immediately.
- `suricata`: IDS monitoring service.

---

### Summary

This starts Suricata IDS monitoring.

---

## 🔍 Step 14 — Verify Sysmon Events

### Command Overview

### Command

```powershell
Get-WinEvent -LogName "Microsoft-Windows-Sysmon/Operational"
```

---

### Explanation

- `Get-WinEvent`: Reads Windows Event Logs.
- `-LogName`: Specifies the event log.
- `Sysmon/Operational`: Sysmon telemetry logs.

---

### Summary

This verifies that Sysmon telemetry is working correctly.

---

## 📊 Step 15 — Verify Splunk Data Ingestion

### Example Splunk Query

```spl
index=*
| stats count by sourcetype
```

---

### Purpose

- Verifies data ingestion
- Confirms log forwarding
- Validates SIEM telemetry collection

---

## 🧪 Step 16 — Malware Analysis Workflow

### Workflow Steps

1. Download malware sample from MalwareBazaar
2. Transfer sample into isolated VM
3. Execute malware safely
4. Monitor Sysmon telemetry
5. Monitor Splunk dashboards
6. Analyze network traffic
7. Detect persistence mechanisms
8. Correlate activity with MITRE ATT&CK
9. Validate detections
10. Restore clean VM snapshot

---

## 📊 Step 17 — Example Splunk Detection Queries

### 🔍 Process Creation Monitoring

```spl
index=windows EventCode=4688
| table _time host Account_Name New_Process_Name Command_Line Parent_Process_Name
| sort -_time
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

## 🛡️ Security Best Practices

- Use Host-Only networking
- Never expose malware VMs to the internet
- Use VM snapshots before malware execution
- Never upload live malware to GitHub
- Use sanitized screenshots only
- Store malware hashes instead of binaries
- Use redacted logs when publishing findings

---

## 📁 Recommended Screenshot Collection

- VMware Configuration
- Windows 11 Setup
- RHEL Installation
- Splunk Dashboards
- Sysmon Logs
- Malware Execution
- Suricata Alerts
- PowerShell Activity
- Detection Rules
- Incident Response Workflow

---

## 📚 References

### 🖥️ VMware Workstation Pro

https://docs.vmware.com/en/VMware-Workstation-Pro/index.html

---

### 📊 Splunk Enterprise

https://docs.splunk.com/Documentation/Splunk

---

### 🖥️ Sysmon

https://learn.microsoft.com/en-us/sysinternals/downloads/sysmon

---

### 🛡️ Suricata

https://docs.suricata.io/

---

### 🎯 MITRE ATT&CK

https://attack.mitre.org/

---

## 👨‍💻 Author

James Banday

- LinkedIn: https://www.linkedin.com/in/james-allen-morta-banday-62a391128/
- GitHub: https://github.com/jbanday808/Enterprise-Threat-Hunting/tree/main

---

## 📄 License

This project is intended for educational, cybersecurity research, and threat hunting training purposes only.

---