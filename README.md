# 🛡️ Wazuh Threat Detection Lab

A full lab setup for installing and using Wazuh to detect endpoint threats.  
Includes server installation, agent setup, alert visualization, and a sample incident report.

---

## 📌 Table of Contents
- 🎯 Learning Objectives
- 🧱 Wazuh Server Installation
- 🛰️ Wazuh Agent Installation (Windows)
- 📸 Screenshots & Diagrams
- 📝 Sample SOC Report
- 🧰 Technologies Used
- 📂 Project Structure

---

## 🎯 Learning Objectives
- Deploy a Wazuh All-In-One server
- Install and register a Windows agent
- Generate detection alerts based on suspicious activity
- Analyze and report incidents in a SOC-style format

---

## 🧱 Wazuh Server Installation

```bash
curl -sO https://packages.wazuh.com/4.7/wazuh-install.sh
sudo bash ./wazuh-install.sh -a --ignore-check
```

📍 After installation:  
Access the dashboard at: `https://<server-ip>:5601`

(See `setup/install_wazuh_server.md` for full guide.)

---

## 🛰️ Wazuh Agent Installation (Windows)

1. Download MSI: https://packages.wazuh.com/4.x/windows/wazuh-agent-4.7.2.msi  
2. Server IP: `<your-wazuh-server-ip>`  
3. Group: `default`

Run:
```cmd
sc start wazuh
```

(See `setup/install_agent_windows.md` for full guide.)

---

## 📸 Screenshots & Diagrams

| Wazuh Architecture | Sample Alert |
|-------------------|-------------|
| ![Arch](alerts/screenshots_alerts/wazuh_architecture.png) | ![Alert](alerts/screenshots_alerts/example_alert.png) |

---

## 📝 Sample SOC Report

See: `report/incident_report.md`

---

## 🧰 Technologies Used

Linux, Bash, Windows, Wazuh, SOC Practices

---

## 📂 Project Structure

```
Wazuh-Threat-Detection-Lab/
├── README.md
├── setup/
│   ├── install_wazuh_server.md
│   └── install_agent_windows.md
├── alerts/
│   └── screenshots_alerts/
│       ├── wazuh_architecture.png
│       └── example_alert.png
├── report/
│   └── incident_report.md
```
