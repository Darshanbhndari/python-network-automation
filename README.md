# Python Network Automation

## Overview
This project focuses on automating network switch configuration using Python and Netmiko over SSH. It is designed for learning and practicing network automation in a lab environment.

## Objectives
- Automate VLAN creation.
- Assign switch ports to VLANs.
- Configure Switched Virtual Interfaces (SVIs).
- Collect switch information using show commands.
- Accept switch credentials and configuration parameters dynamically.
- Verify configurations and troubleshoot connection issues.

## Technologies Used
- Python
- Netmiko
- SSH
- Cisco switches
- VS Code

## Features
- Dynamic switch IP, username, and password input.
- Dynamic VLAN ID and interface selection.
- Access-port configuration.
- SVI IP address and subnet-mask configuration.
- Configuration output and verification.
- Basic exception handling and SSH session cleanup.

## Project Structure

```text
python-network-automation/
├── vlan-automation.py
├── port-assignment.py
├── svi-configuration.py
├── requirements.txt
└── README.md
```

## Prerequisites
- Python 3 installed.
- A compatible network switch with SSH enabled.
- Network connectivity to the switch management IP.
- A user account with the required configuration privileges.

## Installation

Clone this repository:

```bash
git clone https://github.com/YOUR-USERNAME/python-network-automation.git
cd python-network-automation
```

Install the required library:

```bash
pip install netmiko
```

## Usage

Run a script:

```bash
python vlan-automation.py
```

Enter the requested switch credentials, VLAN ID, interface name, and SVI details when prompted.

## Example Configuration

Example VLAN and access-port configuration:

```text
vlan 30
exit
interface GigabitEthernet1/0/5
switchport mode access
switchport access vlan 30
exit
interface vlan 30
ip address 192.168.30.1 255.255.255.0
no shutdown
```

The commands shown are illustrative. Verify that your switch model and firmware support the syntax before applying it.

## Verification

Use supported switch commands to verify the configuration, for example:

```text
show vlan
show interfaces status
show ip interface
```

## Security
- Never commit passwords, API keys, or other secrets.
- Use secure SSH authentication.
- Test configuration changes in a lab before applying them to production networks.
- Confirm VLAN IDs, interface names, and IP addressing before execution.

## Learning Outcomes
- Python scripting for network engineers.
- SSH-based device management.
- VLAN and access-port configuration.
- SVI configuration and verification.
- Basic network automation troubleshooting.

## Disclaimer
This project is intended for educational and lab use. Command syntax and feature availability depend on the switch model, firmware, and Netmiko driver.

## Author
**Darshan**

Network Engineering | Python Network Automation | VLANs | Switching | Routing
