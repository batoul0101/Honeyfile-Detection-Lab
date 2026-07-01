# Splunk Queries

This document contains the basic Splunk searches used in this project.

---

# 1. View All Sysmon Events

This query displays all events collected from Sysmon.

```spl
index=sysmon
```

---

# 2. Process Creation (Event ID 1)

This query shows every process executed on the endpoint.

```spl
index=sysmon EventCode=1
```

Why is it useful?

- Detect PowerShell
- Detect CMD
- Identify suspicious processes

---

# 3. Network Connections (Event ID 3)

Shows processes that created network connections.

```spl
index=sysmon EventCode=3
```

Why is it useful?

- Detect outbound connections
- Investigate malware communication

---

# 4. File Creation (Event ID 11)

Displays newly created files.

```spl
index=sysmon EventCode=11
```

Why is it useful?

- Detect suspicious files
- Detect dropped payloads

---

# 5. Search for a Honeyfile

Search for activity related to the honeyfile.

```spl
index=sysmon Passwords.xlsx
```

Why is it useful?

- Detect interaction with the honeyfile
- Start an investigation
