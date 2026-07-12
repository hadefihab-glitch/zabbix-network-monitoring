# Zabbix Network Monitoring

## 📖 Project Overview

This project demonstrates the deployment of **Zabbix 7.0** on Ubuntu for monitoring Linux servers in a virtual environment.

The monitoring platform supervises CPU, memory, disk usage and automatically executes a remediation script when CPU utilization exceeds 90%.

---

# Project Architecture

```
                +----------------------+
                |    Zabbix Server     |
                |   Ubuntu 24.04 LTS   |
                | Apache2 + MariaDB    |
                +----------+-----------+
                           |
        -----------------------------------------
        |                                       |
+-------------------+                  +-------------------+
|   RH Client       |                  |  FINANCE Client   |
| Ubuntu + Agent    |                  | Ubuntu + Agent    |
+-------------------+                  +-------------------+
```

---

# Features

- Install Zabbix Server
- Configure Apache2
- Configure MariaDB
- Install Zabbix Agent
- Add monitored hosts
- CPU Monitoring
- Memory Monitoring
- Disk Monitoring
- Trigger creation
- Automatic CPU remediation
- Automatic action execution
- Dashboard monitoring

---

# Services Verification

## Apache2

![](screenshots/10-service-apache2.png)

---

## MariaDB

![](screenshots/11-service-mariadb.png)

---

## Zabbix Server

![](screenshots/12-service-zabbix-server.png)

---

## Zabbix Agent

![](screenshots/13-service-zabbix-agent.png)

---

# Hosts Configuration

Both monitored hosts are successfully connected to the Zabbix server.

![](screenshots/01-hotes-rh-finance-connectes.png)

---

# System Monitoring

## FINANCE Host

![](screenshots/08-supervision-finance.png)

---

## RH Host

![](screenshots/09-supervision-rh.png)

---

# CPU Trigger

A High severity trigger detects when CPU utilization exceeds 90%.

```text
last(/FINANCE/system.cpu.util)>90
```

![](screenshots/02-declencheur-cpu-90.png)

---

# Automatic Remediation Script

The script is executed remotely by the Zabbix Agent.

![](screenshots/03-script-correction-cpu.png)

---

# Automatic Action

The trigger automatically launches the remediation script.

![](screenshots/04-action-remediation-cpu.png)

---

# CPU Alert

Zabbix detects CPU overload.

![](screenshots/06-alerte-cpu-superieur-90.png)

---

# Automatic Resolution

The remediation script successfully resolves the issue.

![](screenshots/07-remediation-reussie.png)

---

# Dashboard

Global monitoring dashboard.

![](screenshots/05-dashboard-zabbix.png)

---

# Technologies

- Ubuntu Linux
- Zabbix 7.0
- Apache2
- MariaDB
- PHP
- Bash
- Oracle VirtualBox

---

# Project Structure

```
zabbix-network-monitoring/
│
├── README.md
│
└── screenshots/
    ├── 01-hotes-rh-finance-connectes.png
    ├── 02-declencheur-cpu-90.png
    ├── 03-script-correction-cpu.png
    ├── 04-action-remediation-cpu.png
    ├── 05-dashboard-zabbix.png
    ├── 06-alerte-cpu-superieur-90.png
    ├── 07-remediation-reussie.png
    ├── 08-supervision-finance.png
    ├── 09-supervision-rh.png
    ├── 10-service-apache2.png
    ├── 11-service-mariadb.png
    ├── 12-service-zabbix-server.png
    └── 13-service-zabbix-agent.png
```

---

# Author

**Ihab Hadaf**

Digital Infrastructure & Network Engineering Student

Network • Cloud • Linux • Zabbix
