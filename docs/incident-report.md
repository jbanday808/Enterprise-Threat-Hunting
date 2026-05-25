# 🚨 Enterprise Threat Hunting Incident Report

---

# 📖 Executive Summary

---

## 📌 Incident Overview

Incident ID: INC-2026-TH-001

Incident Severity: High

Incident Status: Resolved

Detection Date: May 24, 2026

Security Platform: Splunk Enterprise SIEM

Affected System: Windows 11 Enterprise Endpoint

Malware Family: TrickBot

Investigation Environment:

- VMware Workstation Pro
- Windows 11 Enterprise
- RHEL 10.2
- Splunk Enterprise
- Sysmon
- Splunk Universal Forwarder
- Microsoft Defender
- Suricata IDS
- Kali Linux
- VirusTotal
- MalwareBazaar
- YARA

---

## 📖 Incident Summary

On May 24, 2026, the enterprise Security Operations Center (SOC) detected suspicious malware execution activity within the isolated VMware Host-Only threat hunting environment.

The incident involved the execution of a TrickBot malware sample obtained from MalwareBazaar for enterprise threat hunting, malware analysis, and SIEM detection engineering validation.

The malware activity generated multiple security alerts within Splunk Enterprise, Sysmon, and Microsoft Defender telemetry logs.

The Security Operations Center successfully identified:

- Suspicious executable execution
- Malware persistence activity
- Suspicious process creation
- Potential command-and-control behavior
- Windows Defender malware detections
- Threat intelligence matches

The malware was safely contained inside an isolated VMware Host-Only network environment without impacting external systems.

---

# 🎯 Key Findings

---

## ✅ Malware Execution

The malware sample successfully executed inside the Windows 11 Enterprise virtual machine.

---

## ✅ Splunk Detection

Splunk Enterprise detected suspicious malware activity through:

- Sysmon logs
- Windows Event Logs
- Microsoft Defender telemetry
- Threat hunting queries
- Detection engineering rules

---

## ✅ Malware Persistence

The malware copied itself into:

```text
C:\Users\james\AppData\Roaming\winapp\
```

and renamed itself to:

```text
sqhbjans.exe
```

---

## ✅ Threat Intelligence Correlation

Threat intelligence validation confirmed:

- TrickBot malware indicators
- Malicious reputation
- Suspicious malware signatures
- Multiple antivirus detections

---

## ✅ SOC Visibility

The enterprise threat hunting platform successfully provided:

- Endpoint telemetry visibility
- Malware execution visibility
- Process monitoring
- Threat hunting dashboards
- Detection engineering validation
- Incident response workflows

---

# 🏗️ Incident Architecture

---

## 🖼️ Enterprise Threat Hunting Architecture

![Enterprise Threat Hunting Architecture](../screenshots/architecture/Threat%20Hunting%20Architecture.png)

### Figure 1

Enterprise VMware Host-Only Threat Hunting Lab architecture showing endpoint telemetry collection, Splunk SIEM monitoring, malware analysis, and SOC investigation workflows.

### References

AWS Pricing Calculator User Guide: This guide provides detailed instructions on using the AWS Pricing Calculator to estimate costs for different AWS services.

---

## 🖼️ TrickBot Malware Execution Flow

![TrickBot Malware Execution Flow](../screenshots/architecture/trickbot%20malware%20execution%20flow.png)

### Figure 2

TrickBot malware execution workflow showing malware execution stages, persistence behavior, telemetry collection, and enterprise incident response visibility.

### References

AWS Pricing Calculator User Guide: This guide provides detailed instructions on using the AWS Pricing Calculator to estimate costs for different AWS services.

---

# 🖥️ Affected Systems

---

| System | Role | Status |
|---|---|---|
| Windows 11 Enterprise | Malware Execution Endpoint | Compromised |
| Splunk Enterprise SIEM | Log Collection & Detection | Operational |
| Kali Linux | Analyst Workstation | Operational |
| Suricata IDS | Network Monitoring | Operational |

---

# 🧬 Technical Analysis

---

# ⚡ Initial Detection

---

## 📖 Detection Summary

The malware activity was identified through multiple security telemetry sources including:

- Sysmon Event Logs
- Windows Defender
- Splunk Enterprise
- Threat hunting dashboards
- Malware detection queries

---

## 🖼️ Splunk Malware Detection Dashboard

![Splunk Malware Detection Dashboard](../screenshots/dynamic-analysis/splunk-malware-detectio.png)

### Figure 3

Splunk Enterprise detection dashboard identifying suspicious malware activity, malicious executable paths, and Microsoft Defender malware detections.

### References

AWS Pricing Calculator User Guide: This guide provides detailed instructions on using the AWS Pricing Calculator to estimate costs for different AWS services.

---

# 🧪 Malware Analysis

---

## 📖 Malware Sample

The malware sample analyzed during the investigation was identified as TrickBot malware.

---

## 🖼️ MalwareBazaar Threat Intelligence

![MalwareBazaar Threat Intelligence](../screenshots/static-analysis/MalwareBazaar.png)

### Figure 4

MalwareBazaar intelligence analysis identifying the TrickBot malware family, malware hashes, and threat intelligence indicators.

### References

AWS Pricing Calculator User Guide: This guide provides detailed instructions on using the AWS Pricing Calculator to estimate costs for different AWS services.

---

## 🖼️ VirusTotal Threat Intelligence

![VirusTotal Threat Intelligence](../screenshots/static-analysis/virustotal-trickbot-analysis.png)

### Figure 5

VirusTotal malware intelligence analysis showing antivirus detections, suspicious indicators, and malware reputation associated with the TrickBot sample.

### References

AWS Pricing Calculator User Guide: This guide provides detailed instructions on using the AWS Pricing Calculator to estimate costs for different AWS services.

---

## 🖼️ Windows PE Executable Analysis

![Windows PE Executable Analysis](../screenshots/static-analysis/sqhbjans[.exe].png)

### Figure 6

Static malware analysis identifying the TrickBot sample as a 32-bit Windows Portable Executable (PE32) binary.

### References

AWS Pricing Calculator User Guide: This guide provides detailed instructions on using the AWS Pricing Calculator to estimate costs for different AWS services.

---

# 📡 Sysmon Investigation

---

## 📖 Overview

Sysmon telemetry captured malware activity including:

- Process creation
- File creation
- Registry persistence
- Network connections
- Suspicious parent-child relationships

---

## 📊 Important Sysmon Event IDs

---

| Event ID | Description |
|---|---|
| 1 | Process Creation |
| 3 | Network Connections |
| 11 | File Create |
| 13 | Registry Persistence |
| 22 | DNS Queries |

---

# ⚡ Threat Hunting Queries

---

## 🔍 Process Creation Investigation

```spl
index=sysmon EventCode=1
| table _time host Image ParentImage CommandLine User
| sort -_time
```

---

## 🔍 Registry Persistence Investigation

```spl
index=sysmon EventCode=13
| table _time host TargetObject Details Image
```

---

## 🔍 Network Connection Investigation

```spl
index=sysmon EventCode=3
| table _time host Image DestinationIp DestinationPort
```

---

# 🎯 MITRE ATT&CK Mapping

---

| Technique ID | Technique |
|---|---|
| T1059.001 | PowerShell |
| T1547.001 | Registry Run Keys |
| T1105 | Ingress Tool Transfer |
| T1055 | Process Injection |
| T1218 | Signed Binary Proxy Execution |

---

# 📊 Incident Timeline

---

| Time | Activity |
|---|---|
| 2:11 PM | TrickBot malware executed |
| 2:12 PM | Sysmon process creation logged |
| 2:13 PM | Windows Defender alert generated |
| 2:14 PM | Splunk detection triggered |
| 2:15 PM | Threat hunting investigation initiated |
| 2:18 PM | Threat intelligence validated |
| 2:20 PM | Malware isolated |
| 2:25 PM | VM snapshot restored |

---

# 🚨 Incident Response Actions

---

## ✅ Containment Actions

- Isolated VMware Host-Only network
- Blocked suspicious activity
- Preserved forensic evidence
- Restored clean VM snapshot
- Removed malware sample

---

## ✅ Eradication Actions

- Deleted malicious executable
- Validated Microsoft Defender status
- Confirmed endpoint cleanup
- Verified clean telemetry logs

---

## ✅ Recovery Actions

- Restored clean VMware snapshot
- Re-enabled endpoint monitoring
- Verified Splunk ingestion
- Validated Sysmon telemetry

---

# 🧠 Lessons Learned

---

## ✅ Security Findings

- Sysmon significantly improved endpoint visibility
- Splunk Enterprise successfully detected malware activity
- Threat intelligence improved malware identification
- VMware Host-Only networking safely isolated malware execution
- Detection engineering improved SOC investigation workflows

---

# 🔐 Security Recommendations

---

## ✅ Recommended Improvements

- Expand Sysmon logging coverage
- Improve SIEM alert correlation
- Expand YARA detection rules
- Improve PowerShell monitoring
- Add additional Suricata IDS detections
- Automate threat intelligence enrichment
- Improve malware sandboxing visibility

---

# 📚 References

---

## 📊 Splunk Enterprise

https://docs.splunk.com/Documentation/Splunk

---

## 🖥️ Sysmon

https://learn.microsoft.com/en-us/sysinternals/downloads/sysmon

---

## 🎯 MITRE ATT&CK

https://attack.mitre.org/

---

## 🛡️ Suricata

https://docs.suricata.io/

---

## 🧾 YARA

https://yara.readthedocs.io/

---

## ☁️ MalwareBazaar

https://bazaar.abuse.ch/

---

## 📊 VirusTotal

https://docs.virustotal.com/

---

# 👨‍💻 Author

James Banday

- LinkedIn: https://www.linkedin.com/in/james-allen-morta-banday-62a391128/
- GitHub: https://github.com/jbanday808
- Medium: https://medium.com/@jamesbanday

---

# 📄 License

This project is intended for educational, cybersecurity research, and threat hunting training purposes only.

---
