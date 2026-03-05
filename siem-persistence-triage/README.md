## SIEM Alert Triage – Persistence (Suspicious Scheduled Task)

### Objective
Investigate a SIEM-generated alert indicating suspicious scheduled task creation and determine whether it represents malicious persistence.

---

### Alert Overview

A SIEM alert identified the creation of a scheduled task on a Windows workstation.

Scheduled tasks are frequently abused by attackers to maintain persistence on compromised systems, enabling automated execution of malicious commands.

Log analysis revealed the creation of the task **AssessmentTaskOne** on host **WIN-H015** under user **oliver.thompson**.

---

### Investigation Findings

Analysis of the scheduled task configuration revealed that the task executes **PowerShell**, which uses **certutil.exe** to download an external file.

The downloaded payload:
rv.exe


was saved as:


DataCollector.exe


and executed using a **Start-Process** command.

Process activity indicates the task was created through:


cmd.exe


Further log review identified that the associated session originated from workstation:


DEV-QA-SERVER


These behaviors strongly suggest malicious persistence activity.

---

### Case Classification

**Verdict:** True Positive – Malicious Persistence Mechanism

---

### Indicators Identified

Host: WIN-H015  
User: oliver.thompson  
Task Name: AssessmentTaskOne  
Parent Process: cmd.exe  
Payload: DataCollector.exe  
Source Workstation: DEV-QA-SERVER  

---

### Skills Demonstrated

- SIEM alert triage
- Windows event log analysis
- Persistence detection
- Scheduled task investigation
- Evidence-based escalation
