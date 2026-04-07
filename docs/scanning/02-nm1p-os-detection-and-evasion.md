# 🧠 Lab 02: Nmap OS Detection & Firewall Evasion

---

## 📸 Aggressive Scan Results

![Aggressive Scan](../screenshots/scanning/02-aggressive-scan.png)

**Explanation:**  
The `-A` flag enables:
- OS detection
- Version detection
- Script scanning
- Traceroute

---

## 📸 Service + OS Details

![Service OS](../screenshots/scanning/02-service-os.png)

**Explanation:**  
Reveals detailed service information including:
- IIS web server
- Kerberos
- LDAP
- SMB

👉 Strong indicator of a **Windows Server environment**

---

## 📸 NSE Script (SMB OS Discovery)

![SMB OS](../screenshots/scanning/02-smb-os.png)

**Explanation:**  
Using NSE scripts, Nmap identified:
- Windows Server 2022
- Domain name: CEH.com
- Hostname: Server2022

---

## 🔎 Findings

- Target OS: **Windows Server 2022**
- Domain detected
- Multiple enterprise services exposed

---

# 🛡️ 2. Firewall / IDS Evasion Techniques

---

## ⚙️ Techniques Used

### Packet Fragmentation

nmap -f 10.10.1.11


### Decoy Scan

nmap -D RND:10 10.10.1.11


### MTU Manipulation

nmap --mtu 8 10.10.1.11


### Source Port Manipulation

nmap -g 80 10.10.1.11


---

## 📸 Fragmented Scan

![Fragmented](../screenshots/scanning/02-fragmented.png)

**Explanation:**  
Breaks packets into smaller fragments to bypass firewall inspection.

---

## 📸 Decoy Scan

![Decoy](../screenshots/scanning/02-decoy.png)

**Explanation:**  
Generates multiple fake IP addresses to hide the real attacker.

---

## 📸 MTU Scan

![MTU](../screenshots/scanning/02-mtu.png)

**Explanation:**  
Adjusts packet size to evade detection systems.

---

## 📸 Source Port Manipulation

![Source Port](../screenshots/scanning/02-source-port.png)

**Explanation:**  
Uses trusted ports (like 80) to bypass firewall rules.

---

## 📸 Packet Capture (Wireshark Evidence)

![Wireshark](../screenshots/scanning/02-wireshark.png)

**Explanation:**  
Shows fragmented and manipulated packets being sent across the network.

---

## 📸 Firewall State

![Firewall](../screenshots/scanning/02-firewall.png)

**Explanation:**  
Demonstrates how firewall configurations impact scan results.

---

## 🔎 Findings

- Evasion techniques still revealed open ports
- Firewalls filtered most traffic
- Some scans bypassed restrictions

---

## 🛡️ Security Insight

Attackers use these techniques to:

- Avoid detection by IDS/IPS
- Bypass firewall rules
- Obfuscate scanning behavior

⚠️ Traditional defenses may not detect advanced scans.

---

## 🧾 Key Takeaways

- OS detection reveals valuable target information
- NSE scripts provide deep insights into systems
- Evasion techniques can bypass weak defenses
- Packet manipulation changes how scans are detected

---

## 💼 Real-World Application

**SOC Analyst**
- Detects abnormal scan patterns

**Security Analyst**
- Identifies exposed services and OS fingerprints

**Penetration Tester**
- Uses evasion techniques to avoid detection

**IT / Help Desk**
- Understands how firewall rules impact connectivity

---

## 🚀 Final Insight

> The more stealthy the scan, the harder it is to detect.

Understanding evasion techniques is critical for building strong defenses.
