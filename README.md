# Wazuh SOC Home Lab

A hands-on Wazuh security monitoring lab built for learning and experimentation. The lab uses an Ubuntu virtual machine as the Wazuh Manager and a Windows endpoint as the Wazuh Agent. It demonstrates endpoint onboarding, dashboard visibility, File Integrity Monitoring (FIM), and controlled validation of file-change detection.

> **Project status:** Completed learning lab / portfolio project

## Objectives

- Deploy a Wazuh Manager in an Ubuntu virtual machine.
- Connect a Windows endpoint as a Wazuh Agent.
- Verify endpoint visibility in the Wazuh Dashboard.
- Configure and validate File Integrity Monitoring.
- Perform controlled file operations and observe the resulting security events.
- Document the setup, evidence, observations, and lessons learned.

## Lab Architecture

![Wazuh lab architecture](architecture/wazuh-lab-architecture.png)

| Component | Environment | Role |
|---|---|---|
| Wazuh Manager | Ubuntu VM / VirtualBox | Collects, analyzes, and stores agent data |
| Wazuh Agent | Windows host | Sends endpoint logs and system events |
| Dashboard | Wazuh web interface | Visualizes agents, alerts, and FIM events |

## Key Work Completed

### 1. Wazuh Manager
Ubuntu was used as the Wazuh Manager environment inside VirtualBox. The manager and dashboard were deployed and accessed from the lab network.

See [`setup/wazuh-manager.md`](setup/wazuh-manager.md).

### 2. Windows Agent
A Windows endpoint was installed and registered with the Wazuh Manager. The agent was verified in the dashboard.

See [`setup/wazuh-agent.md`](setup/wazuh-agent.md).

### 3. File Integrity Monitoring
A Windows test directory was monitored for file activity. Files were created, modified, and deleted as controlled test actions, and the resulting events were reviewed in the Wazuh Dashboard.

See [`detections/file-integrity-monitoring.md`](detections/file-integrity-monitoring.md).

### 4. Investigation / Validation
The FIM activity was documented as a controlled security-monitoring investigation rather than a real-world intrusion.

See [`investigations/incident-001-file-integrity.md`](investigations/incident-001-file-integrity.md).

## Evidence

- [Active Wazuh agent](screenshots/active-agent.png)
- [Monitored Windows folder](screenshots/monitored-folder.png)
- [FIM events](screenshots/fim-events.png)
- [FIM event details](screenshots/fim-event-details.png)
- [Video evidence notes](evidence/video-timestamps.md)

## Technologies

- Wazuh
- Ubuntu Linux
- Windows
- VirtualBox
- Wazuh Dashboard
- File Integrity Monitoring (Syscheck)

## What I Learned

- How a SIEM/security monitoring platform is structured around a manager and endpoint agents.
- How to onboard a Windows endpoint into Wazuh.
- How endpoint file changes can be monitored through FIM.
- How to validate detections using controlled activity.
- How to interpret security events in a monitoring dashboard.
- How to document technical evidence for a security lab.

## Limitations and Next Steps

This is a small educational home lab and should not be presented as a production SOC. Future extensions can include additional endpoints, Sysmon telemetry, custom Wazuh rules, authentication-event investigations, vulnerability detection, and controlled attack simulations in an isolated environment.

## Reference

The initial lab procedure was based on the Wazuh Home Lab guide and accompanying video by Royden Rebello (The Social Dork). The repository documents my own implementation, testing, and evidence rather than claiming the reference lab as original work.

Reference video: https://youtu.be/QT81wcuoRFY

## Disclaimer

This project is for educational and authorized security testing only. All experiments were performed in a controlled home-lab environment.
