# Project 12 – SOC Incident Response Case

## Objective

- Conduct a full end-to-end SOC incident investigation based on an alert of a compromised user account.
- Analyze evidence from multiple log sources, including Windows Security Logs, VPN logs, PowerShell logs, DNS logs, and Antivirus logs.
- Build a timeline of events and produce a formal incident report with findings and recommendations.

## Environment

- Splunk Enterprise (version 10.4.1)
- Windows 11 Host Machine
- SOC Lab Index (soc_lab)
- Sample Security Logs (Windows, VPN, PowerShell, DNS, Antivirus)

## Skills Practiced

- Multi-source log correlation
- Timeline construction
- Proactive incident detection
- Alert handling and analysis
- Dashboard and SIEM investigation techniques
- Writing formal incident reports

## Steps Performed

1. Received a security alert indicating multiple failed login attempts on a user account (FrancisHP).
2. Investigated Windows security logs for failed and successful login attempts, noting timestamps and user context.
3. Analyzed VPN logs to identify unusual geographic login attempts (Orlando, Atlanta, Russia).
4. Reviewed PowerShell logs for suspicious commands, particularly web requests to known malicious domains.
5. Examined DNS logs for any outbound requests to suspicious domains.
6. Checked antivirus logs to see if malware was detected and quarantined.
7. Correlated all evidence by timestamp, grouping events to build a timeline of suspicious activities.
8. Documented findings in a structured incident report, detailing the evidence, timeline, impact, and recommended next steps.

## Screenshots

### 01 Incident Alert Search

![01 Incident Alert Search](screenshots/Project12/01%20Incident%20Alert%20Search.png)

---

### 02 Windows Authentication Investigation

![02 Windows Authentication Investigation](screenshots/Project12/02%20Windows%20Authentication%20Investigation.png)

---

### 03 VPN Investigation

![03 VPN Investigation](screenshots/Project12/03%20VPN%20Investigation.png)

---

### 04 PowerShell Investigation

![04 PowerShell Investigation](screenshots/Project12/04%20PowerShell%20Investigation.png)

---

### 05 DNS Investigation

![05 DNS Investigation](screenshots/Project12/05%20DNS%20Investigation.png)

---

### 06 Antivirus Investigation

![06 Antivirus Investigation](screenshots/Project12/06%20Antivirus%20Investigation.png)

---

### 07 Incident Timeline

![07 Incident Timeline](screenshots/Project12/07%20Incident%20Timeline.png)

---

### 08 Incident Findings

![08 Incident Findings](screenshots/Project12/08%20Incident%20Findings.png)

## Lessons Learned

- I learned how to correlate evidence from multiple log sources to understand the full scope of an incident.
- I practiced constructing a timeline to visualize the sequence of events clearly.
- I developed skills in identifying suspicious activity across different security logs and using them together to uncover threats.
- I realized how critical it is to have a structured approach—starting from an alert, gathering evidence, and ending with a formal report.

## SOC Analyst Takeaways

- A successful SOC investigation requires pulling evidence from multiple sources and verifying each piece against others to build a complete picture.
- Timelines help show the sequence of events, which is crucial for understanding how a compromise unfolded.
- Formal incident reports must connect the data points, explain the impact, and offer clear next steps for remediation and prevention.
- By practicing end-to-end investigations, I improve both my analytical skills and my ability to communicate findings clearly to leadership.
