# sentinelops
# SentinelOPS

A lightweight Security Operations Center (SOC) automation project that detects security events using Wazuh SIEM and sends real-time alerts to Telegram while displaying events on a custom Flask dashboard.

---

## Project Overview

SentinelOPS was developed to demonstrate a real-world SOC workflow involving:

* Log collection and monitoring
* Threat detection
* Alert generation
* Incident notification
* Dashboard visualization

The project uses Wazuh as the SIEM platform and Python for alert automation.

---

## Features

### Real-Time Threat Detection

* SSH Brute Force Detection
* Failed Login Detection
* Non-Existent User Login Attempts
* System Security Events
* Network Activity Monitoring

### Automated Alerting

* Telegram Bot Integration
* Instant Alert Notifications
* Custom Alert Formatting

### Dashboard Monitoring

* Flask-based Web Dashboard
* Live Security Event Display
* Alert History Visualization

---

## Technology Stack

| Component         | Technology       |
| ----------------- | ---------------- |
| SIEM              | Wazuh            |
| Backend           | Python           |
| Dashboard         | Flask            |
| Alerting          | Telegram Bot API |
| Operating System  | Ubuntu Server    |
| Attack Simulation | Kali Linux       |
| Tools Used        | Hydra, Nmap      |

---

## Architecture

Kali Linux (Attacker)

↓

Hydra SSH Brute Force

↓

Ubuntu Target Server

↓

Wazuh Manager

↓

alerts.json

↓

Python Monitor Script

↓

Telegram Bot Alerts

↓

Flask Dashboard

---

## Attack Simulation

### SSH Brute Force

Attack Tool:

```bash
hydra -l ubuntu -P passwords.txt ssh://TARGET_IP
```

Detected By:

* Wazuh SSH Rules
* PAM Authentication Monitoring
* Brute Force Detection Rules

Generated Alerts:

* Failed Authentication Attempts
* Invalid User Attempts
* SSH Brute Force Detection

---

## Screenshots

### SSH Brute Force Attack

(Add screenshot here)

### Telegram Alert

(Add screenshot here)

### SentinelOPS Dashboard

(Add screenshot here)

### Wazuh Detection

(Add screenshot here)

---

## How It Works

1. Wazuh monitors system authentication logs.
2. Security events are written to alerts.json.
3. monitor.py continuously watches for new alerts.
4. High-priority alerts are processed.
5. telegram_alert.py sends notifications to Telegram.
6. Flask dashboard displays detected events.

---

## Project Outcome

Successfully implemented a SOC monitoring workflow capable of:

* Detecting SSH brute force attacks
* Generating real-time alerts
* Delivering notifications through Telegram
* Visualizing events through a web dashboard

---

## Future Enhancements

* MITRE ATT&CK Mapping
* Severity-Based Alert Filtering
* Dark Mode Dashboard
* Elasticsearch Integration
* Email Notifications
* Threat Intelligence Feeds
* GeoIP Attack Mapping

---

## Author

Aryan Shrivastav

Cybersecurity Enthusiast | SOC Analyst Aspirant | Blue Teaming | SIEM Engineering
