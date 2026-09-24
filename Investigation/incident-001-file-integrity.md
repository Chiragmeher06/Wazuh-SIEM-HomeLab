# Investigation 001 – Controlled File Integrity Test

## Case type

Controlled security-monitoring validation

## Objective

Determine whether the Wazuh deployment detects and reports file changes on the monitored Windows endpoint.

## Environment

- Windows endpoint with Wazuh Agent
- Ubuntu VM running Wazuh Manager
- Wazuh Dashboard
- Monitored test directory

## Trigger

A controlled test was performed by operating on files in the monitored directory. This was an intentional lab action, not a real-world intrusion.

## Evidence reviewed

1. Windows test directory.
2. Wazuh agent status in the dashboard.
3. File Integrity Monitoring event list.
4. Expanded event/document details.

## Observations

The Wazuh dashboard displayed file-integrity events associated with the monitored endpoint. The event list showed file activity such as added/modified/deleted states, and an individual event could be expanded for additional document details.

## Analysis

The evidence supports that the endpoint was successfully communicating with the Wazuh Manager and that the configured FIM workflow was producing dashboard-visible security telemetry.

## Disposition

No incident response action was required because the activity was intentionally generated for validation. In a production environment, unexpected file changes would require contextual investigation before determining whether they were malicious, administrative, or application-related.

## Lessons learned

- A detection should be validated with controlled activity.
- Alert context is important before classifying an event.
- Evidence screenshots make a security investigation reproducible.
- A home lab can demonstrate the monitoring workflow without claiming production SOC experience.
