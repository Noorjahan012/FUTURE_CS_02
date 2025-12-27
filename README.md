# Security Alert Monitoring & Incident Response

**Intern Name:** Noorjahan  
**Internship:** Cyber Security Internship – Future Interns  

---

## Overview
This project simulates a SOC environment using Splunk Enterprise SIEM to monitor and analyze security logs. The goal was to identify suspicious activities, assess their severity, and propose mitigation actions.

---

## Objectives
- Monitor and analyze server and web logs.  
- Identify suspicious IPs and failed login attempts.  
- Detect abnormal HTTP requests and access to sensitive files.  
- Classify alerts and recommend response actions.  

---

## Tools Used
- **Splunk Enterprise** for log ingestion, searching, and pattern identification.  
- Logs analyzed: SSH login attempts and Apache access logs.  

---

## Key Steps
1. **Log Analysis**: Monitored SSH and web logs for failed logins, HTTP errors (`404`, `403`, `500`), and sensitive file access (`/wp-admin`, `.php`, `admin`).  
2. **Suspicious Activity**:  
   - **222.14.252.108** – SSH brute force attempts  
   - **193.185.55.253 & 130.237.218.8** – High web request volume  
3. **Evidence Collected**: Repeated failed logins, multiple HTTP errors, sensitive file access.  
4. **Severity**:  
   - High: SSH brute force (222.14.252.108)  
   - Medium: Web reconnaissance (193.185.55.253, 130.237.218.8)  
5. **Alerts**:

| Alert ID | Description                                     | Severity |
|----------|-----------------------------------------------|----------|
| A1       | Multiple failed SSH logins                     | High     |
| A2       | Repeated access to sensitive web files        | Medium   |
| A3       | Multiple HTTP errors (404/403/500)            | Medium   |
| A4       | Single failed login                            | Low      |

---

## Incident Response
- Block malicious IPs and monitor logs.  
- Reset admin/root passwords and enable MFA.  
- Apply account lockout policies.  

---

## Conclusion
Splunk SIEM helped identify high-risk SSH attacks and medium-risk web reconnaissance attempts. The project provided practical exposure to SOC operations, log analysis, and incident response.

---


