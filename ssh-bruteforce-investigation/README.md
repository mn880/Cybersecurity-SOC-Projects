## SSH Brute-Force Investigation – Linux Authentication Logs

### Objective
Investigate repeated SSH authentication failures to identify potential brute-force login attempts using Linux authentication logs.

---

### Case Overview

Suspicious SSH login activity was observed on a Linux host, involving repeated authentication failures targeting multiple user accounts.

Log analysis revealed multiple login attempts originating from external IP addresses within a short timeframe, significantly exceeding expected legitimate login behavior.

---

### Investigation Findings

- Repeated `Failed password` authentication attempts detected
- Multiple user accounts targeted including:
  - root
  - sol
  - roy
  - user
- Login attempts originated from multiple external IP addresses
- Rapid succession of login failures observed across accounts

This behavior is consistent with automated credential-guessing or distributed brute-force login attempts.

---

### Case Classification

**Verdict:** True Positive – SSH Brute-Force Attempt

---

### Indicators Identified

- Multiple external IP addresses attempting authentication
- Targeted privileged and standard user accounts

---

### Key Skills Demonstrated

- Linux authentication log analysis
- Detection of automated login abuse
- Pattern-based threat identification
- Evidence-based alert classification
- Differentiation between user error and brute-force activity

---

### Notes
This project documents SSH authentication abuse investigation from a SOC analyst perspective.  
Detailed analysis is maintained in a separate offline report.
