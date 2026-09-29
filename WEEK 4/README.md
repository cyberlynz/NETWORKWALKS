<div align="center">

# 🏥 NetworkWalks Week 04 — Mediroza General Hospital Penetration Testing

**Cybersecurity & Ethical Hacking — Batch B083**

</div>

---

## 🎯 Objectives

The project was divided into four milestones:

- **M1 — Initial Access:** Attack the website and retrieve 3 confidential patient PDF lab reports.
- **M2 — Data Extraction:** Crack the encryption on all 3 retrieved files.
- **M3 — Attack (cracking):** Find staff salaries and shareholder details of the hospital.
- **M4 — Pentest Report:** Write a professional penetration-testing report for the client.

---

## 📋 Engagement Details

| Item | Details |
|---|---|
| Client | Mediroza General Hospital |
| Target | `https://medirozahospital.com` |
| Project Type | Penetration Testing & Vulnerability Assessment |
| Testing Type | Black-box Pentest |
| Duration | 5 Days |
| Authorization | Written permission granted |
| Scope | Target domain only |
| Restrictions | No social engineering, no denial of service, and no testing outside the agreed scope |

I carried out the work within the scope and rules provided for the NetworkWalks project.

---

# M1 — Initial Access

I began with reconnaissance of the target to identify publicly exposed information and possible entry points.

The M1 brief required me to:

- Conduct reconnaissance on the target.
- Identify exposed entry points.
- Analyse the behaviour of authentication mechanisms.
- Look for weaknesses in how the application handles user input.
- Gain access to a restricted area of the site.

## Reconnaissance

I accessed:

`https://medirozahospital.com`

During the supplied walkthrough, I reviewed the publicly accessible website and its navigation.

The navigation included:

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

This provided an authentication point for further assessment.

### Doctors Page

I opened the Doctors page and reviewed the information presented about the hospital's doctors.

### Contact Page

I opened the Contact page and reviewed the displayed:

- Address
- Phone number
- Email
- Opening hours

### Home Page

I returned to the homepage and reviewed the main content, including:

- Book an appointment
- Meet our doctors
- Our Departments

The page displayed:

**“Compassionate care, advanced medicine.”**

### About Page

I opened the About page and reviewed information about:

- The hospital
- Its values
- Accreditation

## M1 — Technical Assessment

After the initial reconnaissance, I moved to the areas specified in the brief:

### Exposed Entry Points

I documented the entry points identified during reconnaissance and the functionality they exposed.

### Authentication Behaviour

I examined the identified authentication mechanism and documented how the application responded during testing.

### User Input Handling

I examined the application's handling of user input and recorded the relevant behaviour observed during testing.

### Restricted Access

I documented the path used to reach the restricted area and the point at which access to the confidential patient reports was obtained.

### Patient PDF Reports

The M1 deliverable required three confidential patient PDF lab reports.

## M1 Evidence

| # | Evidence | Purpose |
|---|---|---|
| 01 | `01-reconnaissance.png` | Reconnaissance |
| 02 | `02-exposed-entry-point.png` | Exposed entry point |
| 03 | `03-authentication.png` | Authentication behaviour |
| 04 | `04-input-testing.png` | User-input testing |
| 05 | `05-restricted-area.png` | Restricted-area access |
| 06 | `06-patient-report-1.png` | Patient PDF 1 |
| 07 | `07-patient-report-2.png` | Patient PDF 2 |
| 08 | `08-patient-report-3.png` | Patient PDF 3 |

**M1 Deliverable:** Proof of access and the 3 retrieved PDF files.

---

# M2 — Data Extraction

After retrieving the three PDF files, I moved to the second milestone.

The task was to **crack the encryption on all 3 retrieved files**.

The brief required me to:

1. Analyse the encryption on each file.
2. Select appropriate tools and wordlists to recover the contents.
3. Not assume that one approach would work for all three files.
4. Try another method when one approach failed.

## PDF 1

I documented the encryption/protection identified, the tool and wordlist used, and the recovery result.

| Item | Details |
|---|---|
| Filename | To be taken from evidence |
| Encryption / protection | To be recorded |
| Tool(s) used | To be recorded |
| Wordlist used | To be recorded |
| Recovery result | To be recorded |

## PDF 2

| Item | Details |
|---|---|
| Filename | To be taken from evidence |
| Encryption / protection | To be recorded |
| Tool(s) used | To be recorded |
| Wordlist used | To be recorded |
| Recovery result | To be recorded |

## PDF 3

| Item | Details |
|---|---|
| Filename | To be taken from evidence |
| Encryption / protection | To be recorded |
| Tool(s) used | To be recorded |
| Wordlist used | To be recorded |
| Recovery result | To be recorded |

## M2 Evidence

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

**M2 Deliverable:** Recovered contents of all 3 files with proof of successful access.

---

# M3 — Attack (Cracking)

For M3, I went back through everything retrieved during M1 and M2 and looked for the further critical exposure described in the brief.

The brief required me to:

- Conduct a thorough analysis of everything retrieved so far.
- Look beyond the obvious content.
- Examine all file properties carefully.
- Follow the finding that points to a further critical exposure on the server.

AI tools were also permitted and encouraged for data analysis and reporting.

## File and Property Analysis

I examined the retrieved material and its properties for information that could provide the lead to the additional exposure.

The review covered:

- File properties
- Metadata
- Other relevant information recovered from the files
- Any lead pointing to another exposed resource on the server

## Critical Data Exposure

I documented the finding that led from the recovered information to the further exposure on the client server.

### Staff Salaries

The first required finding was the salaries of all hospital employees.

I recorded the relevant information and supporting evidence.

### Shareholder Details

The second required finding was the shareholder details of the hospital.

I recorded the relevant information and supporting evidence.

## M3 Evidence

| # | Evidence | Purpose |
|---|---|---|
| 18 | `18-file-properties.png` | File properties / metadata |
| 19 | `19-critical-exposure.png` | Finding leading to the exposure |
| 20 | `20-staff-salaries.png` | Staff salary evidence |
| 21 | `21-shareholder-details.png` | Shareholder details evidence |

**M3 Deliverable:** Full documented evidence of the exposure and a readable summary of the confidential data uncovered.

---

# M4 — Pentest Report

For M4, I brought the work from the previous milestones together into the final penetration-testing report.

The report structure required by the project brief was:

## 01 — Executive Summary

A concise overview of the engagement, key findings, and overall risk to the client.

## 02 — Scope and Methodology

I documented:

- Target
- Tools used
- Approach taken
- Any limitations encountered

## 03 — Findings and Proof of Exploitation

I documented each vulnerability with:

- The finding
- How it was identified
- The relevant access or exploitation path
- Screenshots and supporting evidence

## 04 — Risk Rating

Each vulnerability was rated:

- Critical
- High
- Medium
- Low

with justification.

## 05 — Recommendations and Remediation

I documented actionable steps the client could take to fix each identified issue.

## M4 Evidence

| # | Evidence | Purpose |
|---|---|---|
| 22 | `22-final-report.png` | Final penetration-testing report / submission |

**M4 Deliverable:** A complete professional penetration-testing report submitted to the instructor.

---

# 📸 Evidence Index

All supporting screenshots are referenced from this single README so that the documentation and evidence remain together.

| Range | Milestone | Evidence |
|---|---|---|
| 01–08 | M1 | Reconnaissance, entry point, authentication, input handling, restricted access, and 3 patient PDFs |
| 09–17 | M2 | Encryption analysis, recovery, and verification for the 3 PDFs |
| 18–21 | M3 | File properties, critical exposure, staff salaries, and shareholder details |
| 22 | M4 | Final penetration-testing report |

For any screenshot containing patient, employee, or shareholder information, unnecessary sensitive information should be redacted before publication.

---

# 🧠 What I Learned

This project helped me understand how a black-box penetration test moves from reconnaissance to initial access, protected-file recovery, further investigation, and final reporting.

I also learned the importance of examining information beyond what is immediately visible. The M3 task specifically required careful analysis of the retrieved files and their properties to identify the next lead.

Keeping evidence in sequence also made it easier to connect each finding to the step where it was identified.

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
