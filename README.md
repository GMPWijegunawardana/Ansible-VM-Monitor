# 🖥️ Ansible VM Monitor

**Ansible-VM-Monitor** is an automation project designed to monitor the health of Virtual Machines (VMs) and generate system reports using **Ansible playbooks**.  
It simplifies **infrastructure monitoring** by automating the collection of key system metrics (CPU, memory, disk, and network usage) and delivering reports to administrators.  

This project demonstrates how **Infrastructure as Code (IaC)** tools like Ansible can go beyond provisioning and configuration to handle **monitoring and operational workflows**.

---

## 🚀 Why This Project?

Manual VM monitoring can be tedious, error-prone, and inconsistent.  
With Ansible, we can:

- Automate repetitive monitoring tasks
- Run on any number of VMs in parallel
- Standardize the way reports are generated and delivered
- Easily extend functionality with new playbooks, roles, or templates

This project is also a **practical showcase of DevOps & Ansible skills** for infrastructure automation.

---

## ✨ Features

- 🔍 **Collect VM Metrics**: CPU load, memory usage, disk utilization, and network stats  
- 📑 **Custom Reports**: Generate reports using Jinja2 templates (text/HTML formats)  
- 📧 **Automated Delivery**: Send reports via email (or extend to Slack, PagerDuty, etc.)  
- ⚡ **Agentless Setup**: Uses Ansible over SSH – no agent required on VMs  
- 🔧 **Configurable Thresholds**: Define alert levels for CPU, memory, or disk usage  
- 🧩 **Modular Design**: Separate playbooks for collection, reporting, and sending  

---

## 🏗️ Project Structure

```bash
Ansible-VM-Monitor/
├── ansible.cfg            # Ansible configuration file
├── inventory/             # Define VM hosts and groups
│   └── hosts.ini
├── group_vars/            # Group/host-specific variables
│   └── all.yaml
├── playbook.yaml          # Main playbook (orchestrator)
├── collect_metrics.yaml   # Playbook to gather VM stats
├── send_report.yaml       # Playbook to send reports
├── templates/             # Jinja2 templates for reports
│   └── report_template.j2
├── docs/                  # Documentation files
│   └── setup_steps.md
└── README.md              # Project documentation
