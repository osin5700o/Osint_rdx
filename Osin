# Complete OSINT Guide: Core Basics + 100 Advanced Techniques + 100 Passive Recon + 100 Active Recon

## **SECTION 1: OSINT FUNDAMENTALS**

---

## **What is OSINT?**

**OSINT (Open Source Intelligence)** is gathering intelligence from **publicly available sources**. These are sources legally accessible to anyone:

- Websites (news, social media, blogs)
- Public records (government databases, registries)
- Forums and message boards
- Images and videos
- Published research and reports

---

## **PCPAD Methodology**

PCPAD is the foundational 5-step framework for OSINT investigations:

| Step | What It Means |
|------|--------------|
| **P - Preparation** | Define what you're looking for and your limits |
| **C - Collection** | Gather data from sources |
| **P - Processing** | Organize and clean the data |
| **A - Analysis** | Find patterns and meaning in the data |
| **D - Dissemination** | Share your findings |

---

## **Passive Reconnaissance (Stealth Gathering)**

**Definition:** Collect information WITHOUT directly contacting the target. They won't know you're looking.

**How it works:**
- No interaction with the target
- Low risk of being detected
- Data may not be current

**Basic Examples:**
- Google searching public profiles
- Looking up WHOIS information on domains
- Checking DNS records via third-party websites
- Reading news articles about a person/company
- Browsing someone's public social media

**Why it matters:** You gather info without alerting anyone.

---

## **Active Reconnaissance (Direct Probing)**

**Definition:** Directly interact with the target. They may know you're investigating.

**How it works:**
- Direct contact with the target
- High risk of being detected
- Data is current and real

**Basic Examples:**
- Scanning a website with tools like Nmap
- Searching Shodan to find devices
- Sending emails to see responses
- Probing web applications for information
- Directly querying target systems

**Why it matters:** You get fresh, specific information but risk alerting the target.

---

## **The Core Difference**

| Aspect | Passive | Active |
|--------|---------|--------|
| **Contact** | None | Direct |
| **Detection Risk** | Low | High |
| **Data Type** | Public/Archived | Real-time |
| **Example** | Reading a blog post | Scanning a server |

---

## **Most Basic OSINT Workflow**

1. **Start with Passive** → Search public info (Google, social media, WHOIS)
2. **Analyze What You Find** → Look for patterns and connections
3. **Go Deeper with Passive** → Check archives, old pages, leaked databases
4. **Only Then Go Active** → If needed, directly probe the target
5. **Compile Results** → Document everything you found

---

## **Core OSINT Techniques (The Essentials)**

### **Search Engines**
- Use Google with special commands (site:, filetype:, intitle:)
- Bing, DuckDuckGo also have advanced search

### **Social Media**
- Look at public profiles on Facebook, Twitter, Instagram
- Find email addresses and phone numbers
- Track connections between people

### **Public Records**
- WHOIS lookups (who owns a domain)
- DNS records (what servers run a domain)
- Government records, business registrations

### **Images & Metadata**
- Reverse image search (TinEye, Google Images)
- Extract EXIF data (location, camera info from photos)
- Geolocation from photos

### **People Searches**
- Email lookup (Hunter.io)
- Username searches (KnowEm, Namechk)
- Phone number lookup
- Data breach searches (HaveIBeenPwned)

### **Domain & Website Info**
- WHOIS history
- DNS records
- Website change tracking
- SSL certificate info

---

## **Most Basic Tools**

These are the **core tools** every OSINT person should know:

1. **Google** - Search engine mastery
2. **WHOIS lookup sites** - Find domain owners
3. **Wayback Machine** - See old versions of websites
4. **Hunter.io** - Find email addresses
5. **Maltego** - Map relationships between data
6. **Shodan** - Search internet-connected devices
7. **TheHarvester** - Gather emails and subdomains
8. **TinEye** - Reverse image search
9. **HaveIBeenPwned** - Check leaked passwords
10. **Spiderfoot** - Automated reconnaissance

---

## **The Golden Rule of OSINT**

✅ **Start Passive, Stay Legal, Document Everything**

- Gather as much as possible without contacting the target
- Only use publicly available information
- Keep records of what you found and where from
- Respect privacy laws and regulations

---

## **Why OSINT Matters**

- **Security Teams** use it to find vulnerabilities before attackers
- **Journalists** use it to verify stories
- **Law Enforcement** uses it to investigate crimes
- **Businesses** use it for competitive intelligence
- **Individuals** use it for personal security

---

**The absolute core:** OSINT is finding public information efficiently, organizing it, understanding what it means, and sharing those insights—without breaking laws or alerting the target.

---

---

# SECTION 2: 100+ ADVANCED OSINT TECHNIQUES & METHODS

---

## **1. Search Engine Mastery (7 techniques)**

1. Advanced Google Dorking (site:, intitle:, filetype:, inurl:, etc.)
2. Bing Advanced Search operators
3. Yandex Reverse Search
4. DuckDuckGo search modifiers
5. Dark web search engines (Ahmia via TOR)
6. Metadata extraction via search (filetype:pdf site:gov)
7. Cached content exploration (Wayback Machine, Google cache)
8. # Google Dorking Commands - Complete Reference Guide

**⚠️ DISCLAIMER:** These commands are for educational purposes only. Only use these techniques for authorized security testing, legitimate research, or bug bounty programs. Unauthorized access to systems or data is illegal.

---

## Table of Contents

1. [Core Search Operators (1-20)](#core-search-operators-1-20)
2. [URL & Directory Dorks (21-40)](#url--directory-dorks-21-40)
3. [File Type Dorks (41-60)](#file-type-dorks-41-60)
4. [Sensitive Data Dorks (61-80)](#sensitive-data-dorks-61-80)
5. [Logical Operators & Modifiers (81-100)](#logical-operators--modifiers-81-100)
6. [Advanced File Discovery (101-120)](#advanced-file-discovery-101-120)
7. [Environment & Configuration Files (121-140)](#environment--configuration-files-121-140)
8. [Cloud & API Keys (141-160)](#cloud--api-keys-141-160)
9. [Database Exposure (161-180)](#database-exposure-161-180)
10. [Vulnerability & Security Testing (181-200)](#vulnerability--security-testing-181-200)
11. [Specific Technologies (201-220)](#specific-technologies-201-220)
12. [Credentials & Secrets (221-240)](#credentials--secrets-221-240)
13. [Personal & Contact Information (241-260)](#personal--contact-information-241-260)
14. [Medical & Legal (261-280)](#medical--legal-261-280)
15. [Financial & Banking (281-300)](#financial--banking-281-300)

---

## Core Search Operators (1-20)

| # | Command | Description | Example |
|---|---------|-------------|---------|
| 1 | `site:` | Search within a specific website or domain | `site:example.com` |
| 2 | `inurl:` | Find pages with a specific term in the URL | `inurl:admin` |
| 3 | `intitle:` | Find pages with keywords in the title | `intitle:"index of"` |
| 4 | `filetype:` | Search for specific file types/extensions | `filetype:pdf` |
| 5 | `ext:` | Search by file extension (alternative to filetype) | `ext:pdf` |
| 6 | `intext:` | Search for keywords within page text/body | `intext:"password"` |
| 7 | `link:` | Find pages that link to a specific URL | `link:example.com` |
| 8 | `cache:` | Show cached version of a page | `cache:example.com` |
| 9 | `allinurl:` | All search terms must be in the URL | `allinurl:admin login` |
| 10 | `allintitle:` | All search terms must be in the page title | `allintitle:login admin` |
| 11 | `allintext:` | All search terms must be in the text | `allintext:username password` |
| 12 | `related:` | Find websites similar to a given URL | `related:example.com` |
| 13 | `info:` | Get information about a specific URL | `info:example.com` |
| 14 | `define:` | Get definitions of words | `define:security` |
| 15 | `stocks:` | Search stock information | `stocks:AAPL` |
| 16 | `weather:` | Check weather information | `weather:london` |
| 17 | `movie:` | Search for movie information | `movie:inception` |
| 18 | `map:` | Search for maps | `map:paris` |
| 19 | `book:` | Search for books | `book:1984` |
| 20 | `scholar:` | Search academic papers | `scholar:machine learning` |

---

## URL & Directory Dorks (21-40)

| # | Command | Description | Example |
|---|---------|-------------|---------|
| 21 | `intitle:"index of"` | Find directory listings | `intitle:"index of"` |
| 22 | `intitle:"index of" parent directory` | Open directories with parent access | `intitle:"index of" parent directory` |
| 23 | `inurl:/admin/` | Find admin panels | `inurl:/admin/` |
| 24 | `inurl:config` | Locate configuration files | `inurl:config` |
| 25 | `inurl:backup` | Find backup files | `inurl:backup` |
| 26 | `inurl:.git` | Expose Git repositories | `inurl:.git` |
| 27 | `inurl:uploads` | Find upload directories | `inurl:uploads` |
| 28 | `inurl:private` | Locate private directories | `inurl:private` |
| 29 | `inurl:sensitive` | Find sensitive files | `inurl:sensitive` |
| 30 | `inurl:confidential` | Locate confidential documents | `inurl:confidential` |
| 31 | `inurl:secret` | Find secret files | `inurl:secret` |
| 32 | `inurl:wp-admin` | Find WordPress admin panels | `inurl:wp-admin` |
| 33 | `inurl:phpmyadmin` | Locate phpMyAdmin installations | `inurl:phpmyadmin` |
| 34 | `inurl:cpanel` | Find cPanel login pages | `inurl:cpanel` |
| 35 | `inurl:plesk` | Locate Plesk panels | `inurl:plesk` |
| 36 | `inurl:webmail` | Find webmail interfaces | `inurl:webmail` |
| 37 | `inurl:control` | Find control panels | `inurl:control` |
| 38 | `inurl:user` | Find user directories | `inurl:user` |
| 39 | `inurl:administrator` | Locate administrator pages | `inurl:administrator` |
| 40 | `inurl:password` | Find pages with passwords in URL | `inurl:password` |

---

## File Type Dorks (41-60)

| # | Command | Description | Example |
|---|---------|-------------|---------|
| 41 | `filetype:pdf` | Find PDF files | `filetype:pdf` |
| 42 | `filetype:doc` | Find Word documents | `filetype:doc` |
| 43 | `filetype:docx` | Find modern Word documents | `filetype:docx` |
| 44 | `filetype:xls` | Find Excel spreadsheets | `filetype:xls` |
| 45 | `filetype:xlsx` | Find modern Excel files | `filetype:xlsx` |
| 46 | `filetype:ppt` | Find PowerPoint presentations | `filetype:ppt` |
| 47 | `filetype:sql` | Find SQL database files | `filetype:sql` |
| 48 | `filetype:xml` | Find XML configuration files | `filetype:xml` |
| 49 | `filetype:conf` | Find configuration files | `filetype:conf` |
| 50 | `filetype:ini` | Find INI settings files | `filetype:ini` |
| 51 | `filetype:cfg` | Find config files | `filetype:cfg` |
| 52 | `filetype:log` | Find log files | `filetype:log` |
| 53 | `filetype:txt` | Find text files | `filetype:txt` |
| 54 | `filetype:bak` | Find backup files | `filetype:bak` |
| 55 | `filetype:tar` | Find tar archives | `filetype:tar` |
| 56 | `filetype:gz` | Find compressed files | `filetype:gz` |
| 57 | `filetype:zip` | Find ZIP archives | `filetype:zip` |
| 58 | `filetype:7z` | Find 7-Zip archives | `filetype:7z` |
| 59 | `filetype:rar` | Find RAR archives | `filetype:rar` |
| 60 | `filetype:iso` | Find ISO images | `filetype:iso` |

---

## Sensitive Data Dorks (61-80)

| # | Command | Description | Example |
|---|---------|-------------|---------|
| 61 | `intext:"password"` | Find exposed passwords | `intext:"password"` |
| 62 | `intext:"username"` | Find exposed usernames | `intext:"username"` |
| 63 | `intext:"api_key"` | Find exposed API keys | `intext:"api_key"` |
| 64 | `intext:"secret"` | Find secrets in text | `intext:"secret"` |
| 65 | `intext:"token"` | Find authentication tokens | `intext:"token"` |
| 66 | `intext:"credentials"` | Find login credentials | `intext:"credentials"` |
| 67 | `intext:"email"` | Find email addresses | `intext:"email"` |
| 68 | `intext:"phone"` | Find phone numbers | `intext:"phone"` |
| 69 | `intext:"ssn"` | Find social security numbers | `intext:"ssn"` |
| 70 | `intext:"credit card"` | Find credit card information | `intext:"credit card"` |
| 71 | `intext:"confidential"` | Find confidential documents | `intext:"confidential"` |
| 72 | `intext:"private"` | Find private information | `intext:"private"` |
| 73 | `intext:"database"` | Find database references | `intext:"database"` |
| 74 | `intitle:"password"` | Pages with passwords in title | `intitle:"password"` |
| 75 | `intitle:"login"` | Find login pages | `intitle:"login"` |
| 76 | `intitle:"admin"` | Find admin pages | `intitle:"admin"` |
| 77 | `"Index of /" database` | Find exposed databases | `"Index of /" database` |
| 78 | `"Index of /" database.sql` | Find SQL database dumps | `"Index of /" database.sql` |
| 79 | `intext:"database.sql"` | Find SQL dumps in text | `intext:"database.sql"` |
| 80 | `intext:"mysql_dump"` | Find MySQL dumps | `intext:"mysql_dump"` |

---

## Logical Operators & Modifiers (81-100)

| # | Command | Description | Example |
|---|---------|-------------|---------|
| 81 | `-` (Minus) | Exclude results with specific terms | `filetype:log -github.com` |
| 82 | `OR` | Search for either term | `inurl:admin OR inurl:login` |
| 83 | `\|` (Pipe) | Alternative to OR operator | `inurl:admin \| inurl:login` |
| 84 | `AND` | Include all search terms | `inurl:admin AND intext:password` |
| 85 | `+` (Plus) | Force inclusion of a term | `+password +username` |
| 86 | `""` (Quotes) | Search for exact phrases | `"confidential document"` |
| 87 | `*` (Asterisk) | Wildcard for any word | `"index of" *.db` |
| 88 | `..` (Range) | Search within a numeric range | `2020..2025` |
| 89 | `$` (Dollar sign) | Price searches | `$100..$500` |
| 90 | `@` (At symbol) | Social media/email searches | `@twitter` |
| 91 | `#` (Hashtag) | Find hashtags | `#security` |
| 92 | `()` (Parentheses) | Group search terms | `(admin OR administrator)` |
| 93 | `?` (Question mark) | Single character wildcard | `file?.txt` |
| 94 | `AROUND()` | Find terms near each other | `password AROUND(2) username` |
| 95 | `~` (Tilde) | Find synonyms | `~security` |
| 96 | `//` (Double slash) | Alternative site search | `//example.com` |
| 97 | `intitle:index.of` | Find directory indexes (variation) | `intitle:index.of` |
| 98 | `inurl:upload filetype:php` | Find PHP upload forms | `inurl:upload filetype:php` |
| 99 | `site:example.com inurl:admin` | Find admin on specific site | `site:example.com inurl:admin` |
| 100 | `filetype:pdf site:example.com` | Find PDFs on specific site | `filetype:pdf site:example.com` |

---

## Advanced File Discovery (101-120)

| # | Command | Description | Example |
|---|---------|-------------|---------|
| 101 | `intitle:"index of" parent directory` | Find open directories with parent access | `intitle:"index of" parent directory` |
| 102 | `intitle:"index of" "backup"` | Find backup directory listings | `intitle:"index of" "backup"` |
| 103 | `intitle:"index of" "database"` | Find database directory listings | `intitle:"index of" "database"` |
| 104 | `intitle:"index of" ".git"` | Expose Git repositories | `intitle:"index of" ".git"` |
| 105 | `intitle:"index of" ".svn"` | Expose Subversion repositories | `intitle:"index of" ".svn"` |
| 106 | `intitle:"index of" ".env"` | Find environment files | `intitle:"index of" ".env"` |
| 107 | `intitle:"index of" ".htaccess"` | Find Apache configuration files | `intitle:"index of" ".htaccess"` |
| 108 | `intitle:"index of" ".passwd"` | Find password files | `intitle:"index of" ".passwd"` |
| 109 | `intitle:"index of" ".mysql"` | Find MySQL configuration files | `intitle:"index of" ".mysql"` |
| 110 | `intitle:"index of" "web.config"` | Find IIS configuration files | `intitle:"index of" "web.config"` |
| 111 | `intitle:"index of" "config.php"` | Find PHP config files | `intitle:"index of" "config.php"` |
| 112 | `intitle:"index of" "settings.py"` | Find Django settings files | `intitle:"index of" "settings.py"` |
| 113 | `intitle:"index of" "application.yml"` | Find YAML config files | `intitle:"index of" "application.yml"` |
| 114 | `intitle:"index of" "secrets.json"` | Find secrets files | `intitle:"index of" "secrets.json"` |
| 115 | `intitle:"index of" "credentials.txt"` | Find credentials files | `intitle:"index of" "credentials.txt"` |
| 116 | `intitle:"index of" "private_key"` | Find private key files | `intitle:"index of" "private_key"` |
| 117 | `intitle:"index of" "ssh"` | Find SSH directories | `intitle:"index of" "ssh"` |
| 118 | `intitle:"index of" "certificates"` | Find certificate directories | `intitle:"index of" "certificates"` |
| 119 | `intitle:"index of" "keys"` | Find encryption key directories | `intitle:"index of" "keys"` |
| 120 | `intitle:"index of" "uploads"` | Find upload directories | `intitle:"index of" "uploads"` |

---

## Environment & Configuration Files (121-140)

| # | Command | Description | Example |
|---|---------|-------------|---------|
| 121 | `inurl:.env -github` | Find environment files outside GitHub | `inurl:.env -github` |
| 122 | `inurl:.env.local` | Find local environment files | `inurl:.env.local` |
| 123 | `inurl:.env.example` | Find example environment files | `inurl:.env.example` |
| 124 | `inurl:wp-config.php -github` | Find WordPress config files | `inurl:wp-config.php -github` |
| 125 | `inurl:config.php -github` | Find PHP config files | `inurl:config.php -github` |
| 126 | `inurl:database.yml` | Find database configuration files | `inurl:database.yml` |
| 127 | `inurl:secrets.yml` | Find secrets configuration files | `inurl:secrets.yml` |
| 128 | `inurl:settings.ini` | Find INI configuration files | `inurl:settings.ini` |
| 129 | `inurl:application.properties` | Find Java application properties | `inurl:application.properties` |
| 130 | `inurl:appsettings.json` | Find .NET app settings | `inurl:appsettings.json` |
| 131 | `inurl:web.xml` | Find web application configuration | `inurl:web.xml` |
| 132 | `inurl:pom.xml` | Find Maven project files | `inurl:pom.xml` |
| 133 | `inurl:build.gradle` | Find Gradle build files | `inurl:build.gradle` |
| 134 | `inurl:package.json` | Find Node.js package files | `inurl:package.json` |
| 135 | `inurl:requirements.txt` | Find Python requirements files | `inurl:requirements.txt` |
| 136 | `inurl:Gemfile` | Find Ruby Gemfile | `inurl:Gemfile` |
| 137 | `inurl:docker-compose.yml` | Find Docker compose files | `inurl:docker-compose.yml` |
| 138 | `inurl:dockerfile` | Find Dockerfile | `inurl:dockerfile` |
| 139 | `inurl:kubernetes.yml` | Find Kubernetes config files | `inurl:kubernetes.yml` |
| 140 | `inurl:terraform.tf` | Find Terraform files | `inurl:terraform.tf` |

---

## Cloud & API Keys (141-160)

| # | Command | Description | Example |
|---|---------|-------------|---------|
| 141 | `intext:"AKIA"` | Find AWS access keys | `intext:"AKIA"` |
| 142 | `intext:"aws_secret_access_key"` | Find AWS secret keys | `intext:"aws_secret_access_key"` |
| 143 | `intext:"api.github.com"` | Find GitHub API references | `intext:"api.github.com"` |
| 144 | `intext:"github_token"` | Find GitHub tokens | `intext:"github_token"` |
| 145 | `intext:"github_secret"` | Find GitHub secrets | `intext:"github_secret"` |
| 146 | `intext:"stripe_api_key"` | Find Stripe API keys | `intext:"stripe_api_key"` |
| 147 | `intext:"stripe_secret"` | Find Stripe secrets | `intext:"stripe_secret"` |
| 148 | `intext:"slack_token"` | Find Slack tokens | `intext:"slack_token"` |
| 149 | `intext:"slack_webhook"` | Find Slack webhooks | `intext:"slack_webhook"` |
| 150 | `intext:"twilio_api_key"` | Find Twilio API keys | `intext:"twilio_api_key"` |
| 151 | `intext:"sendgrid_api_key"` | Find SendGrid keys | `intext:"sendgrid_api_key"` |
| 152 | `intext:"mailgun_api_key"` | Find Mailgun keys | `intext:"mailgun_api_key"` |
| 153 | `intext:"digitalocean_token"` | Find DigitalOcean tokens | `intext:"digitalocean_token"` |
| 154 | `intext:"heroku_api_key"` | Find Heroku API keys | `intext:"heroku_api_key"` |
| 155 | `intext:"firebase_api_key"` | Find Firebase keys | `intext:"firebase_api_key"` |
| 156 | `intext:"google_api_key"` | Find Google API keys | `intext:"google_api_key"` |
| 157 | `intext:"microsoft_graph_token"` | Find Microsoft Graph tokens | `intext:"microsoft_graph_token"` |
| 158 | `intext:"azure_access_key"` | Find Azure access keys | `intext:"azure_access_key"` |
| 159 | `intext:"gcp_service_account"` | Find GCP service accounts | `intext:"gcp_service_account"` |
| 160 | `intext:"alibaba_access_key"` | Find Alibaba Cloud keys | `intext:"alibaba_access_key"` |

---

## Database Exposure (161-180)

| # | Command | Description | Example |
|---|---------|-------------|---------|
| 161 | `intext:"mysql_dump"` | Find MySQL database dumps | `intext:"mysql_dump"` |
| 162 | `intext:"SQL dump"` | Find SQL database dumps | `intext:"SQL dump"` |
| 163 | `intext:"BEGIN; SELECT"` | Find SQL backup formats | `intext:"BEGIN; SELECT"` |
| 164 | `filetype:sql "CREATE TABLE"` | Find SQL table creation statements | `filetype:sql "CREATE TABLE"` |
| 165 | `filetype:sql "INSERT INTO"` | Find SQL insert statements | `filetype:sql "INSERT INTO"` |
| 166 | `filetype:sql "UPDATE"` | Find SQL update statements | `filetype:sql "UPDATE"` |
| 167 | `filetype:sql "DELETE FROM"` | Find SQL delete statements | `filetype:sql "DELETE FROM"` |
| 168 | `filetype:sql "password"` | Find SQL files with passwords | `filetype:sql "password"` |
| 169 | `filetype:sql "email"` | Find SQL files with emails | `filetype:sql "email"` |
| 170 | `filetype:sql "phone"` | Find SQL files with phone numbers | `filetype:sql "phone"` |
| 171 | `filetype:sql "credit_card"` | Find SQL files with credit cards | `filetype:sql "credit_card"` |
| 172 | `filetype:sql "ssn"` | Find SQL files with SSNs | `filetype:sql "ssn"` |
| 173 | `filetype:db "sqlite"` | Find SQLite database files | `filetype:db "sqlite"` |
| 174 | `filetype:backup "database"` | Find database backups | `filetype:backup "database"` |
| 175 | `filetype:dump "mysql"` | Find MySQL dumps | `filetype:dump "mysql"` |
| 176 | `"database.sql"` | Find exposed database files | `"database.sql"` |
| 177 | `"backup.sql"` | Find backup SQL files | `"backup.sql"` |
| 178 | `"export.sql"` | Find SQL export files | `"export.sql"` |
| 179 | `"users.sql"` | Find user SQL files | `"users.sql"` |
| 180 | `"admin.sql"` | Find admin SQL files | `"admin.sql"` |

---

## Vulnerability & Security Testing (181-200)

| # | Command | Description | Example |
|---|---------|-------------|---------|
| 181 | `intitle:"phpinfo()"` | Find PHP info pages | `intitle:"phpinfo()"` |
| 182 | `intitle:"Test Page"` | Find test/debug pages | `intitle:"Test Page"` |
| 183 | `intitle:"ERROR"` | Find error pages with information disclosure | `intitle:"ERROR"` |
| 184 | `intitle:"Warning"` | Find warning pages with stack traces | `intitle:"Warning"` |
| 185 | `intitle:"Exception"` | Find exception pages with traces | `intitle:"Exception"` |
| 186 | `intitle:"Debug"` | Find debug pages | `intitle:"Debug"` |
| 187 | `intitle:"Development"` | Find development pages | `intitle:"Development"` |
| 188 | `intitle:"Staging"` | Find staging environment pages | `intitle:"Staging"` |
| 189 | `intext:"Stack trace"` | Find pages showing stack traces | `intext:"Stack trace"` |
| 190 | `intext:"Exception in thread"` | Find Java exceptions | `intext:"Exception in thread"` |
| 191 | `intext:"Traceback"` | Find Python tracebacks | `intext:"Traceback"` |
| 192 | `intext:"call stack"` | Find call stack information | `intext:"call stack"` |
| 193 | `inurl:"/admin/login"` | Find admin login pages | `inurl:"/admin/login"` |
| 194 | `inurl:"/admin/panel"` | Find admin panels | `inurl:"/admin/panel"` |
| 195 | `inurl:"/administrator/"` | Find administrator directories | `inurl:"/administrator/"` |
| 196 | `inurl:"/user/login"` | Find user login pages | `inurl:"/user/login"` |
| 197 | `inurl:"/user/register"` | Find user registration pages | `inurl:"/user/register"` |
| 198 | `inurl:"/api/v1/"` | Find API endpoints | `inurl:"/api/v1/"` |
| 199 | `inurl:"/api/admin"` | Find admin API endpoints | `inurl:"/api/admin"` |
| 200 | `inurl:"/api/users"` | Find user API endpoints | `inurl:"/api/users"` |

---

## Specific Technologies (201-220)

| # | Command | Description | Example |
|---|---------|-------------|---------|
| 201 | `intitle:"Dashboard [Jenkins]"` | Find Jenkins dashboards | `intitle:"Dashboard [Jenkins]"` |
| 202 | `intitle:"Grafana"` | Find Grafana dashboards | `intitle:"Grafana"` |
| 203 | `intitle:"Kibana"` | Find Kibana dashboards | `intitle:"Kibana"` |
| 204 | `intitle:"Splunk"` | Find Splunk dashboards | `intitle:"Splunk"` |
| 205 | `intitle:"Docker Registry"` | Find Docker registries | `intitle:"Docker Registry"` |
| 206 | `intitle:"GitLab"` | Find GitLab instances | `intitle:"GitLab"` |
| 207 | `intitle:"Redmine"` | Find Redmine project management | `intitle:"Redmine"` |
| 208 | `intitle:"Jira"` | Find Jira instances | `intitle:"Jira"` |
| 209 | `intitle:"Confluence"` | Find Confluence wikis | `intitle:"Confluence"` |
| 210 | `intitle:"phpMyAdmin"` | Find phpMyAdmin interfaces | `intitle:"phpMyAdmin"` |
| 211 | `intitle:"Adminer"` | Find Adminer database tools | `intitle:"Adminer"` |
| 212 | `intitle:"WebDAV"` | Find WebDAV directories | `intitle:"WebDAV"` |
| 213 | `intitle:"FTP List"` | Find FTP listings | `intitle:"FTP List"` |
| 214 | `intitle:"SFTP"` | Find SFTP interfaces | `intitle:"SFTP"` |
| 215 | `inurl:":3000"` | Find services on port 3000 | `inurl:":3000"` |
| 216 | `inurl:":5000"` | Find services on port 5000 | `inurl:":5000"` |
| 217 | `inurl:":8000"` | Find services on port 8000 | `inurl:":8000"` |
| 218 | `inurl:":8080"` | Find services on port 8080 | `inurl:":8080"` |
| 219 | `inurl:":8443"` | Find services on port 8443 | `inurl:":8443"` |
| 220 | `inurl:":9000"` | Find services on port 9000 | `inurl:":9000"` |

---

## Credentials & Secrets (221-240)

| # | Command | Description | Example |
|---|---------|-------------|---------|
| 221 | `intext:"password =" filetype:conf` | Find password assignments | `intext:"password =" filetype:conf` |
| 222 | `intext:"password: " filetype:txt` | Find password listings | `intext:"password: " filetype:txt` |
| 223 | `intext:"user: " intext:"pass: "` | Find user/pass pairs | `intext:"user: " intext:"pass: "` |
| 224 | `intext:"username: " intext:"password: "` | Find credentials | `intext:"username: " intext:"password: "` |
| 225 | `intext:"login: " intext:"password: "` | Find login credentials | `intext:"login: " intext:"password: "` |
| 226 | `intext:"db_user" intext:"db_password"` | Find database credentials | `intext:"db_user" intext:"db_password"` |
| 227 | `intext:"mysql_user" intext:"mysql_password"` | Find MySQL credentials | `intext:"mysql_user" intext:"mysql_password"` |
| 228 | `intext:"root:" filetype:txt` | Find root credentials | `intext:"root:" filetype:txt` |
| 229 | `intext:"admin:" filetype:txt` | Find admin credentials | `intext:"admin:" filetype:txt` |
| 230 | `intext:"ssh_key" filetype:txt` | Find SSH keys | `intext:"ssh_key" filetype:txt` |
| 231 | `intext:"private_key" filetype:txt` | Find private keys | `intext:"private_key" filetype:txt` |
| 232 | `intext:"rsa_private_key"` | Find RSA private keys | `intext:"rsa_private_key"` |
| 233 | `intext:"dsa_private_key"` | Find DSA private keys | `intext:"dsa_private_key"` |
| 234 | `intext:"-----BEGIN PRIVATE KEY-----"` | Find encrypted private keys | `intext:"-----BEGIN PRIVATE KEY-----"` |
| 235 | `intext:"-----BEGIN RSA PRIVATE KEY-----"` | Find RSA keys | `intext:"-----BEGIN RSA PRIVATE KEY-----"` |
| 236 | `intext:"-----BEGIN OPENSSH PRIVATE KEY-----"` | Find OpenSSH keys | `intext:"-----BEGIN OPENSSH PRIVATE KEY-----"` |
| 237 | `intext:"password123"` | Find common passwords | `intext:"password123"` |
| 238 | `intext:"admin123"` | Find admin passwords | `intext:"admin123"` |
| 239 | `intext:"letmein"` | Find weak passwords | `intext:"letmein"` |
| 240 | `intext:"qwerty"` | Find keyboard pattern passwords | `intext:"qwerty"` |

---

## Personal & Contact Information (241-260)

| # | Command | Description | Example |
|---|---------|-------------|---------|
| 241 | `intext:"email@example.com"` | Find email addresses | `intext:"email@example.com"` |
| 242 | `intext:"contact@"` | Find contact emails | `intext:"contact@"` |
| 243 | `intext:"support@"` | Find support emails | `intext:"support@"` |
| 244 | `intext:"info@"` | Find info emails | `intext:"info@"` |
| 245 | `intext:"phone:" filetype:txt` | Find phone numbers | `intext:"phone:" filetype:txt` |
| 246 | `intext:"mobile:" filetype:txt` | Find mobile numbers | `intext:"mobile:" filetype:txt` |
| 247 | `intext:"fax:" filetype:txt` | Find fax numbers | `intext:"fax:" filetype:txt` |
| 248 | `intext:"address:" filetype:txt` | Find addresses | `intext:"address:" filetype:txt` |
| 249 | `intext:"zip code:" filetype:txt` | Find ZIP codes | `intext:"zip code:" filetype:txt` |
| 250 | `intext:"ssn:" filetype:txt` | Find social security numbers | `intext:"ssn:" filetype:txt` |
| 251 | `intext:"social security"` | Find SSN references | `intext:"social security"` |
| 252 | `intext:"driver license"` | Find driver license references | `intext:"driver license"` |
| 253 | `intext:"passport"` | Find passport references | `intext:"passport"` |
| 254 | `intext:"credit card"` | Find credit card references | `intext:"credit card"` |
| 255 | `intext:"cvv:" filetype:txt` | Find CVV numbers | `intext:"cvv:" filetype:txt` |
| 256 | `intext:"expiration date:" filetype:txt` | Find credit card expiration | `intext:"expiration date:" filetype:txt` |
| 257 | `intext:"name:" intext:"email:" intext:"phone:"` | Find contact lists | `intext:"name:" intext:"email:" intext:"phone:"` |
| 258 | `intext:"employee" intext:"contact" filetype:xls` | Find employee lists | `intext:"employee" intext:"contact" filetype:xls` |
| 259 | `intext:"customer" intext:"email" filetype:csv` | Find customer lists | `intext:"customer" intext:"email" filetype:csv` |
| 260 | `intext:"member" intext:"password" filetype:txt` | Find member lists | `intext:"member" intext:"password" filetype:txt` |

---

## Medical & Legal (261-280)

| # | Command | Description | Example |
|---|---------|-------------|---------|
| 261 | `filetype:pdf "patient"` | Find patient documents | `filetype:pdf "patient"` |
| 262 | `filetype:pdf "medical record"` | Find medical records | `filetype:pdf "medical record"` |
| 263 | `filetype:pdf "prescription"` | Find prescription records | `filetype:pdf "prescription"` |
| 264 | `filetype:pdf "diagnosis"` | Find diagnosis documents | `filetype:pdf "diagnosis"` |
| 265 | `filetype:pdf "confidential" "medical"` | Find confidential medical docs | `filetype:pdf "confidential" "medical"` |
| 266 | `filetype:doc "patient name" "diagnosis"` | Find patient documents | `filetype:doc "patient name" "diagnosis"` |
| 267 | `filetype:xls "patient" "treatment"` | Find patient treatment records | `filetype:xls "patient" "treatment"` |
| 268 | `filetype:pdf "contract"` | Find contracts | `filetype:pdf "contract"` |
| 269 | `filetype:pdf "agreement"` | Find agreements | `filetype:pdf "agreement"` |
| 270 | `filetype:pdf "legal"` | Find legal documents | `filetype:pdf "legal"` |
| 271 | `filetype:pdf "confidential" "legal"` | Find confidential legal docs | `filetype:pdf "confidential" "legal"` |
| 272 | `filetype:doc "NDA"` | Find NDAs | `filetype:doc "NDA"` |
| 273 | `filetype:doc "proprietary"` | Find proprietary information | `filetype:doc "proprietary"` |
| 274 | `filetype:doc "confidential"` | Find confidential documents | `filetype:doc "confidential"` |
| 275 | `filetype:pdf "cease and desist"` | Find C&D letters | `filetype:pdf "cease and desist"` |
| 276 | `filetype:pdf "litigation"` | Find litigation documents | `filetype:pdf "litigation"` |
| 277 | `filetype:xls "case" "notes"` | Find case notes | `filetype:xls "case" "notes"` |
| 278 | `filetype:pdf "attorney"` | Find attorney documents | `filetype:pdf "attorney"` |
| 279 | `filetype:pdf "law firm"` | Find law firm documents | `filetype:pdf "law firm"` |
| 280 | `filetype:pdf "court"` | Find court documents | `filetype:pdf "court"` |

---

## Financial & Banking (281-300)

| # | Command | Description | Example |
|---|---------|-------------|---------|
| 281 | `intext:"routing number"` | Find routing numbers | `intext:"routing number"` |
| 282 | `intext:"account number"` | Find account numbers | `intext:"account number"` |
| 283 | `intext:"swift code"` | Find SWIFT codes | `intext:"swift code"` |
| 284 | `intext:"iban"` | Find IBAN information | `intext:"iban"` |
| 285 | `filetype:pdf "invoice"` | Find invoices | `filetype:pdf "invoice"` |
| 286 | `filetype:xls "invoice"` | Find invoice spreadsheets | `filetype:xls "invoice"` |
| 287 | `filetype:pdf "receipt"` | Find receipts | `filetype:pdf "receipt"` |
| 288 | `filetype:pdf "statement"` | Find bank statements | `filetype:pdf "statement"` |
| 289 | `filetype:xls "balance"` | Find balance spreadsheets | `filetype:xls "balance"` |
| 290 | `filetype:pdf "transaction"` | Find transaction documents | `filetype:pdf "transaction"` |
| 291 | `filetype:xls "payment"` | Find payment records | `filetype:xls "payment"` |
| 292 | `filetype:xls "refund"` | Find refund records | `filetype:xls "refund"` |
| 293 | `filetype:pdf "tax return"` | Find tax returns | `filetype:pdf "tax return"` |
| 294 | `filetype:xls "tax"` | Find tax spreadsheets | `filetype:xls "tax"` |
| 295 | `filetype:pdf "w-2"` | Find W-2 forms | `filetype:pdf "w-2"` |
| 296 | `filetype:pdf "1099"` | Find 1099 forms | `filetype:pdf "1099"` |
| 297 | `filetype:xls "financial"` | Find financial spreadsheets | `filetype:xls "financial"` |
| 298 | `filetype:pdf "financial statement"` | Find financial statements | `filetype:pdf "financial statement"` |
| 299 | `filetype:xls "payroll"` | Find payroll records | `filetype:xls "payroll"` |
| 300 | `filetype:pdf "salary"` | Find salary documents | `filetype:pdf "salary"` |

---

## Advanced Search Combinations

### Example Queries

**Find Admin Panels with Credentials:**
```
inurl:admin filetype:txt intext:"password"
site:example.com inurl:admin
```

**Discover Database Files:**
```
filetype:sql "CREATE TABLE" OR filetype:db
intext:"mysql_dump" OR intext:"database.sql"
```

**Locate API Keys and Secrets:**
```
intext:"api_key" OR intext:"secret" filetype:json
intext:"AKIA" OR intext:"aws_secret_access_key"
```

**Find Exposed Backups:**
```
intitle:"index of" "backup" OR "backup.zip" OR "backup.tar.gz"
filetype:bak OR filetype:backup
```

**Discover Configuration Files:**
```
inurl:.env OR inurl:wp-config.php OR inurl:config.php -github
filetype:xml OR filetype:ini OR filetype:conf
```

**Look for Sensitive Documents:**
```
filetype:pdf "confidential" OR "proprietary" OR "secret"
filetype:doc "password" OR "credentials"
```

---

## Important Safety & Legal Guidelines

### ✅ LEGAL USES:
- Authorized security testing and penetration testing
- Legitimate research and educational purposes
- Finding and reporting your own exposed information
- Bug bounty programs with explicit permission
- Security awareness training (with proper authorization)
- Competitive research on publicly available information
- Academic studies on information disclosure

### ❌ ILLEGAL USES:
- Unauthorized access to computer systems
- Data theft or exfiltration
- Identity theft or fraud
- Corporate espionage
- Privacy violations
- Hacking or exploitation
- Extortion or blackmail
- Any unauthorized use of discovered information

### 📋 RESPONSIBLE DISCLOSURE:
If you discover sensitive information:
1. Do NOT access systems you're not authorized to access
2. Do NOT download or store confidential data
3. Report findings to the organization immediately
4. Use responsible disclosure practices
5. Give reasonable time for remediation
6. Follow ethical hacking guidelines

### ⚖️ LEGAL CONSEQUENCES:
Unauthorized access or exploitation can result in:
- Criminal charges and imprisonment
- Civil lawsuits and damages
- Fines up to $250,000+ (in some jurisdictions)
- Permanent criminal record
- Loss of employment and professional licenses

---

## Resources for Learning

- [Google Advanced Search Help](https://support.google.com/websearch/answer/2466433)
- [OWASP Security Testing Guide](https://owasp.org/www-project-web-security-testing-guide/)
- [HackerOne Bug Bounty Platform](https://www.hackerone.com/)
- [Bugcrowd Security Testing](https://www.bugcrowd.com/)
- [Defensive Security Mindset](https://www.defensivesecurity.org/)

---

**Last Updated:** 2026-04-23  
**Total Commands:** 300+  
**Status:** Complete Reference Guide

# Google Dorking Commands

## Basic Operators
1. `"search term"` - Searches for the exact phrase.
2. `site:example.com` - Searches within a specific site.
3. `filetype:pdf` - Searches for files of a specific type.
4. `intitle:"keyword"` - Searches for pages with a specific keyword in the title.
5. `inurl:"keyword"` - Searches for URLs containing a specific keyword.

## Advanced Operators
6. `cache:example.com` - Shows the cached version of a webpage.
7. `link:example.com` - Finds links to a specific website.
8. `related:example.com` - Finds sites related to a specific website.
9. `info:example.com` - Provides information about a particular website.
10. `allintext:keyword` - Searches for pages with all terms in the body text.

## Security and Vulnerability Searching
11. `intext:"password"` - Searches for pages containing the word "password".
12. `inurl:login` - Searches for login pages.
13. `inurl:admin` - Searches for admin login pages.
14. `inurl:wp-login.php` - Searches for WordPress login pages.
15. `filetype:sql` - Searches for SQL files potentially containing sensitive data.

## File Searches
16. `filetype:xls` - Searches for Excel files.
17. `filetype:doc` - Searches for Word documents.
18. `filetype:ppt` - Searches for PowerPoint presentations.
19. `filetype:xml` - Searches for XML files.
20. `filetype:csv` - Searches for CSV files.

## Indexing and Data Searching
21. `site:gov` - Searches government websites.
22. `site:edu` - Searches educational institution websites.
23. `site:org` - Searches non-profit organization websites.
24. `intext:"credit card"` - Searches for pages containing "credit card" information.
25. `intext:"social security"` - Searches for social security numbers.

## Combine Searches
26. `"search term" OR "alternative term"` - Searches for either term.
27. `"search term" AND "other term"` - Searches for results containing both terms.
28. `"search term" -exclude_term` - Searches for results excluding a specific term.
29. `"search term" AROUND(3) "other term"` - Searches for terms within a certain distance from each other.
30. `"search term" * "other term"` - Searches for results with anything in between.

## Location-Based Searches
31. `"keyword" inurl:location` - Searches for pages containing a location.
32. `"keyword" site:.uk` - Searches for UK sites.
33. `"keyword" site:.ca` - Searches for Canadian sites.
34. `"keyword" site:.au` - Searches for Australian sites.
35. `"keyword" site:.de` - Searches for German sites.

## Miscellaneous Searches
36. `"keyword" define:` - Finds definitions for a keyword.
37. `"keyword" movie:` - Searches for movies related to the keyword.
38. `"keyword" recipe:` - Searches for recipes related to the keyword.
39. `"keyword" news:` - Searches for news related to the keyword.
40. `"keyword" sports:` - Searches for sports news related to the keyword.

## Custom Finance Searches
41. `"investing" filetype:pdf` - Searches for investing PDF guides.
42. `"stock market" intext:"crash"` - Looks for stock market crash discussions.
43. `"financial report" filetype:xls` - Searches for financial Excel reports.
44. `"budget" filetype:doc` - Searches for budgeting documents.
45. `"financial analysis" site:edu` - Looks for academic financial analysis papers.

## Academic Searches
46. `"thesis" filetype:pdf` - Searches for academic theses.
47. `"research paper" site:edu` - Searches for educational research papers.
48. `"dissertation" filetype:doc` - Searches for doctoral dissertations.
49. `"conference paper" filetype:ppt` - Searches for conference presentations.
50. `"journal article" filetype:pdf` - Searches for academic articles.

## Creative Content Searches
51. `"music lyrics"` - Searches for song lyrics.
52. `"art portfolio"` - Searches for artist portfolios.
53. `"graphic design" filetype:pdf` - Searches for PDF files related to graphic design.
54. `"photography" site:500px.com` - Searches for specific photography sites.
55. `"architecture" blueprint filetype:jpg` - Searches for blueprint images.

## Employment Searches
56. `"Job Title" site:linkedin.com` - Searches for job postings on LinkedIn.
57. `"resume" filetype:pdf` - Searches for PDF resumes.
58. `"interview tips"` - Searches for interview tips resources.
59. `"career advice"` - Searches for career advice articles.
60. `"salary" site:glassdoor.com` - Searches for salary information.

## Code and Development Searches
61. `"code samples" filetype:py` - Searches for Python code samples.
62. `"API documentation"` - Searches for API documentation.
63. `"web development" site:github.com` - Searches for GitHub web development projects.
64. `"open-source project" filetype:zip` - Searches for downloadable open-source projects.
65. `"software development" inurl:blog` - Searches for software development blogs.

## Government & Legal Searches
66. `"lawsuit" filetype:pdf` - Searches for PDF files related to lawsuits.
67. `"legislation" site:gov` - Searches for legal documents on government websites.
68. `"public records" filetype:csv` - Searches for public records in CSV format.
69. `"court case" site:uscourts.gov` - Searches for federal court cases.
70. `"legal advice"` - Searches for legal advice articles.

## Technology Searches
71. `"gadget review"` - Searches for reviews on gadgets.
72. `"tech news"` - Searches for technology news articles.
73. `"programming languages"` - Searches for information on programming languages.
74. `"hardware specifications"` - Searches for hardware specifications.
75. `"software updates"` - Searches for recent software updates.

## Health & Wellness Searches
76. `"fitness tips"` - Searches for fitness-related articles.
77. `"diet plans"` - Searches for weight loss diet plans.
78. `"hospital information" site:gov` - Searches for government hospital resources.
79. `"medical research" filetype:pdf` - Searches for medical research papers.
80. `"healthcare policy"` - Searches for healthcare policy discussions.

## Travel Searches
81. `"travel tips"` - Searches for travel tips.
82. `"flight deals"` - Searches for flight deals and discounts.
83. `"hotel reviews"` - Searches for hotel reviews.
84. `"travel blogs"` - Searches for travel blogs.
85. `"tourist attractions"` - Searches for popular tourist attractions.

## Real Estate Searches
86. `"homes for sale" site:realestate.com` - Searches for homes for sale.
87. `"rental properties" site:apartmentfinder.com` - Searches for rental properties.
88. `"real estate market analysis" filetype:pdf` - Searches for PDF real estate analyses.
89. `"property investment tips"` - Searches for property investment advice.
90. `"mortgage rates"` - Searches for current mortgage rates.

## Personal Development Searches
91. `"self-help books"` - Searches for self-help book suggestions.
92. `"motivational quotes"` - Searches for motivational quotes.
93. `"goal setting strategies"` - Searches for goal-setting articles.
94. `"time management tips"` - Searches for time management techniques.
95. `"mindfulness practices"` - Searches for mindfulness and meditation tips.

## Environmental Searches
96. `"climate change research" filetype:pdf` - Searches for climate change studies.
97. `"renewable energy technologies"` - Searches for renewable energy articles.
98. `"environmental policy" site:gov` - Searches for government environmental policies.
99. `"conservation efforts"` - Searches for conservation-related initiatives.
100. `"sustainable practices"` - Searches for sustainability practices in various fields.


## Additional Commands

### Business and Finance
101. `"investment strategies"` - Searches for investment advice.
102. `"credit score tips"` - Searches for ways to improve credit scores.
103. `"business plan templates" filetype:doc` - Searches for business plan templates.
104. `"market research" filetype:pdf` - Searches for market research reports.
105. `"financial literacy"` - Searches for financial literacy resources.

### Social Media and Marketing
106. `"social media trends"` - Searches for information about social media trends.
107. `"influencer marketing"` - Searches for tips on influencer marketing.
108. `"blogging tips"` - Searches for blogging advice.
109. `"SEO strategies"` - Searches for search engine optimization strategies.
110. `"content marketing"` - Searches for content marketing techniques.

### Parenting and Family
111. `"parenting tips"` - Searches for parenting advice.
112. `"newborn care"` - Searches for resources on caring for newborns.
113. `"educational activities for kids"` - Searches for educational activities.
114. `"family vacation ideas"` - Searches for family-friendly vacation ideas.
115. `"teenage issues"` - Searches for advice on dealing with teenage issues.

### Science and Technology
116. `"quantum computing"` - Searches for information on quantum computing.
117. `"artificial intelligence research" filetype:pdf` - Searches for AI research papers.
118. `"blockchain technology"` - Searches for resources on blockchain.
119. `"space exploration"` - Searches for space exploration articles.
120. `"biotechnology"` - Searches for biotechnology advancements.

### Lifestyle and Hobbies
121. `"cooking recipes"` - Searches for various cooking recipes.
122. `"hiking trails"` - Searches for popular hiking trails.
123. `"DIY projects"` - Searches for do-it-yourself project ideas.
124. `"home improvement tips"` - Searches for home renovation advice.
125. `"gardening tips"` - Searches for gardening advice.

### Arts and Culture
126. `"art exhibitions"` - Searches for art exhibitions.
127. `"literary reviews"` - Searches for reviews of literature.
128. `"music concerts"` - Searches for information on music concerts.
129. `"film reviews"` - Searches for film critiques.
130. `"theater performances"` - Searches for theater events.

### Technology and Gadgets
131. `"latest smartphones"` - Searches for information on latest smartphones.
132. `"computer hardware reviews"` - Searches for computer hardware assessments.
133. `"digital cameras"` - Searches for latest digital cameras.
134. `"software comparisons"` - Searches for comparisons of software products.
135. `"tech gadgets"` - Searches for new technology gadgets.

### Fitness and Health
136. `"workout plans"` - Searches for exercise plans.
137. `"nutrition guides"` - Searches for nutrition information.
138. `"mental health resources"` - Searches for mental health support.
139. `"wellness tips"` - Searches for general wellness advice.
140. `"yoga practices"` - Searches for yoga techniques.

### Travel and Adventure
141. `"adventure travel"` - Searches for adventure travel ideas.
142. `"best travel destinations"` - Searches for top travel locations.
143. `"budget travel tips"` - Searches for travel on a budget.
144. `"road trips"` - Searches for popular road trip routes.
145. `"cultural experiences"` - Searches for cultural travel experiences.

### Personal Finance
146. `"saving strategies"` - Searches for ways to save money.
147. `"retirement plans"` - Searches for retirement planning resources.
148. `"debt relief options"` - Searches for information on relieving debt.
149. `"credit repair tips"` - Searches for repairing credit scores.
150. `"investing basics"` - Searches for beginner investing information.

### Food and Dining
151. `"local restaurants"` - Searches for restaurants in a specific area.
152. `"food truck events"` - Searches for food truck gatherings.
153. `"cooking classes"` - Searches for cooking courses available.
154. `"ethnic cuisines"` - Searches for different types of ethnic foods.
155. `"wine tasting events"` - Searches for wine tasting opportunities.

### Home and Garden
156. `"interior design ideas"` - Searches for home decor inspirations.
157. `"landscaping tips"` - Searches for landscaping advice.
158. `"home organization"` - Searches for tips on organizing the home.
159. `"sustainable gardening"` - Searches for eco-friendly gardening practices.
160. `"real estate trends"` - Searches for current real estate trends.

### Career Development
161. `"professional networking"` - Searches for networking opportunities.
162. `"career advancement tips"` - Searches for ways to advance in a career.
163. `"online courses"` - Searches for available online courses.
164. `"skill development"` - Searches for skills development resources.
165. `"mentorship opportunities"` - Searches for mentorship programs.

### History and Culture
166. `"historical research papers" filetype:pdf` - Searches for historical studies.
167. `"cultural heritage"` - Searches for cultural preservation topics.
168. `"art history"` - Searches for art movements and history.
169. `"significant historical events"` - Searches for major historical occurrences.
170. `"ethnic studies"` - Searches for information on various ethnic groups.

### Technology and Innovations
171. `"latest tech news"` - Searches for up-to-date technology news.
172. `"gadget reviews"` - Searches for reviews on the latest gadgets.
173. `"software updates"` - Searches for information about newly released software updates.
174. `"app comparisons"` - Searches for comparisons of mobile applications.
175. `"tech career paths"` - Searches for information on technology-related careers.

### Sports and Recreation
176. `"team schedules"` - Searches for sports team schedules.
177. `"fitness challenges"` - Searches for competitive fitness events.
178. `"sports betting tips"` - Searches for tips on sports betting.
179. `"outdoor sports activities"` - Searches for outdoor sporting events.
180. `"eSports competitions"` - Searches for eSports tournament information.

### Education and Learning
181. `"online learning platforms"` - Searches for platforms offering online education.
182. `"study tips"` - Searches for effective study methodologies.
183. `"learning resources for students"` - Searches for educational materials.
184. `"home schooling tips"` - Searches for advice on home schooling.
185. `"curriculum development"` - Searches for curriculum planning resources.

### Arts and Crafts
186. `"art supplies"` - Searches for local craft stores.
187. `"craft tutorials"` - Searches for crafting instruction videos.
188. `"art workshops"` - Searches for available art classes.
189. `"DIY home decor"` - Searches for do-it-yourself decor projects.
190. `"community art projects"` - Searches for local art initiatives.

### Community and Society
191. `"volunteer opportunities"` - Searches for local volunteering possibilities.
192. `"community events"` - Searches for happenings in a community.
193. `"non-profit organizations"` - Searches for local non-profits.
194. `"social activism"` - Searches for information about social justice movements.
195. `"support groups"` - Searches for various support communities.

### Environmental Issues
196. `"climate change impacts"` - Searches for effects of climate change.
197. `"sustainability practices"` - Searches for sustainable living advice.
198. `"wildlife conservation"` - Searches for wildlife protection initiatives.
199. `"eco-friendly products"` - Searches for green product alternatives.
200. `"pollution solutions"` - Searches for ways to combat pollution.

---

## **2. Social Media Intelligence - SOCMINT (10 techniques)**

8. Facebook Graph Search and legacy API extraction
9. Twitter/X API scraping and archive searches
10. LinkedIn Sales Navigator filters and profile mapping
11. Instagram account & hashtag mapping
12. Reddit topic tracking (Pushshift, SubredditStats)
13. TikTok profile mapping and geolocation
14. Snapchat Snap Map exploration
15. Telegram channel and group scraping
16. Mastodon and decentralized platform intelligence
17. Social connection analysis via Maltego

---

## **3. People & Entity Tracing (8 techniques)**

18. Email tracing (Hunter.io, EmailRep.io)
19. Username research (KnowEm, Namechk, WhatsMyName)
20. Phone number lookup (NumVerify, TrueCaller)
21. Address and property records search
22. Deep people search (Pipl, Spokeo, BeenVerified)
23. Data breach searching (HaveIBeenPwned, Dehashed)
24. Paste site monitoring (Pastebin, Ghostbin)
25. Public records analysis (corporate filings, SEC.gov)

---

## **4. Geolocation & GeoINT (8 techniques)**

26. Satellite imagery comparison (Google Earth Pro, Sentinel Hub)
27. EXIF data extraction (ExifTool)
28. Crowd-sourced map analysis (OpenStreetMap, Wikimapia)
29. Social media geo-tag correlation (Geofeedia)
30. Sun/shadow analysis for time/location confirmation (SunCalc)
31. Video geolocation with frame analysis
32. Terrain and structure identification (Terraserver)
33. Air traffic tracking (Flightradar24, ADS-B)

---

## **5. Image & Video Analysis (6 techniques)**

34. Reverse image search (Google, TinEye, Yandex)
35. Deepfake and manipulation detection (FotoForensics, InVID)
36. Hash-based similarity searching (PDQ, pHash)
37. Forensic watermark recovery
38. Crowd-sourced photo verification (Bellingcat)
39. Facial recognition tools (PimEyes, FindClone)

---

## **6. Domain & Network Investigation (7 techniques)**

40. WHOIS history and DNS discovery (DomainTools, SecurityTrails)
41. Subdomain enumeration (Amass, Sublist3r)
42. Passive DNS history lookup
43. SSL certificate transparency logs
44. Website change detection (Visualping, ChangeTower)
45. Hosting infrastructure tracking
46. IoT and host discovery (Censys, Shodan, ZoomEye)

---

## **7. Dark Web & Threat Monitoring (4 techniques)**

47. Onion site scraping and indexing (OnionSearch, Recon-ng)
48. Forum and marketplace monitoring
49. Surface and dark web credential leakage checks
50. Dark web reputation network mapping

---

## **8. Data Analytics & Visualization (5 techniques)**

51. Relationship pivoting in Maltego
52. Graph analysis (Linkurious, Gephi)
53. Email network visualization
54. Time-series analysis (Excel, Kibana, Splunk)
55. Cluster analysis from leaks/dumps

---

## **9. Automation & Scripting (5 techniques)**

56. Scrapy for large-scale web scraping
57. Python BeautifulSoup for targeted extraction
58. Selenium and Puppeteer for browser automation
59. OSINT automation with Spiderfoot
60. Google Dork automation scripts

---

## **10. Specialized Topic Research (6 techniques)**

61. Cryptocurrency transaction tracking (Blockchair, Etherscan)
62. Scam/phishing tracking (PhishTank, URLscan.io)
63. Shipping/logistics tracing (MarineTraffic, VesselFinder)
64. Vehicle identification via VIN lookup
65. News leak and publication monitoring
66. Financial due diligence (OpenCorporates, Orbis)

---

## **11. Email Investigation (3 techniques)**

67. Email header analysis for source location
68. Mail server and MX record verification
69. Alias finding with Hunter.io/LinkedIn

---

## **12. Code & Software OSINT (4 techniques)**

70. Code search on GitHub, GitLab
71. Exposed credential discovery in public repos
72. StackOverflow sensitive information monitoring
73. Dependency and package vulnerability enumeration

---

## **13. Password & Hash Analysis (2 techniques)**

74. Hash lookup (haveibeenpwned, hashdd.com)
75. Weak hash brute-forcing for leaks

---

## **14. Monitoring & Alerting (3 techniques)**

76. Google Alerts for names and entities
77. Content theft and infringement monitoring
78. RSS feed aggregation for news

---

## **15. Physical/Real-World OSINT (3 techniques)**

79. FOIA (Freedom of Information Act) requests
80. Utility and business license lookups
81. Patent and trademark searches

---

## **16. Advanced Techniques (4 techniques)**

82. OpSec: Anonymization (Tails, Qubes OS, VPN, TOR)
83. Digital evidence chain of custody
84. Complex network path tracing (BGPView, RIPEstat)
85. Cross-language OSINT (Baidu, Sogou, Cyrillic queries)

---

## **17. Essential OSINT Tools & Frameworks (15+ tools)**

86. **Maltego** - Entity resolution and relationship mapping
87. **Spiderfoot** - Automated reconnaissance framework
88. **Recon-ng** - Modular intelligence reconnaissance
89. **TheHarvester** - Email and host enumeration
90. **FOCA** - Metadata extraction tool
91. **Shodan** - Internet device search engine
92. **Censys** - Host and certificate search
93. **OSINT Framework** - Web-based tool repository
94. **Social-Searcher** - Multi-platform social search
95. **InVID** - Video verification suite
96. **IntelligenceX** - Archives and leak searches
97. **GreyNoise** - Internet noise context
98. **AIL Framework** - Automated leak analysis
99. **Bellingcat Toolkit** - Visual investigation tools
100. **Dehashed** - Data breach search platform

---

## **Key Principles for Effective OSINT**

✅ **Remain Anonymous** - Use VPNs, TOR, and operational security practices  
✅ **Document Everything** - Maintain chain of custody for findings  
✅ **Cross-Reference** - Verify information from multiple sources  
✅ **Stay Legal & Ethical** - Only use publicly available data; respect privacy laws  
✅ **Automate Strategically** - Use tools and scripts to scale investigations  
✅ **Think Visually** - Use mind maps and graphs to understand relationships  
✅ **Go Passive First** - Gather as much as possible before active techniques  

---

## **Summary: From Basic to Advanced**

**Basic Level:**
- Google Dorking
- Social media searching
- WHOIS lookups
- Reverse image search
- Email finding

**Intermediate Level:**
- Subdomain enumeration
- DNS analysis
- Data breach checking
- Website monitoring
- Metadata extraction

**Advanced Level:**
- Maltego relationship mapping
- Dark web monitoring
- Cryptocurrency tracking
- Facial recognition
- Automated frameworks (Spiderfoot, Recon-ng)
- Custom scripting and automation

---

---

# SECTION 3: 100 PASSIVE RECONNAISSANCE TECHNIQUES

---

## **PASSIVE RECON - NO DIRECT CONTACT, UNDETECTED**

### **Category 1: Search Engine & Web-Based Passive Recon (12 techniques)**

1. **Google Dorking for publicly exposed files** (site:, filetype:pdf, filetype:xls)
2. **Google Dorking for directory listings** (intitle:"index of" site:target.com)
3. **Google Dorking for admin pages** (intitle:"admin" OR intitle:"administrator" site:target.com)
4. **Google Dorking for sensitive documents** (filetype:doc OR filetype:docx "confidential")
5. **Google Dorking for login pages** (intitle:"login" OR inurl:"login" site:target.com)
6. **Google Dorking for backup files** (filetype:bak OR filetype:backup site:target.com)
7. **Bing Advanced Search operators** (ip:xxx.xxx.xxx.xxx, domain:target.com)
8. **DuckDuckGo site-specific searches** (site:target.com)
9. **Yandex search for non-indexed content** (searching Russian/Cyrillic sources)
10. **Cached content via Google Cache** (cache:target.com)
11. **Cached content via Bing Cache** (searching archived versions)
12. **Search operator combinations** (Multiple operators for refined searches)

---

### **Category 2: Wayback Machine & Web Archives (8 techniques)**

13. **Wayback Machine basic searches** (Finding historical snapshots of websites)
14. **Wayback Machine calendar view** (Identifying when changes were made)
15. **Wayback Machine robots.txt checking** (See what was hidden)
16. **Wayback Machine admin/config files** (Finding exposed configuration)
17. **Archive.org snapshots analysis** (Historical data extraction)
18. **Common Crawl dataset searches** (Large-scale web archive)
19. **Alternate Archive services** (archive.is, archive.ph)
20. **DNS history via Wayback** (Seeing historical DNS records)

---

### **Category 3: WHOIS & DNS Passive Lookups (10 techniques)**

21. **WHOIS domain registration lookup** (Who owns the domain)
22. **WHOIS registrar information** (Registration company details)
23. **WHOIS creation date analysis** (How old is the domain)
24. **WHOIS historical lookups** (DomainTools, SecurityTrails)
25. **WHOIS name server information** (DNS server providers)
26. **Reverse WHOIS lookups** (Find other domains by registrant)
27. **DNS A record lookup** (IP address of domain)
28. **DNS MX record lookup** (Mail server information)
29. **DNS TXT record lookup** (SPF, DKIM, DMARC records)
30. **DNS NS record lookup** (Nameserver information)

---

### **Category 4: IP Address & Geolocation Passive Recon (10 techniques)**

31. **IP geolocation lookup** (MaxMind, IPinfo.io, GeoIP databases)
32. **IP ASN (Autonomous System Number) lookup** (Network owner info)
33. **IP reverse DNS lookups** (What domain points to this IP)
34. **IP WHOIS information** (Regional Internet Registry data)
35. **IP historical data** (Past configurations of IPs)
36. **IP reputation checks** (GreyNoise, AbuseIPDB)
37. **IP blocking status** (Is IP blacklisted)
38. **IP range mapping** (Finding other IPs in same range)
39. **BGP route analysis** (Path to IP address)
40. **IP fingerprinting** (OS and service identification via passive means)

---

### **Category 5: Domain Intelligence & SSL Certificates (9 techniques)**

41. **SSL certificate analysis** (Certificate transparency logs)
42. **SSL certificate subject alternative names (SANs)** (Finding subdomains)
43. **SSL certificate history** (crt.sh, Censys)
44. **SSL certificate issuer analysis** (CA details)
45. **SSL certificate fingerprinting** (Identifying services)
46. **Subdomain discovery via certificates** (All subdomains with certs)
47. **Email addresses from certificates** (Admin contact info)
48. **Organization names from certificates** (Business entity research)
49. **Certificate validity period analysis** (When cert expires/renewed)

---

### **Category 6: Subdomain & DNS Enumeration (Passive) (8 techniques)**

50. **Passive subdomain enumeration via DNS** (SecurityTrails, VirusTotal)
51. **Subdomain discovery via certificate transparency** (crt.sh, Google)
52. **Subdomain discovery via DNS history** (Looking for old records)
53. **Subdomain discovery via search engines** (Bing, Google)
54. **Subdomain discovery via archives** (Wayback Machine)
55. **Passive DNS database queries** (SecurityTrails, Farsight)
56. **AXFR zone transfer (passive observation)** (Watching DNS responses)
57. **DNS forwarder identification** (Finding DNS providers)

---

### **Category 7: Social Media Intelligence (SOCMINT) - Passive (12 techniques)**

58. **Facebook profile search** (Public information only)
59. **Twitter/X advanced search** (User, keyword, date filters)
60. **LinkedIn profile analysis** (Public profile information)
61. **Instagram hashtag research** (Public posts, geolocation)
62. **Instagram bio analysis** (Username, location, website links)
63. **TikTok profile research** (Public videos, follower data)
64. **Reddit user history** (Public post analysis)
65. **Reddit subreddit analysis** (Community information)
66. **Telegram public channel analysis** (Open channel info)
67. **Discord server research** (Public server information)
68. **Snapchat username lookups** (Public profile data)
69. **BeReal post analysis** (Geolocation data from shared posts)

---

### **Category 8: Email & People Search - Passive (11 techniques)**

70. **Email finding via Hunter.io** (Email format discovery)
71. **Email finding via RocketReach** (Professional email databases)
72. **Email finding via Clearbit** (Company employee discovery)
73. **Email finding via Pipl** (Email & people data)
74. **Username research via KnowEm** (Username availability checks)
75. **Username research via Namechk** (Username existence checks)
76. **Username research via WhatsMyName** (Social media username search)
77. **Data breach searching via HaveIBeenPwned** (Leaked password checking)
78. **Data breach searching via Dehashed** (Breach database searches)
79. **Alias discovery via email variations** (firstname.lastname, first+last)
80. **Phone number OSINT** (TrueCaller, NumVerify reverse lookup)

---

### **Category 9: Image & Metadata Analysis - Passive (10 techniques)**

81. **Reverse image search via Google Images** (Finding where image appears)
82. **Reverse image search via TinEye** (Image source tracking)
83. **Reverse image search via Yandex** (Image location on internet)
84. **EXIF data extraction** (Location, camera, timestamp from photos)
85. **Metadata extraction from documents** (PDF, Office files via FOCA)
86. **Image geolocation via landmarks** (Visual analysis)
87. **Image geolocation via Google Maps** (Matching locations)
88. **Image geolocation via reverse streets view** (Street View analysis)
89. **Deepfake detection** (FotoForensics analysis)
90. **Image manipulation detection** (Forensic analysis tools)

---

### **Category 10: Company & Organization Research - Passive (10 techniques)**

91. **SEC filings research** (edgar.sec.gov for public companies)
92. **Corporate records lookup** (State business registries)
93. **Business license verification** (Local government databases)
94. **Patent & trademark searches** (USPTO, WIPO)
95. **News archive searches** (Company mentions in news)
96. **Press release databases** (PR Newswire, Business Wire)
97. **Company financials** (OpenCorporates, Crunchbase)
98. **Company website analysis** (Technology used, hosting provider)
99. **Company employee lists** (LinkedIn, Crunchbase)
100. **Company API documentation** (Publicly exposed API docs)

---

### **Tools Used for Passive Recon (Top 25):**

1. **Google** - Search engine
2. **Wayback Machine** (archive.org) - Web archive
3. **DomainTools** - WHOIS & DNS
4. **SecurityTrails** - DNS & subdomain
5. **Censys** - Certificate & host search
6. **VirusTotal** - Domain/IP analysis
7. **Hunter.io** - Email finding
8. **HaveIBeenPwned** - Breach checking
9. **Maltego** - Relationship mapping
10. **Shodan** - Device search (passive queries)
11. **Recon-ng** - Automated framework
12. **Spiderfoot** - Automated OSINT
13. **TheHarvester** - Email/subdomain enumeration
14. **crt.sh** - Certificate search
15. **Pipl** - People search
16. **Clearbit** - Email/company data
17. **Robtex** - DNS/IP research
18. **OSINT Framework** - Tool compilation
19. **IntelligenceX** - Search engine for leaks
20. **Dehashed** - Breach database
21. **TinEye** - Reverse image search
22. **FOCA** - Metadata extraction
23. **Exiftool** - Metadata analysis
24. **Social-Searcher** - Multi-platform search
25. **Bellingcat Toolkit** - Visual investigation

---

---

# SECTION 4: 100 ACTIVE RECONNAISSANCE TECHNIQUES

---

## **ACTIVE RECON - DIRECT INTERACTION, HIGH DETECTION RISK**

### **Category 1: Port Scanning & Service Enumeration (12 techniques)**

101. **Nmap basic port scan** (TCP SYN scan)
102. **Nmap UDP port scan** (UDP service discovery)
103. **Nmap service version detection** (-sV flag)
104. **Nmap OS detection** (-O flag)
105. **Nmap aggressive scanning** (-A flag with version, OS, scripts)
106. **Nmap script scanning** (NSE - Nmap Scripting Engine)
107. **Nmap vulnerability scanning** (vuln scripts)
108. **Masscan for rapid port scanning** (Fast port discovery)
109. **Zmap for internet-wide scanning** (Large-scale port scanning)
110. **Nessus vulnerability scanning** (Comprehensive vulnerability assessment)
111. **OpenVAS scanning** (Open-source vulnerability scanner)
112. **GVM (Greenbone Vulnerability Manager)** (Advanced scanning)

---

### **Category 2: Web Application Scanning (12 techniques)**

113. **Burp Suite web crawling** (Mapping application)
114. **Burp Suite active scanning** (Vulnerability detection)
115. **OWASP ZAP active scanning** (Web app vulnerability scanning)
116. **Nikto web server scanning** (Web server vulnerability check)
117. **WPScan for WordPress** (WordPress vulnerability scanning)
118. **Joomscan for Joomla** (Joomla vulnerability scanning)
119. **Drupal security scanning** (Drupal-specific checks)
120. **SQLmap SQL injection testing** (Database vulnerability testing)
121. **XSStrike XSS vulnerability testing** (Cross-site scripting check)
122. **WAFW00F WAF detection** (Web Application Firewall detection)
123. **Wappalyzer technology detection** (Identifying web technologies)
124. **Whatweb web scanner** (Web server identification)

---

### **Category 3: DNS Enumeration & Brute Force (10 techniques)**

125. **DNS zone transfer attempts** (AXFR requests)
126. **DNS brute force attacks** (Sublist3r, Amass active mode)
127. **DNS wildcard detection** (Testing for wildcard records)
128. **DNS NSEC walking** (DNS enumeration via NSEC records)
129. **DNS DIG queries** (Direct DNS queries)
130. **DNS NSLOOKUP queries** (Direct DNS interrogation)
131. **DNS reverse lookup brute force** (Reverse IP enumeration)
132. **DNS cache snooping** (DNS recursion abuse)
133. **Dnsrecon enumeration** (Multi-technique DNS tool)
134. **Fierce DNS enumeration** (Subdomain brute force)

---

### **Category 4: Network Mapping & Traceroute (8 techniques)**

135. **Traceroute to target** (Route path discovery)
136. **MTR (My Traceroute)** (Continuous route analysis)
137. **Ping sweeps** (Network host discovery)
138. **ARP scanning** (Local network host discovery)
139. **Network topology mapping** (Graphing network structure)
140. **BGP route analysis** (Tracing AS paths)
141. **Ping sweep with nmap** (Host discovery)
142. **ICMP echo requests** (Ping probes)

---

### **Category 5: Email & SMTP Enumeration (9 techniques)**

143. **SMTP user enumeration** (VRFY, EXPN commands)
144. **SMTP banner grabbing** (Server version identification)
145. **Email address verification** (Sending test emails)
146. **SMTP open relay testing** (Testing for relay vulnerabilities)
147. **Email header analysis** (Sending test messages)
148. **SPF record testing** (Mail authentication check)
149. **DKIM record testing** (Email signature verification)
150. **DMARC record testing** (Email policy checking)
151. **Haraka SMTP testing** (Direct SMTP probing)

---

### **Category 6: Directory & File Enumeration (11 techniques)**

152. **Directory brute force with Gobuster** (Common directory discovery)
153. **Directory enumeration with DirBuster** (Web directory scanning)
154. **Directory fuzzing with Fuff** (Fast fuzzing)
155. **Parameter fuzzing** (Testing unknown parameters)
156. **File enumeration with extensions** (.bak, .old, .tmp)
157. **Hidden file discovery** (.git, .svn folders)
158. **Backup file detection** (*.backup, *.sql)
159. **Configuration file discovery** (web.config, config.php)
160. **Source code exposure checks** (.env, .htaccess)
161. **API endpoint discovery** (/api/v1/, /api/v2/)
162. **Admin panel discovery** (/admin, /administrator)

---

### **Category 7: SSL/TLS Certificate Enumeration (8 techniques)**

163. **SSL certificate grabbing** (openssl s_client)
164. **Certificate validity checking** (Expiration date verification)
165. **Certificate chain analysis** (Full cert path examination)
166. **Cipher suite enumeration** (nmap, ssllabs)
167. **TLS version detection** (sslscan, testssl.sh)
168. **SSL/TLS vulnerability scanning** (Heartbleed, POODLE check)
169. **Certificate pinning detection** (Testing for pinning)
170. **Self-signed certificate identification** (Cert validation checks)

---

### **Category 8: Credential & Authentication Testing (10 techniques)**

171. **Default credential testing** (Common username/password pairs)
172. **Hydra brute force** (Multi-protocol password cracking)
173. **Medusa brute force** (Parallel password testing)
174. **Hashcat offline cracking** (Hash password cracking)
175. **John the Ripper** (Password cracking)
176. **Dictionary attacks** (Password list testing)
177. **Common password lists** (rockyou.txt, etc.)
178. **Credential spraying** (Multiple username/password attempts)
179. **OAuth token testing** (Bearer token analysis)
180. **API key discovery** (Scanning for exposed keys)

---

### **Category 9: Shodan & Internet Search Scanning (8 techniques)**

181. **Shodan API queries** (Device search)
182. **Shodan filters for vulnerabilities** (Vulnerable device search)
183. **Censys API queries** (Host & certificate search)
184. **ZoomEye scanning** (Chinese search engine for devices)
185. **Censys.io host probing** (Direct device enumeration)
186. **Internet-wide scanning** (Zmap for specific ports)
187. **IoT device discovery** (Searching for specific devices)
188. **Industrial control system scanning** (SCADA device detection)

---

### **Category 10: Virtual Host Enumeration (7 techniques)**

189. **Host header enumeration** (Testing different Host headers)
190. **Virtual host brute force** (Testing subdomain variations)
191. **SNI (Server Name Indication) enumeration** (TLS SNI probing)
192. **Reverse DNS lookups** (IP to hostname mapping)
193. **HTTP method testing** (OPTIONS, TRACE, etc.)
194. **Vhost scanning with Burp** (Web app virtual host discovery)
195. **Subdomain takeover scanning** (Finding vulnerable subdomains)

---

### **Category 11: Crawling & Spidering (7 techniques)**

196. **Burp Suite Spider** (Web application crawling)
197. **OWASP ZAP Spider** (Automated crawling)
198. **Wget recursive download** (Full site mirroring)
199. **Curl with follow redirects** (Manual page discovery)
200. **Python Scrapy** (Custom crawling scripts)
201. **Selenium browser automation** (JavaScript-enabled crawling)
202. **HTTrack website copying** (Full site mirroring)

---

### **Category 12: Database Scanning & Enumeration (8 techniques)**

203. **SQL injection vulnerability scanning** (SQLmap)
204. **Database version detection** (SQL injection for version)
205. **Database user enumeration** (SQL queries)
206. **Database table discovery** (Schema enumeration)
207. **Database credential testing** (Direct database connection)
208. **Oracle database scanning** (TNS listener probing)
209. **MongoDB unauth access testing** (Direct connection attempts)
210. **MySQL unauth access testing** (Default credential attempts)

---

### **Category 13: Firewall & IDS Evasion Testing (9 techniques)**

211. **Firewall rule testing** (Packet filtering checks)
212. **IDS evasion techniques** (Fragmentation, spoofing)
213. **WAF evasion methods** (Web Application Firewall bypass)
214. **Proxy detection** (Testing for proxy presence)
215. **Rate limiting detection** (Testing request thresholds)
216. **Bot detection evasion** (User-agent manipulation)
217. **Geo-blocking bypass** (VPN/proxy testing)
218. **DDoS protection detection** (Cloudflare, Akamai detection)
219. **Anti-bot detection** (CAPTCHA, JavaScript challenges)

---

### **Category 14: Exploit & Vulnerability Testing (9 techniques)**

220. **Known CVE testing** (Exploiting known vulnerabilities)
221. **Metasploit exploit modules** (Vulnerability exploitation)
222. **Custom exploit development** (Creating specific exploits)
223. **Buffer overflow testing** (Memory vulnerability checks)
224. **Format string attacks** (Printf vulnerability testing)
225. **Command injection testing** (OS command execution)
226. **Path traversal testing** (Directory traversal attacks)
227. **LDAP injection testing** (LDAP query manipulation)
228. **XXE (XML External Entity) testing** (XML vulnerability checks)

---

### **Category 15: Wireless & Network Protocol Scanning (8 techniques)**

229. **WiFi network scanning** (Aircrack-ng, kismet)
230. **WiFi WEP/WPA cracking** (Aircrack-ng)
231. **Bluetooth scanning** (Bluetoothctl, bleah)
232. **SNMP enumeration** (UDP port 161 probing)
233. **SNMP community string brute force** (Default credentials)
234. **NetBIOS enumeration** (nmblookup, nbtscan)
235. **SMB enumeration** (smbclient, enum4linux)
236. **LDAP enumeration** (ldapsearch, LdapMiner)

---

### **Category 16: API Endpoint Testing (9 techniques)**

237. **API endpoint discovery** (Burp Suite, Postman)
238. **API authentication testing** (Bearer token checks)
239. **API rate limiting bypass** (Header manipulation)
240. **API parameter fuzzing** (Testing various parameters)
241. **API response analysis** (Error message disclosure)
242. **GraphQL introspection** (Schema enumeration)
243. **REST API enumeration** (Endpoint discovery)
244. **API version detection** (Version identification)
245. **API documentation discovery** (/docs, /swagger, /graphql)

---

### **Category 17: Privilege Escalation Testing (7 techniques)**

246. **Local file inclusion (LFI) testing** (File read vulnerabilities)
247. **Remote file inclusion (RFI) testing** (Remote code execution)
248. **Sudo privilege testing** (Privilege escalation via sudo)
249. **SUID binary enumeration** (Special permission checks)
250. **Kernel vulnerability testing** (OS-level exploit testing)
251. **Misconfiguration exploitation** (Service privilege abuse)
252. **Weak password policy testing** (Password strength checks)

---

### **Category 18: Source Code & Configuration Exposure (8 techniques)**

253. **Git repository exposure** (.git folder access)
254. **SVN repository exposure** (.svn folder access)
255. **Backup file discovery** (web.config.bak, config.php.bak)
256. **Environment variable exposure** (.env files)
257. **Private key discovery** (SSH keys, API keys)
258. **Hardcoded credentials discovery** (Credentials in code)
259. **Build file analysis** (pom.xml, package.json, Dockerfile)
260. **Docker container enumeration** (Image scanning)

---

### **Category 19: Client-Side Vulnerability Testing (7 techniques)**

261. **Reflected XSS testing** (Cookie/session stealing)
262. **Stored XSS testing** (Persistent script injection)
263. **DOM-based XSS testing** (Client-side script manipulation)
264. **CSRF testing** (Cross-site request forgery)
265. **Session fixation testing** (Session hijacking)
266. **Clickjacking testing** (UI redressing)
267. **Insecure deserialization testing** (Object injection)

---

### **Category 20: Infrastructure & Cloud Testing (10 techniques)**

268. **AWS S3 bucket enumeration** (Cloud storage discovery)
269. **Azure blob storage probing** (Cloud storage testing)
270. **GCP bucket enumeration** (Google Cloud storage)
271. **Cloud IAM role enumeration** (Permission discovery)
272. **CDN configuration testing** (Content delivery network checks)
273. **Cloud function discovery** (Serverless function enumeration)
274. **Load balancer detection** (ALB, NLB identification)
275. **DNS amplification testing** (DDoS vector check)
276. **NTP amplification testing** (DDoS vector check)
277. **Container registry scanning** (Docker Hub, ECR, ACR)

---

### **Tools Used for Active Recon (Top 30):**

1. **Nmap** - Port scanning & service enumeration
2. **Masscan** - Fast port scanning
3. **Burp Suite** - Web application testing
4. **OWASP ZAP** - Web vulnerability scanning
5. **Nikto** - Web server scanner
6. **SQLmap** - SQL injection testing
7. **Nessus** - Vulnerability assessment
8. **OpenVAS** - Open vulnerability scanner
9. **Metasploit** - Exploitation framework
10. **WPScan** - WordPress vulnerability scanner
11. **Joomscan** - Joomla vulnerability scanner
12. **Hydra** - Brute force password cracking
13. **Medusa** - Parallel password testing
14. **Hashcat** - GPU password cracking
15. **John the Ripper** - Password cracking
16. **Sublist3r** - Subdomain brute force
17. **Amass** - Subdomain enumeration
18. **Fierce** - DNS enumeration
19. **Dnsrecon** - DNS reconnaissance
20. **Dirb/Dirbuster** - Directory brute force
21. **Gobuster** - Directory/DNS/vhost brute force
22. **Ffuf** - Fast web fuzzer
23. **ZAProxy** - Web proxy & scanner
24. **Shodan CLI** - Internet search queries
25. **Censys API** - Host/certificate probing
26. **SSL Labs** - SSL/TLS testing
27. **testssl.sh** - TLS/SSL scanning
28. **OpenSSL** - Certificate examination
29. **Wireshark** - Network packet capture
30. **Aircrack-ng** - WiFi cracking suite

---

---

# COMPLETE SUMMARY

## **OSINT Framework Breakdown:**

| Category | Passive Techniques | Active Techniques | Risk Level |
|----------|-------------------|-------------------|------------|
| **Search & Web** | 12 | 12 | Low → High |
| **DNS & Network** | 18 | 18 | Low → High |
| **Social Media** | 12 | 0 | Low |
| **People Search** | 11 | 10 | Low → Medium |
| **Images & Metadata** | 10 | 0 | Low |
| **Company Research** | 10 | 10 | Low → Medium |
| **Scanning & Enumeration** | 0 | 90 | High |
| **Exploitation** | 0 | 30 | Critical |
| **Infrastructure** | 0 | 10 | High |
| **Total** | **100** | **100+** | Varies |

---

## **Best Practices:**

✅ Always start with **Passive Recon** first  
✅ **Document everything** for chain of custody  
✅ Use **VPN/TOR** for anonymity in active recon  
✅ **Get written permission** before active scanning  
✅ Know your **legal jurisdiction** (CFAA in US, GDPR in EU)  
✅ **Cross-reference** multiple sources  
✅ Keep findings **organized and searchable**  
✅ Maintain **operational security (OpSec)**  

---

This comprehensive guide covers everything from the absolute basics of OSINT through 100 passive reconnaissance techniques, 100+ active reconnaissance techniques, and all essential tools!
