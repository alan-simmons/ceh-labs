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
📸 Screenshot

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
Used DomainTools / Whois lookup
Queried: certifiedhacker.com
📸 Screenshots
Whois Summary

Detailed Whois Record

🔎 Findings
Registrar: Network Solutions, LLC
Domain created: 2002
Name servers:
ns1.bluehost.com
ns2.bluehost.com
Hosting provider identified
Domain privacy enabled (Perfect Privacy, LLC)

🛡️ Security Insight

Whois data can reveal:

Ownership details (if privacy not enabled)
Infrastructure providers
Domain age and credibility

⚠️ Older domains often indicate established infrastructure

# 🌐 3. DNS Footprinting
⚙️ Steps
Linux / Online Tool
Queried DNS records using nslookup
Windows CLI
nslookup
set type=a
certifiedhacker.com

Additional queries:

set type=cname
set type=soa
set type=ns
📸 Screenshots
DNS Query Interface

DNS A Record Result

Windows nslookup Output

🔎 Findings
A Record:
162.241.216.11
Name Servers:
ns1.bluehost.com
ns2.bluehost.com
CNAME:
www → certifiedhacker.com
SOA Record:
Shows DNS authority and admin email

# 🛡️ Security Insight

DNS data allows attackers to:

Map infrastructure
Identify mail servers and services
Discover additional subdomains
Target specific systems for further enumeration


# 🧾 Key Takeaways
OSINT provides powerful intelligence without direct interaction
Social media expands attack surface through human targets
Whois reveals ownership and infrastructure
DNS exposes technical architecture of systems
