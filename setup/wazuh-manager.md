# Wazuh Manager Setup

## Environment

- Host OS: Windows
- Virtualization: Oracle VirtualBox
- Manager OS: Ubuntu
- Component: Wazuh Manager / Dashboard

## Installation workflow

The supplied guide uses Ubuntu in VirtualBox as the Wazuh Manager. The recorded implementation follows that overall workflow.

### 1. Add the Wazuh GPG key

```bash
curl -s https://packages.wazuh.com/key/GPG-KEY-WAZUH | sudo gpg --dearmor -o /usr/share/keyrings/wazuh-archive-keyring.gpg
```

### 2. Download and run the installation script

```bash
curl -sO https://packages.wazuh.com/4.12/wazuh-install.sh
sudo bash ./wazuh-install.sh -a -i
```

The supplied guide describes `-a` as installing the required Wazuh components and `-i` as interactive mode.

### 3. Access the dashboard

The Ubuntu VM IP address was used to reach the Wazuh Dashboard from the lab environment. The dashboard was then used to verify agent status and inspect events.

## Evidence

See the screenshots in `../screenshots/` and the original screen recording supplied with this project.

## Security note

Do not publish Wazuh dashboard credentials, agent keys, private keys, API tokens, or other secrets in this repository.
