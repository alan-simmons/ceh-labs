🧠 Lab 03: Core OSINT Techniques (Social, Whois, DNS)

## 🎯 Objective
Perform foundational OSINT techniques to gather information about a target using:
- Social media footprinting
- Whois lookup
- DNS enumeration

---

## 🧠 Concept

Before active scanning or exploitation, attackers gather intelligence using publicly available data.

These techniques allow you to identify:
- People (social engineering targets)
- Domain ownership and infrastructure
- DNS configuration and services

---

# 👤 1. Social Media Footprinting (Sherlock)

## ⚙️ Steps

 bash
python3 sherlock "Elon Musk"
📸 Screenshots
Sherlock Results

🔎 Findings
Multiple social profiles discovered across platforms
Username reuse across services
Publicly exposed personal and professional presence
🛡️ Security Insight

Attackers use this to:

Build social engineering profiles
Identify high-value individuals
Discover reused usernames and credentials




# 🌍 2. Whois Footprinting
⚙️ Steps
Navigated to DomainTools Whois Lookup
Queried: certifiedhacker.com
Reviewed both the summary page and detailed Whois record


# 📸 Screenshots
DomainTools Whois Lookup Page

Whois Summary

Detailed Whois Record

# 🔎 Findings
Registrar: Network Solutions, LLC
Domain created: 2002
Name servers:
ns1.bluehost.com
ns2.bluehost.com
IP address identified:
162.241.216.11
Domain privacy enabled through Perfect Privacy, LLC

# 🛡️ Security Insight

Whois data can reveal:

Ownership details (if privacy is not enabled)
Registrar and hosting relationships
Domain age and history
Name server infrastructure

⚠️ Even when privacy protection is enabled, Whois can still provide valuable infrastructure intelligence.

# 🌐 3. DNS Footprinting
⚙️ Steps
Online nslookup Tool
Opened an online nslookup interface
Queried certifiedhacker.com
Tested multiple record types:
A
CNAME
NS
SOA
MX
Windows CLI
nslookup
set type=a
www.certifiedhacker.com

Additional queries performed:

set type=cname
www.certifiedhacker.com

set type=soa
certifiedhacker.com

set type=a
ns1.bluehost.com


# 📸 Screenshots
DNS Query Type Selection

DNS A Record Result

Windows nslookup Output

# 🔎 Findings
A Record:
certifiedhacker.com → 162.241.216.11
CNAME:
www.certifiedhacker.com → certifiedhacker.com
Name Servers:
ns1.bluehost.com
ns2.bluehost.com
SOA Record revealed:
Primary name server
Responsible admin address
Serial number
Refresh / retry / expire values
Default TTL

# 🛡️ Security Insight

DNS data allows attackers to:

Map infrastructure
Identify mail servers and DNS providers
Understand how domains resolve
Discover additional systems for further enumeration

⚠️ DNS records often provide the technical blueprint of a target environment.

# 🧾 Key Takeaways
OSINT provides powerful intelligence without direct interaction
Social media expands attack surface through human targets
Whois reveals ownership and infrastructure relationships
DNS exposes technical architecture and service dependencies
