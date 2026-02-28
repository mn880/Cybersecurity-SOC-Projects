## SIEM Alert Triage – Initial Access (Brute-Force Detection)

### Objective
Validate a SIEM-generated brute-force authentication alert using Linux SSH log data and determine whether escalation is required.

---

### Alert Overview

A SIEM alert indicating potential brute-force login activity was triggered based on multiple failed SSH authentication attempts targeting a Linux host.

Log analysis revealed a high number of failed login attempts associated with user account `john.smith`, originating from an internal IP address within a short timeframe.

---

### Investigation Findings

- Over 500 failed SSH login attempts observed
- Repeated authentication attempts targeting user:
  - john.smith
- Login activity originating from:
  - 10.10.242.248
- Login attempts occurred within ~5 minutes
- Successful authentication event identified following repeated failures
- Post-authentication behavior indicates potential root-level access

These findings are consistent with automated brute-force login activity resulting in unauthorized access.

---

### Case Classification

**Verdict:** True Positive – Unauthorized Access Attempt

---

### Indicators Identified

- Source IP Address: 10.10.242.248  
- Targeted User Account: john.smith  
- Authentication Mechanism: SSH Login  

---

### Escalation Decision

Based on login attempt frequency, successful authentication, and potential privilege escalation, this alert represents a confirmed unauthorized access attempt and should be escalated for further investigation.

---

### Key Skills Demonstrated

- SIEM alert triage
- SSH authentication log analysis
- Brute-force detection
- Log correlation and validation
- Evidence-based escalation
