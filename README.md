# 🔎 Nmap Lab

> **Summary:** Practiced host discovery, port scanning, service and OS enumeration, and special scanning techniques such as the **Xmas scan**. Strengthened reconnaissance fundamentals essential for vulnerability assessment and penetration testing.

---

## 🎯 Objective
Use Nmap to perform host discovery, service and OS enumeration, and advanced scanning techniques in order to identify and analyze networked systems in a controlled lab environment.

---

## 🛠️ Environment
- Platform: TryHackMe — *Nmap* room  
- Tool: **Nmap (Network Mapper)**  
- Focus Areas:  
  - Host discovery  
  - Port scanning (TCP & stealth techniques)  
  - Service & version detection  
  - OS fingerprinting  
  - Advanced scans (Xmas scan)  
  - Output & reporting  

---

## 🚀 Workflow

### 1) Host Discovery
- Used ping sweep (`-sn`) to identify live hosts.  
- Applied techniques to bypass simple firewall restrictions.  
  ```bash
  nmap -sn <target>
  
### 2) Port Scanning
- Ran full TCP SYN scans (`-sS`) and TCP connect scans (`-sT`) to enumerate open ports.
- Tuned scan timing with `-T1` (stealthier) and `-T4` (faster).
  ```bash
  nmap -sS <target>
  nmap -sT <target>
  
## 3) Service & Version Detection
- Used service enumeration to identify application versions:
  ```bash
  nmap -sv <target>
- Example findings included older SSH and web server versions.

## 4) OS Fingerprinting & Aggressive Scans
- Used OS detection (-O) and aggressive scan (-A) to gather deeper host insights.
  ```bash
  nmap -O <target>
  nmap -A <target>

## 5) Advanced Scanning — Xmas Scan
- Performed an Xmas scan to probe how the system responds to unusual flag combinations (FIN, PSH, URG).
  ```bash
  nmap -sX <target>
- Outcome: Showed closed vs. open/filtered port behavior, demonstrating how stealth scans can bypass certain firewall rules.
  
## 6) Output & Reporting
- Practiced saving scan results in multiple formats for reporting:
  ```bash
  nmap -oN nmap-results.txt <target>
  nmap -oX nmap-results.xml <target>

---

## ✅ Outcome
Successfully enumerated hosts and open services on the target.
Gained practical experience with stealth scanning (Xmas scan) in addition to common TCP/UDP scans.
Learned how to capture and document Nmap findings for vulnerability management workflows.

---

## 🧩 Skills Demonstrated
Proficiency with Nmap scanning techniques (-sS, -sT, -sV, -O, -A, -sX)
Understanding of stealth scanning and its role in reconnaissance
Host discovery and port/service enumeration
Structured scan output and reporting for security documentation













