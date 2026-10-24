# Hey, I'm Manoj

BCA grad from Bengaluru, trying to get into a SOC analyst role.

I got into security during my cybersecurity internship, where I ended up spending most of my time breaking into test systems. These days I'm more interested in the other half: what an attack looks like in the logs and on the wire, and how a SOC catches it.

I'm looking for SOC Analyst, Security Analyst or Associate Engineer (Security) roles. I'm in Bengaluru and can start right away.

## What I spend my time on

Mostly malware PCAPs. I take a capture of an infected machine, find the host, follow it as it phones home to the attacker's server, pull out the IOCs and write the whole thing up with a timeline. It's basically packet-level detective work and I'm properly hooked. I try to be careful about what I actually saw in the traffic versus what I'm guessing, and I say which is which in the write-up. I've also stopped trusting automated scores blindly, after finding a C2 domain rated 0/89 that had 10+ malicious files talking to it.

The other big thing is my home SOC lab. I run a Wazuh instance on Kali, deploy agents across a few VMs, and keep a deliberately vulnerable Windows Active Directory machine around to attack. Then I go check whether the detections fired on the other side, and if they didn't, I write my own rules. Doing both sides taught me more than either one alone.

I also write Python to automate the boring parts of log analysis, because running the same Wireshark filter 50 times by hand gets old fast.

## Malware cases I've worked through

Each one has a write-up, an IOC list and an ATT&CK mapping:

- **AsyncRAT**: HTTP-based C2, spotted from an odd amount of traffic to one host
- **Lumma Stealer**: a dead-drop resolver on Pastebin, and an exfiltration puzzle I had to work through slowly
- **IcedID**: traced from the raw traffic
- **Angler EK to CryptoWall**: a full drive-by chain with domain shadowing. The ransomware never showed up as its own file because it was decrypted and run in memory, which took me a while to figure out
- **Spearphishing to dbx.exe**: the one where I had the actual email, so I could catch the spoofed sender and failed SPF check right from the headers
- **macOS AMOS-style infostealer**: payload download, C2 check-in, a roughly 3 MB archive of stolen data going out, all from a 19-minute capture

I also did an independent investigation of the 2026 Novo Nordisk breach using only public reporting. I rebuilt the timeline and mapped it to ATT&CK myself.

## Stuff I've built

- **SIEM Log Analyzer**: Python and Flask. Reads system and server logs and flags SSH brute force, SQL injection, privilege escalation and data exfiltration, maps them to ATT&CK and shows severity on a dashboard
- **PhishGuard**: checks SPF, DKIM and DMARC and scans URLs and attachments. I built it after watching people click very obviously fake emails
- **HybridPentest**: runs Nmap, SQLmap, Metasploit, Hydra, Gobuster and Nikto one after another and writes up a CVSS-scored report
- **AnalystAI**: you ask a question in plain English and get a chart back. Made for a hackathon, and I'm proud that it admits when it's unsure instead of making things up
- **Cryptography Toolkit**: a terminal app with SHA-256, AES-256 and RSA-2048, because I wanted to understand encryption and not treat it like a black box

## Tools I use

- **Security:** Wireshark (the one I stare at most), Wazuh, Splunk, Nmap, Burp Suite, Metasploit
- **Code:** Python, Bash.
- **Where I practise:** Kali Linux, a vulnerable Windows Server and AD lab, Ubuntu .

## What I'm learning right now

Writing better Wazuh detection rules based on what I see when I attack my own lab, getting deeper into log analysis, and getting better at Python for security automation. And more PCAPs, always more PCAPs.

## Background

I did a 2-month Cybersecurity and Ethical Hacking internship at ApexPlanet (with AICTE) in early 2026. I ran a pentest, documented 27 vulnerabilities and scored them with CVSS, and spent a lot of time on DVWA and Metasploitable.

I finished the Cisco Cybersecurity Defense Analyst career path in July 2026, and my BCA at Bengaluru City University in 2026.

## Get in touch

- LinkedIn: [manoj-n-naik-2ab040391](https://www.linkedin.com/in/manoj-n-naik-2ab040391)
- Email: 1105manoj.n@gmail.com
- Bengaluru, India
