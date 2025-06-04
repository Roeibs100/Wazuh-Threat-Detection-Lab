# 📝 SOC Incident Report Example

**Date:** 2025-06-04  
**Analyst:** Roei  
**Tool Used:** Wazuh 4.7.5  
**Incident Type:** Malicious Executable Detected

## 🧪 Summary
Wazuh detected a suspicious executable named `update.exe` running from a user temp directory.

## 🔍 Timeline
- 08:31 - Agent sent alert about process execution
- 08:32 - Analyst confirmed unsigned binary
- 08:34 - Checked with VirusTotal - confirmed malicious

## 📌 Indicators of Compromise (IOCs)
- File: `C:\Users\User\AppData\Local\Temp\update.exe`
- Hash: `b4c0ffee123456789abcdef...`
- IP: `185.245.87.20`

## 🛡️ Actions Taken
- Blocked the IP on the firewall
- Deleted the file and scanned the system
- Reported the incident to the CSIRT team

## ✅ Conclusion
Attack was contained before damage occurred.
