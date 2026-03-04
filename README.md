# Cybersecurity-labs
# Wazuh SIEM Lab (Blue Team)

## Overview
This project documents a personal lab where I implemented a Wazuh SIEM to monitor endpoints, collect security logs, and generate alerts for suspicious activity.

## Objectives
- Deploy a Wazuh server in a test environment
- Connect a Windows endpoint using the Wazuh agent
- Validate log collection and alert generation
- Practice basic incident triage and analysis

## Lab Architecture
- Wazuh Manager: (VM / Linux)  
- Endpoint: Windows 10/11 with Wazuh Agent  
- Network: Internal lab network (no public exposure)

> Diagram: see `architecture/diagram.png`

## Tools Used
- Wazuh (Manager + Dashboard)
- Windows Event Logs
- Sysmon (optional, if used)
- Basic Linux administration

## What I Implemented
- Installed and configured Wazuh Manager and Dashboard
- Enrolled a Windows endpoint and validated connectivity
- Generated test security events (failed logins / brute force simulation)
- Reviewed alerts in the Wazuh dashboard and performed initial triage

## Evidence (Screenshots)
- Agent connected: `evidence/agent-connected.png`
- Security alert example: `evidence/alert-example.png`
- Dashboard view: `evidence/dashboard.png`

## Detection & Triage Notes
When an alert is triggered, I validate:
1. Source host and user context
2. Frequency and time window of events
3. Related Windows events (e.g., authentication failures)
4. Whether the behavior matches a known technique (MITRE ATT&CK)

## Lessons Learned
- Key configuration steps for stable agent enrollment
- Common pitfalls (time sync, firewall rules, agent keys)
- How to structure a basic SOC triage workflow

## Security Notice
All sensitive information (IPs, hostnames, usernames, tokens) was removed or anonymized before publishing.
