# 🛡️ SIEM Threat Detection Lab Using Splunk & Atomic Red Team

This project simulates a small-scale Security Operations Center (SOC) using **Splunk**, **Sysmon**, **Splunk Universal Forwarder**, and **Atomic Red Team**. The lab demonstrates real-world threat detection, alerting, and correlation of attacker behavior mapped to the **MITRE ATT&CK framework**.

---

## 📌 Project Summary

In this lab, a Windows 10 virtual machine was configured to simulate attacker behavior, while an Ubuntu Server VM hosted Splunk Enterprise to ingest logs for detection. Logs were forwarded using Splunk Universal Forwarder, and deep telemetry was collected via Sysmon. Atomic Red Team was used to safely simulate adversary techniques such as:

- Brute force login attempts
- Suspicious PowerShell execution
- Registry-based persistence

Multiple Splunk dashboards, alerts, and correlation rules were implemented to detect these behaviors in real time.

---

## 🧰 Tools & Technologies Used

- **Splunk Enterprise**
- **Splunk Universal Forwarder**
- **Sysmon (SwiftOnSecurity config)**
- **Atomic Red Team (Invoke-AtomicRedTeam)**
- **Windows 10 VM (SOC Simulation)**
- **Ubuntu Server 22.04 VM (SIEM Server)**
- **VirtualBox**

---

## 🧠 Key MITRE ATT&CK Techniques Detected

| Use Case                                     | Technique ID          | Technique Name                                      |
|----------------------------------------------|-----------------------|-----------------------------------------------------|
| Suspicious PowerShell Execution              | T1059.001             | Command & Scripting Interpreter: PowerShell         |
| Brute Force Login Attempts                   | T1110.001             | Brute Force: Password Guessing                      |
| Registry Key Persistence                     | T1547.001    	       | Boot/Logon Autostart Execution: Registry Keys       |
| Brute Force Followed by Successful Login     | T1110 + T1078	       | Valid Accounts Used After Brute Force               |
| PowerShell Followed by Registry Persistence  | T1059.001 + T1547.001 | Multi-Stage Persistence with Scripting              |

---

## 📊 Splunk Features Implemented

- ✅ Real-time dashboards with visual panels
- ✅ Alerts triggered by detection logic
- ✅ Correlation rules for multi-stage attack detection
- ✅ Reports saved for correlation use cases

---

## 🚀 How to Run the Project

1. **Set up VMs** with VirtualBox: Windows 10 (SOC) and Ubuntu Server (Splunk)
2. **Install Splunk Enterprise** on Ubuntu Server
3. **Install Splunk Universal Forwarder + Sysmon** on Windows 10 VM
4. **Ingest logs into Splunk**, verify via search
5. **Simulate attacks** using Atomic Red Team on Windows
6. **Visualize detections** in dashboards
7. **Set alerts** for real-time detection
8. **Run correlation SPL queries** and save as reports

---

## 📝 Key Learnings

- Configured log forwarding & Sysmon for visibility
- Simulated MITRE-mapped attacks using ART
- Developed dashboards, alerts, and multi-event correlation SPL
- Strengthened SIEM analysis and detection engineering skills

---

## 📸 Sample Screenshots

You can find screenshots of the dashboard panels, alerts, reports, and test results in the `/screenshots/` folder.

---

## 🔗 Resources

- [Atomic Red Team](https://github.com/redcanaryco/atomic-red-team)
- [SwiftOnSecurity Sysmon Config](https://github.com/SwiftOnSecurity/sysmon-config)
- [MITRE ATT&CK Framework](https://attack.mitre.org/)
- [Splunk Enterprise](https://www.splunk.com/)
