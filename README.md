# Future-Interns-CyberSecurity-Task1
Vulnerability Assessment Report on zero.webappsecurity.com - Future Interns Task 1
# 🛡️ Vulnerability Assessment Report (Passive Audit)

## 📌 Project Overview
This repository contains the practical deliverables for **Task 1 of the Future Interns Cybersecurity Internship**. This project focuses on performing a safe, non-intrusive, and purely passive vulnerability assessment against a public sandbox web application to map its external attack surface, identify configuration flaws, and provide technical remediation strategies.

---

## 🔍 Assessment Scope & Methodology
* **Target Domain:** `http://zero.webappsecurity.com`
* **Assessment Type:** Read-Only Passive Audit (Zero Exploitation / No System Disruption)
* **Testing Frameworks:** Mapped directly to **OWASP Top 10 (2021)** and **CWE (Common Weakness Enumeration)** standards.

---

## 🛠️ Tooling & Environment
* **OS:** Kali Linux (Hosted inside Oracle VirtualBox)
* **Reconnaissance & Port Analysis:** Nmap v7.98
* **Dynamic Header & Policy Analysis:** cURL
* **Passive Automated Vulnerability Scanning:** OWASP ZAP v2.17.0

---

## 📊 High-Level Risk Metrics
* 🔴 **High Risk:** 1 (SQL Injection via SQLite - Time Based)
* 🟡 **Medium Risk:** 3 (Missing CSP/Anti-Clickjacking, Cross-Domain CORS Misconfiguration, Absence of Anti-CSRF Tokens)
* 🔵 **Low Risk:** 2 (Outdated Server Software Banners, Missing HSTS Protocol)

---

## 📸 Technical Proofs & Evidence

### 1. HTTP Response Header Enumeration (cURL)
Missing security controls and verbose server header exposure verified:
![cURL Output](evidence/curl_headers.png)
<img width="543" height="220" alt="interntask13" src="https://github.com/user-attachments/assets/1a6c01ea-a1c0-400d-99d5-2fc70af2914a" />

### 2. Port & Service Version Fingerprinting (Nmap)
Exposed development port 8080 and severely outdated production software (Apache 2.2.6) detected:
![Nmap Output](evidence/nmap_scan.png)
<img width="777" height="276" alt="interntask14" src="https://github.com/user-attachments/assets/597a8daf-998c-424f-878a-3251b48489d5" />

### 3. Automated Vulnerability Dashboard (OWASP ZAP)
Comprehensive tracking chart validating targeted risk severity profiles:
![OWASP ZAP Alerts](evidence/owasp_zap_alerts.png)
<img width="887" height="852" alt="interntask24" src="https://github.com/user-attachments/assets/727229fd-4ca3-4cf7-871a-37697578856c" />

---

## 📂 Final Consulting Deliverable
The complete, executive-ready 11-page security consulting report has been compiled and is accessible here:
📄 **[Download the Full PDF Report](report/Vulnerability_Assessment_Report.pdf)**
https://github.com/kavibharathi1001/Future-Interns-CyberSecurity-Task1/blob/c88fedc42809bdb6b131741bd5a333f39faf38a3/Cyber%20Security%20Task1-Report.pdf
---

## ⚖️ Ethics & Scope Disclaimer
This assessment was performed strictly using passive, read-only methodologies in complete compliance with the provided internship guidelines. No active exploitation vectors, denial of service payloads, or configuration alterations were attempted against the targeted host asset infrastructure.
