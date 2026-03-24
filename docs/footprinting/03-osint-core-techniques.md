# 🧠 Lab 03: Core OSINT Techniques (Social, Whois, DNS)

## 🎯 Objective
Perform foundational OSINT techniques to gather information about a target using:
- Social media footprinting
- Whois lookup
- DNS enumeration

---

## 🧠 Concept
Before active scanning or exploitation, attackers gather intelligence using publicly available data.

These techniques help identify:
- People and potential social engineering targets
- Domain ownership and infrastructure details
- DNS configuration and exposed services

---

# 👤 1. Social Media Footprinting (Sherlock)

## ⚙️ Steps

  bash
python3 sherlock "Elon Musk"
📸 Screenshot + Explanation

🔗 View Image

Explanation:
Sherlock scans multiple platforms for username matches and shows how identities can be linked across services, enabling detailed profiling of a target.

🔎 Findings
Multiple social profiles discovered
Username reuse across platforms
Public exposure of identity
🛡️ Security Insight

Attackers use this to:

Build social engineering attacks
Identify high-value individuals
Correlate identities across platforms



# 🌍 2. Whois Footprinting
⚙️ Steps
Used DomainTools Whois lookup
Queried: certifiedhacker.com
📸 Screenshots + Explanations
Whois Lookup Page

🔗 View Image

Explanation:
The lookup interface allows querying domain registration data to retrieve ownership and infrastructure details.

Whois Summary

🔗 View Image

Explanation:
Provides a high-level overview including registrar, domain age, IP address, and hosting provider.

Full Whois Record

🔗 View Image

Explanation:
Contains detailed domain registration data such as name servers, registration dates, and administrative information.

🔎 Findings
Registrar: Network Solutions, LLC
Domain created: 2002
Name servers:
ns1.bluehost.com
ns2.bluehost.com
Domain privacy enabled
🛡️ Security Insight

Whois data reveals:

Infrastructure providers
Domain age and credibility
Potential ownership data

⚠️ Even with privacy enabled, valuable infrastructure information is still exposed.



# 🌐 3. DNS Footprinting
⚙️ Steps
Online Tool
Queried DNS records for certifiedhacker.com
Windows CLI
nslookup
set type=a
www.certifiedhacker.com
📸 Screenshots + Explanations
DNS Query Types

🔗 View Image

Explanation:
Shows available DNS record types such as A, MX, NS, and SOA, which define how a domain operates.

DNS A Record Result

🔗 View Image

Explanation:
Displays the IP address associated with the domain, revealing where the website is hosted.

Windows nslookup Output

🔗 View Image

Explanation:
Shows detailed DNS responses including A records, CNAME mappings, and name server information.

🔎 Findings
A Record:
certifiedhacker.com → 162.241.216.11
CNAME:
www → certifiedhacker.com
Name Servers:
ns1.bluehost.com
ns2.bluehost.com
🛡️ Security Insight

DNS data allows attackers to:

Map infrastructure
Identify services and dependencies
Discover potential attack targets

⚠️ DNS records act as a blueprint of the target environment.


# 🧾 Key Takeaways
OSINT provides intelligence without direct interaction
Social media expands the human attack surface
Whois reveals domain infrastructure
DNS exposes technical architecture


# 💼 Real-World Application

SOC Analyst

-Understand reconnaissance behavior
-Security Analyst
-Assess external exposure
-Help Desk / IT
-Understand DNS and domain dependencies
-Penetration Tester
-Use OSINT as the first phase of engagement
