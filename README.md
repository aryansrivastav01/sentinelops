# 🛡️ SentinelOPS

### Real-Time SOC Monitoring & Threat Detection Platform

> A lightweight Security Operations Center (SOC) automation platform built using **Wazuh, Python, Flask, and Telegram** for real-time threat detection, alerting, and monitoring.

---

## 🚀 Project Overview

SentinelOPS simulates a modern SOC workflow by detecting security incidents, processing alerts, and delivering notifications instantly.

The platform continuously monitors Wazuh alerts and automatically sends high-priority security events to Telegram while displaying them on a custom dashboard.

---

## 🎯 Key Features

✅ Real-Time Security Monitoring

✅ SSH Brute Force Detection

✅ Failed Login Detection

✅ Wazuh SIEM Integration

✅ Telegram Alert Automation

✅ Flask-Based Security Dashboard

✅ Attack Simulation using Hydra & Nmap

---

## 🏗️ Architecture

```text
┌──────────────────┐
│  Kali Linux      │
│  (Attacker)      │
└────────┬─────────┘
         │
         ▼
┌──────────────────┐
│ SSH Brute Force  │
│  Hydra Attack    │
└────────┬─────────┘
         │
         ▼
┌──────────────────┐
│ Ubuntu Server    │
│ Target Machine   │
└────────┬─────────┘
         │
         ▼
┌──────────────────┐
│ Wazuh SIEM       │
│ Detection Engine │
└────────┬─────────┘
         │
         ▼
┌──────────────────┐
│ alerts.json      │
│ Event Stream     │
└────────┬─────────┘
         │
         ▼
┌──────────────────┐
│ monitor.py       │
│ Alert Processor  │
└──────┬─────┬─────┘
       │     │
       ▼     ▼
┌─────────┐ ┌─────────┐
│Telegram │ │Flask UI │
│ Alerts  │ │Dashboard│
└─────────┘ └─────────┘
```

---

## 🔥 Attack Demonstration

### Reconnaissance

```bash
nmap -sS -A TARGET_IP
```

### SSH Brute Force

```bash
hydra -l ubuntu -P passwords.txt ssh://TARGET_IP
```

### Detection

Wazuh successfully detected:

* Invalid User Login Attempts
* Authentication Failures
* SSH Brute Force Activity
* PAM Login Failures

---

## 📸 Screenshots

### 🔍 Attack Simulation

<p align="center">
<img src="screenshots/hydra-attack.png" width="900">
</p>

---

### 🚨 Telegram Alerting

<p align="center">
<img src="screenshots/telegram-alert.png" width="500">
</p>

---

### 📊 SentinelOPS Dashboard

<p align="center">
<img src="screenshots/dashboard.png" width="900">
</p>

---

### ⚙️ Backend Processing

<p align="center">
<img src="screenshots/backend-monitor.png" width="900">
</p>

---

## 🛠️ Tech Stack

| Category          | Technology         |
| ----------------- | ------------------ |
| SIEM              | Wazuh              |
| Programming       | Python             |
| Dashboard         | Flask              |
| Alerting          | Telegram Bot API   |
| Operating System  | Ubuntu Server      |
| Attack Simulation | Kali Linux         |
| Tools             | Hydra, Nmap        |
| Log Monitoring    | Wazuh Rules Engine |

---

## 📂 Project Structure

```text
SentinelOPS/
│
├── screenshots/
│   ├── hydra-attack.png
│   ├── telegram-alert.png
│   ├── dashboard.png
│   └── backend-monitor.png
│
├── app.py
├── monitor.py
├── telegram_alert.py
├── requirements.txt
├── README.md
└── docs/
```

---

## ⚡ Installation

### Clone Repository

```bash
git clone https://github.com/yourusername/SentinelOPS.git

cd SentinelOPS
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

### Run Dashboard

```bash
python3 app.py
```

### Run Alert Monitor

```bash
sudo python3 monitor.py
```

---

## 🧪 Example Alert

```yaml
🚨 SentinelOPS Alert

Rule:
sshd: brute force trying to get access to the system

Severity:
10

Source:
192.168.x.x

Status:
Blocked
```

---

## 📈 Skills Demonstrated

* SIEM Engineering
* Security Monitoring
* Threat Detection
* SOC Operations
* Log Analysis
* Linux Administration
* Security Automation
* Incident Response
* Python Development
* Blue Team Operations

---

## 🔮 Future Improvements

* MITRE ATT&CK Mapping
* GeoIP Attack Visualization
* Threat Intelligence Integration
* Elasticsearch Support
* User Authentication
* Alert Severity Filtering
* Dark Mode Dashboard

---

## 👨‍💻 Author

**Aryan Shrivastav**

Cybersecurity Enthusiast • SOC Analyst Aspirant • Blue Teaming • SIEM Engineering

---

⭐ If you found this project useful, consider starring the repository.
