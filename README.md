# Comparative Review of Penetration Testing Tools

## 🔹 Overview
This project evaluates four popular penetration testing tools — **Nmap, Burp Suite, SQLmap, and Metasploit** — in a controlled virtual lab environment.  

The aim was to compare the tools based on:
- Ease of Use / Interface
- Reporting & Analysis Capabilities
- Performance (CPU, RAM, Memory)

👉 Findings show that while each tool has strengths in different areas, using them together provides the most effective penetration testing strategy.

---

## 🔹 Lab Setup

- **Host Machine:** AMD Ryzen 7 5800X, 32GB RAM, 500GB SSD  
- **Virtualisation:** VirtualBox  
- **VMs Used:**
  - Kali Linux (attacker)  
  - Metasploitable 2 (victim)  

---

## 🔹 Tools Reviewed

### 1. **Nmap (Network Mapper)**
- CLI-based tool for **network discovery & security auditing**.
- Supports TCP SYN scans, UDP scans, OS detection, and decoy scanning.
- **Strengths:** Fast, lightweight, versatile for reconnaissance.  
- **Limitations:** Command-line heavy, not beginner-friendly.  
- **Performance:** ~42MB RAM, 4% CPU.

---

### 2. **Burp Suite**
- GUI + CLI tool for **web application penetration testing**.
- Features: Proxy, Intruder, Repeater, Scanner (Pro only).
- Captures HTTP requests/responses, brute force testing, and manipulation of web traffic.
- **Strengths:** Excellent UI, strong web app testing, detailed reports.  
- **Limitations:** Community version limited (no automated scanning).  
- **Performance:** ~780MB RAM, 0.4% CPU.

---

### 3. **SQLmap**
- CLI-based tool for **detecting and exploiting SQL injection vulnerabilities**.  
- Automates database enumeration, data extraction, and password cracking.  
- **Strengths:** Powerful for SQL injection testing, automated exploitation.  
- **Limitations:** High CPU usage (~93%), CLI only.  
- **Performance:** ~63MB RAM, 93% CPU.

---

### 4. **Metasploit**
- CLI (free) / GUI (Pro) **framework for exploitation & post-exploitation**.  
- Large exploit & payload library.  
- Example: exploited vsftpd service on Metasploitable 2 → gained root access.  
- **Strengths:** Strong exploitation capabilities, industry standard.  
- **Limitations:** CLI learning curve, resource-heavy in large tests.  
- **Performance:** ~433MB RAM, 1.3% CPU.

---

## 🔹 Comparison Table

| Tool       | Interface       | Reporting      | Strengths                         | Limitations              |
|------------|-----------------|----------------|-----------------------------------|--------------------------|
| **Nmap**   | CLI             | Text/XML       | Recon, fast scans                 | CLI-heavy for beginners  |
| **Burp**   | GUI + CLI       | HTML, PDF, JSON| Web app testing, reporting        | Limited in free version  |
| **SQLmap** | CLI             | Logs/Text      | SQL injection exploitation        | Very CPU intensive       |
| **Metasploit** | CLI / GUI (Pro) | HTML, PDF, CSV | Exploits, payloads, post-exploit | Steep learning curve     |

---

## 🔹 Key Findings
- **Nmap + SQLmap** → Best for scanning, database testing.  
- **Burp Suite + Metasploit** → Best for web applications and exploitation.  
- No single “best tool” → effectiveness depends on scenario.  
- In practice, penetration testers often **combine all four**.  

---

## 🔹 Conclusion
This project demonstrated how penetration testing tools differ in usability, performance, and scope.  

**Key takeaways:**
- Reconnaissance is best handled by **Nmap**.  
- Web application testing is best with **Burp Suite**.  
- Database vulnerabilities are best tested with **SQLmap**.  
- Exploitation & post-exploitation are strongest with **Metasploit**.  

👉 A layered approach — using multiple tools together — ensures more effective security assessments.  


```markdown
![Nmap TCP SYN Scan](images/nmap-scan.png)
![Burp Suite Dashboard](images/burp-dashboard.png)
![SQLmap Results](images/sqlmap-results.png)
![Metasploit Exploit](images/metasploit-exploit.png)
