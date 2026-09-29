<div align="center">

# 🏥 Mediroza General Hospital — Penetration Testing Project

**NetworkWalks Cybersecurity & Ethical Hacking — Batch B083 | Week 04**

</div>

---

## 🎯 Objectives

The project was divided into four milestones:

- **M1 — Initial Access:** Attack the website and retrieve 3 confidential patient PDF lab reports.
- **M2 — Data Extraction:** Crack the encryption on all 3 retrieved files.
- **M3 — Attack (cracking):** Find staff salaries and shareholder details of the hospital.
- **M4 — Pentest Report:** Write a professional penetration-testing report for the client.

---

## 📋 Project Details

| Item | Details |
|---|---|
| Client | Mediroza General Hospital |
| Target | `https://medirozahospital.com` |
| Project Type | Penetration Testing & Vulnerability Assessment |
| Testing | Black-box Pentest |
| Duration | 5 Days |
| Authorization | Written authorization granted |
| Scope | Target domain only |

The assessment was restricted to the target domain. The project rules did not allow social engineering, denial-of-service testing, or testing outside the agreed scope.

---

# M1 — Initial Access

I started with reconnaissance because the first milestone required me to understand what was exposed on the target before attempting to reach the restricted area.

The project brief directed me to:

- Conduct reconnaissance on the target.
- Identify exposed entry points.
- Analyse the behaviour of authentication mechanisms.
- Look for weaknesses in how the application handles user input.
- Gain unauthorised access to a restricted area of the site.

### Target Reconnaissance

I accessed:

`https://medirozahospital.com`

From the supplied walkthrough, I reviewed the public-facing website and its navigation.

The visible navigation included:

- Home
- About
- Doctors
- Contact
- Patient Portal
- Staff Login

### Staff Login

I opened the **Staff Login** page.

The page contained:

- Staff ID
- Password
- Sign in

It also displayed:

**Internal staff access only.**

This identified an authentication mechanism that formed part of the M1 assessment.

### Doctors Page

I opened the Doctors page and reviewed the information presented about the hospital's doctors.

### Contact Page

I opened the Contact and find us page and reviewed the information displayed there, including:

- Address
- Phone number
- Email
- Opening hours

### Home Page

I returned to the homepage and reviewed the main content, including:

- Book an appointment
- Meet our doctors
- Our Departments

The homepage also displayed the statement:

**“Compassionate care, advanced medicine.”**

### About Page

I opened the About Mediroza page and reviewed the sections covering:

- The hospital
- Its values
- Accreditation

### M1 Testing

After the initial reconnaissance, I focused on the specific areas required by the brief:

**Exposed entry points:** I documented the entry points identified during reconnaissance.

**Authentication:** I examined the behaviour of the identified authentication mechanism.

**User input:** I checked how the application handled the relevant input.

**Restricted access:** I documented the path used to reach the restricted area.

**Patient reports:** The required outcome was retrieval of the 3 confidential patient PDF lab reports.

### M1 Evidence

The evidence for M1 should follow the order of the work:

| # | Evidence | Purpose |
|---|---|---|
| 01 | `01-reconnaissance.png` | Reconnaissance |
| 02 | `02-exposed-entry-point.png` | Exposed entry point |
| 03 | `03-authentication.png` | Authentication behaviour |
| 04 | `04-input-testing.png` | User-input handling |
| 05 | `05-restricted-area.png` | Restricted-area access |
| 06 | `06-patient-report-1.png` | Patient PDF 1 |
| 07 | `07-patient-report-2.png` | Patient PDF 2 |
| 08 | `08-patient-report-3.png` | Patient PDF 3 |

**Deliverable:** Proof of access and the 3 retrieved PDF files.

---

# M2 — Data Extraction

After retrieving the three PDF files, I moved to the second milestone.

The task was to **crack the encryption on all 3 retrieved files**.

The brief gave four specific instructions:

1. Analyse the encryption on each file.
2. Select appropriate tools and wordlists to recover the contents.
3. Do not assume a single approach will work for all 3 files.
4. Think carefully when one method fails and try another.

I therefore treated each file separately rather than assuming the same recovery process would work for all three.

### PDF 1

| Item | Details |
|---|---|
| Filename | |
| Encryption / protection | |
| Tool(s) used | |
| Wordlist used | |
| Recovery result | |

### PDF 2

| Item | Details |
|---|---|
| Filename | |
| Encryption / protection | |
| Tool(s) used | |
| Wordlist used | |
| Recovery result | |

### PDF 3

| Item | Details |
|---|---|
| Filename | |
| Encryption / protection | |
| Tool(s) used | |
| Wordlist used | |
| Recovery result | |

### M2 Evidence

For each file, I documented:

- The protection identified.
- The tool or approach used.
- The wordlist used where applicable.
- The recovery result.
- Proof that the recovered file could be accessed.

| # | Evidence | Purpose |
|---|---|---|
| 09 | `09-pdf1-analysis.png` | PDF 1 encryption/protection analysis |
| 10 | `10-pdf1-recovery.png` | PDF 1 recovery |
| 11 | `11-pdf1-verified.png` | PDF 1 successful access |
| 12 | `12-pdf2-analysis.png` | PDF 2 encryption/protection analysis |
| 13 | `13-pdf2-recovery.png` | PDF 2 recovery |
| 14 | `14-pdf2-verified.png` | PDF 2 successful access |
| 15 | `15-pdf3-analysis.png` | PDF 3 encryption/protection analysis |
| 16 | `16-pdf3-recovery.png` | PDF 3 recovery |
| 17 | `17-pdf3-verified.png` | PDF 3 successful access |

**Deliverable:** Recovered contents of all 3 files with proof of successful access.

---

# M3 — Attack (Cracking)

For M3, I went back through everything I had retrieved during M1 and M2.

The brief specifically required me to:

- Conduct a thorough analysis of everything retrieved so far.
- Look beyond the obvious content.
- Examine all file properties carefully.
- Follow the finding that points to a further critical exposure on the server.

AI tools were also permitted and encouraged for data analysis and reporting.

### Reviewing the Retrieved Files

I examined the recovered files and their properties for information that could provide the next lead.

The review included:

- File properties
- Metadata
- Other information contained in the recovered material
- Anything that could point to another exposed resource on the server

### Critical Data Exposure

The next step was to follow the lead from the retrieved information to the further exposure on the server.

I documented:

- What the lead was.
- Where it came from.
- How it pointed to the additional exposure.
- What information was exposed.

### Staff Salaries

The first M3 task was to find the salaries of all hospital employees.

I recorded the information found and kept supporting evidence.

### Shareholder Details

The second M3 task was to find the shareholder details of the hospital.

I recorded the information found and kept supporting evidence.

The final information should be presented as a readable summary rather than an unnecessary raw dump.

### M3 Evidence

| # | Evidence | Purpose |
|---|---|---|
| 18 | `18-file-properties.png` | File properties / metadata |
| 19 | `19-critical-exposure.png` | Finding leading to the further exposure |
| 20 | `20-staff-salaries.png` | Staff salary evidence |
| 21 | `21-shareholder-details.png` | Shareholder details evidence |

**Deliverable:** Full documented evidence of the exposure and a readable summary of the confidential data uncovered.

---

# M4 — Pentest Report

For the final milestone, I brought the work from M1 to M3 together into one professional penetration-testing report.

The required report structure was:

## 01 — Executive Summary

A concise overview of the engagement, key findings, and overall risk to the client.

## 02 — Scope and Methodology

I documented:

- The target.
- The tools used.
- The approach taken.
- Any limitations encountered.

## 03 — Findings and Proof of Exploitation

I documented each confirmed vulnerability with:

- The finding.
- How it was identified.
- The relevant exploitation or access path.
- Supporting screenshots and evidence.

## 04 — Risk Rating

Each confirmed vulnerability was rated:

- Critical
- High
- Medium
- Low

with justification.

## 05 — Recommendations and Remediation

I documented actionable steps the client could take to address each confirmed issue.

### M4 Evidence

`22-final-report.png`

**Deliverable:** A complete professional penetration-testing report submitted to the instructor.

---

# 📸 Evidence Index

All evidence is kept in this README so the project can be followed from beginning to end without separate milestone folders.

| Evidence | Stage |
|---|---|
| 01–08 | M1 — Initial Access |
| 09–17 | M2 — Data Extraction |
| 18–21 | M3 — Attack (Cracking) |
| 22 | M4 — Pentest Report |

For screenshots containing patient, employee, or shareholder information, unnecessary sensitive information should be redacted before the screenshots are published.

---

# 🧠 What I Learned

This project helped me understand the flow of a black-box penetration test from reconnaissance to final reporting.

I learned that the first stage is not just about finding a login page. I needed to look at the publicly exposed parts of the application, identify possible entry points, examine authentication and input handling, and then use the findings to reach the restricted information required by the project.

The second stage showed me why protected files need to be analysed individually. The project specifically required me to be prepared to change approach when one recovery method did not work.

The third stage required a deeper review of information already collected. Instead of stopping after recovering the files, I had to examine their properties and look for the clue that could lead to another exposure.

Finally, I learned the importance of keeping evidence organised throughout the assessment so that the final report can clearly connect each finding to the work that produced it.

---

## 🔐 Ethical Use

This assessment was carried out as part of an authorised NetworkWalks training exercise. The techniques documented here are intended for authorised testing only.

---

## 📋 Project Information

| Item | Details |
|---|---|
| Training Program | NetworkWalks Cybersecurity & Ethical Hacking |
| Batch | B083 |
| Week | 04 |
| Project | Mediroza General Hospital Penetration Testing |
| Target | `https://medirozahospital.com` |
| Testing Type | Black-box Pentest |
| Duration | 5 Days |
| Author | Collins |
