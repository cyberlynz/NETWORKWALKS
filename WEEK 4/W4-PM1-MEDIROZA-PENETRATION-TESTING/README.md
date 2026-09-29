<div align="center">

# 🏥 W4-PM — Mediroza General Hospital Penetration Testing

**NetworkWalks Cybersecurity & Ethical Hacking — Batch B083**  
**Week 04 | Penetration Testing Project**

</div>

---

## 🎯 Objectives

The project was divided into four milestones:

- **M1 — Initial Access:** Attack the website and retrieve 3 confidential patient PDF lab reports.
- **M2 — Data Extraction:** Crack the encryption on all 3 retrieved files.
- **M3 — Attack (cracking):** Find staff salaries and shareholder details of the hospital.
- **M4 — Pentest Report:** Write a professional penetration-testing report for the client.

---

## Project Details

| Item | Details |
|---|---|
| Client | Mediroza General Hospital |
| Target | `https://medirozahospital.com` |
| Type | Black-box Pentest |
| Duration | 5 Days |
| Authorization | Written authorization granted |
| Scope | Target domain only |

The rules for the assessment were to stay within the target domain, with no social engineering, no denial of service, and no testing outside the agreed scope.

---

# M1 — Initial Access

I started with reconnaissance of the target before moving into the restricted areas required by the project.

The project brief directed me to look for exposed entry points, understand the behaviour of authentication mechanisms, examine how the application handled user input, and then gain access to the restricted area containing the patient reports.

## Reconnaissance

I accessed:

`https://medirozahospital.com`

I reviewed the publicly available website and its navigation.

The walkthrough showed these areas:

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

This was one of the authentication points I examined during the assessment.

### Doctors Page

I reviewed the **Doctors** page and the information presented about the hospital's doctors.

### Contact Page

I reviewed the **Contact and find us** page and noted the displayed:

- Address
- Phone number
- Email
- Opening hours

### Home Page

I returned to the homepage and reviewed the main content, including:

- Book an appointment
- Meet our doctors
- Our Departments

The page also displayed the introduction:

**“Compassionate care, advanced medicine.”**

### About Page

I reviewed the **About Mediroza** page, including information about the hospital, its values, and accreditation.

## M1 Assessment Points

The remaining M1 work is documented around the exact areas given in the project brief:

| Area | What I documented |
|---|---|
| Reconnaissance | Publicly exposed information and accessible areas |
| Entry points | Points that could be used to reach restricted functionality |
| Authentication | Behaviour of the identified login mechanism |
| User input | Application behaviour when handling input |
| Restricted access | The path used to reach the protected area |
| Patient reports | Retrieval of the 3 confidential PDF lab reports |

## Evidence

The M1 evidence should follow the same order:

1. Target and reconnaissance
2. Exposed entry point
3. Authentication behaviour
4. Input handling
5. Restricted-area access
6. Patient PDF report 1
7. Patient PDF report 2
8. Patient PDF report 3

---

# M2 — Data Extraction

After obtaining the three PDF files from M1, I moved to the second milestone.

The project brief requires me to analyse the encryption on each file and select the appropriate tools and wordlists to recover the contents.

The brief also makes it clear that I should **not assume one approach will work for all three files**. Where one method fails, I should try another.

## File 1

I documented the following for the first PDF:

| Item | Details |
|---|---|
| Filename | To be taken from the captured evidence |
| Protection / encryption | To be identified |
| Tool(s) used | To be recorded |
| Wordlist used | To be recorded |
| Recovery result | To be recorded |

## File 2

| Item | Details |
|---|---|
| Filename | To be taken from the captured evidence |
| Protection / encryption | To be identified |
| Tool(s) used | To be recorded |
| Wordlist used | To be recorded |
| Recovery result | To be recorded |

## File 3

| Item | Details |
|---|---|
| Filename | To be taken from the captured evidence |
| Protection / encryption | To be identified |
| Tool(s) used | To be recorded |
| Wordlist used | To be recorded |
| Recovery result | To be recorded |

## M2 Evidence

For each file, I will keep evidence showing:

- The protection identified.
- The method used to recover the file.
- The successful result.
- Proof that the recovered file can be accessed.

---

# M3 — Attack (Cracking)

For M3, I went back through everything recovered during M1 and M2 and looked for the further exposure described in the project brief.

The important part of this stage is not just the visible contents of the files. I also needed to examine their properties carefully because one finding is expected to point to another critical exposure on the server.

AI tools were also permitted and encouraged for data analysis and reporting.

## File and Information Review

I checked the recovered material for information that could provide a lead to the additional exposure.

This included:

- File properties
- Metadata
- Other information contained in the recovered material
- Any lead pointing to another exposed resource on the server

## Required Findings

The two specific findings required by the milestone are:

### Staff Salaries

I documented the salary information for the hospital employees found during the assessment.

### Shareholder Details

I documented the shareholder information found during the assessment.

The information should be presented as a readable summary rather than an unnecessary raw dump.

## Evidence

The M3 evidence should show:

1. The file property or other clue that led to the additional exposure.
2. How I reached the exposed information.
3. The staff salary information.
4. The shareholder information.

---

# M4 — Pentest Report

For the final milestone, I brought the work from M1 to M3 together into the penetration-testing report required by NetworkWalks.

## 01 — Executive Summary

I summarised the engagement, the important findings, and the overall risk to the client.

## 02 — Scope and Methodology

I documented:

- The target
- Tools used
- Approach taken
- Any limitations encountered

## 03 — Findings and Proof of Exploitation

For each confirmed finding, I included the relevant explanation and supporting screenshots/evidence from the corresponding milestone.

## 04 — Risk Rating

Each confirmed vulnerability was assigned one of the required ratings:

- Critical
- High
- Medium
- Low

with justification.

## 05 — Recommendations and Remediation

I provided practical actions for addressing the confirmed issues identified during the assessment.

---

# Evidence Organisation

The evidence is kept in the same sequence as the project:

| Milestone | Evidence |
|---|---|
| **M1** | Reconnaissance, entry points, authentication, input handling, restricted access, 3 patient PDFs |
| **M2** | Analysis and recovery of all 3 protected files |
| **M3** | File properties/metadata, critical exposure, staff salaries, shareholder details |
| **M4** | Final penetration-testing report |

Sensitive patient, employee, or shareholder information should be redacted where it is not necessary to demonstrate the finding.

---

## Conclusion

This project took me through the stages of a black-box penetration test, starting with reconnaissance and moving through initial access, recovery of protected files, further investigation, and final reporting.

The main focus was to follow the project sequence, keep evidence for each stage, and relate the findings back to the steps used during the assessment.

---

## Project Information

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

---

[← Back to NETWORKWALKS](../../README.md)
