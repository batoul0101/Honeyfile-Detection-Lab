# Detection Logic

## Objective

The goal of this project is to detect unauthorized access to honeyfiles using Sysmon and Splunk.

---

## Detection Flow

Attacker

↓

Opens Honeyfile

↓

Sysmon Records the Event

↓

Windows Event Log

↓

Splunk

↓

SOC Analyst Investigates

---

## Event IDs Used

### Event ID 1

Process Creation

Used to identify which process accessed the system.

---

### Event ID 3

Network Connection

Used to monitor network communication.

---

### Event ID 11

File Creation

Used to monitor newly created files.

---

## Why Honeyfiles?

Honeyfiles are fake sensitive files placed on a system.

Normal users should never open them.

If someone accesses them, it may indicate suspicious activity.

---

## Conclusion

By monitoring a few important Sysmon Event IDs, a SOC analyst can quickly detect suspicious behavior and begin an investigation.
