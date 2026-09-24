# Wazuh Windows Agent Setup

## Environment

- Endpoint OS: Windows
- Manager OS: Ubuntu VM
- Agent component: Wazuh Agent

## Installation and enrollment

The Windows endpoint was configured as the monitored agent. The supplied guide uses the Wazuh Agent Manager GUI and the manager-side `manage_agents` utility for enrollment.

### Manager-side agent registration

```bash
sudo /var/ossec/bin/manage_agents
```

The workflow used in the guide is:

1. Add a new agent.
2. Assign an agent name.
3. Extract the agent authentication key.
4. Apply the key in the Windows Wazuh Agent Manager.
5. Configure the Ubuntu manager address.
6. Restart the Windows agent service.

### Verification

The Windows endpoint was visible in the Wazuh Dashboard with an active status during the recorded demonstration.

## Evidence

- `../screenshots/active-agent.png`
- `../evidence/video-timestamps.md`

## Security note

Never commit an actual Wazuh agent key or other enrollment secrets to GitHub.
