# Home-SOC-Lab-With-Wazuh-SIEM
Built a Home SOC (Security Operations Center)  Lab using Wazuh SIEM on ARM64 VMs to monitor endpoint activity, ingest logs, and detect real-world cyberattacks.

## Overview
This project demonstrates a hands-on implementation of a **Security Information and Event Management (SIEM)** system using **Wazuh** to detect and analyze brute-force attacks in a controlled lab environment.

The goal was to simulate real-world attack scenarios and validate detection capabilities using log analysis, rule matching, and event visualization.

---

## Objectives
- Deploy and configure a Wazuh SIEM environment
- Install and register a Wazuh agent
- Simulate a brute-force SSH attack
- Monitor and analyze security events
- Validate detection using Wazuh rules

---

## Lab Architecture

- **Wazuh Manager + Dashboard** (SIEM Server)
- **Wazuh Agent** (Monitored Endpoint)
- **Attack Source** (Same machine using SSH brute force simulation



---

## Tools & Technologies
- Wazuh SIEM
- Ubuntu Linux
- SSH (Secure Shell)
- Nmap (for scanning)
- System logs (auth.log)
- Virtualization (UTM / VM)

---

## Implementation Steps

### 1. Install Wazuh Server
- Deployed Wazuh manager and dashboard
- Accessed dashboard via browser

### 2. Install Wazuh Agent
- Installed agent on endpoint
- Registered agent with manager
- Verified active connection

### 3. Simulate Attack
Executed repeated SSH login attempts:

```bash
for i in {1..20}; do ssh fakeuser@localhost; done
