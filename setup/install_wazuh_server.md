# 🧱 Wazuh Server Installation Guide

1. Download the installation script:
```bash
curl -sO https://packages.wazuh.com/4.7/wazuh-install.sh
```

2. Run the script with all-in-one option:
```bash
sudo bash ./wazuh-install.sh -a --ignore-check
```

3. Access the Wazuh dashboard at:
```
https://<your-server-ip>:5601
```

Make sure port 5601 is open in the firewall.
