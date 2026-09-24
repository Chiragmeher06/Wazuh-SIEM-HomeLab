# File Integrity Monitoring (FIM)

## Objective

Validate that Wazuh can detect changes to files in a monitored Windows directory.

## Configuration

The supplied guide configures a Windows directory for real-time monitoring using the Wazuh agent `ossec.conf` file. The example uses the `realtime="yes"` attribute.

Example from the guide:

```xml
<directories realtime="yes">C:\Users\abc\Test</directories>
```

For this project, use the actual test path from your own environment if you later reproduce the configuration. Do not publish personal usernames or sensitive paths unnecessarily.

## Controlled validation

The screen recording shows a test folder and subsequent Wazuh File Integrity Monitoring events. The test activity included file creation/modification/deletion operations.

## Expected behavior

Wazuh FIM records file attributes and detects changes in monitored paths. The resulting events can be reviewed in the Wazuh Dashboard.

## Evidence

- `../screenshots/monitored-folder.png`
- `../screenshots/fim-events.png`
- `../screenshots/fim-event-details.png`

## Result

The recorded lab demonstrates that the Windows endpoint was reporting FIM activity to the Wazuh Dashboard and that individual file events could be inspected.
