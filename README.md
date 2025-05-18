# 🛡️ Network Penetration Testing with Real-World Exploits and Security Remediation

This project simulates real-world network attacks and defense strategies using Kali Linux as the attacker machine and Metasploitable as the target. It includes scanning, enumeration, exploitation, password cracking, and remediation — all performed in a controlled lab environment for ethical learning purposes.

---

                                                  


## 🎯 Objectives

- Understand and simulate real-world network attacks
- Perform scanning, enumeration, and exploitation using tools like Nmap and Metasploit
- Crack Linux password hashes using John the Ripper
- Identify outdated services and recommend security remediations

---

## 💻 Lab Setup

### 🖥️ Operating Systems
- **Kali Linux** – Attacker Machine
- **Metasploitable 2** – Target Machine

### 🛠️ Tools Used
- `nmap` – Port, OS, and service version scanning
- `Metasploit` – Exploitation
- `John the Ripper` – Password hash cracking
- Linux built-in commands – user management and enumeration

---

## 🚀 Tasks Performed

### 🔍 Network Scanning
- `nmap -v IP` – Basic scan
- `nmap -v -p- IP` – Full port scan
- `nmap -sV IP` – Service version detection
- `nmap -O IP` – OS detection
- ![Screenshot_2025-05-17_15_01_36](https://github.com/user-attachments/assets/592c28eb-9a6b-4cc0-b327-b9d1d5bbe57e)
![Screenshot_2025-05-17_15_02_39](https://github.com/user-attachments/assets/b4eb1df7-78d6-4796-8bc3-ad911bbd8270)
![Screenshot_2025-05-17_15_02_59](https://github.com/user-attachments/assets/6889f9bf-d012-469d-85e2-3771f3939d7a)


### 🔐 Hidden Ports Discovered
Ports like `8787`, `36588`, `53204`, etc., found through full port scans.

### 📡 Enumeration
- OS: Linux 2.6.x (Metasploitable)
- Open services: vsftpd, OpenSSH, Apache, MySQL, Samba, etc.
- Vulnerable ports: 21 (FTP), 445 (SMB), 512–514 (R Services)

### 💥 Exploitation
- **vsftpd 2.3.4** backdoor
- **SMB 3.0.20-Debian** using Metasploit
- **Rexec/Rlogin/Rsh** services using script-based vulnerabilities
- ![Screenshot_2025-05-17_15_03_45](https://github.com/user-attachments/assets/ccd0cd3c-73df-43b7-8a52-495368656b4b)
![Screenshot_2025-05-17_15_03_59](https://github.com/user-attachments/assets/6b130ea4-a2c6-4a13-99b3-915cf6b2787e)


### 👤 Privilege Escalation
- Created user `vipin` with root permissions
- Extracted and cracked password hash using John the Ripper

### 🔧 Remediation Steps
| Service   | Vulnerability                  | Fix                              |
|-----------|--------------------------------|----------------------------------|
| vsftpd    | Backdoor (CVE-2011-2523)       | Upgrade to 3.0.5 / use SFTP      |
| SMB       | RCE, Null Sessions             | Upgrade to Samba 4.20.1          |
| R Services| Plaintext creds (CVE-1999-0651)| Disable & use SSH instead        |

---

## 📚 Major Learning

Through this project, I learned how to create and manage users in Linux, analyze system files, crack password hashes, and detect services using Nmap. I practiced using commands like `nmap -sV`, `nmap -O`, and `john` to identify system weaknesses. I also understood how outdated services like FTP, SMB, and R services pose serious security risks and how to patch or replace them.

---

## ⚠️ Disclaimer

This project is for **educational purposes only**. All activities were performed in a **safe, offline lab environment**. Do not attempt these techniques on real networks without explicit permission.

---

## 📎 References

- [CVE-2011-2523](https://nvd.nist.gov/vuln/detail/CVE-2011-2523)
- [Metasploit Documentation](https://docs.rapid7.com/metasploit/)
- [John the Ripper](https://www.openwall.com/john/)
- [Apache Vulnerabilities](https://httpd.apache.org/security/)
