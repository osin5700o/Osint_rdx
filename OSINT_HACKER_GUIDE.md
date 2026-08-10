# 🕵️ The Complete OSINT Playbook: Dorking, Recon & Intel Gathering
## A Hacker's Guide to Information Warfare

> *"The best hackers aren't the ones who break in. They're the ones who were never supposed to be locked out in the first place."*

---

## 📋 Table of Contents
1. [Google Dorking Fundamentals](#google-dorking-fundamentals)
2. [Top 20 Advanced Google Dorks](#top-20-advanced-google-dorks)
3. [Passive Reconnaissance Techniques](#passive-reconnaissance-techniques)
4. [Active Reconnaissance Techniques](#active-reconnaissance-techniques)
5. [OSINT Fundamentals Every Pro Needs](#osint-fundamentals)
6. [Operational Security (OPSEC)](#operational-security)

---

## 🔍 Google Dorking Fundamentals

### What is Google Dorking?
Google dorking leverages advanced search operators to find sensitive information, misconfigurations, and data leaks hidden in plain sight. It's the art of speaking Google's language.

### Core Operators You MUST Know

| Operator | Syntax | Use Case |
|----------|--------|----------|
| `site:` | `site:example.com` | Restrict results to specific domain |
| `inurl:` | `inurl:admin` | Find pages with keyword in URL |
| `intitle:` | `intitle:admin panel` | Find pages with keyword in title |
| `intext:` | `intext:password` | Find keyword in page content |
| `filetype:` | `filetype:pdf` | Search for specific file types |
| `cache:` | `cache:example.com` | View Google's cached version |
| `link:` | `link:example.com` | Find pages linking to target |
| `related:` | `related:example.com` | Find similar websites |
| `"exact match"` | `"confidential"` | Search exact phrase |
| `OR / AND` | `password OR credentials` | Boolean operators |
| `-` | `-filetype:html` | Exclude results |
| `..` | `2015..2020` | Number range |

---

## 🎯 Top 20 Advanced Google Dorks

### 1. **Database Exposures**
```
inurl:phpmyadmin OR inurl:admin/db site:target.com
```
Finds exposed database management interfaces.

### 2. **Backup Files**
```
site:target.com (filetype:bak OR filetype:backup OR filetype:old OR filetype:sql)
```
Uncovers forgotten backup files with potential credentials.

### 3. **Configuration Files**
```
site:target.com (filetype:xml OR filetype:conf OR filetype:config)
```
Locates exposed configuration with sensitive settings.

### 4. **Git Repositories**
```
site:target.com/.git/config
```
Finds exposed `.git` directories leaking source code.

### 5. **Document Metadata**
```
site:target.com filetype:pdf intitle:"confidential"
```
Documents containing sensitive keywords in metadata.

### 6. **Directory Listings**
```
site:target.com "index of" ("backup" OR "admin" OR "uploads")
```
Apache directory listings exposing file structures.

### 7. **Error Messages**
```
site:target.com ("MySQL syntax" OR "SQL error" OR "Warning: mysql_fetch")
```
Database errors revealing structure and versions.

### 8. **Credentials in Files**
```
site:target.com filetype:txt ("username:" OR "password:" OR "api_key:")
```
Accidentally exposed credentials in text files.

### 9. **Sensitive Logs**
```
site:target.com (filetype:log OR filetype:logs) ("error" OR "failed" OR "warning")
```
Application and server logs with debugging info.

### 10. **API Endpoints**
```
site:target.com (inurl:api OR inurl:/v1/ OR inurl:/v2/) filetype:json
```
Exposed API documentation and endpoints.

### 11. **Jenkins CI/CD**
```
site:target.com:8080/jenkins OR inurl:jenkins intitle:"Dashboard"
```
Unprotected CI/CD pipelines with build artifacts.

### 12. **AWS S3 Buckets**
```
site:s3.amazonaws.com target.com
```
S3 buckets associated with target domain.

### 13. **Wordpress Admin**
```
site:target.com wp-admin OR site:target.com wp-login
```
Wordpress installations with login endpoints exposed.

### 14. **FTP Credentials**
```
"ftp://" "username:" "password:" site:target.com
```
FTP credentials hardcoded in pages.

### 15. **RSA Private Keys**
```
site:target.com "BEGIN RSA PRIVATE KEY"
```
Exposed SSH/SSL private keys (catastrophic).

### 16. **Google Maps API Keys**
```
site:target.com "AIza" OR "AIza[0-9A-Za-z\-_]{35}"
```
Exposed API keys for abuse and unauthorized usage.

### 17. **Slack Tokens**
```
site:github.com "xoxp-" OR "xoxb-" ("token" OR "slack")
```
Exposed Slack webhooks and bot tokens.

### 18. **Financial Data**
```
site:target.com (filetype:xls OR filetype:xlsx) ("bank" OR "account" OR "credit card")
```
Spreadsheets with financial information.

### 19. **User Information**
```
site:target.com (filetype:csv OR filetype:txt) ("email" OR "username" OR "phone")
```
Exposed contact lists and user databases.

### 20. **Vulnerable Gadgets**
```
site:target.com ("admin panel" OR "administrator" OR "root") intitle:("log in" OR "login")
```
Endpoints with weak authentication patterns.

---

## 🕵️ Passive Reconnaissance Techniques

### Definition
Gathering intelligence WITHOUT direct contact with target systems. No alerts, no traces.

### Key Passive Recon Techniques

#### 1. **WHOIS & Domain Enumeration**
```bash
whois target.com
nslookup target.com
dig target.com ANY
```
- Reveals registrar, admin contacts, nameservers
- Low risk, completely legal

#### 2. **DNS Reconnaissance**
```bash
# Subdomain discovery
assetfinder target.com
subfinder -d target.com -o subs.txt
crt.sh (certificate transparency logs)
```
- DNS records: A, MX, NS, TXT, SOA, CNAME
- Subdomain enumeration via certificates

#### 3. **Search Engine Caching**
```
cache:target.com
site:target.com cache
```
- Google, Bing cached versions
- Wayback Machine: archive.org snapshots
- Reveals historical changes

#### 4. **Social Media & HUMINT**
- LinkedIn profiles (employee enumeration)
- Twitter/X for tech stack hints
- GitHub profiles revealing code/projects
- Facebook for organizational structure

#### 5. **Public Code Repositories**
```bash
# Search GitHub for target mentions
site:github.com "target.com" OR "target-api"
```
- Exposed credentials in repos
- Project dependencies
- Internal tool references

#### 6. **Certificate Transparency Logs**
```bash
# crt.sh web interface or API
curl "https://crt.sh/?q=%.target.com&output=json"
```
- All issued SSL certificates
- Historical domain ownership
- Subdomain mapping

#### 7. **Shodan & Internet Scanning**
```
Shodan queries: "target.com" port:22,23,3389
```
- Connected devices and services
- Versions and banners
- Geolocation data

#### 8. **Job Postings**
- Indicates technologies in use
- Employee skill requirements
- Infrastructure hints
- Team structure

#### 9. **Public Records**
- Business registrations
- Patents filed
- Press releases
- Court documents

#### 10. **Metadata Analysis**
```bash
# Extract metadata from documents
exiftool document.pdf
strings binary_file
```
- Author names
- Software versions
- File paths
- Creation timestamps

---

## ⚡ Active Reconnaissance Techniques

### Definition
Direct interaction with target systems. Creates logs. More dangerous but comprehensive.

### Key Active Recon Techniques

#### 1. **Network Scanning**
```bash
# Port scanning
nmap -sV -p- target.com
masscan -p0-65535 target.com --rate=10000

# Service enumeration
nmap -A target.com
```
- Identifies open ports
- Service version detection
- OS fingerprinting

#### 2. **Web Application Scanning**
```bash
# Directory enumeration
gobuster dir -u https://target.com -w wordlist.txt
ffuf -u https://target.com/FUZZ -w wordlist.txt

# Screenshot taking
eyewitness -f targets.txt
wkhtmltoimage
```
- Hidden directories
- Visual reconnaissance
- Admin panels

#### 3. **DNS Zone Transfer**
```bash
nslookup
> server ns1.target.com
> ls -d target.com
```
- Attempts to grab full DNS records
- Often misconfigured
- Reveals infrastructure

#### 4. **Web Server Fingerprinting**
```bash
curl -I https://target.com
nikto -h target.com
```
- Server headers
- Version identification
- Common vulnerabilities

#### 5. **SSL/TLS Analysis**
```bash
nmap --script ssl-enum-ciphers -p 443 target.com
testssl.sh target.com
```
- Certificate info
- Cipher strengths
- Protocol versions
- Vulnerabilities

#### 6. **Application Fuzzing**
```bash
wfuzz -z file,payload.txt https://target.com/FUZZ
```
- Input validation testing
- Error responses
- Logic flaws

#### 7. **API Enumeration**
```bash
# Swagger/OpenAPI discovery
curl https://target.com/swagger.json
curl https://target.com/api-docs
```
- Endpoint mapping
- Parameters
- Authentication requirements

#### 8. **Technology Stack Detection**
```bash
wappalyzer target.com
builtwith.com (web interface)
```
- Frontend frameworks
- Backend technologies
- CMS platforms
- Analytics tools

#### 9. **Social Engineering Recon**
```bash
# Email format discovery
hunter.io API
clearbit.com API
```
- Employee email formats
- Phone number patterns
- Office locations

#### 10. **Routing & BGP Analysis**
```bash
# Identify ISPs and infrastructure
traceroute target.com
AS number lookup
```
- Network topology
- ISP information
- Geographic routing

---

## 🧠 OSINT Fundamentals Every Professional Should Know

### 1. **The OODA Loop**
```
Observe → Orient → Decide → Act
↑__________________________|
```
- Continuous cycle
- Faster loops = advantage
- Apply to recon phases

### 2. **Information Classification**

| Level | Type | Risk |
|-------|------|------|
| **White** | Public knowledge | None |
| **Gray** | Partially obscured info | Medium |
| **Black** | Hidden/illegal to access | Critical |

**Stay in White/Gray zones. Never cross into Black.**

### 3. **Chain of Custody**
- Document all sources
- Screenshot timestamps
- Archive original pages
- Maintain integrity
- Admissible in court if needed

### 4. **Source Validation**
```
Credibility Check:
├─ Primary Source? (direct)
├─ Corroborating sources (3+)
├─ Historical accuracy
├─ Author expertise
└─ Absence of bias
```

### 5. **Threat Intelligence Lifecycle**

```
Planning → Collection → Analysis → Dissemination → Feedback
↑___________________________________________________________|
```

### 6. **OPSEC Mindset**
- Assume you're being monitored
- Compartmentalize information
- Use VPNs, proxies, Tor
- Rotate identities
- Leave no digital footprint

### 7. **The Intelligence Pyramid**

```
         ▲
        /|\
       / | \
      /  |  \
     / VERIFIED \
    /     |      \
   / MULTIPLE    \
  /    SOURCES    \
 /__________|_______\
/  SINGLE SOURCES   \
```

### 8. **Data Correlation Techniques**
- Cross-reference across platforms
- Timeline analysis
- Relationship mapping
- Geolocation verification
- Pattern recognition

### 9. **Tool Ecosystem Know-How**
```
Dorking Tools:
├─ Google Advanced Search
├─ Google Alerts
├─ Bing Advanced
└─ DuckDuckGo

Passive Recon:
├─ Shodan
├─ Censys
├─ ZoomEye
├─ Fofa
└─ SecurityTrails

DNS & Subdomain:
├─ DNSDumpster
├─ Sublist3r
├─ Amass
├─ Knockpy
└─ Subfinder

Metadata:
├─ ExifTool
├─ Strings
├─ Binwalk
└─ Volatility

Visualization:
├─ Maltego
├─ SpiderFoot
├─ Shodan Maps
└─ Karto
```

### 10. **Legal & Ethical Framework**
```
✅ LEGAL                          ❌ ILLEGAL
├─ Public information            ├─ Unauthorized access
├─ Search engines                ├─ Hacking systems
├─ WHOIS lookups                 ├─ Eavesdropping
├─ DNS queries                   ├─ Social engineering
├─ Port scanning (authorized)    ├─ Spoofing
├─ Certificate analysis          ├─ Impersonation
└─ Public documents              └─ Privacy violations
```

### 11. **Target Profiling Template**
```markdown
## Target: [Organization]

### Basic Info
- Domain: 
- Founded: 
- Employees: 
- Industry: 

### Technology Stack
- Web Framework: 
- CMS: 
- Server: 
- Database: 

### Digital Footprint
- Subdomains: 
- IP Ranges: 
- Public Repositories: 
- Social Media: 

### Potential Vectors
- Weak points identified: 
- Technologies with known CVEs: 

### Intelligence Priority
- High: 
- Medium: 
- Low: 
```

### 12. **Reconnaissance Workflow**
```
1. Scoping
   ├─ Define target
   ├─ Set boundaries
   └─ Document rules of engagement

2. Information Gathering
   ├─ Passive sources
   ├─ Search engines
   ├─ Public databases
   └─ Social media

3. Analysis
   ├─ Correlation
   ├─ Timeline building
   ├─ Relationship mapping
   └─ Threat assessment

4. Reporting
   ├─ Evidence documentation
   ├─ Visualization
   ├─ Recommendations
   └─ Archive for future reference
```

---

## 🛡️ Operational Security (OPSEC)

### Critical Rules

#### Rule 1: Never Use Your Real Identity
```bash
# ❌ BAD
Email: yourname@gmail.com
Username: john_smith_123

# ✅ GOOD
Email: [random]@protonmail.com
Username: [random UUID]
VPN: Active
Tor: Ready
```

#### Rule 2: Compartmentalize Data
```
Investigation A ─┐
                 ├─→ Separate VPN
Investigation B ─┤   Separate Browser
                 └─→ Separate Identity
Investigation C
```

#### Rule 3: Use Proxying Layers
```
You → Tor → VPN → Proxy → Target
```

#### Rule 4: Assume Attribution
Every query leaves a trace. Assume it will be found.

#### Rule 5: Operational Discipline
- No sleep-talk about investigations
- No casual mentions in logs
- No metadata in reports
- Clean your digital trail regularly

### OPSEC Checklist
```
□ VPN/Tor active
□ Browser in private mode
□ JavaScript disabled
□ Tracking blockers enabled
□ No extensions tracking behavior
□ Separate OS/VM for sensitive work
□ Time offset on system clock
□ MAC address spoofed (if applicable)
□ No correlation between identities
□ Logging/history cleared after session
```

---

## 🎓 Quick Reference Cheat Sheet

### Dork Combinations
```bash
# Exposed Files
site:target.com (filetype:doc OR filetype:pdf OR filetype:xls) ("confidential" OR "secret" OR "internal")

# Admin Access
site:target.com (inurl:admin OR inurl:administrator OR inurl:cpanel) intitle:"login"

# Database Leaks
site:target.com (inurl:phpmyadmin OR inurl:mysql OR inurl:adminer)

# Code Exposure
site:target.com (filetype:php OR filetype:asp OR filetype:jsp) (error OR warning OR debug)

# Keys & Tokens
site:target.com ("BEGIN RSA" OR "api_key" OR "password" OR "secret")
```

### Passive Tools One-Liners
```bash
# Subdomain enumeration
assetfinder --subs-only target.com | sort -u

# Certificate transparency
curl "https://crt.sh/?q=%.target.com&output=json" | jq -r '.[].name_value' | sort -u

# DNS bruteforce
gobuster dns -d target.com -w wordlist.txt

# Whois & DNS
whois target.com && dig target.com ANY
```

### Active Scan Sequence
```bash
# 1. Port sweep
nmap -p- --min-rate=5000 target.com

# 2. Service enumeration
nmap -sV -p[open ports] target.com

# 3. Web enumeration
ffuf -u https://target.com/FUZZ -w /usr/share/wordlists/dirbuster/directory-list.txt

# 4. Certificate analysis
echo | openssl s_client -connect target.com:443
```

---

## 🔗 Essential Resources

### Platforms
- **Shodan**: Powered device search
- **Censys**: Internet scanning
- **VirusTotal**: File/URL analysis
- **AbuseIPDB**: IP reputation
- **SecurityTrails**: Domain intelligence
- **Hunter.io**: Email finding
- **Epieos**: Email OSINT
- **Breach Database**: Have I Been Pwned

### Reference Databases
- **CVE Database**: vulnerability.org
- **Exploit DB**: exploitdb.com
- **GitHub Dorks**: List of notorious leaks
- **Shodan Dorks**: Community queries

### Communities
- **OSINT Framework**: osintframework.com
- **IHBWiki**: Intelligence online resources
- **OSINT Curious**: Twitter/X community
- **r/OSINT**: Reddit intelligence community

---

## ⚠️ Final Warnings

> **This knowledge is powerful. With power comes responsibility.**

1. **Legal Boundaries**: Know what's legal in your jurisdiction
2. **Ethical Usage**: Report vulnerabilities responsibly
3. **Attribution Risk**: Assume you can be traced
4. **Consequences**: Jail time is real for unauthorized access
5. **Disclosure Timing**: Responsible disclosure = protection

---

## 📝 Remember

```
The greatest intelligence operatives are invisible.
They gather. They analyze. They fade.
No noise. No traces. No victims.
Just information.
```

**Stay curious. Stay safe. Stay ethical.**

---

*Last Updated: 2026*
*Status: For Educational Purposes Only*
*Classification: Public - White Information*
