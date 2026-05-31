# OSINT - Passive Subdomain Enumeration Tool

OSINT is a lightweight, high-speed passive reconnaissance tool written in Python 3. It leverages open-source intelligence (OSINT) feeds to rapidly map the attack surface of a target domain by extracting its unique subdomains. The utility completely avoids direct interactions with the target infrastructure, ensuring 100% stealth during the intelligence-gathering phase.

---

## ✨ Features

- **🕵️ 100% Passive Reconnaissance**: Gathers infrastructure mapping data via third-party intelligence feeds, leaving absolutely zero log trails on the target system's firewalls or IDS/WAF solutions.
- **🚀 Stable OSINT Integration**: Utilizes the highly reliable HackerTarget Hostsearch API to instantly aggregate subdomains without requiring premium API keys or complex setups.
- **🧹 Data Sanitization & Validation**: Automatically filters out internal duplicates, drops corrupt entries, and strips secondary metadata (like cross-referenced IP fields) to maintain strict domain data integrity.
- **📄 Structured Reporting**: Automatically sorts discovered endpoints and exports clean, production-ready assets into a localized text report (`<domain>_subdomains.txt`) for immediate integration into automated pipeline checkers (like `httpx` or `nuclei`).

---

## 📋 Requirements & Installation

This project requires **Python 3.x** and the standard `requests` HTTP communication library.

1. Clone or download this repository into your dedicated local folder:
```bash
git clone https://github.com
cd Pymap-OSINT
```

2. Setup the required Python dependencies:
```bash
pip install requests urllib3
```

---

## 🚀 Usage Guide

1. Fire up your terminal inside the script folder and execute the interactive script:
```bash
python osint_scanner.py
```

2. When prompted by the system interface, input your target root domain destination:
```text
Введите целевой домен (например, google.com): targetdomain.com
```

### Expected Telemetry Output:
- **Console Matrix**: Instantly formats a distinct command-line tree displaying all successfully discovered target subdomains.
- **File System**: Automatically generates a persistent dictionary artifact named `<targetdomain.com>_subdomains.txt` containing sorted, clean subdomains for further attack surface analysis.

---

## ⚖️ Legal & Educational Disclaimer

**IMPORTANT NOTICE:** This utility is engineered exclusively for authorized security audits, legitimate OSINT infrastructure analysis, corporate attack surface mitigation mapping, and educational Bug Bounty research. 

Passive information gathering from publicly accessible internet aggregators complies with standard data collection protocols. However, the author holds **no liability** for any strategic misuse, subsequent active probing without explicit owner authorization, or legal conflicts arising from data interpretation conducted via this technical framework.
