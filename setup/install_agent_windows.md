# 🛰️ Windows Agent Installation Guide

1. Download the Wazuh agent for Windows:
   https://packages.wazuh.com/4.x/windows/wazuh-agent-4.7.2.msi

2. During installation:
   - Manager IP: `<your-wazuh-server-ip>`
   - Agent Name: choose a hostname
   - Group: `default`

3. Start the service:
```cmd
sc start wazuh
```

Check logs at `C:\Program Files (x86)\ossec-agent\logs\ossec.log`
