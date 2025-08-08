| **OWASP Category**                                | **Status** | **Mapped Vulnerabilities in DVWA**                                         


| **A01: Broken Access Control**                    | ✅          | SQL Injection for Authentication Bypass, CSRF Password Reset      

         |
| **A02: Cryptographic Failures**                   | ⚠️         | No HTTPS/TLS in the default DVWA setup                                     

| **A03: Injection**                                | ✅          | SQL Injection via `id` parameter, including automated SQLMap exploitation  |

| **A04: Insecure Design**                          | ⚠️         | Predictable structure, weak form logic (e.g., CSRF with no tokens)         |

| **A05: Security Misconfiguration**                | ✅          | Apache status page exposed, directory listing enabled, Nikto scan findings |

| **A06: Vulnerable and Outdated Components**       | ✅          | PHP backdoors, outdated Apache version, vulnerable WordPress files         |

| **A07: Identification & Authentication Failures** | ✅          | Bypassing login with `' OR '1'='1`, password stored in weak MD5 hash       |

| **A08: Software and Data Integrity Failures**     | ⚠️         | (Not directly tested — applies more to CI/CD and software updates)         |

| **A09: Security Logging and Monitoring Failures** | ⚠️         | DVWA doesn't log failed login attempts or suspicious activities            |                                            |
