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

![](screenshots/vérification apach.png)

---

## MariaDB

![](screenshots/vérification mariadb.png)

---

## Zabbix Server

![](screenshots/Vérification zabbix .png)

---

## Zabbix Agent

![](screenshots/vérification zabbix.agent.png)

---

# Hosts Configuration

![](screenshots/Connexion des clients RH et Finance au serveur Zabbix.png)

---

# System Monitoring

## FINANCE

![](screenshots/Surveillance des ressources système du client FINANCE dans Zabbix.png)

---

## RH

![](screenshots/Surveillance des ressources système du client RH dans Zabbix.png)

---

# CPU Trigger

![](screenshots/Création d'un déclencheur pour la surveillance du CPU.png)

---

# Automatic Remediation Script

![](screenshots/Création d'un script de correction automatique du CPU dans Zabbix.png)

---

# Automatic Action

![](screenshots/Création d'une action pour exécuter automatiquement le script de correction CPU.png)

---

# CPU Alert

![](screenshots/Déclenchement d'une alerte CPU lorsque l'utilisation dépasse 90 %.png)

---

# Automatic Resolution

![](screenshots/Exécution réussie de la remédiation automatique et résolution du problème CPU dans Zabbix.png)

---

# Dashboard

![](screenshots/Dashboard ZABBIX.png)
---

# Technologies

- Ubuntu Linux
- Zabbix 7.0
- Apache2
- MariaDB
- PHP
- Bash
- Oracle VirtualBox

