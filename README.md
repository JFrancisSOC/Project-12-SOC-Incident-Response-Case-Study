# Project 12 – SOC Incident Response Case Study

## Overview

In this project, I performed a complete Security Operations Center (SOC) incident investigation using Splunk Enterprise. Beginning with an incident alert, I investigated multiple security log sources, correlated evidence across the environment, reconstructed an attack timeline, and documented the findings in a formal incident report.

The investigation combined Windows Security, VPN, PowerShell, DNS, and Antivirus logs to determine whether the endpoint had been compromised and to recommend appropriate response actions.

---

## Objective

- Investigate a suspected endpoint compromise.
- Correlate multiple security log sources.
- Build an incident timeline.
- Determine indicators of compromise (IOCs).
- Produce a formal SOC incident report.
- Recommend containment and remediation actions.

---

## Lab Environment

- Windows 11
- Splunk Enterprise 10.4.1
- Splunk Search & Reporting
- SOC Lab Index (soc_lab)
- Sample Security Logs

---

## Skills Practiced

- Incident Response
- Threat Hunting
- Event Correlation
- Timeline Reconstruction
- Windows Security Analysis
- VPN Analysis
- DNS Investigation
- PowerShell Investigation
- Malware Investigation
- Incident Documentation

---

## Tools Used

- Splunk Enterprise
- Windows 11
- GitHub

---

## Investigation Process

### Step 1

Received a high-priority incident alert involving suspicious account activity.

---

### Step 2

Investigated Windows authentication logs.

Observed:

- Three failed logon attempts
- One successful authentication

---

### Step 3

Investigated VPN activity.

Observed VPN logins from:

- Orlando
- Atlanta
- Russia
- Unknown Location (Failed)

---

### Step 4

Investigated PowerShell activity.

Observed:

- Invoke-WebRequest
- Connection attempt to malware-download.net/payload

---

### Step 5

Investigated DNS activity.

Observed requests to:

- malware-download.net
- evilexample

---

### Step 6

Investigated Antivirus logs.

Observed:

- Trojan.Win32.Agent detected
- Threat quarantined successfully

---

### Step 7

Correlated all evidence and constructed an incident timeline.

---

### Step 8

Completed the incident report with findings and recommendations.

---

## Incident Timeline

| Time | Event |
|------|-------|
| 11:14 PM | Trojan.Win32.Agent detected and quarantined |
| 11:17 PM | PowerShell executed Invoke-WebRequest |
| 11:18 PM | DNS requests to malware-download.net and evilexample |
| 11:18 PM | VPN logins observed from Orlando, Atlanta, Russia, and one failed unknown location |
| 11:19 PM | Three failed Windows logons followed by one successful logon |

---

## Investigation Findings

### Windows Authentication

- Three failed logons
- One successful logon

Possible credential compromise.

---

### VPN Investigation

Multiple VPN logins occurred from different geographic locations within a short period.

Locations included:

- Orlando
- Atlanta
- Russia

This behavior is considered suspicious.

---

### PowerShell Investigation

PowerShell executed:

- Invoke-WebRequest

Attempted connection:

- malware-download.net/payload

This activity indicates an attempted malware download.

---

### DNS Investigation

DNS requests observed:

- malware-download.net
- evilexample

These domains were treated as suspicious indicators.

---

### Antivirus Investigation

Antivirus detected:

- Trojan.Win32.Agent

The threat was successfully quarantined.

---

## Analyst Conclusion

The evidence collected from Windows Security, VPN, PowerShell, DNS, and Antivirus logs indicates that the FrancisHP endpoint experienced multiple indicators of compromise.

Although the antivirus successfully quarantined the detected Trojan, the presence of suspicious authentication activity, malicious PowerShell execution, DNS requests, and abnormal VPN activity warranted escalation for further investigation.

---

## Recommended Actions

- Isolate the affected endpoint.
- Reset the compromised account password.
- Review VPN sessions.
- Block malicious domains.
- Perform a complete antivirus scan.
- Review PowerShell history.
- Continue monitoring for additional suspicious activity.

---

# Screenshots

### 01 Incident Alert Search
![01 Incident Alert Search](01%20Incident%20Alert%20Search%20.png)

---

### 02 Windows Authentication Investigation

![02 Windows Authentication Investigation](02%20Windows%20Authentication%20Investigation.png)

---

### 03 VPN Investigation

![03 VPN Investigation](03%20VPN%20Investigation.png)

---

### 04 PowerShell Investigation

![04 PowerShell Investigation](04%20PowerShell%20Investigation.png)

---

### 05 DNS Investigation

![05 DNS Investigation](05%20DNS%20Investigation.png)

---

### 06 Antivirus Investigation

![06 Antivirus Investigation](06%20Antivirus%20Investigation.png)

---

### 07 Incident Timeline

![07 Incident Timeline](07%20Incident%20Timeline.png)

---

### 08 Incident Findings

![08 Incident Findings](08%20Incident%20Findings.png)

---

## Lessons Learned

- Learned how to investigate a security incident using multiple log sources.
- Correlated authentication, VPN, DNS, PowerShell, and antivirus events.
- Built an evidence-based incident timeline.
- Practiced documenting findings using a professional SOC incident report.
- Improved analytical thinking by correlating events across different systems.

---

## SOC Analyst Takeaways

Modern SOC investigations require analysts to gather evidence from multiple log sources rather than relying on a single event. Correlating authentication logs, VPN activity, DNS requests, PowerShell execution, and antivirus detections provides a complete understanding of the incident.

This project simulated the workflow used by SOC analysts during real incident response engagements, from receiving an alert to producing an evidence-based incident report with remediation recommendations.
