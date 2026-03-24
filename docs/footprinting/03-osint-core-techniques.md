# 🧠 Lab 03: Core OSINT Techniques (Social, Whois, DNS)

## 🎯 Objective
Perform foundational OSINT techniques to gather information about a target using:
- Social media footprinting
- Whois lookup
- DNS enumeration

---

# 👤 1. Social Media Footprinting (Sherlock)

## ⚙️ Steps
python3 sherlock "Elon Musk"
📸 Screenshot + Explanation

🔗 Open Image

Explanation:
Sherlock identifies usernames across multiple platforms, helping correlate identities and build a profile of a target.

## 🌍 2. Whois Footprinting
📸 Screenshots + Explanations
Whois Lookup

🔗 Open Image

Explanation:
Used to retrieve domain registration and infrastructure details.

Whois Summary

🔗 Open Image

Explanation:
Shows registrar, domain age, and hosting-related data.

Whois Full Record

🔗 Open Image

Explanation:
Detailed domain data including name servers and registration info.

## 🌐 3. DNS Footprinting
📸 Screenshots + Explanations
DNS Record Types

🔗 Open Image

Explanation:
Displays available DNS record types such as A, MX, NS, and SOA.

DNS A Record

🔗 Open Image

Explanation:
Maps the domain to its IP address.

nslookup Output

🔗 Open Image

Explanation:
Shows DNS resolution results including IP and name servers.

🛡️ Security Insight

These techniques allow attackers to:

Map infrastructure
Identify services
Build attack paths without touching the system
