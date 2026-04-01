�️ Windows Security Monitoring Lab (Elastic SIEM)
� Overview

This project demonstrates a hands-on SIEM (Security Information and Event Management) lab using the Elastic Stack to monitor and analyze Windows security events.

The goal was to simulate how a Security Operations Center (SOC) detects and investigates suspicious authentication activity such as failed login attempts and potential brute force attacks.

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
<img width="1620" height="1232" alt="siem photo" src="https://github.com/user-attachments/assets/12c0b6ad-acae-4aaa-a5e1-e7a867547d3f" />

Monitoring authentication activity
Identifying suspicious login behavior
Building dashboards used in real-world SOC environments
