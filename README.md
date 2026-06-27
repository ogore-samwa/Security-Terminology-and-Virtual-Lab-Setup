# Week 1 — Day 2: Security Terminology & Virtual Lab Setup

> **Course Structure:** Part 1 — Security Terminology (Theory, 1hr) | Part 2 — Virtual Lab Setup (Hands-On, 1hr)


## Objectives

- Speak the language of cybersecurity professionals fluently
- Understand real-world attack mechanisms and corresponding defensive structures
- Analyze threat intelligence briefings, documentation, and forum logs efficiently
- Navigate technical job interviews and professional certifications (Security+, CEH, OSCP)
- Deploy a fully operational, isolated virtual hacking environment


## 1. Core Security Terminology

### Common Attack Glossary

| Term | Definition |
|------|------------|
| **Exploit** | Code, scripts, or techniques used to take advantage of a system vulnerability |
| **Payload** | The malicious software or script component delivered to a target by an exploit |
| **Zero-Day** | A flaw completely unknown to the vendor — 0 days available for remediation |
| **Backdoor** | A covert method to bypass standard authentication for persistent access |


### Attack Methods & Techniques

| Attack | Description |
|--------|-------------|
| **Brute Force** | Systematically trying every possible character combination to crack credentials |
| **Dictionary Attack** | Automated credential cracking using pre-compiled lists of common passwords |
| **Man-in-the-Middle (MITM)** | Actively intercepting or altering data between two communicating parties |
| **Denial of Service (DoS)** | Flooding a network or system to render it inaccessible to legitimate users |


### Network-Specific Threats

| Threat | Description |
|--------|-------------|
| **Packet Sniffing** | Capturing and inspecting raw data traffic across a network interface |
| **ARP Spoofing** | Sending falsified ARP messages to redirect local traffic to an attacker |
| **Port Scanning** | Probing a remote server to map open ports and running services |
| **SQL Injection (SQLi)** | Inserting malicious database commands into vulnerable application entry fields |


### Web Application Risks

| Risk | Description |
|------|-------------|
| **XSS (Cross-Site Scripting)** | Injecting client-side scripts into trusted web pages to steal cookies or session tokens |
| **CSRF (Cross-Site Request Forgery)** | Forcing authenticated users to execute unauthorized account actions |
| **LFI / RFI** | Exploiting unsafe file handling to read local data or execute remote scripts |
| **Directory Traversal** | Using crafted inputs to escape the application's restricted root directory |


### Malware Classification

| Type | Description |
|------|-------------|
| **C2 / C&C** | Centralized infrastructure used to send instructions to infected machines |
| **Botnet** | A network of compromised machines controlled under a single C2 entity |
| **RAT (Remote Access Trojan)** | Stealth software granting attackers full remote control over a host |
| **Rootkit** | Malware designed to hide malicious processes from security software |
| **Cryptojacking** | Hijacking hardware resources to mine cryptocurrency without authorization |


### Vulnerability Evaluation

| Term | Definition |
|------|------------|
| **Vulnerability** | A flaw, bug, misconfiguration, or weakness within a host infrastructure |
| **CVE** | Common Vulnerabilities and Exposures — a standardized reference ID for known flaws |
| **CVSS** | Common Vulnerability Scoring System — scores flaw severity from 0 to 10 |
| **Attack Surface** | The total sum of exposure areas where unauthorized input can be attempted |
| **Hardening** | Fortifying systems by reducing the overall vulnerability footprint |


### Incident Response & Digital Forensics

| Term | Definition |
|------|------------|
| **Incident** | A verified security event that breaches confidentiality, integrity, or availability |
| **Incident Response (IR)** | Preparation → Detection → Containment → Eradication → Recovery |
| **Digital Forensics** | Scientific collection, preservation, and analysis of post-incident electronic evidence |
| **IOC (Indicator of Compromise)** | Forensic artifacts confirming a network has been penetrated |


### Security Frameworks & Compliance

| Framework | Description |
|-----------|-------------|
| **NIST** | US agency establishing standard computer security practices |
| **ISO 27001** | Global standard validating information security management structures |
| **OWASP** | Foundation mapping web application security risks |
| **PCI DSS** | Regulatory standard governing electronic credit card transactions |
| **GDPR** | European framework dictating data privacy standards |


## 2. Defense & Infrastructure Safeguards

| Control | Description |
|---------|-------------|
| **Firewall** | Evaluates traffic to block unauthorized communication packets |
| **IDS** | Intrusion Detection System — scans network events and flags malicious operations |
| **IPS** | Intrusion Prevention System — intercepts traffic inline to actively mitigate live attacks |
| **Antivirus / Antimalware** | Discovers, isolates, and erases malicious executable software |
| **Patch** | Software updates distributed by vendors to close identified vulnerabilities |


## 3. Access Control Architecture

| Concept | Definition |
|---------|------------|
| **Authentication** | Confirming the exact identity of an entity requesting access |
| **Authorization** | Mapping execution privileges to a verified identity |
| **MFA / 2FA** | Fortifying login gates by verifying independent possession and knowledge factors |
| **Privilege Escalation** | Exploiting flaws to cross into unauthorized access tiers |
| **Least Privilege Principle** | Restricting access strictly to what is required for a given role |


## 4. Cryptographic Foundations

| Term | Definition |
|------|------------|
| **Encryption** | Encoding readable data into ciphertext using cryptographic key sets |
| **Decryption** | Converting ciphertext back into plaintext using the corresponding key |
| **Hash** | Running input through a one-way algorithm to produce a unique fingerprint |
| **Digital Signature** | Verifying transmission integrity and source authenticity using encryption pairs |


## 5. Penetration Testing Operations

### Ethical Engagement Framework

| Role / Test Type | Description |
|-----------------|-------------|
| **Penetration Test** | An authorized, simulated offensive engagement evaluating infrastructure resilience |
| **Red Team** | Offensive security — maps attack surfaces and attempts to breach access |
| **Blue Team** | Defensive security — monitors systems and tracks anomalous behaviors |
| **Purple Team** | Collaborative engagement merging offensive techniques with defensive tracking |
| **White Box Testing** | Full transparency — operator has comprehensive network details |
| **Black Box Testing** | Zero-knowledge testing — models a blind external threat actor |


### Reconnaissance Methodology

| Type | Description |
|------|-------------|
| **Reconnaissance** | Initial scoping phase focused on aggregating threat intelligence |
| **Passive Recon** | Information gathering from a distance — no direct network interaction |
| **Active Recon** | Direct network probing — creates logged footprint entries |
| **OSINT** | Public scoping using open-source intelligence platforms |


### Ethics Matrix

| Hat | Description |
|-----|-------------|
| **White Hat** | Ethical security operators conducting permitted assessments |
| **Black Hat** | Illicit hackers exploiting systems to cause harm or steal assets |
| **Gray Hat** | Non-malicious actors who access environments without permission but report findings ethically |
| **Script Kiddie** | Operators using pre-packaged scripts without understanding fundamental concepts |


## 6. Virtual Lab Setup

### Lab Architecture

```
┌────────────────────────────────────────────────────────┐
│                   VIRTUALBOX HYPERVISOR                │
│                                                        │
│  ┌─────────────────┐             ┌──────────────────┐  │
│  │   KALI LINUX    │             │ METASPLOITABLE 2 │  │
│  │ (Attacker Node) │             │  (Target Server) │  │
│  └────────┬────────┘             └────────┬─────────┘  │
│           │                               │            │
│           └───────► Host-Only Network ◄───┘            │
│                      (Isolated Lab)                    │
└────────────────────────────────────────────────────────┘
```

---

### Hardware Requirements

| Component | Requirement |
|-----------|-------------|
| **Processor** | Virtualization-capable Intel or AMD |
| **RAM** | 8GB minimum / 16GB recommended |
| **Storage** | 50GB unallocated disk space |
| **BIOS** | Hardware Virtualization must be enabled |

---

### Node Deployment

#### Node 1 — Oracle VirtualBox
- Download installer from the official VirtualBox repository
- Run installer and map environment directories
- Accept baseline setup and confirm system permission updates

#### Node 2 — Kali Linux (Attacker)
- Download official VirtualBox appliance template
- Decompress archive and import `.ova` into VirtualBox
- Launch and log in:
  - **Username:** `kali`
  - **Password:** `kali`
- Confirm toolchain availability: Terminal, Nmap, Burp Suite, Metasploit, Wireshark

#### Node 3 — Metasploitable 2 (Target)
- Download Metasploitable 2 from SourceForge
- Create a new VM with Linux base configuration
- Point virtual hard disk to the downloaded `.vmdk` file
- Boot and log in:
  - **Username:** `msfadmin`
  - **Password:** `msfadmin`
- Confirm IP with: `ifconfig`

#### Node 4 — DVWA (Damn Vulnerable Web Application)
- Keep Metasploitable 2 powered on
- Note its IP address via `ifconfig`
- On Kali, open a browser and navigate to:
  ```
  http://[Target_IP_Address]/dvwa
  ```
- Log in with:
  - **Username:** `admin`
  - **Password:** `password`


### Virtual Network Modes

| Mode | Behavior |
|------|----------|
| **NAT (Default)** | Allows internet access; inbound connections blocked |
| **Host-Only (Recommended)** | Creates an isolated internal network — no external traffic leakage |

> Use **Host-Only** for lab sessions to keep all traffic contained.


### Network Isolation Steps

1. Open VirtualBox **Preferences → Network**
2. Create a new **Host-Only Adapter**
3. On both Kali and Metasploitable 2, set their network adapter to this Host-Only segment


## 7. Hypervisor Features to Know

| Feature | Purpose |
|---------|---------|
| **Snapshots** | Capture VM state before risky operations — easy rollback |
| **Shared Folders** | Bridge host storage to guest VM for file transfer |
| **Bidirectional Clipboard** | Copy/paste commands between host and guest |
| **Guest Additions** | Improves display resolution and mouse integration |


## 8. Troubleshooting

| Issue | Fix |
|-------|-----|
| **VT-x / AMD-V error** | Enable hardware virtualization in BIOS/UEFI |
| **VM running slowly** | Increase RAM allocation; close background apps |
| **VMs can't ping each other** | Verify both VMs are on the same Host-Only adapter |
| **Display scaling issues** | Adjust display scaling in VM settings |


## 9. Legal Notice

> **All testing must remain inside the sandbox lab.**
> Unauthorized testing of external systems is strictly prohibited.
> Written authorization is mandatory before assessing any production environment.


## 10. Post-Module Tasks

- [ ] Navigate configuration screens and file indexing across test machines
- [ ] Create snapshots on both VMs before making changes
- [ ] Run `ping` between Kali and Metasploitable 2 to confirm connectivity
- [ ] Complete the core terminology definition chart for the upcoming assessment
