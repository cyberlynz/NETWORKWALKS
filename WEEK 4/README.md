<div align="center">

# 🏥 Penetration Testing Project — Mediroza General Hospital

**NetworkWalks Cybersecurity & Ethical Hacking — Batch B083**  
**Week 04 | Project Module (W4-PM)**

![Cybersecurity](https://img.shields.io/badge/Cybersecurity-Penetration%20Testing-blue)
![Black-box](https://img.shields.io/badge/Type-Black--box%20Pentest-557C94)
![NetworkWalks](https://img.shields.io/badge/NetworkWalks-B083-green)

</div>

---

## 📌 Project Overview

For Week 04, I'm working on a full black-box penetration test against **Mediroza General Hospital**.

The engagement runs for **5 days** and follows the four milestones provided in the project brief. My work is centred on the target website, the three confidential patient PDF lab reports, the protected files recovered from the assessment, the further data exposure described in M3, and the final client report.

| | |
|---|---|
| Client | Mediroza General Hospital |
| Target | medirozahospital.com |
| Type | Black-box pentest |
| Duration | 5 days |
| Authorization | Written permission granted |
| Scope | Target domain only |

### Rules of Engagement

Testing is limited to the target domain.

- No social engineering.
- No denial of service.
- No testing outside the agreed scope.

---

## 🎯 Objectives

The project was divided into four milestones:

- **M1 — Initial Access:** Attack the website and retrieve 3 confidential patient PDF lab reports.
- **M2 — Data Extraction:** Crack the encryption on all 3 retrieved files.
- **M3 — Attack (cracking):** Find staff salaries and shareholder details of the hospital.
- **M4 — Pentest Report:** Write a professional penetration-testing report for the client.

---

# 🔎 M1 — Initial Access

**Written Permission: GRANTED**

## What I need to do

Attack the website and find the **3 confidential PDF lab reports of patients**.

## Hints

The brief points me to:

- Conduct reconnaissance on the target.
- Identify exposed entry points.
- Analyse the behaviour of any authentication mechanisms I find.
- Look for weaknesses in how the application handles user input.
- Gain unauthorised access to a restricted area of the site.

## Recon Notes

I started my reconnaissance against:

`https://medirozahospital.com/`

I used **Nikto v2.6.1** to identify information exposed by the web server and to enumerate potentially interesting directories.

### Nikto Results

The scan identified the following target information:

| Item | Result |
|---|---|
| Target IP | `199.188.201.16` |
| Target Hostname | `medirozahospital.com` |
| Target Port | `443` |
| Web Server | LiteSpeed |
| Platform | Unknown |

The SSL information shown by Nikto included:

- Subject: `/CN=medirozahospital.com`
- CN: `medirozahospital.com`
- SAN: `medirozahospital.com, www.medirozahospital.com`
- Cipher: `TLS_AES_256_GCM_SHA384`
- Issuer: `/C=US/O=SSL.com TLS Issuing RSA CA R1`

### Directory Enumeration

Nikto identified several accessible directories and entries that required further investigation:

| Path | Nikto Result |
|---|---|
| `/staff/` | Directory indexing found — **CWE-548** |
| `/patient/` | Directory indexing found — **CWE-548** |
| `/old/` | Directory indexing found — **CWE-548** |

Nikto also reported entries in `/robots.txt`:

| Entry | Result |
|---|---|
| `/staff` | Returned a non-forbidden or redirect HTTP response (200) |
| `/patient` | Returned a non-forbidden or redirect HTTP response (200) |
| `/old` | Returned a non-forbidden or redirect HTTP response |

The scan reported that `/robots.txt` contained **3 entries which should be manually viewed**.

### Other Reconnaissance Observations

The scan also reported:

- Allowed HTTP methods: `OPTIONS, HEAD, GET, POST`
- Missing suggested `strict-transport-security` header
- Missing suggested `referrer-policy` header
- Missing suggested `content-security-policy` header
- Missing suggested `x-content-type-options` header
- Missing suggested `permissions-policy` header

At this stage, these are reconnaissance observations from the Nikto scan. I use them as leads for the next part of the assessment rather than treating every observation as a confirmed vulnerability.

### Reconnaissance Evidence

**Screenshot:** `01-nikto-reconnaissance.png`

This screenshot shows the Nikto scan output, including the target details, web server information, exposed directories, and `robots.txt` entries.

## Vulnerability Identified

**Finding:**  
____________________________________________

**Why it is exploitable:**  
____________________________________________

## How I Got In

1. ____________________________________________
2. ____________________________________________
3. ____________________________________________

## Where I Landed

**Restricted area:**  
____________________________________________

**Patient PDF 1:**  
____________________________________________

**Patient PDF 2:**  
____________________________________________

**Patient PDF 3:**  
____________________________________________

## Evidence

The screenshots for M1 should show the reconnaissance, exposed entry point, authentication/input testing, the restricted area, and the three retrieved PDFs.

## Deliverable

- [ ] Proof of access
- [ ] The 3 retrieved PDF files

---

# 🔐 M2 — Data Extraction

**Written Permission: GRANTED**

## What I need to do

Crack whatever is protecting the **3 files retrieved in M1**.

## Hints

The brief is specific about the approach:

- Analyse the encryption on each file.
- Select appropriate tools and wordlists to recover the contents.
- Do not assume a single approach will work for all 3 files.
- Think carefully when one method fails and try another.

## File 1

| | |
|---|---|
| Filename | |
| What's protecting it | |
| Tools I tried | |
| Wordlist used | |
| Outcome | |

## File 2

| | |
|---|---|
| Filename | |
| What's protecting it | |
| Tools I tried | |
| Wordlist used | |
| Outcome | |

## File 3

| | |
|---|---|
| Filename | |
| What's protecting it | |
| Tools I tried | |
| Wordlist used | |
| Outcome | |

## Evidence

Command output and screenshots will be used to show the protection on each file, the recovery process, and successful access to the recovered contents.

## Deliverable

- [ ] Contents of all 3 files recovered
- [ ] Proof of access for each

---

# 🕵️ M3 — Critical Data Exposure

**Written Permission: GRANTED**

## What I need to do

Find the **critical data exposure on the client server**.

This stage builds directly on M1 and M2. I need to go back over what I have already recovered and look closely for the lead to the further exposure.

## Hints

The brief tells me to:

- Conduct a thorough analysis of everything retrieved so far.
- Look beyond the obvious content.
- Examine all file properties carefully.
- Follow the finding that points to a further critical exposure on the server.
- Use AI tools where useful for data analysis and reporting.

## Tasks

- [ ] Find the salaries of all hospital employees.
- [ ] Find the shareholder details of the hospital.

## Going Back Over What I've Got

I will examine the files recovered in M2 and check their properties and metadata for the lead described in the brief.

The important point here is to look beyond the visible document contents and identify the information that can take me to the next exposure.

## What It Turned Out To Be

**Exposure:**  
____________________________________________

**How I found it:**  
____________________________________________

**Why it matters:**  
____________________________________________

## What I Found

| | |
|---|---|
| Staff salaries | |
| Shareholder details | |

I will summarise the information rather than include an unnecessary raw dump.

## Evidence

Screenshots and command output will show:

- The file property or other clue.
- How that clue led to the exposure.
- The staff salary information.
- The shareholder information.

## Deliverable

- [ ] Full evidence of the exposure
- [ ] A readable summary of what was uncovered

---

# 📝 M4 — Pentest Report

**Milestone 4**

## What I need to do

Bring M1 through M3 into one professional penetration-testing report.

## Structure I'm Following

| # | Section | What I will document |
|---|---|---|
| 01 | **Executive Summary** | Concise overview of the engagement, key findings, and overall risk to the client |
| 02 | **Scope and Methodology** | Target, tools used, approach taken, and any limitations encountered |
| 03 | **Findings and Proof of Exploitation** | Each vulnerability with screenshots and evidence for every milestone |
| 04 | **Risk Rating** | Critical, High, Medium, or Low with justification |
| 05 | **Recommendations and Remediation** | Actionable steps the client should take to fix each identified issue |

## Findings Summary

| Milestone | Vulnerability | Risk | Notes |
|---|---|---|---|
| M1 | | | |
| M2 | | | |
| M3 | | | |

## Deliverable

- [ ] Final penetration-testing report submitted to the instructor
- [ ] All supporting evidence from M1–M3 attached or linked

---

## ✅ Evidence Checklist

| Milestone | Deliverable | Evidence |
|---|---|---|
| M1 | Proof of access + 3 retrieved PDFs | ⬜ |
| M2 | Recovered contents of all 3 files | ⬜ |
| M3 | Evidence of the exposure + readable summary | ⬜ |
| M4 | Final penetration-testing report | ⬜ |

---

## 🧠 What I Learned

I'll complete this section after the practical work is finished so that it reflects what actually worked, what failed, and what I learned from the assessment rather than simply listing tools or repeating the project brief.

---

## 🔒 Security & Ethical Use

This project is being carried out in a controlled, authorised training environment. The techniques documented here are for authorised security testing only and should not be applied to any system without explicit written permission from the owner.

---

## 📋 Project Information

| | |
|---|---|
| Program | NetworkWalks Cybersecurity & Ethical Hacking |
| Batch | B083 |
| Week | 04 |
| Project | W4-PM |
| Project Title | Penetration Testing Project — Mediroza General Hospital |
| Target | medirozahospital.com |
| Author | Collins |

---

[← Back to NETWORKWALKS](../README.md)
