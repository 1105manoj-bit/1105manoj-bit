# Hey, I'm Manoj

BCA graduate from Bengaluru. Got into security during an internship where I was supposed to do regular dev work — ended up spending most of my time breaking into test systems instead. Never looked back.

## What I'm actually doing right now

Spending way too much time staring at malware PCAPs trying to figure out how infected machines phone home to attacker servers. It's basically packet-level detective work and I'm genuinely hooked on it.

Also building out a home SOC lab with Wazuh — running my own SIEM instance, deploying agents across VMs, and setting up a deliberately vulnerable Windows Active Directory target so I can attack it myself and watch the detections actually fire on the other end. Closing the loop between "breaking things" and "catching it happening" has taught me more than either side alone.

Also writing Python scripts to automate the repetitive parts of log analysis — because running the same Wireshark filter 50 times manually is nobody's idea of fun.

## Tools I use

**Security:**
- Wireshark — my most used and most stared-at tool
- Wazuh — self-hosted SIEM/XDR, home lab
- Nmap for network recon
- Burp Suite for web app testing
- Metasploit for exploitation in lab environments

**Development:**
- Python — mainly for security automation and building tools
- Bash for quick scripts
- JavaScript/React when I need a proper interface

**Where I practice:**
- Kali Linux as my main workspace, running the Wazuh manager
- A dedicated Windows Server VM (Metasploitable 3 / vulnerable AD) as an attack target
- Ubuntu on WSL2 for dev work
- TryHackMe when I want structured challenges

## Projects I've built

**[Malware Traffic Analysis]**
Working through real malware PCAPs from public datasets, one full case at a time — finding infected hosts, tracing C2 infrastructure, and extracting IOCs. Four cases in so far, each a different infection style:
- **AsyncRAT** — HTTP-based C2, spotted through abnormal packet volume to a single host
- **Lumma Stealer** — dead-drop resolver pattern via Pastebin, plus a real Tx/Rx exfiltration puzzle I had to work through carefully
- **Angler EK → CryptoWall** — a full drive-by chain, including tracing domain shadowing and figuring out why the actual ransomware payload never showed up as its own file (decrypted and run entirely in memory)
- **Spearphishing → dbx.exe downloader** — the one case where I had the actual phishing email, not just traffic; caught a spoofed sender and failed SPF check directly from the headers

Every case gets a full write-up and IOC list, mapped to MITRE ATT&CK. Started this because I wanted proof I can actually analyze threats — not just talk about tools I've heard of.

**[Independent Breach Case Study — Novo Nordisk]**
Self-directed OSINT investigation into a real 2026 data breach, built entirely from public reporting with no inside access. Reconstructed the full attack timeline and mapped it to MITRE ATT&CK myself — including a genuine mistake on my first pass (misclassified a stage as Reconnaissance instead of Credential Access) that I caught and corrected, and left in the write-up on purpose.

**[SIEM Log Analyzer]**
Python tool that monitors logs for attack patterns like SSH brute force, SQL injection attempts, and privilege escalation. Maps findings to MITRE ATT&CK because that's the language security teams actually speak.

**[PhishGuard]**
Email security analyzer that detects phishing and spoofing using SPF/DKIM/DMARC validation. Built it after watching people click obviously fake emails one too many times.

**[AnalystAI]**
Data visualization tool where you ask questions in plain English and get charts back. Built for a hackathon. Proud of this one because it actually handles uncertainty instead of confidently making things up.

**[Cryptography Toolkit]**
Terminal app with SHA-256, AES-256, RSA-2048 implementations. Built it because I wanted to actually understand encryption — not just use it like a black box.

## What I'm working on learning

Getting deeper into log analysis and writing detection rules that actually catch real attack patterns — right now that means writing custom Wazuh rules based on what I actually see when I attack my own lab, not just reading about detection theory. Also improving Python for security automation.

## Background

2-month cybersecurity internship where I:
- Ran a full pentest and documented 27 vulnerabilities across OWASP Top 10
- Exploited real vulnerabilities on DVWA and Metasploitable
- Learned how attacks actually work — not just the theory version

## Find me

- LinkedIn: [manoj-n-naik-2ab040391](https://www.linkedin.com/in/manoj-n-naik-2ab040391)
- Email: 1105manoj.n@gmail.com
- Bengaluru, India
