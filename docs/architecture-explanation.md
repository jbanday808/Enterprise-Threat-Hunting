# 🏗️ Enterprise Threat Hunting Architecture Explanation

---

## 📖 Overview

This document explains the architecture, components, data flow, detection workflow, and security monitoring design of the Advanced Enterprise Threat Hunting and Malware Analysis Platform.

The environment simulates a real-world enterprise Security Operations Center (SOC) using VMware Workstation Pro, Windows 11 Enterprise, Red Hat Enterprise Linux (RHEL 10.2), Splunk Enterprise, Sysmon, Splunk Universal Forwarder, Suricata IDS, NGINX, Cloudflare SSL, and MITRE ATT&CK.

The platform is designed to safely execute malware in an isolated VMware Host-Only network while collecting telemetry, forwarding logs into Splunk Enterprise, correlating detections, monitoring threats, and supporting SOC investigations.

---

## 🏗️ Enterprise Threat Hunting Architecture

![Enterprise Threat Hunting Architecture](../screenshots/architecture/Threat%20Hunting%20Architecture.png)

### Figure 1

Enterprise VMware Host-Only Threat Hunting Lab architecture showing Windows 11 telemetry collection, Splunk Enterprise SIEM, Suricata IDS monitoring, Cloudflare HTTPS access, and SOC dashboard visibility.

### References

AWS Pricing Calculator User Guide: This guide provides detailed instructions on using the AWS Pricing Calculator to estimate costs for different AWS services.

---

## 🧬 TrickBot Malware Execution Flow

![TrickBot Malware Execution Flow](../screenshots/architecture/trickbot%20malware%20execution%20flow.png)

### Figure 2

TrickBot malware execution workflow showing process creation, persistence activity, Sysmon telemetry collection, Splunk log forwarding, and SOC threat detection workflows.

### References

AWS Pricing Calculator User Guide: This guide provides detailed instructions on using the AWS Pricing Calculator to estimate costs for different AWS services.

---

## 🌐 VMware Host-Only Network Architecture

### Network Overview

The environment uses a VMware Host-Only network to isolate malware activity from the public internet while allowing communication between virtual machines.

### Network Configuration

| Component | Value |
|---|---|
| Network Type | VMware Host-Only |
| Subnet | 192.168.159.0/24 |
| Gateway | 192.168.159.2 |
| DHCP | 192.168.159.254 |

---

## 🖥️ Windows 11 Enterprise Endpoint

### Purpose

The Windows 11 Enterprise virtual machine acts as the malware analysis endpoint and telemetry source.

### Responsibilities

- Malware Execution
- Sysmon Telemetry Collection
- Windows Event Logging
- PowerShell Monitoring
- Splunk Log Forwarding
- Threat Detection Validation

### Installed Components

| Component | Purpose |
|---|---|
| Sysmon | Endpoint telemetry collection |
| Splunk Universal Forwarder | Log forwarding |
| Microsoft Defender | Malware protection |
| PowerShell | Administrative scripting |

---

## 🐧 RHEL 10.2 Splunk Enterprise SIEM

### Purpose

The RHEL 10.2 virtual machine hosts Splunk Enterprise and functions as the centralized SIEM platform.

### Responsibilities

- Log Aggregation
- Security Event Correlation
- Threat Hunting
- Dashboard Visualization
- Detection Engineering
- SOC Monitoring
- Splunk App Management

### Installed Components

| Component | Purpose |
|---|---|
| Splunk Enterprise | SIEM platform |
| NGINX | Reverse proxy |
| Suricata | IDS monitoring |
| Splunk Security Essentials | Security detections |
| Sysmon Add-on | Sysmon log parsing |

---

## 🛡️ Splunk Enterprise Services

### Splunk Web Interface

| Port | Purpose |
|---|---|
| 8000 | Splunk Web Management |

---

### Splunk Receiver

| Port | Purpose |
|---|---|
| 9997 | Receives forwarded logs |

---

### Splunk Deployment Server

| Port | Purpose |
|---|---|
| 8089 | App and forwarder management |

---

## 🌐 NGINX Reverse Proxy

### Purpose

NGINX provides secure HTTPS access to the Splunk Enterprise web interface.

### Responsibilities

- HTTPS Encryption
- Reverse Proxy Services
- SSL/TLS Termination
- Secure Web Access

### Traffic Flow

```text
HTTPS 443 → NGINX → Splunk Web 8000
```

---

## ☁️ Cloudflare DNS and SSL

### Purpose

Cloudflare provides DNS management and SSL/TLS certificate protection for secure Splunk access.

### Responsibilities

- DNS Resolution
- SSL/TLS Encryption
- HTTPS Security
- Secure Analyst Access

### Example DNS Configuration

| Setting | Value |
|---|---|
| Domain | splunk.caremedix.net |
| IP Address | 192.168.159.129 |

---

## 📡 Splunk Universal Forwarder

### Purpose

The Splunk Universal Forwarder securely forwards endpoint telemetry from Windows 11 Enterprise into Splunk Enterprise.

### Forwarded Logs

- Windows Security Logs
- Windows System Logs
- Windows Application Logs
- Sysmon Operational Logs

### Example Forwarding Port

```text
TCP 9997
```

---

## 🖥️ Sysmon Endpoint Telemetry

### Purpose

Sysmon provides advanced endpoint visibility and security telemetry.

### Collected Events

| Event ID | Description |
|---|---|
| 1 | Process Creation |
| 3 | Network Connections |
| 7 | Image Loaded |
| 11 | File Creation |
| 12 | Registry Object Create/Delete |
| 13 | Registry Value Set |
| 22 | DNS Queries |

---

## 🛡️ Suricata IDS Monitoring

### Purpose

Suricata monitors network traffic for suspicious activity and malware communications.

### Detection Capabilities

- Command-and-Control Detection
- Suspicious DNS Traffic
- Network Intrusion Detection
- Threat Intelligence Matching
- Malware Network Activity

---

## 📊 Splunk Security Dashboards

### Purpose

Splunk dashboards provide SOC visibility into endpoint activity, malware behavior, authentication activity, and threat detections.

### Dashboard Features

- Threat Hunting Dashboards
- Process Monitoring
- MITRE ATT&CK Mapping
- Authentication Monitoring
- IOC Investigation
- PowerShell Monitoring
- LOLBins Detection
- Suricata IDS Alerts

---

## 🔥 Detection Engineering Workflow

### Workflow Overview

1. Collect Endpoint Telemetry
2. Forward Logs into Splunk
3. Parse and Normalize Events
4. Correlate Threat Indicators
5. Detect Suspicious Activity
6. Generate SOC Alerts
7. Investigate Threat Activity
8. Validate Malware Behavior
9. Perform Incident Response
10. Restore Clean Environment

---

## 🎯 MITRE ATT&CK Integration

### Purpose

MITRE ATT&CK techniques are used to map malware behaviors and detection logic.

### Example Techniques

| Technique ID | Description |
|---|---|
| T1059.001 | PowerShell |
| T1055 | Process Injection |
| T1547.001 | Registry Run Keys |
| T1218 | Signed Binary Proxy Execution |
| T1105 | Ingress Tool Transfer |

---

## 🧪 Malware Analysis Workflow

### Static Analysis

Static analysis investigates malware without executing the sample.

### Static Analysis Activities

- Hash Analysis
- String Extraction
- PE Header Analysis
- YARA Scanning
- VirusTotal Analysis

---

### Dynamic Analysis

Dynamic analysis safely executes malware inside the isolated VMware environment.

### Dynamic Analysis Activities

- Process Monitoring
- Registry Monitoring
- Network Traffic Monitoring
- Persistence Detection
- PowerShell Monitoring
- IOC Collection

---

## 🚨 Incident Response Workflow

### SOC Investigation Process

1. Alert Detection
2. Threat Validation
3. IOC Investigation
4. Malware Analysis
5. Containment
6. Remediation
7. Recovery
8. Documentation

---

## 🔄 Malware Data Flow

### Execution Flow

```text
Malware Execution → Sysmon Telemetry → Universal Forwarder → Splunk Enterprise → Detection Rules → Dashboards → SOC Investigation
```

---

## 🔐 Security Controls

### Security Protections

- VMware Isolation
- Host-Only Networking
- HTTPS Encryption
- Sysmon Monitoring
- Suricata IDS
- Splunk SIEM Monitoring
- Microsoft Defender Protection
- Threat Intelligence Correlation

---

## 🛠️ Splunk Troubleshooting Workflow

### Splunk Restart Issue

The Splunk SIEM server experienced a restart failure caused by stuck helper processes.

### Troubleshooting Screenshot

![Splunk Troubleshooting](../screenshots/rhel/splunkd%204475%20troubleshooting.png)

### Figure 3

Splunk Enterprise troubleshooting workflow showing failed restart attempts, process termination using pkill, and successful SIEM recovery procedures.

### References

AWS Pricing Calculator User Guide: This guide provides detailed instructions on using the AWS Pricing Calculator to estimate costs for different AWS services.

---

### Troubleshooting Commands

#### Command Overview

### Command

```bash
sudo pkill -f splunk
```

---

### Explanation

- `sudo`: Runs as administrator.
- `pkill`: Terminates running processes.
- `-f`: Matches the full process name.
- `splunk`: Targets Splunk processes.

---

### Summary

This forcefully terminates stuck Splunk services and helper processes.

---

#### Command Overview

### Command

```bash
sudo /opt/splunk/bin/splunk start --accept-license --answer-yes --no-prompt --run-as-root
```

---

### Explanation

- `start`: Starts Splunk services.
- `--accept-license`: Accepts the license agreement.
- `--answer-yes`: Automatically confirms prompts.
- `--no-prompt`: Disables interactive prompts.
- `--run-as-root`: Runs Splunk as root.

---

### Summary

This restarts Splunk Enterprise after terminating failed or stuck processes.

---

## 📁 Architecture Components Summary

| Component | Purpose |
|---|---|
| VMware Workstation Pro | Virtualization platform |
| Windows 11 Enterprise | Malware analysis endpoint |
| RHEL 10.2 | SIEM server |
| Splunk Enterprise | Security monitoring |
| Sysmon | Endpoint telemetry |
| Universal Forwarder | Log forwarding |
| Suricata | IDS monitoring |
| NGINX | Reverse proxy |
| Cloudflare SSL | HTTPS encryption |
| Kali Linux | Analyst workstation |

---

## 🧠 Key Learning Outcomes

- Built an enterprise SIEM architecture
- Implemented Sysmon telemetry collection
- Configured Splunk Enterprise monitoring
- Integrated Suricata IDS monitoring
- Performed malware analysis safely
- Implemented MITRE ATT&CK mapping
- Developed SOC investigation workflows
- Practiced detection engineering
- Investigated endpoint telemetry
- Monitored malicious network traffic

---

## ⚠️ Security Notice

This environment is intended for educational cybersecurity research and malware analysis purposes only.

### 🚫 Do NOT Upload

- Live malware samples
- Credentials
- Private keys
- Sensitive logs
- API keys
- VM memory dumps

### ✅ Safe Uploads

- Sanitized screenshots
- Redacted logs
- YARA rules
- Detection queries
- Architecture diagrams
- Threat hunting reports

---

## 👨‍💻 Author

James Banday

- LinkedIn: https://www.linkedin.com/in/james-allen-morta-banday-62a391128/
[- GitHub: https://github.com/jbanday808](https://github.com/jbanday808/Enterprise-Threat-Hunting/tree/main)
- Medium: https://medium.com/@jamesbanday

---

## 📄 License

This project is intended for educational, cybersecurity research, and threat hunting training purposes only.

---
