# Incident Report

## Honeyfile Detection Lab

**Date:** June 2026

**Author:** Batoul ITL

---

# Executive Summary

This report documents a simulated security incident in which a honeyfile was accessed on a Windows endpoint. The activity was monitored using Sysmon and analyzed in Splunk.

The objective of this investigation was to demonstrate how a Security Operations Center (SOC) analyst can identify suspicious file access and perform a basic incident investigation.

---

# Incident Details

| Item | Value |
|------|-------|
| Incident Type | Honeyfile Access |
| Severity | Medium |
| Status | Closed |
| Detection Method | Sysmon + Splunk |

---

# Investigation Timeline

| Time | Event |
|------|-------|
| 10:20 | User logged into Windows |
| 10:21 | Explorer.exe started |
| 10:22 | Passwords.xlsx accessed |
| 10:22 | Sysmon generated an event |
| 10:23 | Event indexed in Splunk |
| 10:24 | Investigation started |

---

# Evidence

The following evidence was collected during the investigation:

- Windows Event Logs
- Sysmon Events
- Splunk Search Results
- Honeyfile Activity

---

# Findings

The investigation confirmed that the honeyfile was accessed.

No malware execution or data exfiltration was observed during this simulation.

The activity successfully generated the expected Sysmon events and demonstrated the effectiveness of centralized log monitoring using Splunk.

---

# MITRE ATT&CK

| Technique | Description |
|-----------|-------------|
| T1083 | File and Directory Discovery |
| T1005 | Data from Local System |

---

# Lessons Learned

- Honeyfiles provide an effective early detection mechanism.
- Sysmon offers detailed endpoint visibility.
- Splunk simplifies log analysis and investigation.
- Proper monitoring can reduce incident response time.

---

# Conclusion

This lab successfully demonstrated the deployment of a honeyfile detection strategy using Sysmon and Splunk.

The project provides a practical introduction to SOC monitoring, log analysis, and basic incident investigation in a controlled environment.
