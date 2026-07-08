# Inhibit System Recovery Investigation (T1490)

## Overview

In this short project, I investigated MITRE ATT&CK T1490 (Inhibit System Recovery) using Splunk Enterprise and Windows attack datasets provided by Atomic Red Team.

T1490 is an impact technique where attackers remove or disable recovery options on a system. This technique is commonly used during ransomware attacks to prevent organizations from restoring files and recovering affected systems.

## What is T1490?

T1490 is a technique where attackers attempt to stop system recovery by deleting backups or disabling recovery features.

Common attacker actions include:

- Deleting Windows Volume Shadow Copies
- Removing backup files
- Deleting Windows Backup Catalogs
- Disabling Windows Recovery options

For example, before encrypting files, ransomware operators may delete Volume Shadow Copies. This prevents victims from using previous backups to restore their data.

## Project Goal

The goal of this project was to learn how to detect and investigate T1490 activity using Splunk.

I analyzed Windows Security Logs and Sysmon Logs to understand how attackers attempt to remove recovery options and how security analysts can detect this behavior.

During the investigation, I focused on:

- Process creation events
- Suspicious commands used to delete backups
- PowerShell activity related to recovery removal
- Indicators of compromise (IOCs) associated with T1490 activity

## Investigations

I broke this project into multiple investigations. Each folder below shows the investigation process, including what I searched for, what I observed, and how each step helped identify attacker activity.

01-Windows_Sysmon-Logs-Investigation (Process and command analysis)

02-Windows_Security-Logs-Investigation (Event ID 4688 investigation)

Each investigation contains:

- Splunk queries
- Investigation steps
- Observations
- Findings
- Indicators of Compromise (IOCs)
- Conclusion

