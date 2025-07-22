# 🛡️ Wazuh Installation on Ubuntu (Self-Hosted)

This guide will walk you through installing Wazuh (Manager, Dashboard, Filebeat, and Elasticsearch/OpenSearch) on Ubuntu. It’s ideal for learning, SOC simulation, and threat detection use cases.

---

## 📌 Prerequisites

- Fresh Ubuntu 20.04/22.04 machine (VM or cloud)
- sudo privileges
- 4GB RAM minimum (8GB recommended)
- Internet access

---

## 1. 🧰 System Update & Required Packages

bash
sudo apt update && sudo apt upgrade -y
sudo apt install curl unzip wget gnupg apt-transport-https lsb-release software-properties-common -y


2. 📥 Download and Run Wazuh Installation Script

curl -sO https://packages.wazuh.com/4.7/wazuh-install.sh
chmod +x wazuh-install.sh
sudo ./wazuh-install.sh --wazuh-manager --dashboard --filebeat


3. ✅ Verify Wazuh Services Are Running

sudo systemctl status wazuh-manager
sudo systemctl status wazuh-dashboard
sudo systemctl status filebeat


If needed:

sudo systemctl restart wazuh-manager
sudo systemctl restart wazuh-dashboard
sudo systemctl restart filebeat


4. 🌐 Access Wazuh Dashboard
Open your browser: https://<YOUR_SERVER_IP>

Default credentials:

Username: admin

Password: admin

🖼️ You can add a screenshot of the dashboard login here:
<img src="screenshots_wazuh/Login%20details.jpg" alt="Login details" width="400"/>




5. 🤖 Add a Wazuh Agent (Local Test)
Install agent on the same machine (optional for local monitoring):

curl -sO https://packages.wazuh.com/4.7/wazuh-agent.deb
sudo dpkg -i wazuh-agent.deb


Edit agent config:

sudo nano /var/ossec/etc/ossec.conf
Replace manager IP:

<server>
  <address>your IP </address>
</server>
Start agent:

sudo systemctl enable wazuh-agent
sudo systemctl start wazuh-agent



