# CTI IOC Parser

Python-based tool designed to extract, normalize and export Indicators of Compromise (IOCs) from threat intelligence reports, logs, emails or raw text.

This project was created as a practical Cyber Threat Intelligence (CTI) portfolio project focused on:
- IOC extraction
- IOC normalization (refang)
- Threat intelligence automation
- Blue Team workflows
- SIEM enrichment preparation

---

# Features

- Extracts:
  - IP addresses
  - Domains
  - URLs
  - Emails
  - MD5/SHA1/SHA256 hashes

- Refangs obfuscated indicators:
  - hxxp → http
  - [.] → .

- Exports results to:
  - JSON
  - CSV

- Simple and lightweight
- Easy to integrate into SOC/CTI workflows

---

# Example

Input text:

text The attacker connected to 185[.]220[.]101[.]45 and downloaded malware from hxxps://evil-domain[.]com/payload.exe MD5: 44d88612fea8a8f36de82e1278abb02f 

Output:

json {   "ips": [     "185.220.101.45"   ],   "domains": [     "evil-domain.com"   ],   "urls": [     "https://evil-domain.com/payload.exe"   ],   "hashes": [     "44d88612fea8a8f36de82e1278abb02f"   ] } 

---

# Installation

Clone the repository:

bash git clone https://github.com/YOUR-USERNAME/cti-ioc-parser.git cd cti-ioc-parser 

Install dependencies:

bash pip install -r requirements.txt 

---

# Usage

Run the parser against a text file:

bash python parser.py sample.txt 

The tool will:
- extract IOCs
- normalize indicators
- generate:
  - output.json
  - output.csv

---

# Project Structure

text cti-ioc-parser/ │ ├── parser.py ├── sample.txt ├── requirements.txt ├── README.md ├── output.json └── output.csv 

---

# Possible Improvements

Future enhancements planned:

- VirusTotal integration
- MISP integration
- STIX/TAXII export
- ASN enrichment
- IOC reputation scoring
- PDF parsing
- Telegram feed ingestion
- Threat actor tagging

---

# Skills Demonstrated

- Cyber Threat Intelligence (CTI)
- IOC handling
- Python automation
- Regex parsing
- Threat data normalization
- Defensive security tooling
- Blue Team workflow automation

---

# MITRE ATT&CK Relevance

This tool can support:
- IOC enrichment
- Threat Hunting
- Detection Engineering
- Intelligence workflows
- SOC investigations

---

# Disclaimer

This project is intended for:
- educational purposes
- research
- defensive cybersecurity operations

Use responsibly.

---

# Author

Cybersecurity & Threat Intelligence Portfolio Project
