# 🔎 Footprinting & Reconnaissance with Kali Linux

**NetworkWalks Cybersecurity & Ethical Hacking — Batch B083**  
**Week 02 | Project Module 1 (W2-PM1)**

This project documents practical **footprinting and reconnaissance** activities completed during NetworkWalks Week 02 using Kali Linux against `networkwalks.com`.

## 📚 Tasks, Results & Evidence

### 01 — WHOIS

```bash
whois networkwalks.com
```

**Result:** WHOIS returned domain registration details including GoDaddy as the registrar, registration and expiry dates, domain status, and nameservers. The registrant information was privacy-protected.

![WHOIS](https://github.com/cyberlynz/B083-W2-PM1-FOOTPRINTING-RECONNAISSANCE/raw/main/whois-screenshot.png)

[Task documentation](https://github.com/cyberlynz/B083-W2-PM1-FOOTPRINTING-RECONNAISSANCE/tree/main/task-01-whois) · [Command output](https://github.com/cyberlynz/B083-W2-PM1-FOOTPRINTING-RECONNAISSANCE/blob/main/task-01-whois/output.txt)

---

### 02 — WhatWeb

```bash
whatweb networkwalks.com
```

**Result:** WhatWeb identified Apache, WordPress 7.1, WordPress Download Manager, Bootstrap, jQuery, Google Tag Manager, and other web technologies. The HTTP version redirected to HTTPS, which returned `200 OK`.

![WhatWeb](https://github.com/cyberlynz/B083-W2-PM1-FOOTPRINTING-RECONNAISSANCE/raw/main/whatweb-screenshot.png)

[Task documentation](https://github.com/cyberlynz/B083-W2-PM1-FOOTPRINTING-RECONNAISSANCE/tree/main/task-02-whatweb) · [Command output](https://github.com/cyberlynz/B083-W2-PM1-FOOTPRINTING-RECONNAISSANCE/blob/main/task-02-whatweb/output.txt)

---

### 03 — NSLookup

```bash
nslookup networkwalks.com
```

**Result:** The lookup resolved `networkwalks.com` to **192.232.216.135**. The query also showed a timeout communicating with `8.8.8.8`, while a non-authoritative answer was returned.

![NSLookup](https://github.com/cyberlynz/B083-W2-PM1-FOOTPRINTING-RECONNAISSANCE/raw/main/nslookup-screenshot.png)

[Task documentation](https://github.com/cyberlynz/B083-W2-PM1-FOOTPRINTING-RECONNAISSANCE/tree/main/task-03-nslookup) · [Command output](https://github.com/cyberlynz/B083-W2-PM1-FOOTPRINTING-RECONNAISSANCE/blob/main/task-03-nslookup/output.txt)

---

### 04 — cURL

```bash
curl -I https://networkwalks.com
```

**Result:** The server returned **HTTP/2 200 OK**. The headers revealed Apache, WordPress-related endpoints and cookies, content type information, caching headers, and security-related policies.

![cURL](https://github.com/cyberlynz/B083-W2-PM1-FOOTPRINTING-RECONNAISSANCE/raw/main/curl-screenshot.png)

[Task documentation](https://github.com/cyberlynz/B083-W2-PM1-FOOTPRINTING-RECONNAISSANCE/tree/main/task-04-curl) · [Command output](https://github.com/cyberlynz/B083-W2-PM1-FOOTPRINTING-RECONNAISSANCE/blob/main/task-04-curl/output.txt)

---

### 05 — Wafw00f

```bash
wafw00f networkwalks.com
```

**Result:** Wafw00f identified **ModSecurity (SpiderLabs) WAF** protecting the website after two requests.

![Wafw00f](https://github.com/cyberlynz/B083-W2-PM1-FOOTPRINTING-RECONNAISSANCE/raw/main/wafw00f-screenshot.png)

[Task documentation](https://github.com/cyberlynz/B083-W2-PM1-FOOTPRINTING-RECONNAISSANCE/tree/main/task-05-wafw00f) · [Command output](https://github.com/cyberlynz/B083-W2-PM1-FOOTPRINTING-RECONNAISSANCE/blob/main/task-05-wafw00f/output.txt)

---

### 06 — DNSRecon

```bash
dnsrecon -d networkwalks.com
```

**Result:** DNSRecon discovered SOA, NS, MX, A, and SRV records. It resolved the main domain to **192.232.216.135**, identified mail infrastructure, and found **8 SRV records**. The scan also reported no answer for the DNSSEC query.

![DNSRecon](https://github.com/cyberlynz/B083-W2-PM1-FOOTPRINTING-RECONNAISSANCE/raw/main/dnsrecon-screenshot.png)

[Task documentation](https://github.com/cyberlynz/B083-W2-PM1-FOOTPRINTING-RECONNAISSANCE/tree/main/task-06-dnsrecon) · [Command output](https://github.com/cyberlynz/B083-W2-PM1-FOOTPRINTING-RECONNAISSANCE/blob/main/task-06-dnsrecon/output.txt)

## 🧠 What I Learned

- How WHOIS can be used to collect domain registration and nameserver information during passive reconnaissance.
- How WhatWeb helps identify technologies, frameworks, web servers, and other components exposed by a website.
- How NSLookup can resolve a domain to an IP address and show DNS query behaviour.
- How cURL can reveal useful HTTP response headers and information about server configuration.
- How Wafw00f can identify whether a website is protected by a Web Application Firewall and which WAF may be in use.
- How DNSRecon can enumerate different DNS records and provide a broader view of a domain's DNS infrastructure.
- Most importantly, how combining multiple reconnaissance tools provides a more complete picture than relying on a single tool.

## ✅ Evidence Checklist

| Task | Tool | Screenshot | Output |
|---|---|---|---|
| 01 | WHOIS | ✅ | ✅ |
| 02 | WhatWeb | ✅ | ✅ |
| 03 | NSLookup | ✅ | ✅ |
| 04 | cURL | ✅ | ✅ |
| 05 | Wafw00f | ✅ | ✅ |
| 06 | DNSRecon | ✅ | ✅ |

## 🔒 Security & Ethical Use

This project is for educational and authorised security testing only. Reconnaissance activities should be performed only against systems that are owned, provided for training, or explicitly authorised for testing.

## 📌 Project Information

| Item | Details |
|---|---|
| Training Program | NetworkWalks Cybersecurity & Ethical Hacking |
| Batch | B083 |
| Week | 02 |
| Project | W2-PM1 |
| Project Title | Footprinting & Reconnaissance Attacks with Multiple Kali Tools |
| Target | `networkwalks.com` |
| Author | Collins |

---

[← Back to NETWORKWALKS Internship](https://github.com/cyberlynz/NETWORKWALKS)  
[View Full Project Repository](https://github.com/cyberlynz/B083-W2-PM1-FOOTPRINTING-RECONNAISSANCE)