# Network Walks Cybersecurity Internship – Week 4

## Mediroza General Hospital – Black-Box Vulnerability Assessment

**Internship Provider:** Network Walks  
**Batch:** B084  
**Project:** Week 4 – Penetration Testing  
**Assessment Type:** Authorized Educational Security Assessment  
**Duration:** 5 Days

---

## 1. Project Overview

This project involved conducting an authorized black-box vulnerability assessment of the Mediroza General Hospital educational web application.

The assessment focused on identifying potential web application vulnerabilities, investigating authentication mechanisms, examining document security, assessing password protection and documenting security findings.

All documents and patient information used during the exercise were simulated educational data.

## 2. Project Objectives

- Perform initial reconnaissance and automated security scanning.
- Identify and investigate potential web application vulnerabilities.
- Examine authentication and access control mechanisms.
- Assess password protection on supplied PDF documents.
- Investigate potential sensitive-data exposure.
- Document findings, supporting evidence, severity and remediation recommendations.

## 3. Tools and Technologies

| Tool | Purpose |
|---|---|
| Kali Linux | Security testing environment |
| OWASP ZAP | Automated vulnerability scanning |
| Burp Suite | HTTP request and response inspection |
| cURL | HTTP response-header investigation |
| John the Ripper | Password recovery assessment |
| RockYou Wordlist | Dictionary-based password testing |
| Nano | Hash file creation and editing |

## 4. Assessment Modules

### Module 1 – Reconnaissance and Initial Assessment
- Established access to the authorized educational application.
- Conducted automated scanning using OWASP ZAP.
- Examined captured HTTP requests and responses.
- Identified potential security configuration weaknesses.

### Module 2 – Vulnerability Identification
- Investigated the application's login functionality.
- Identified SQL injection through authorized testing.
- Examined application access to simulated documents.

### Module 3 – Document Security and Password Assessment
- Assessed three password-protected PDF documents.
- Successfully recovered the first two documents using tutor-provided tools.
- Used John the Ripper and the RockYou wordlist to assess the remaining document.

### Module 4 – Findings and Reporting
- Consolidated assessment observations.
- Reviewed HTTP security-header configurations.
- Documented identified weaknesses and potential impacts.
- Prepared appropriate remediation recommendations.

## 5. Key Security Findings

The assessment identified the following areas requiring security attention:

- SQL injection in the application's authentication functionality.
- Missing Content Security Policy header.
- Missing anti-clickjacking protection header.
- Missing Strict-Transport-Security header.
- Missing X-Content-Type-Options header.
- Cache-control directives requiring further review.
- PDF password protection requiring security assessment.

Severity ratings and supporting evidence are documented in the relevant assessment sections.

## 6. HTTP Security Header Investigation

The following command was used to inspect the target's HTTP response headers:

```bash
curl -I https://www.medirozahospital.com
```

The server returned HTTP/2 200. However, several recommended security headers were not visible in the response.

This observation informed further investigation and remediation recommendations.

## 7. Remediation Recommendations

Recommended defensive measures included:

- Use prepared statements and parameterized queries to prevent SQL injection.
- Implement appropriate Content Security Policy directives.
- Configure anti-clickjacking protection.
- Enforce HTTPS using HTTP Strict Transport Security.
- Configure `X-Content-Type-Options: nosniff`.
- Apply appropriate Cache-Control directives to sensitive resources.
- Enforce strong passwords and appropriate document encryption.

## 8. Repository Structure

```text
Network-Walks-Week-4-Mediroza-Penetration-Testing/
│
├── README.md
│
├── documentation/
│   ├── 01-project-overview.md
│   ├── 02-reconnaissance-and-access.md
│   ├── 03-vulnerability-assessment.md
│   ├── 04-document-security.md
│   └── 05-findings-and-recommendations.md
│
├── evidence/
│   ├── 01-reconnaissance/
│   ├── 02-vulnerability-assessment/
│   ├── 03-document-security/
│   ├── 04-exposure-analysis/
│   └── 05-http-headers/
│
└── report/
    └── final-assessment-report.pdf
```

## 9. Learning Outcomes

This project strengthened my practical understanding of:

- Web application reconnaissance.
- Automated and manual vulnerability assessment.
- SQL injection identification.
- HTTP security headers.
- PDF password protection.
- Dictionary-based password recovery.
- Technical evidence collection and reporting.
- Security risk assessment and remediation recommendations.

## 10. Conclusion

The Week 4 assessment provided practical experience in identifying web application security weaknesses, investigating document protection and documenting security observations.

It reinforced the importance of critical thinking, evidence-based testing and understanding both offensive security techniques and their corresponding defensive measures.

**Project Status:** Assessment and documentation.

**Disclaimer:** This project was conducted as an authorized educational exercise. All patient records and documents used were simulated. No real patient information was involved.
