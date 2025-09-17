# Ansible VM Monitor

Ansible-VM-Monitor is a project for automated monitoring of virtual machines (VMs) health and generating reports via Ansible. It streamlines collecting metrics, alerting/reporting, and can be customized for different VM environments.

---

## Table of Contents

- [Features](#features)  
- [Architecture / Components](#architecture--components)  
- [Requirements](#requirements)  
- [Setup & Installation](#setup--installation)  
- [Usage](#usage)  
- [Configuration](#configuration)  
- [How It Works](#how-it-works)  
- [Contributing](#contributing)  
- [License](#license)  

---

## Features

- Automatically collect VM health metrics (CPU, memory, disk, network, etc.)  
- Send periodic reports (e.g. via email or other channels)  
- Modular playbooks to separate concerns – collecting data, formatting, sending reports  
- Flexible configuration via Ansible inventory / group_vars  
- Template support for customizing report format  

---

## Architecture / Components

The project includes the following main components:

| Component | Purpose |
|-----------|---------|
| `collect_metrics.yaml` | Gathers metrics from target VMs (e.g. system load, disk usage, memory) |
| `send_report.yaml` | Takes the collected data and sends out a report |
| `playbook.yaml` | Top-level orchestrator playbook that ties together collection & report sending |
| `ansible.cfg` | Configuration file for Ansible, e.g. settings for inventory, roles, etc. |
| `inventory/` | List of hosts / VMs to monitor |
| `group_vars/` | Variables per group (or host) for customizing behavior per environment |
| `templates/` | Jinja2 templates for formatting reports (e.g. HTML, text) |
| Documentation (Steps Doc) | Describes how to set up, run, maintain the monitor |

---

## Requirements

To use this project, you will need:

- Ansible (version **2.x** or newer)  
- SSH access to VMs with appropriate user / privileges  
- Python and required libraries on VMs (if using any collector scripts)  
- Mail system / other transport (if reports are emailed)  
- Inventory file set properly (defining groups/hosts)  

---

## Setup & Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/jaiswaladi246/Ansible-VM-Monitor.git
   cd Ansible-VM-Monitor
