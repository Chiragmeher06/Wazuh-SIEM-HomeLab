# Lessons Learned

## Technical

- Wazuh uses a manager/agent architecture for endpoint monitoring.
- The Windows agent can provide endpoint telemetry to the manager.
- FIM can be used to detect changes in monitored files and directories.
- The dashboard provides a central place to inspect agent status and security events.

## Security operations

- Detection is only the first step; analysts need context and evidence to interpret an event.
- Controlled test activity is useful for validating that a detection works as expected.
- Screenshots, timestamps, and a clear investigation narrative improve technical documentation.

## Portfolio lesson

This project should be presented as a hands-on learning lab, not as production SOC experience. The next improvement is to add more realistic but isolated detections and document the investigation process for each one.
