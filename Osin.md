# The OSINT Master Guide
### Methodology, Mindset, Recon Techniques, Tools & Google Dorks

---

## 1. What is OSINT?

**Open Source Intelligence (OSINT)** is the practice of collecting, processing, and analyzing publicly available information to produce actionable intelligence. "Open source" doesn't mean free or informal — it means the information is legally and openly accessible: no hacking, no unauthorized access, no social engineering that crosses legal lines.

OSINT draws from:
- Websites, blogs, forums, and social media
- Public records (business registries, court filings, property records)
- Search engines and their cached/indexed data
- DNS, WHOIS, and internet infrastructure metadata
- Images, videos, geolocation metadata
- Code repositories, paste sites, breach databases (for defensive/awareness purposes)
- Academic papers, news archives, government publications

OSINT is used by security researchers (attack surface mapping, red teaming, bug bounty recon), journalists (investigations), law enforcement, threat intelligence teams, due diligence analysts, and individuals doing digital self-audits.

> **Legal & ethical note:** OSINT should only be performed on information that is publicly accessible and, where applicable, within the scope of authorization (e.g., an approved penetration test or bug bounty program). Always respect terms of service, privacy laws (GDPR, CCPA, etc.), and platform rules. This guide is for defensive security, authorized testing, journalism, and research purposes.

---

## 2. The OSINT Mindset

1. **Curiosity over assumption** — every data point raises two more questions. Don't stop at the first answer.
2. **Patience** — good OSINT is iterative, not a single search. Depth beats speed.
3. **Skepticism** — verify everything. Social media bios lie, WHOIS data is often stale or privacy-masked, screenshots can be faked.
4. **Pattern recognition** — usernames, writing style, photo backgrounds, and posting times all correlate identities across platforms.
5. **Documentation discipline** — record sources, timestamps, and screenshots as you go. If you can't prove where a fact came from, it's not usable intelligence.
6. **OPSEC awareness** — your own footprint matters. Use sock puppet accounts, VPNs/VMs, and non-attributable infrastructure when appropriate to avoid tipping off a target or polluting your own results with personalization bias.
7. **Ethical restraint** — just because information *can* be found doesn't mean it *should* be used, published, or acted on without a legitimate purpose.

---

## 3. Planning & Methodology

A structured OSINT engagement follows an intelligence cycle:

### Step 1 — Define Objectives (PIRs)
Set **Priority Intelligence Requirements**: What exactly do you need to know? (e.g., "map the external attack surface of company X" or "verify the identity behind this account"). Vague goals produce noisy, unusable results.

### Step 2 — Scoping
- Define what's in-scope (domains, people, organizations) and explicitly out-of-scope.
- Identify legal/ethical boundaries.
- Set a time budget — OSINT can expand infinitely; timebox each phase.

### Step 3 — Source Identification
List candidate sources: search engines, social platforms, public records, technical databases (DNS/WHOIS/certificate transparency), code repos, etc.

### Step 4 — Collection (Passive → Active)
Always start **passive** (zero-touch, no direct interaction with the target) before moving to **active** (direct interaction, e.g., port scanning, visiting the target's own site directly). This preserves stealth and avoids alerting the target prematurely.

### Step 5 — Processing & Normalization
Convert raw findings into structured data: spreadsheets, link-analysis graphs (Maltego, Neo4j), timelines. Deduplicate and tag by confidence level.

### Step 6 — Analysis
Correlate data points. Look for overlaps: shared emails, reused usernames, shared infrastructure (IP/ASN/certs), shared writing style, shared images (reverse image search).

### Step 7 — Verification
Cross-reference every key finding with at least 2 independent sources before treating it as fact. Assign confidence levels (Confirmed / Probable / Possible / Unverified).

### Step 8 — Reporting / Dissemination
Present findings clearly: executive summary, methodology, evidence, confidence ratings, and — for security engagements — remediation recommendations.

### Step 9 — OPSEC Review
Clean up: close sock puppets appropriately, secure your collected data, and consider whether your activity left any trace on target-controlled systems.

---

## 4. What to Gain First — Priority Order

When starting a new target (person, company, or domain), gather in this order:

1. **Root identifiers** — primary domain(s), full legal name, known aliases/usernames, or company registration details.
2. **Infrastructure map** — subdomains, IP ranges, ASN, hosting provider, DNS records, mail servers.
3. **People map** — employees, executives, org chart (via LinkedIn), personal usernames tied to the org.
4. **Digital footprint** — social media accounts, forums, code repositories, breach exposure.
5. **Technology stack** — CMS, frameworks, exposed services, cloud providers (via Wappalyzer, BuiltWith, Shodan).
6. **Physical/geolocation data** — office locations, EXIF metadata, image geolocation.
7. **Historical data** — archived versions of sites/profiles (Wayback Machine) to see what changed and when.
8. **Relationship graph** — connections between people, companies, and infrastructure that reveal the bigger picture.

---

## 5. Passive & Active Recon — 100 Essential Techniques

Passive recon = no direct interaction with target-owned systems (uses third parties/caches). Active recon = direct interaction with target infrastructure (still legal/public, but detectable).

### A. Passive Recon (1–50)

1. WHOIS lookup on root domain
2. Historical WHOIS lookup (via WhoisFreaks/DomainTools history)
3. Reverse WHOIS (find other domains registered by same email/org)
4. DNS record enumeration via public resolvers (A, MX, TXT, NS, SPF, DMARC)
5. Passive DNS history lookup (SecurityTrails, RiskIQ)
6. Certificate Transparency log search (crt.sh) for subdomains
7. Wayback Machine snapshot review of target site
8. Google cache review of pages
9. Search engine dorking (see Section 6)
10. Shodan passive search (no active probe) for exposed assets
11. Censys passive search for certs/services
12. BuiltWith / Wappalyzer technology fingerprinting
13. LinkedIn employee enumeration
14. LinkedIn job postings analysis (reveals tech stack, growth areas)
15. Company registry lookup (state Secretary of State, Companies House, OpenCorporates)
16. SEC EDGAR filings review (for public companies)
17. Patent and trademark database search (USPTO, WIPO)
18. Court records / PACER search
19. Social media username enumeration across platforms
20. Reverse image search (Google Images, TinEye, Yandex)
21. EXIF metadata extraction from public images
22. Public GitHub/GitLab repo review for the org
23. GitHub code search for leaked secrets/keys (dorking)
24. Paste site monitoring (Pastebin search engines)
25. Breach database lookup (Have I Been Pwned, DeHashed) for exposure awareness
26. Google Alerts setup for ongoing monitoring
27. RSS/news feed monitoring for target mentions
28. Public financial disclosures / annual reports review
29. Job board scraping for internal tool/vendor names
30. Glassdoor/Indeed reviews for internal process leaks
31. Domain typosquat enumeration (dnstwist, urlcrazy — passive generation)
32. Subdomain enumeration via public datasets (crt.sh, SecurityTrails, VirusTotal passive DNS)
33. ASN and IP range lookup (BGP.he.net, RIPE, ARIN)
34. Netblock ownership lookup
35. Mail exchanger (MX) provider identification
36. SPF/DMARC record analysis for third-party mail services used
37. Social media metadata (post times → timezone inference)
38. Forum and community post history review
39. Archived job listings for org structure clues
40. Google Maps/Street View public imagery review
41. Public Wi-Fi SSID databases (WiGLE) for physical location correlation
42. Public code documentation/API docs review
43. NPM/PyPI package registry search for org-published packages
44. Public Slack/Discord invite link discovery (via dorking)
45. Academic paper/author search (Google Scholar) for research staff
46. Conference talk/speaker bio review
47. Public bug bounty program scope review (HackerOne, Bugcrowd directories)
48. Domain generation pattern analysis from known subdomains
49. Third-party trust/vendor page review ("who we work with" pages)
50. Wayback Machine diff analysis (compare snapshots over time to detect changes)

### B. Active Recon (51–100)

*(All performed only within authorized/legal scope)*

51. Direct visit to target website (headers, cookies, robots.txt, sitemap.xml)
52. robots.txt and sitemap.xml manual review
53. HTTP response header analysis (server, tech stack banners)
54. SSL/TLS certificate inspection (subject alt names reveal subdomains)
55. DNS zone transfer attempt (AXFR — only if authorized)
56. Live subdomain brute-forcing (Sublist3r, Amass active mode)
57. Port scanning (Nmap) within authorized scope
58. Service/banner grabbing on open ports
59. Web crawling/spidering the target site (Burp Suite, ZAP spider)
60. Directory/file brute-forcing (ffuf, gobuster, dirb)
61. Technology fingerprinting via active probing (WhatWeb)
62. Favicon hash lookup (Shodan favicon search) to find related assets
63. HTTP methods enumeration (OPTIONS, TRACE)
64. Login page/portal discovery via crawling
65. Form field enumeration for input validation review
66. API endpoint discovery (active crawling + JS analysis)
67. JavaScript file analysis for hidden endpoints/keys
68. Cookie and session token analysis
69. CMS version fingerprinting (WordPress, Drupal scanners)
70. Plugin/module enumeration on CMS platforms
71. Error message triggering to fingerprint backend stack
72. Web application firewall (WAF) detection/fingerprinting
73. Content Security Policy (CSP) header review for third-party domains
74. Cross-Origin Resource Sharing (CORS) policy review
75. Email harvesting from live site contact forms (with authorization)
76. Active social engineering-adjacent recon (e.g., calling published numbers to confirm business hours — only if in-scope)
77. Physical site visit/observation (for authorized red team engagements)
78. Wireless network scanning near target premises (authorized only)
79. Active subdomain takeover testing (checking for dangling DNS records)
80. Cloud storage bucket enumeration (S3, Azure Blob, GCS) for misconfigured public access
81. Cloud metadata endpoint testing (only in authorized cloud pentest scope)
82. API rate-limit/behavior testing to map API surface
83. GraphQL introspection query testing (if enabled)
84. Active WHOIS refresh queries against registrar servers
85. Traceroute/path analysis to map network topology
86. Active certificate transparency monitoring for newly issued certs
87. Live crawling of linked third-party/vendor domains
88. Session/cookie fixation and expiry testing
89. Login brute-force *rate* testing (non-destructive, authorized only) to assess lockout policy
90. Active fuzzing of URL parameters for reflected input
91. File upload endpoint testing for type/size validation
92. Active DNS cache snooping (authorized recursive resolvers only)
93. SNMP/UPnP scanning on exposed network devices (authorized only)
94. VPN endpoint fingerprinting
95. Mobile app APK/IPA download and static analysis for endpoints/keys
96. Mobile app network traffic interception (authorized test devices)
97. IoT device banner scanning within scope
98. Active email deliverability testing (SPF/DKIM alignment checks by sending test mail)
99. Active social media interaction testing (e.g., verifying support bot behavior) within platform ToS
100. Live re-verification of all passive findings to confirm they're still current before reporting

---

## 6. 100 Essential Google Dorks

Google dorking uses advanced search operators to surface indexed content not easily found through normal searches. Use responsibly and only against in-scope/authorized targets or your own assets.

### Core Operators Reference
`site:` `inurl:` `intitle:` `intext:` `filetype:` `ext:` `cache:` `related:` `link:` `AROUND(n)` `"exact phrase"` `-exclude` `OR` `*wildcard*`

### A. Site & Subdomain Discovery
1. `site:example.com`
2. `site:*.example.com`
3. `site:example.com -www`
4. `site:example.com inurl:admin`
5. `site:example.com inurl:login`
6. `site:example.com inurl:dashboard`
7. `site:example.com inurl:portal`
8. `site:example.com inurl:staging`
9. `site:example.com inurl:dev`
10. `site:example.com inurl:test`

### B. File & Document Exposure
11. `site:example.com filetype:pdf`
12. `site:example.com filetype:xls OR filetype:xlsx`
13. `site:example.com filetype:doc OR filetype:docx`
14. `site:example.com filetype:ppt OR filetype:pptx`
15. `site:example.com filetype:txt`
16. `site:example.com filetype:csv`
17. `site:example.com filetype:xml`
18. `site:example.com filetype:sql`
19. `site:example.com filetype:log`
20. `site:example.com filetype:bak`
21. `site:example.com filetype:conf OR filetype:cfg`
22. `site:example.com filetype:env`
23. `site:example.com filetype:json`
24. `site:example.com filetype:yml OR filetype:yaml`
25. `site:example.com ext:php intitle:"index of"`

### C. Login & Sensitive Portals
26. `site:example.com intitle:"login"`
27. `site:example.com intitle:"admin panel"`
28. `site:example.com inurl:wp-admin`
29. `site:example.com inurl:phpmyadmin`
30. `site:example.com inurl:cpanel`
31. `site:example.com inurl:webmail`
32. `site:example.com intitle:"index of" "parent directory"`
33. `site:example.com intitle:"index of /backup"`
34. `site:example.com intitle:"index of /.git"`
35. `site:example.com inurl:swagger`

### D. Exposed Credentials & Secrets
36. `site:example.com "password" filetype:log`
37. `site:example.com "api_key" filetype:env`
38. `site:example.com "BEGIN RSA PRIVATE KEY"`
39. `site:example.com "aws_access_key_id"`
40. `site:pastebin.com "example.com" password`
41. `site:github.com "example.com" api_key`
42. `site:github.com "example.com" secret`
43. `site:trello.com "example.com"`
44. `site:docs.google.com "example.com"`
45. `intext:"index of" "credentials.txt"`

### E. Error Messages & Debug Info
46. `site:example.com "sql syntax near"`
47. `site:example.com "Warning: mysql_connect()"`
48. `site:example.com "PHP Fatal error"`
49. `site:example.com "stack trace"`
50. `site:example.com intext:"debug mode"`

### F. Employee & Contact Info
51. `site:linkedin.com/in "example.com"`
52. `site:example.com filetype:pdf "confidential"`
53. `site:example.com intext:"@example.com"`
54. `"@example.com" filetype:xls`
55. `site:example.com intitle:"staff directory"`

### G. Cloud & Infrastructure Leakage
56. `site:s3.amazonaws.com "example"`
57. `inurl:blob.core.windows.net "example"`
58. `site:storage.googleapis.com "example"`
59. `intitle:"index of" "docker-compose.yml"`
60. `site:example.com inurl:.aws/credentials`
61. `site:example.com inurl:.ssh/id_rsa`
62. `intitle:"index of" ".env"`
63. `site:example.com intitle:"Kibana"`
64. `site:example.com intitle:"Grafana"`
65. `site:example.com inurl:jenkins`

### H. Network & Device Exposure
66. `intitle:"webcamXP"`
67. `intitle:"IP Camera" inurl:view/view.shtml`
68. `intitle:"index of" "router config"`
69. `site:example.com inurl:printer`
70. `intitle:"Remote Desktop Web Connection"`

### I. CMS-Specific Dorks
71. `site:example.com inurl:wp-content`
72. `site:example.com inurl:wp-json`
73. `site:example.com "powered by WordPress"`
74. `site:example.com inurl:/sites/default/files` (Drupal)
75. `site:example.com "powered by Joomla"`

### J. Social Media & Forums
76. `site:twitter.com "example.com"`
77. `site:reddit.com "example.com"`
78. `site:facebook.com "example.com"`
79. `site:instagram.com "example.com"`
80. `site:stackoverflow.com "example.com" error`

### K. Historical / Cached Content
81. `cache:example.com`
82. `site:web.archive.org example.com`
83. `related:example.com`
84. `site:example.com "this page has been removed"`
85. `site:example.com intitle:"index of" -inurl:(htm|html)`

### L. Vulnerability-Indicator Dorks
86. `site:example.com inurl:?id= intext:"SQL syntax"`
87. `site:example.com inurl:.php?page=`
88. `site:example.com inurl:download.php?file=`
89. `site:example.com "not for public release"`
90. `site:example.com "internal use only" filetype:pdf`

### M. Broad Combination Dorks
91. `site:example.com (inurl:login OR inurl:signin) filetype:php`
92. `site:example.com (intitle:"index of" OR intitle:"directory listing")`
93. `"example.com" ("confidential" OR "internal only") filetype:pdf`
94. `site:example.com (ext:sql OR ext:db OR ext:bak) intitle:"index of"`
95. `site:example.com -site:www.example.com "index of"`
96. `intext:"example.com" intext:"password" -site:example.com`
97. `site:example.com intitle:"index of" "wp-config.php.bak"`
98. `site:example.com "X-Powered-By"`
99. `site:example.com inurl:api/v1`
100. `site:example.com filetype:json "api_key" OR "token" OR "secret"`

---

## 7. 25 Types of OSINT

OSINT isn't one discipline — it branches into specialized categories, each with its own techniques, tools, and data sources.

1. **Username OSINT** — tracing a single handle across platforms to map an identity (Sherlock, Whatsmyname).
2. **Email OSINT** — verifying, tracing, and finding accounts tied to an email address (Hunter.io, Holehe, EmailRep).
3. **Phone Number OSINT** — carrier lookup, owner tracing, linked-account discovery (Truecaller, NumLookup).
4. **People/Identity OSINT** — building a full profile of a person from aliases, addresses, and relatives (Pipl, Spokeo, TruePeopleSearch).
5. **Domain & DNS OSINT** — WHOIS, DNS records, hosting history, and passive DNS mapping.
6. **Subdomain/Infrastructure OSINT** — enumerating an organization's full internet-facing footprint.
7. **IP Address OSINT** — geolocation, ASN ownership, and reverse IP lookups.
8. **Social Media OSINT (SOCMINT)** — profile analysis, post history, follower/following graphs, sentiment.
9. **Image OSINT** — reverse image search, EXIF metadata, visual landmark identification.
10. **Geolocation OSINT (GEOINT-lite)** — pinpointing where a photo/video was taken from shadows, signage, terrain.
11. **Video OSINT** — frame-by-frame analysis, reverse video search, metadata extraction from clips.
12. **Corporate/Business OSINT** — company registries, ownership structures, filings, subsidiaries.
13. **Financial OSINT (FININT-lite)** — public financial disclosures, stock filings, funding rounds, sanctions lists.
14. **Dark Web OSINT** — monitoring onion sites, leak forums, and marketplaces for exposure.
15. **Breach/Credential OSINT** — checking exposed credentials and leaked databases tied to a target.
16. **Code Repository OSINT** — searching GitHub/GitLab for leaked secrets, internal tool names, and dev practices.
17. **Document/Metadata OSINT** — extracting authorship, software version, and edit history from public files.
18. **Academic OSINT** — tracing publications, co-authors, and institutional affiliations (Google Scholar, ORCID).
19. **Government/Public Records OSINT** — court records, property records, voter rolls, licensing databases.
20. **News & Media OSINT** — archived news, press releases, and journalist source-tracing.
21. **Historical/Archive OSINT** — Wayback Machine and cache analysis to track how a target has changed over time.
22. **Wireless/Physical OSINT** — Wi-Fi SSID mapping (WiGLE), Bluetooth device discovery near a location.
23. **Mobile App OSINT** — analyzing public APKs/IPAs for endpoints, permissions, and embedded secrets.
24. **Threat Intelligence OSINT (CTI)** — tracking malware indicators, threat actor infrastructure, and TTPs from open feeds.
25. **Cross-Platform Correlation OSINT** — the "meta" discipline of linking findings from all categories above into a single identity/entity graph (what tools like Maltego are built for).

---

## 8. 100 Best OSINT Tools

### A. General Frameworks & Aggregators (1–10)
1. Maltego — link analysis & entity graphing
2. SpiderFoot — automated OSINT reconnaissance
3. theHarvester — email/subdomain/name harvesting
4. Recon-ng — modular recon framework
5. OSINT Framework (osintframework.com) — curated tool directory
6. Datasploit — automated OSINT collection
7. IntelTechniques Tools (Michael Bazzell's suite)
8. Sherlock — username search across platforms
9. OSRFramework — username/domain/email OSINT suite
10. FinalRecon — all-in-one web recon tool

### B. Domain / DNS / Infrastructure (11–25)
11. WHOIS (whois.domaintools.com)
12. SecurityTrails — passive DNS/history
13. crt.sh — Certificate Transparency search
14. DNSDumpster
15. Amass (OWASP) — subdomain enumeration
16. Sublist3r
17. Censys — internet-wide scan search engine
18. Shodan — internet-connected device search
19. BGP.he.net — ASN/netblock lookup
20. ViewDNS.info
21. dnstwist — typosquat detection
22. MXToolbox — mail server diagnostics
23. Netcraft — site profiling & phishing intel
24. Wayback Machine (archive.org)
25. FOFA — Chinese Shodan-equivalent search engine

### C. Web Recon & Fingerprinting (26–35)
26. Wappalyzer — tech stack fingerprinting
27. BuiltWith — tech stack profiling
28. WhatWeb
29. Nikto — web server scanner
30. Burp Suite — web proxy/spider/scanner
31. OWASP ZAP — web app scanner
32. ffuf — fast web fuzzer
33. Gobuster — directory/DNS brute-forcer
34. HTTrack — website mirroring
35. Wafw00f — WAF fingerprinting

### D. Network Scanning (36–42)
36. Nmap — network/port scanner
37. Masscan — high-speed port scanner
38. Zenmap — Nmap GUI
39. Netcat — network utility
40. Angry IP Scanner
41. RustScan — fast port scanner
42. Unicornscan

### E. Social Media Intelligence (43–58)
43. Sherlock — username enumeration
44. Social Analyzer
45. Twint — Twitter/X intelligence (archived, mirrors exist)
46. Whatsmyname.app — username search
47. NameCheckup.com
48. LinkedIn Sales Navigator (for public profile research)
49. Followerwonk — Twitter/X analytics
50. Social Searcher
51. Ghunt — Google account OSINT
52. Instaloader — Instagram data extraction
53. Facebook Graph Search-style queries (via Sowsearch/Stalkscan alternatives)
54. Snap Map (public Snapchat location data)
55. TikTok public profile analyzers
56. Pipl — people search engine
57. Spokeo — people search aggregator
58. TruePeopleSearch

### F. Image / Geolocation Intelligence (59–70)
59. Google Images reverse search
60. TinEye — reverse image search
61. Yandex Images — strong facial reverse search
62. ExifTool — metadata extraction
63. Jeffrey's Image Metadata Viewer
64. Google Earth Pro
65. Google Street View
66. SunCalc — shadow/sun position analysis for geolocation
67. Overpass Turbo (OpenStreetMap queries)
68. Geoguessr-style manual landmark analysis
69. Mapillary — crowd-sourced street imagery
70. WIGLE.net — Wi-Fi network geolocation database

### G. Email & Breach Intelligence (71–78)
71. Hunter.io — email discovery/verification
72. Have I Been Pwned — breach exposure check
73. DeHashed — breach data search
74. EmailRep.io — email reputation lookup
75. Epieos — email/account OSINT
76. Holehe — check email usage across platforms
77. VoilaNorbert — email finder
78. IntelX (Intelligence X) — leaked data & document search

### H. Code / Technical Repos (79–86)
79. GitHub code search
80. GitRob / Gitleaks — secret scanning in repos
81. TruffleHog — secrets scanner
82. GitLab public search
83. NPM registry search
84. PyPI search
85. Shodan Exploits/CVE search
86. VirusTotal — file/URL/domain reputation

### I. Corporate / Public Records (87–94)
87. OpenCorporates — global company registry
88. SEC EDGAR — public company filings
89. Companies House (UK)
90. USPTO / WIPO — patents & trademarks
91. PACER — US federal court records
92. Crunchbase — company/funding data
93. ZoomInfo — business contact intelligence
94. Glassdoor — employee reviews/org insights

### J. Dark Web & Threat Intel (95–100)
95. Ahmia — dark web search engine (Tor)
96. IntelX Dark Web module
97. Onion search engines (via Tor Browser)
98. Recorded Future — threat intelligence platform
99. AlienVault OTX — open threat exchange
100. Flashpoint — deep/dark web intelligence platform

---

## 9. Quick Reference: A Sample OSINT Workflow

```
1. Define target & objective
2. Passive domain/infra recon (WHOIS, DNS, crt.sh, Shodan passive)
3. Google dork sweep for exposed files/portals
4. People & social footprint mapping (LinkedIn, Sherlock, image search)
5. Technology stack fingerprinting (Wappalyzer, BuiltWith)
6. Breach/credential exposure check (HIBP, DeHashed)
7. Historical analysis (Wayback Machine, cert transparency history)
8. Active recon (only if authorized): port scan, directory brute-force, subdomain takeover check
9. Correlate & verify all findings (2+ source rule)
10. Build report: findings, evidence, confidence levels, recommendations
```

---

*This guide is intended for authorized security research, journalism, due diligence, and personal digital-footprint audits. Always operate within applicable laws and platform terms of service.*
