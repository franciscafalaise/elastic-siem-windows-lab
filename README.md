# Windows SIEM Dashboard – Failed Login Detection

## � Overview
This project demonstrates a hands-on Security Information and Event Management (SIEM) lab using the Elastic Stack to monitor and analyze Windows security events.

The objective was to simulate real-world SOC (Security Operations Center) workflows by detecting and investigating suspicious authentication activity.

---

## � Use Case: Detecting Brute Force Attacks
This lab focuses on identifying brute force login attempts using Windows Security Event Logs.

Windows Event ID **4625 (failed login)** was monitored to detect abnormal authentication patterns and potential unauthorized access attempts.

---

## � Technologies Used
- Elasticsearch  
- Kibana  
- Winlogbeat  
- Windows 10 Virtual Machine  
- VirtualBox  

---

## ⚙️ Architecture
- Windows VM generates security logs  
- Winlogbeat collects event logs  
- Logs are sent to Elasticsearch  
- Kibana visualizes and analyzes the data  

---

## � Detection Logic
- Event ID: **4625 (Failed Login)**
- Query: `event.code: 4625`
- Indicators of compromise:
  - High frequency of failed login attempts  
  - Repeated attempts against specific user accounts  
  - Sudden spikes in authentication failures  

---

## � Dashboard & Analysis

### � Failed Login Monitoring
- Visualized failed login attempts over time  
- Identified spikes indicating possible brute force behavior  

### � Targeted User Analysis
- Highlighted frequently targeted accounts (e.g., Administrator)  
- Identified patterns in attacker behavior  

### �️ Source System Tracking
- Analyzed host systems generating login attempts  
- Confirmed activity origin within lab environment  

### � Authentication Outcomes
- Compared successful vs failed login attempts  
- Provided visibility into authentication trends  

---

## � Findings
- Multiple failed login attempts detected within short time intervals  
- Repeated targeting of privileged accounts (Administrator)  
- All activity originated from the same host (lab simulation)  
- Patterns consistent with brute force attack behavior  

---

## � Screenshots

![Dashboard](.[siem dashboard.pdf](https://github.com/user-attachments/files/26423029/siem.dashboard.pdf)
![Failed Logins](.[Failed login.pdf](https://github.com/user-attachments/files/26423128/Failed.login.pdf)
![Authentication Outcomes](.[Authentication Outcomes.pdf](https://github.com/user-attachments/files/26423236/Authentication.Outcomes.pdf)


---

## � Security Insight
A high volume of Event ID 4625 logs can indicate:
- Brute force attacks  
- Credential stuffing  
- Unauthorized access attempts  

Monitoring these patterns is critical for early threat detection in a SOC environment.

---

## � Future Improvements
- Implement alerting for failed login thresholds  
- Correlate failed logins with successful logins (Event ID 4624)  
- Track source IP addresses for attribution  
- Integrate additional telemetry (Sysmon, network logs)  

---

## � Outcome
This lab provided hands-on experience with:
- SIEM deployment and configuration  
- Log ingestion and analysis  
- Threat detection and investigation  
- Security data visualization  

This project simulates real SOC analyst responsibilities in monitoring and responding to authentication-based threats.
