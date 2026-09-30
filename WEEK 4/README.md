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

The brief directs me to:

- Conduct reconnaissance on the target.
- Identify exposed entry points.
- Analyse the behaviour of any authentication mechanisms I find.
- Look for weaknesses in how the application handles user input.
- Gain unauthorised access to a restricted area of the site.

## Reconnaissance

I started my reconnaissance with **Nikto v2.6.1** against:

`https://medirozahospital.com/`

The scan identified:

- **Target IP:** `199.188.201.16`
- **Port:** `443`
- **Web Server:** LiteSpeed

Nikto also identified directory indexing on:

- `/staff/`
- `/patient/`
- `/old/`

The scan also showed these paths in `/robots.txt`:

- `/staff`
- `/patient`
- `/old`

### Evidence

![Nikto reconnaissance and directory enumeration](./01-nikto-reconnaissance.png)

---

## Staff Login Testing

I followed the `/staff/` entry point and tested:

`https://medirozahospital.com/staff/login.php`

The page required:

- Staff ID
- Password

I made multiple login attempts and received:

**“Invalid username or password”**

I then tested the Staff ID input for **SQL injection**, but the attempts did not produce a successful authentication bypass or any useful result.

### Result

The staff login did not provide access, so I moved on to the next exposed entry point identified during reconnaissance.

### Evidence

**02 — Staff Login, Authentication & SQL Injection Testing**

![Staff login, authentication and SQL injection testing](./02-staff-login-authentication-sqli-testing.png)

---

## Patient Portal Testing

I then tested the Patient Portal identified during reconnaissance:

`https://medirozahospital.com/patient/login.php`

I applied the same input-testing approach used on the staff login. This time, the test was successful and I gained access to:

`https://medirozahospital.com/patient/portal.php`

### Evidence

**03 — Patient Portal SQL Injection & Access**

![Patient Portal SQL injection test and successful access](./03-patient-portal-sqli-access.png)

The combined screenshot shows the Patient Portal login page, the SQL injection input, and the successful access to the portal.

## Retrieve the Patient Reports

After gaining access to the patient portal, I reached the **My lab reports** page.

The portal displayed three password-protected/encrypted PDF pathology reports:

1. **Pathology Report — S. Dlamini**  
   Lab Ref: `LR-2024-1187` | `2024-11-04` | PDF (encrypted)

2. **Pathology Report — P. Reddy**  
   Lab Ref: `LR-2024-1192` | `2024-11-05` | PDF (encrypted)

3. **Pathology Report — E. Thompson**  
   Lab Ref: `LR-2024-1205` | `2024-11-06` | PDF (encrypted)

Each report had a **Download** option.

---

# 🔐 M2 — Data Extraction

**Written Permission: GRANTED**

## What I need to do

Crack the encryption on all 3 retrieved files.

## What I Tried

I first tried **John the Ripper**, but it did not produce a result.

I then used the **NetworkWalks Hash Calculator** to extract a crackable hash from each encrypted PDF.

### Patient Report 1

I uploaded `patient_report_1.pdf` to the Hash Calculator and obtained a crackable PDF hash.

### Patient Report 2

I repeated the same process with `patient_report_2.pdf` and obtained its crackable PDF hash.

### Patient Report 3

I repeated the process with `patient_report_3.pdf` and obtained its crackable PDF hash.

The tool identified each file as encrypted and generated a hash in a **pdf2john / hashcat-compatible format**.

### Result

The three patient PDFs were successfully processed and crackable hashes were extracted after the initial John the Ripper attempt did not work.

### Evidence

**04 — Patient PDF Hash Extraction**

<img src="https://raw.githubusercontent.com/cyberlynz/NETWORKWALKS/main/WEEK%204/04-patient-pdf-hash-extraction.png" alt="Patient PDF hash extraction" width="100%">

The screenshot shows the extracted crackable hashes for all three patient PDFs.


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

[← Back to NETWORKWALKS](../README.md)## Authentication & Input Testing

I first tested the staff login endpoint:

`https://medirozahospital.com/staff/login.php`

The login page required a **Staff ID** and **Password**. Multiple attempts returned:

**“Invalid username or password”**

I also tested the Staff ID input for SQL injection. The attempts did not produce a successful authentication bypass or any useful result.

### Patient Portal Testing

I then applied the same input-testing approach to the Patient Portal:

`https://medirozahospital.com/patient/login.php`

This test was successful and gave me access to:

`https://medirozahospital.com/patient/portal.php`

The portal displayed **three password-protected/encrypted PDF pathology reports**, each with a **Download** option:

- Pathology Report — S. Dlamini
- Pathology Report — P. Reddy
- Pathology Report — E. Thompson

This completed the M1 objective of obtaining the three confidential patient PDF reports required for the next stage.

### Result

- **Staff login:** No successful bypass
- **SQL injection on staff login:** No useful result
- **Patient Portal:** Access obtained
- **Patient reports:** 3 encrypted PDF reports identified and available for download

### Evidence

**02 — Staff Login, Authentication & SQL Injection Testing**

![Staff login, authentication response and SQL injection testing](./02-staff-login-authentication-sqli-testing.png)

**03 — Patient Portal SQL Injection & Access**

![Patient Portal SQL injection test and successful access](./03-patient-portal-sqli-access.png)

The second screenshot combines the Patient Portal login, the SQL injection input test, and the successful portal access showing the three encrypted reports.


