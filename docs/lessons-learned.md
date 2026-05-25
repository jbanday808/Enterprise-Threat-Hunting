# 🧠 Lessons Learned

---

# 📖 Overview

---

This document summarizes the key lessons learned during the development, deployment, malware analysis, threat hunting, and incident response activities performed within the Enterprise Threat Hunting Platform.

The project successfully demonstrated enterprise-level cybersecurity operations using:

- VMware Workstation Pro
- Windows 11 Enterprise
- RHEL 10.2
- Splunk Enterprise
- Sysmon
- Splunk Universal Forwarder
- Microsoft Defender
- Suricata IDS
- PowerShell
- YARA
- VirusTotal
- MalwareBazaar
- MITRE ATT&CK

The environment simulated real-world Security Operations Center (SOC) workflows, malware analysis, SIEM monitoring, detection engineering, and enterprise incident response operations.

---

# 🎯 Project Objectives Achieved

---

## ✅ Enterprise SIEM Deployment

Successfully deployed Splunk Enterprise on RHEL 10.2 for centralized SIEM monitoring and threat hunting.

---

## ✅ Endpoint Telemetry Collection

Successfully configured Sysmon and Splunk Universal Forwarder for advanced endpoint telemetry collection.

---

## ✅ Malware Analysis Environment

Successfully built an isolated VMware Host-Only malware analysis environment for safe malware execution and investigation.

---

## ✅ Threat Hunting Operations

Successfully performed enterprise threat hunting using:

- Splunk queries
- Sysmon telemetry
- PowerShell analysis
- MITRE ATT&CK mapping
- YARA detection rules
- Threat intelligence correlation

---

## ✅ Detection Engineering

Successfully created detection rules and dashboards capable of identifying suspicious malware behavior.

---

## ✅ Incident Response Simulation

Successfully simulated enterprise incident response workflows and malware containment procedures.

---

# 🏗️ Key Technical Lessons Learned

---

# 🖥️ VMware Isolation Is Critical

---

## 📖 Lesson Learned

VMware Host-Only networking provided a safe and isolated environment for malware execution and analysis.

---

## ✅ Key Benefits

- Prevented external malware propagation
- Protected production systems
- Enabled controlled malware analysis
- Allowed safe forensic investigations

---

## 🖼️ Enterprise Threat Hunting Architecture

![Enterprise Threat Hunting Architecture](../screenshots/architecture/Threat%20Hunting%20Architecture.png)

**Figure 1:** Enterprise VMware Host-Only Threat Hunting Lab architecture showing isolated malware analysis, telemetry collection, and SOC investigation workflows.

---

# 📡 Sysmon Greatly Improves Visibility

---

## 📖 Lesson Learned

Sysmon significantly improved endpoint visibility by capturing detailed telemetry related to malware execution and persistence activity.

---

## ✅ Valuable Sysmon Events

| Event ID | Description |
|---|---|
| 1 | Process Creation |
| 3 | Network Connections |
| 11 | File Create |
| 13 | Registry Persistence |
| 22 | DNS Queries |

---

## ✅ Key Benefits

- Improved process visibility
- Better malware detection
- Enhanced forensic investigations
- Improved threat hunting accuracy

---

# 📊 Splunk Enterprise Improves Detection Visibility

---

## 📖 Lesson Learned

Splunk Enterprise successfully centralized logs, detections, dashboards, and threat hunting workflows.

---

## ✅ Key Benefits

- Centralized SIEM visibility
- Faster malware detection
- Improved dashboard visibility
- Better threat correlation
- Faster investigations

---

## 🖼️ Splunk Malware Detection Dashboard

![Splunk Malware Detection Dashboard](../screenshots/dynamic-analysis/trickbot-malware.png)

**Figure 2:** Splunk Enterprise dashboard displaying malware detections, suspicious executable paths, and Windows Defender telemetry generated during malware execution.

---

# 🧬 Threat Intelligence Improves Malware Identification

---

## 📖 Lesson Learned

Threat intelligence platforms improved malware validation and investigation workflows.

---

## ✅ Threat Intelligence Sources

- MalwareBazaar
- VirusTotal
- MITRE ATT&CK
- YARA
- LOLBAS

---

## 🖼️ MalwareBazaar Threat Intelligence

![MalwareBazaar Threat Intelligence](../screenshots/static-analysis/MalwareBazaar.png)

**Figure 3:** MalwareBazaar intelligence analysis showing TrickBot malware classification, malware hashes, and threat intelligence indicators.


---

## 🖼️ VirusTotal Threat Intelligence

![VirusTotal Threat Intelligence](../screenshots/static-analysis/virustotal-trickbot-analysis.png)

**Figure 4:** VirusTotal malware intelligence analysis showing antivirus detections, suspicious indicators, and malware reputation associated with the TrickBot malware sample.

---

# 🎯 MITRE ATT&CK Improves Threat Hunting

---

## 📖 Lesson Learned

MITRE ATT&CK mapping improved visibility into attacker techniques and detection engineering workflows.

---

## ✅ Example ATT&CK Techniques

| Technique ID | Technique |
|---|---|
| T1059.001 | PowerShell |
| T1547.001 | Registry Run Keys |
| T1105 | Ingress Tool Transfer |
| T1218 | Signed Binary Proxy Execution |
| T1055 | Process Injection |

---

## ✅ Key Benefits

- Better threat visibility
- Improved SOC investigations
- Better detection engineering
- Improved incident response workflows

---

# 🧪 Malware Analysis Requires Multiple Tools

---

## 📖 Lesson Learned

No single tool provides complete malware visibility.

Combining multiple security tools significantly improved malware investigations.

---

## ✅ Tools Used

| Tool | Purpose |
|---|---|
| PEStudio | Static analysis |
| Detect It Easy (DIE) | Packer detection |
| Sysmon | Endpoint telemetry |
| Splunk Enterprise | SIEM monitoring |
| YARA | Malware detection |
| VirusTotal | Threat intelligence |
| Wireshark | Network analysis |
| Suricata IDS | Intrusion detection |

---

# 🛡️ Detection Engineering Requires Continuous Improvement

---

## 📖 Lesson Learned

Detection engineering is an ongoing process requiring tuning, testing, and validation.

---

## ✅ Key Improvements

- Improved Splunk detection rules
- Expanded Sysmon visibility
- Added PowerShell monitoring
- Improved YARA detections
- Expanded dashboard monitoring

---

# 🚨 Incident Response Preparation Is Important

---

## 📖 Lesson Learned

Effective incident response depends on preparation, telemetry visibility, and centralized monitoring.

---

## ✅ Important Incident Response Capabilities

- Centralized logging
- Endpoint telemetry
- Threat intelligence
- Malware analysis
- Dashboard monitoring
- Threat hunting workflows

---

# 🔐 Security Best Practices Learned

---

## ✅ Recommended Practices

- Use isolated malware analysis environments
- Never execute malware on production systems
- Use VMware snapshots before malware execution
- Enable Sysmon endpoint telemetry
- Centralize logs into Splunk Enterprise
- Validate detections using threat intelligence
- Document all investigations
- Preserve forensic evidence
- Monitor PowerShell activity
- Implement detection engineering workflows

---

# 📊 Enterprise Skills Demonstrated

---

## ✅ Technical Skills

- SIEM Engineering
- Threat Hunting
- Malware Analysis
- Detection Engineering
- Splunk Administration
- Sysmon Configuration
- Incident Response
- Digital Forensics
- Windows Security Monitoring
- Linux Administration
- Network Security Monitoring
- Threat Intelligence Analysis

---

## ✅ Enterprise Security Concepts

- SOC Operations
- MITRE ATT&CK
- Malware Triage
- Detection Validation
- Threat Correlation
- Incident Management
- Endpoint Security
- Network Security
- SIEM Monitoring

---

# 🚀 Future Improvements

---

## ✅ Planned Enhancements

- Add SOAR automation
- Expand detection engineering
- Add Falco Kubernetes monitoring
- Add cloud threat hunting
- Add GuardDuty integration
- Expand YARA rule coverage
- Add Sigma detection rules
- Add automated alert triage
- Add AI-assisted threat hunting
- Expand Suricata IDS monitoring

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

## 🧾 YARA

https://yara.readthedocs.io/

---

## 📊 VirusTotal

https://docs.virustotal.com/

---

## ☁️ MalwareBazaar

https://bazaar.abuse.ch/

---

## 🛡️ Suricata

https://docs.suricata.io/

---

## 🌐 Wireshark

https://www.wireshark.org/docs/

---

# 👨‍💻 Author

James Banday

- LinkedIn: https://www.linkedin.com/in/james-allen-morta-banday-62a391128/
- GitHub: https://github.com/jbanday808/Enterprise-Threat-Hunting/tree/main

---

# 📄 License

This project is intended for educational, cybersecurity research, and threat hunting training purposes only.

---
