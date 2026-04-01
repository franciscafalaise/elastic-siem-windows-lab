�️ Windows Security Monitoring Lab (Elastic SIEM)
� Overview

This project demonstrates a hands-on SIEM (Security Information and Event Management) lab using the Elastic Stack to monitor and analyze Windows security events.

The goal was to simulate how a Security Operations Center (SOC) detects and investigates suspicious authentication activity such as failed login attempts and potential brute force attacks.
� Threat Detection: Brute Force Login Attack

This lab simulates and detects brute force login attempts on a Windows system using Elastic SIEM.

� Detection Logic
Event ID: 4625 (Failed Login)
Monitored over time for spikes in authentication failures
High volume indicates potential brute force activity
� Key Findings
Multiple failed login attempts observed in short time intervals
Certain user accounts (e.g., Administrator) targeted frequently
All events originated from the same host, indicating attack simulation
� Security Insight

A spike in Event ID 4625 events can indicate:

Brute force attacks
Credential stuffing
Unauthorized access attempts

Monitoring these patterns is critical in a SOC environment.

� Technologies Used
Elasticsearch
Kibana
Winlogbeat
Windows 10 (Virtual Machine)
Oracle VirtualBox
⚙️ Lab Architecture
Windows VM generates security logs
Winlogbeat collects event logs
Data is sent to Elasticsearch
Kibana is used to visualize and analyze events
� Key Features & Detections
� Failed Login Monitoring
Filtered Event ID 4625 (failed logins)
Visualized login attempts over time
Identified spikes in authentication failures
� Targeted User Analysis
Displayed most targeted accounts (e.g., Administrator, labuser)
Helped identify potential attack targets
�️ Source System Tracking
Analyzed originating host (host.name)
Identified systems generating failed login attempts
� Authentication Outcomes
Compared successful vs failed logins
Provided visibility into authentication trends
� Simulation

To test detection capabilities:

Generated multiple failed login attempts manually
Observed real-time ingestion and visualization in Kibana
� Screenshots

Add your screenshots here:

Dashboard overview
Failed login spikes
Authentication breakdown

(Upload images to your repo and drag them here)

� Skills Demonstrated
SIEM setup and configuration
Log ingestion and parsing
Security event analysis
Threat detection (brute force behavior)
Dashboard creation and data visualization
� Future Improvements
Implement alerting for failed login thresholds
Add detection rules for brute force attacks
Integrate additional log sources (Sysmon, network logs)
Automate response workflows
� Outcome

This lab provided practical experience in:
[Screenshot 2026-04-01 181815 copy.png.pdf](https://github.com/user-attachments/files/26422662/Screenshot.2026-04-01.181815.copy.png.pdf)
## � Dashboard

![Failed Logins](./screenshots/failed-logins.png)
![Authentication Breakdown](./screenshots/auth.png)
![Top Users](./screenshots/users.png)
<img width="1620" height="1232" alt="siem photo" src="https://github.com/user-attachments/assets/12c0b6ad-acae-4aaa-a5e1-e7a867547d3f" />

## � Detection Improvement

Future enhancements:
- Alert when failed logins > 10 within 5 minutes
- Correlate with successful logins (Event ID 4624)
- Track source IPs for attack attribution

Monitoring authentication activity
Identifying suspicious login behavior
Building dashboards used in real-world SOC environments
