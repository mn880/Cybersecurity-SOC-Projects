## Phishing Email Investigation – Two Independent Cases

### Objective
Investigate and classify user-reported phishing emails using SOC Level 1 analysis techniques, focusing on evidence-based decision-making and correct incident scoping.

---

### Case Overview

Two independent phishing emails were analyzed and classified as true positives.  
No technical correlation was identified between the cases.

---

### Case 1: Credential Harvesting via Malicious URL
- Brand impersonation using a legitimate service theme
- Embedded URL redirecting to non-legitimate domains
- URL reputation analysis confirmed phishing infrastructure
- Classified as **True Positive – Phishing (Credential Harvesting)**

---

### Case 2: Malicious PDF Attachment
- Email delivered a PDF attachment using social engineering
- Attachment detonated in a sandbox environment
- Observed suspicious execution behavior and network activity
- Classified as **True Positive – Phishing (Malicious Attachment)**

---

### Indicators Identified
- Malicious domains used for redirection
- File hash associated with malicious attachment
- External IP addresses observed during sandbox execution

---

### Key Skills Demonstrated
- Phishing email triage
- Header and sender analysis
- URL and attachment investigation
- Sandbox behavior analysis
- Evidence-based alert classification
- Clear separation of independent incidents

---

### Notes
This project documents phishing investigations performed from a SOC analyst perspective.  
Detailed analysis and screenshots are maintained in a separate offline report.
