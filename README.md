# RDP-Brute-Force-Alert-Investigation

This project documents the investigation of a successful Remote Desktop Protocol (RDP) Brute Force attack identified through SIEM alerting and endpoint analysis. The investigation includes authentication analysis, endpoint inspection, command-line review, network activity analysis, MITRE ATT&CK mapping, and threat intelligence enrichment.
The objective of this investigation was to validate the alert, assess attacker activity, determine compromise scope, and support escalation to the Incident Response (IR) team.

**Scenario Overview**
A SIEM alert was triggered after multiple failed RDP authentication attempts were detected from a single external IP address targeting a Windows 10 client endpoint.

Initial analysis revealed:
* Repeated login attempts against multiple accounts,
* dictionary-style username guessing,
* and a successful authentication event following several failed attempts.

Further investigation confirmed post-compromise activity involving:
* suspicious process interaction,
* command-line reconnaissance,
* and outbound network connections initiated after successful access.

**Investigation Objectives**
* Validate whether the alert represented malicious activity
* Analyze failed and successful authentication events
* Identify attacker behavior following successful access
* Investigate post-compromise endpoint activity
* Perform threat intelligence enrichment on identified indicators
* Assess compromise severity and escalation requirements
* Document findings for Incident Response escalation

**Tools Used**
* SIEM Platform
* Windows Event Viewer
* Endpoint Logs and Process Analysis
* Threat Intelligence Platforms
* MITRE ATT&CK Framework

**Key Findings**
* 14 failed RDP login attempts identified
* 1 Successful RDP authentication confirmed
* Multiple dictionary-based username attempts observed
* Post-compromise reconnaissance activity detected
* Suspicious interaction with Windows authentication-related processes identified
* Outbound network communication observed after compromise

The Incident was triaged as a True Positive alert and escalated to Incident Response for deeper forensic analysis and environment-wide hunting.

