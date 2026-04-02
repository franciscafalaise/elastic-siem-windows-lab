# �️ Elastic SIEM Windows Lab

## � Project Overview
This project demonstrates a hands-on Security Information and Event Management (SIEM) lab using the Elastic Stack (Elasticsearch, Kibana, Winlogbeat).

The goal of this lab was to:
- Ingest Windows event logs
- Monitor authentication activity
- Detect failed login attempts (potential brute force attacks)
- Build visual dashboards for security analysis

---

## � Technologies Used
- Elastic Stack (Elasticsearch + Kibana)
- Winlogbeat (log ingestion)
- Windows 10 VM (target machine)
- Oracle VirtualBox

---

## � Key Detection Use Case

### � Failed Login Detection
- Event ID **4625** → Failed logins  
- Event ID **4624** → Successful logins  

This lab focuses on identifying:
- Brute force login attempts
- Suspicious authentication patterns
- Targeted user accounts

---

## � Dashboard Visualizations

### � Failed Login Attempts Over Time
Shows spikes in failed login activity (Event ID 4625), useful for detecting brute force attacks.
<img width="1496" height="1180" alt="Failed login" src="https://github.com/user-attachments/assets/729c1a9d-2fe3-4e3f-a305-a9a40351fe43" />




---

### � Authentication Outcomes (Success vs Failure)
Compares successful vs failed login attempts.
<img width="756" height="420" alt="Authentication outcomes" src="https://github.com/user-attachments/assets/a4802b05-961b-403a-8c42-405e55889473" />


---

### � Top Targeted User Accounts
Identifies which user accounts are being targeted most frequently.
<img width="673" height="423" alt="top target user accounts" src="https://github.com/user-attachments/assets/9b97fcb8-3219-44bd-a13d-9ee68ef233ab" />


---

### �️ Dashboard Overview
Full SIEM dashboard showing authentication activity across the system.
<img width="1540" height="1194" alt="siem dashboard" src="https://github.com/user-attachments/assets/71fb1674-2cf4-407e-ab49-768f0db32c0c" />




---

## � Skills Demonstrated
- Log ingestion & parsing
- SIEM dashboard creation
- Security event analysis
- Threat detection using event IDs
- Data visualization in Kibana

---

## � What I Learned
- How to collect and analyze Windows logs using Elastic
- How to detect authentication attacks using event IDs
- How to build dashboards for SOC monitoring

---

## � Future Improvements
- Add alerting rules for brute force detection
- Integrate Sysmon for deeper visibility
- Simulate attacks (Hydra / RDP brute force)

---

## � Author
Francisca Falaise  
Aspiring SOC Analyst | Cybersecurity Student
