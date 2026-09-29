<div align="center">

# 🏥 Penetration Testing Project — Mediroza General Hospital

**NetworkWalks Cybersecurity & Ethical Hacking — Batch B083**  
**Week 04 | Project Module**

</div>

---

## 📌 Project Overview

For Week 04, I am carrying out a **full black-box penetration test** against **Mediroza General Hospital**.

The assessment is a **5-day engagement** focused on gaining initial access, recovering three confidential patient PDF lab reports, analysing and cracking the protection on those files, investigating a further critical data exposure, and documenting the work in a professional penetration-testing report.

| Item | Details |
|---|---|
| Client | Mediroza General Hospital |
| Target | [medirozahospital.com](https://medirozahospital.com) |
| Project Type | Penetration Testing & Vulnerability Assessment |
| Testing Type | Black-box Pentest |
| Duration | 5 Days |
| Authorization | Written permission granted |
| Scope | Target domain only |

### Rules of Engagement

I am keeping the testing within the agreed scope:

- Target domain only
- No social engineering
- No denial of service
- No testing outside the agreed scope

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

Attack the website, identify the exposed entry points and weaknesses, gain access to the restricted area, and retrieve the **3 confidential patient PDF lab reports**.

## Hints from the Project Brief

The brief directed me to:

- Conduct reconnaissance on the target.
- Identify exposed entry points.
- Analyse the behaviour of authentication mechanisms.
- Look for weaknesses in how the application handles user input.
- Gain unauthorised access to a restricted area of the site.

## Recon Notes

I started by accessing:

`https://medirozahospital.com`

I reviewed the public-facing website and the available navigation before moving further into the assessment.

The walkthrough showed:

- Home
- About
- Doctors
- Contact
- Patient Portal
- Staff Login

I also inspected the website for exposed paths and application resources. During the reconnaissance shown in the walkthrough, paths including:

- `/old`
- `/robots.txt`
- `/staff`
- `/patient`

were examined as potential sources of information or entry points.

### Staff Login

The **Staff Login** page contained:

- Staff ID
- Password
- Sign in

It also displayed:

**Internal staff access only.**

This provided an authentication mechanism to investigate as part of M1.

### Public Pages Reviewed

**Doctors** — I reviewed the information presented about the hospital's doctors.

**Contact** — I reviewed the displayed address, phone number, email and opening hours.

**Home** — I reviewed the main page content, including **Book an appointment**, **Meet our doctors**, and **Our Departments**.

**About** — I reviewed information about the hospital, its values and accreditation.

## Vulnerability Identified

**Finding:** __________________________________________

Once confirmed, I will document the actual weakness identified, why it worked, and how it allowed access to the restricted area.

## Steps Taken

1. _________________________________________________
2. _________________________________________________
3. _________________________________________________
4. _________________________________________________

## Evidence

I will include screenshots showing:

- Reconnaissance results
- The exposed entry point
- Authentication behaviour
- User-input testing
- Successful access to the restricted area
- The 3 retrieved patient PDF lab reports

## Result

**Access obtained:** __________________________________

**Patient PDF 1:** ___________________________________

**Patient PDF 2:** ___________________________________

**Patient PDF 3:** ___________________________________

## Deliverable

- [ ] Proof of access
- [ ] 3 retrieved patient PDF lab reports

---

# 🔐 M2 — Data Extraction

**Written Permission: GRANTED**

## What I need to do

Crack the encryption on all **3 retrieved files** from M1 and recover their contents.

## Hints from the Project Brief

The brief instructed me to:

- Analyse the encryption on each file.
- Select appropriate tools and wordlists to recover the contents.
- Do not assume a single approach will work for all 3 files.
- Think carefully when one method fails and try another.

## File 1

| Item | Details |
|---|---|
| Filename | |
| Encryption / protection | |
| Tool(s) used | |
| Wordlist used | |
| Outcome | |

### Evidence

- Encryption/protection analysis
- Recovery attempt
- Successful access to the recovered file

## File 2

| Item | Details |
|---|---|
| Filename | |
| Encryption / protection | |
| Tool(s) used | |
| Wordlist used | |
| Outcome | |

### Evidence

- Encryption/protection analysis
- Recovery attempt
- Successful access to the recovered file

## File 3

| Item | Details |
|---|---|
| Filename | |
| Encryption / protection | |
| Tool(s) used | |
| Wordlist used | |
| Outcome | |

### Evidence

- Encryption/protection analysis
- Recovery attempt
- Successful access to the recovered file

## Result

**PDF 1:** __________________________________________

**PDF 2:** __________________________________________

**PDF 3:** __________________________________________

## Deliverable

- [ ] Contents of all 3 files recovered
- [ ] Proof of successful access for each file

---

# 🕵️ M3 — Attack (Cracking)

**Written Permission: GRANTED**

## What I need to do

Find the **critical data exposure on the client server**.

The M3 stage builds on the information recovered during M1 and M2, so I need to go back over what I already have and look for the lead to the additional exposure.

## Hints from the Project Brief

The brief instructed me to:

- Conduct a thorough analysis of everything retrieved so far.
- Look beyond the obvious content.
- Examine all file properties carefully.
- Follow the finding that points to a further critical exposure on the server.
- AI tools are permitted and encouraged for data analysis and reporting.

## Tasks

- [ ] Find the salaries of all hospital employees.
- [ ] Find the shareholder details of the hospital.

## Going Back Over What I Have

I will examine the retrieved files and their properties carefully, including:

- Metadata
- Author or creator information
- Embedded paths
- Comments
- Hidden fields
- Other file properties that may provide a useful lead

The purpose is to identify the finding that points toward the further exposure on the server.

## What It Turned Out To Be

**Exposure identified:** __________________________________

**How I found it:** ______________________________________

**Why it matters:** ______________________________________

## What I Found

| Data | Summary |
|---|---|
| Staff salaries | |
| Shareholder details | |

I will keep the final information as a readable summary rather than a raw dump.

## Evidence

I will include screenshots or command output showing:

1. The relevant file property or other clue.
2. How the clue led to the further exposure.
3. The exposed staff salary information.
4. The exposed shareholder information.

## Deliverable

- [ ] Full evidence of the exposure
- [ ] Readable summary of the confidential information uncovered

---

# 📝 M4 — Pentest Report

**Milestone 4**

## What I need to do

Bring the work from **M1 through M3** together into one professional penetration-testing report for the client.

## Report Structure

| # | Section | What I will document |
|---|---|---|
| 01 | **Executive Summary** | Concise overview of the engagement, key findings and overall risk to the client |
| 02 | **Scope and Methodology** | Target, tools used, approach taken and any limitations encountered |
| 03 | **Findings and Proof of Exploitation** | Each vulnerability with screenshots and evidence for every milestone |
| 04 | **Risk Rating** | Critical, High, Medium or Low with justification |
| 05 | **Recommendations and Remediation** | Actionable steps the client should take to fix each identified issue |

## Findings Summary

| Milestone | Vulnerability / Finding | Risk | Notes |
|---|---|---|---|
| M1 | | | |
| M2 | | | |
| M3 | | | |

## Evidence

I will reference the evidence collected throughout M1, M2 and M3 so that each finding can be traced back to the step where it was identified and demonstrated.

## Deliverable

- [ ] Complete professional penetration-testing report
- [ ] All supporting evidence from M1–M3 included or referenced

---

# 📊 Overall Project Progress

| Milestone | Deliverable | Status |
|---|---|---|
| **M1** | Proof of access + 3 patient PDFs | ⬜ |
| **M2** | Recovered contents of all 3 files | ⬜ |
| **M3** | Evidence of exposure + readable summary | ⬜ |
| **M4** | Final penetration-testing report | ⬜ |

---

## 🧠 What I Learned

I used this project to practise following a penetration-testing workflow from reconnaissance through access, file analysis, further investigation and reporting.

One of the main lessons from the project is that the information obtained during one stage can become the lead for the next stage. M3 especially requires me to go back over the files from M2 and examine their properties rather than stopping at the obvious contents.

I also learned the importance of keeping evidence in the same order as the work so that the final report can clearly show how each finding was identified and demonstrated.

---

## 🔒 Security & Ethical Use

This project is being carried out in a controlled and authorised training environment. The techniques documented here are for authorised security testing only and should not be applied to systems without explicit permission from the owner.

---

## 📋 Project Information

| Item | Details |
|---|---|
| Training Program | NetworkWalks Cybersecurity & Ethical Hacking |
| Batch | B083 |
| Week | 04 |
| Project | W4-PM |
| Project Title | Penetration Testing Project — Mediroza General Hospital |
| Target | `medirozahospital.com` |
| Author | Collins |

---

[← Back to NETWORKWALKS](../README.md)
