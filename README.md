# Mediroza Hospital – Penetration Testing Assessment

## Disclaimer

This repository documents an authorized educational exercise. It is not an assertion of authorization to test any production healthcare system. Sensitive records, credentials and personal information have been excluded or redacted.

**Author:** [IRIE PRECIOUS OGECHI]  
**Batch:** B084  
**Program:** Network Walks Cybersecurity Internship

## Project Overview

This project documents an instructor-assigned penetration-testing exercise against the Mediroza training web application. The assessment focused on reconnaissance, web application security, simulated patient-document retrieval, PDF password recovery, and exposure of staff and shareholder information.

## Scope and Authorization

Testing was conducted as part of the Network Walks internship training assignment, within the instructor-approved exercise scope.

## Tools Used

- Nmap
- WHOIS
- WhatWeb
- DNSRecon
- cURL
- OWASP ZAP
- Gobuster
- John the Ripper

## Assessment Results

| Module | Status |
|---|---|
| M1 – Initial Access | Completed |
| M2 – PDF Password Recovery | Completed |
| M3 – Staff and Shareholder Information | Completed |
| M4 – Reporting | Documented |

## Key Commands

**John the Ripper**
```bash
john hash3.txt --wordlist=/usr/share/wordlists/rockyou.txt
```

**Gobuster**
```bash
gobuster dir -u https://medirozahospital.com -w /usr/share/wordlists/dirb/common.txt
```

## Evidence

Screenshots are organized in the `evidence/` directory by assessment activity.

## Key Learning Outcomes

- Understanding web application reconnaissance.
- Identifying authentication and information-exposure weaknesses.
- Recovering passwords from authorized encrypted training documents.
- Understanding the security implications of exposed database backups.
- Documenting findings and recommending remediation.
