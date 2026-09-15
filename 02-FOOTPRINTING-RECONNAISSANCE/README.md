<div align="center">

# 🔎 Footprinting & Reconnaissance with Kali Linux

**NetworkWalks Cybersecurity & Ethical Hacking — Batch B083**  
**Week 02 | Project Module 1 (W2-PM1)**

![Cybersecurity](https://img.shields.io/badge/Cybersecurity-Reconnaissance-blue)
![Kali Linux](https://img.shields.io/badge/Kali%20Linux-Reconnaissance-557C94)
![NetworkWalks](https://img.shields.io/badge/NetworkWalks-B083-green)

</div>

---

## 📌 Project Overview

This project documents practical **footprinting and reconnaissance** activities completed during NetworkWalks Week 02.

The assessment uses Kali Linux to gather publicly available information about **networkwalks.com** with six reconnaissance tools.

## 🎯 Objectives

- Collect domain registration information with `whois`.
- Identify web technologies with `whatweb`.
- Resolve DNS information with `nslookup`.
- Inspect HTTP headers with `curl -I`.
- Detect WAF protection with `wafw00f`.
- Enumerate DNS records with `dnsrecon`.
- Preserve terminal output and screenshot evidence for each task.

## 📚 Tasks, Results & Evidence

### 01 — WHOIS

```bash
whois networkwalks.com
```

**Result:** WHOIS returned domain registration details including GoDaddy as the registrar, registration/expiry dates, domain status, and nameservers. The registrant information was privacy-protected.

![WHOIS](whois-screenshot.png)

[Task documentation](task-01-whois/README.md) · [Command output](task-01-whois/output.txt)

---

### 02 — WhatWeb

```bash
whatweb networkwalks.com
```

**Result:** WhatWeb identified Apache, WordPress 7.1, WordPress Download Manager, Bootstrap, jQuery, Google Tag Manager, and other web technologies. The HTTP version redirected to HTTPS, which returned `200 OK`.

![WhatWeb](whatweb-screenshot.png)

[Task documentation](task-02-whatweb/README.md) · [Command output](task-02-whatweb/output.txt)

---

### 03 — NSLookup

```bash
nslookup networkwalks.com
```

**Result:** The lookup resolved `networkwalks.com` to **192.232.216.135**. The query also showed a timeout communicating with the configured DNS server at `8.8.8.8`, but a non-authoritative answer was still returned.

![NSLookup](nslookup-screenshot.png)

[Task documentation](task-03-nslookup/README.md) · [Command output](task-03-nslookup/output.txt)

---

### 04 — cURL

```bash
curl -I https://networkwalks.com
```

**Result:** The server returned **HTTP/2 200 OK**. The headers revealed Apache as the server, WordPress-related endpoints and cookies, content type information, caching headers, and security-related policies.

![cURL](curl-screenshot.png)

[Task documentation](task-04-curl/README.md) · [Command output](task-04-curl/output.txt)

---

### 05 — Wafw00f

```bash
wafw00f networkwalks.com
```

**Result:** Wafw00f identified **ModSecurity (SpiderLabs) WAF** protecting the website after two requests.

![Wafw00f](wafw00f-screenshot.png)

[Task documentation](task-05-wafw00f/README.md) · [Command output](task-05-wafw00f/output.txt)

---

### 06 — DNSRecon

```bash
dnsrecon -d networkwalks.com
```

**Result:** DNSRecon discovered SOA, NS, MX, A, and SRV records. It resolved the main domain to **192.232.216.135**, identified mail infrastructure, and found **8 SRV records**. The scan also reported no answer for the DNSSEC query.

![DNSRecon](dnsrecon-screenshot.png)

[Task documentation](task-06-dnsrecon/README.md) · [Command output](task-06-dnsrecon/output.txt)

## 🧠 What I Learned

- I learned how **WHOIS** can be used to collect domain registration and nameserver information during passive reconnaissance.
- I learned how **WhatWeb** helps identify technologies, frameworks, web servers, and other components exposed by a website.
- I learned how **NSLookup** can be used to resolve a domain name to an IP address and observe DNS query behaviour.
- I learned how **cURL** can reveal useful HTTP response headers and information about how a web server is configured.
- I learned how **Wafw00f** can help identify whether a website is protected by a Web Application Firewall and which WAF may be in use.
- I learned how **DNSRecon** can enumerate different DNS records and provide a broader view of a domain's DNS infrastructure.
- Most importantly, I learned that combining multiple reconnaissance tools provides a more complete picture than relying on a single tool.

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


## 📋 Project Information

| Item | Details |
|---|---|
| Training Program | NetworkWalks Cybersecurity & Ethical Hacking |
| Batch | B083 |
| Week | 02 |
| Project | W2-PM1 |
| Project Title | Footprinting & Reconnaissance Attacks with Multiple Kali Tools |
| Target | `networkwalks.com` |
| Author | Collins |
