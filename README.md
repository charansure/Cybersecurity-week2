# 🔐 Week 02 – Footprinting & Network Scanning

![Cybersecurity](https://img.shields.io/badge/Domain-Cybersecurity-red)
![Internship](https://img.shields.io/badge/Internship-Networkwalks-green)
![Platform](https://img.shields.io/badge/Platform-Kali%20Linux-blue)
![Scanning](https://img.shields.io/badge/Network%20Scanning-Zenmap-orange)

## 📌 Project Overview

This project is part of my **Cybersecurity Internship at Networkwalks (Batch B084)**.

During Week 2, I completed two practical modules covering the first two phases of penetration testing:

- **Phase 1:** Reconnaissance & Footprinting
- **Phase 2:** Scanning & Network Discovery

The first activity involved performing footprinting and reconnaissance against the `networkwalks.com` domain using multiple Kali Linux tools.

The second activity involved scanning my own local LAN network using Zenmap (Nmap GUI) to discover active hosts and visualize the network topology.

All activities were conducted within the authorized scope for educational and cybersecurity training purposes.

## 🎯 Objectives

- Understand the reconnaissance and footprinting phases of penetration testing.
- Collect publicly available domain information using WHOIS.
- Identify website technologies using WhatWeb.
- Perform DNS lookups and identify domain IP addresses.
- Analyze HTTP response headers using cURL.
- Identify Web Application Firewall (WAF) technologies using Wafw00f.
- Enumerate DNS records using DNSRecon.
- Identify local network configuration and subnet information.
- Discover active hosts using Zenmap.
- Identify IP and MAC addresses.
- Generate and document network topology.

## 🛠️ Tools & Technologies Used

| Tool | Purpose |
|---|---|
| Kali Linux | Reconnaissance environment |
| WHOIS | Domain registration information |
| WhatWeb | Website technology fingerprinting |
| Nslookup | DNS resolution |
| cURL (`-I`) | HTTP response header inspection |
| Wafw00f | Web Application Firewall detection |
| DNSRecon | DNS record enumeration |
| Zenmap | Network scanning and host discovery |
| Nmap | Network discovery engine |
| Windows CMD | Local IP and MAC address identification |

## ⚙️ Activities Performed

### Phase 1: Reconnaissance & Footprinting

**Target:** `networkwalks.com`

Performed reconnaissance using six different Kali Linux tools to collect publicly available information about the target domain.

### 1. WHOIS – Domain Information Gathering

Used WHOIS to obtain publicly available domain registration information.

**Information examined:**
- Domain registration details.
- Registration and expiry dates.
- Registrar information.
- Domain name servers.
- Hosting-related information.

**Purpose:** Understand the publicly available registration and infrastructure information associated with a domain.

### 2. WhatWeb – Website Technology Fingerprinting

Used WhatWeb to identify technologies and components used by the target website.

**Key observations:**
- WordPress 7.0.4
- WP Download Manager 3.3.58
- Other web technology information exposed by the website.

**Purpose:** Identify the website's technology stack and understand what information can be discovered through technology fingerprinting.

### 3. Nslookup – DNS Resolution

Used Nslookup to resolve the domain name to its IP address.

**Observed result:**

`networkwalks.com` → `192.232.216.135`

**Purpose:** Understand DNS resolution and identify the IP address associated with the domain.

### 4. cURL – HTTP Response Header Analysis

Used the `curl -I` option to inspect the HTTP response headers.

**Key observation:**
- Retrieved HTTP response headers.
- Identified technical information exposed through the web server.
- Observed the WordPress REST API endpoint: `/wp-json/`.

**Purpose:** Understand how HTTP headers can reveal information about a web application and its configuration.

### 5. Wafw00f – Web Application Firewall Detection

Used Wafw00f to identify whether a Web Application Firewall was protecting the website.

**Observed result:**

`ModSecurity (SpiderLabs)`

**Purpose:** Understand WAF detection and identify the security technology protecting a web application.

### 6. DNSRecon – DNS Enumeration

Used DNSRecon to enumerate publicly available DNS records.

**Information examined:**
- NS records
- MX records
- SPF records
- TXT records
- SRV records
- DNS infrastructure information

**Purpose:** Understand how DNS enumeration helps identify domain infrastructure and related services.

---

### Phase 2: Network Scanning & Discovery

**Tool:** Zenmap (Nmap GUI)

For the second activity, I used Zenmap to perform network discovery on my local LAN environment.

### 7. Local IP and Subnet Identification

Used Windows Command Prompt to identify the local IP address and subnet information.

The identified subnet was then used as the target for the network discovery activity.

### 8. Network Scanning with Zenmap

Configured Zenmap with the target subnet and selected the **Ping Scan** profile to identify active hosts.

**Example scan observations documented in the practical:**

- `10.0.2.1`
- `10.0.2.2`
- `10.0.2.3`
- `10.0.2.15`

The practical also included MAC address information for the discovered hosts.

**Purpose:** Identify active devices within the authorized local network and understand basic network discovery.

### 9. Network Topology Visualization

After completing the scan:

- Opened the Topology section in Zenmap.
- Enabled the topology legend.
- Reviewed the discovered network hosts.
- Generated the network topology.
- Saved the topology in PDF format as required by the practical.

**Purpose:** Visualize discovered network devices and understand their representation within a network.

---

## 📊 Key Findings

The following findings were documented during the footprinting and scanning activities.

| Tool | Finding |
|---|---|
| WHOIS | Public domain registration and name server information |
| WhatWeb | WordPress 7.0.4 and WP Download Manager 3.3.58 |
| Nslookup | Domain resolved to 192.232.216.135 |
| cURL | HTTP response headers and `/wp-json/` endpoint |
| Wafw00f | ModSecurity (SpiderLabs) identified |
| DNSRecon | DNS, mail and service-related records |
| Zenmap | Four example live hosts documented in the practical |

**Important:** The four Zenmap IP addresses above are the example results shown in the report. They should not be treated as independently verified actual network results unless confirmed against the original scan output.

## ⚠️ Risk Analysis

Based on the observations, the following potential risks were identified.

| # | Risk / Finding | Risk Level |
|---|---|---|
| 1 | Web technology information exposed | Medium |
| 2 | Server IP address identifiable | Low |
| 3 | HTTP technical information exposed | Low |
| 4 | WAF technology identifiable | Low |
| 5 | DNS infrastructure information exposed | Medium |
| 6 | Multiple live hosts visible on local network | Medium |

**Note:** These are observations from reconnaissance and scanning activities, not confirmed vulnerabilities. No exploitation or vulnerability validation was performed in these modules.

## 🛡️ Security Recommendations

Based on the observations, the following security improvements were recommended:

1. **Review publicly exposed technology information:** Regularly review publicly visible information about web technologies, CMS platforms and plugins.

2. **Keep software updated:** Update CMS platforms, plugins and other web technologies regularly.

3. **Review HTTP headers:** Check HTTP response headers to identify unnecessary technical information exposure.

4. **Review DNS records regularly:** Ensure only required DNS information and services are publicly exposed.

5. **Properly configure and monitor the WAF:** Keep ModSecurity enabled and properly configured.

6. **Perform regular internal network discovery:** Periodically scan authorized internal networks to identify active devices.

7. **Investigate unknown devices:** Verify unexpected devices discovered during network scanning.

8. **Maintain network documentation:** Keep network topology and device information documented and updated.

9. **Perform authorized security testing:** Conduct reconnaissance and scanning only on systems and networks where appropriate authorization has been provided.

## 📸 Screenshots & Evidence

The following screenshots document my Week 2 practical activities.

### Phase 1 – Footprinting & Reconnaissance

#### 1. WHOIS – Domain Information
![WHOIS](Screenshots/01-WHOIS.png)

#### 2. WhatWeb – Technology Fingerprinting
![WhatWeb](Screenshots/02-WhatWeb.png)

#### 3. Nslookup – DNS Resolution
![Nslookup](Screenshots/03-Nslookup.png)

#### 4. cURL – HTTP Response Headers
![cURL](Screenshots/04-Curl-Headers.png)

#### 5. Wafw00f – WAF Detection
![Wafw00f](Screenshots/05-Wafw00f.png)

#### 6. DNSRecon – DNS Enumeration
![DNSRecon](Screenshots/06-DNSRecon.png)

### Phase 2 – Network Scanning

#### 7. Zenmap – Host Discovery
![Zenmap Host Discovery](Screenshots/07-Zenmap-Host-Discovery.png)

#### 8. Zenmap – Network Topology
![Zenmap Network Topology](Screenshots/08-Zenmap-Network-Topology.png)

## 📚 Key Learnings

Through these practical activities, I gained hands-on knowledge of:

- Reconnaissance and footprinting techniques.
- Domain registration information gathering.
- Website technology fingerprinting.
- DNS resolution and enumeration.
- HTTP response header analysis.
- Web Application Firewall identification.
- Network scanning using Zenmap and Nmap.
- Live host discovery and network mapping.
- IP and MAC address identification.
- Network topology visualization.
- Risk identification and security recommendations.
- Professional penetration testing documentation.

## 🔒 Authorization & Disclaimer

All activities were performed within the authorized scope specified for the internship and on my own local LAN environment.

The footprinting and scanning exercises were conducted for educational and research purposes only.

No exploitation or vulnerability validation was performed during these activities.

Unauthorized access to systems and networks is prohibited. Always obtain appropriate permission before performing security assessments.

## 🙏 Acknowledgement

I would like to thank **Waqas Karim (CCIE)** and the **Networkwalks team** for their valuable guidance and support throughout the cybersecurity internship.

## 👨‍💻 Internship Information

- **Name:** Sure Sri Haricharan
- **Role:** Junior Penetration Tester Intern
- **Organization:** Networkwalks
- **Program:** Cybersecurity
- **Batch:** B084
- **Week:** 02
- **Modules:** W2-PM1 and W2-PM5
- **Project:** Footprinting & Network Scanning
- **Date:** 13 November 2026
- **LinkedIn:** https://www.linkedin.com/in/cscharan/

---

⭐ This project represents another step in my cybersecurity learning journey, helping me understand how reconnaissance and network discovery contribute to penetration testing.

**Week 02 Completed! More hands-on cybersecurity projects coming soon.** 🚀

#Networkwalks #Cybersecurity #Footprinting #Reconnaissance #KaliLinux #Zenmap #Nmap #PenetrationTesting
