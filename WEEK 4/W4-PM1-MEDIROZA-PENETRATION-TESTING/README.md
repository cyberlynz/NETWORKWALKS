<div align="center">

# 🏥 W4-PM — Mediroza General Hospital Penetration Testing

**NetworkWalks Cybersecurity & Ethical Hacking — Batch B083**  
**Week 04 | Project Module**

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
| Testing Type | Black-box Pentest |
| Duration | 5 Days |
| Authorization | Written permission granted |
| Scope | Target domain only |
| Restrictions | No social engineering, DoS, or testing outside scope |

The engagement was carried out in the authorised NetworkWalks training environment.

---

# 🔎 M1 — Initial Access

I began with reconnaissance of the target and reviewed the publicly accessible parts of the website before moving toward the restricted areas.

The project brief required me to:

- Conduct reconnaissance.
- Identify exposed entry points.
- Analyse authentication behaviour.
- Look for weaknesses in user-input handling.
- Gain access to a restricted area.
- Retrieve the three confidential patient PDF lab reports.

## Reconnaissance

I accessed:

`https://medirozahospital.com`

During the walkthrough, I reviewed the site's main navigation and publicly accessible pages.

The navigation included:

- Home
- About
- Doctors
- Contact
- Patient Portal
- Staff Login

### Staff Login

I opened the **Staff Login** page and observed a **Staff ID** field, **Password** field, and **Sign in** button. The page also displayed:

> Internal staff access only.

### Other Pages Reviewed

**Doctors:** I reviewed the information presented about the hospital's doctors.

**Contact:** I reviewed the displayed address, phone number, email, and opening hours.

**Home:** I reviewed the main page content, including **Book an appointment**, **Meet our doctors**, and **Our Departments**.

**About:** I reviewed information covering the hospital, its values, and accreditation.

### M1 Evidence

The evidence for this milestone should document the reconnaissance, exposed entry point, authentication behaviour, input testing, restricted-area access, and retrieval of the three PDF reports.

---

# 🔐 M2 — Data Extraction

After retrieving the three files, I moved to the file-recovery stage.

The brief required me to analyse the protection used by each file and select appropriate tools and wordlists. It also specifically required me to avoid assuming that the same method would work for all three files.

For each file, I documented:

| Item | Details |
|---|---|
| Filename | To be recorded from evidence |
| Protection / Encryption | To be identified from evidence |
| Tool(s) Used | To be recorded from evidence |
| Wordlist | To be recorded from evidence |
| Recovery Result | To be recorded from evidence |

### M2 Evidence

Evidence should show:

- The protection identified on each file.
- The recovery method used.
- Successful access to each recovered file.

---

# 🕵️ M3 — Attack: Critical Data Exposure

For M3, I analysed the information collected during the earlier stages to identify a further exposure on the client server.

The brief specifically required me to look beyond the obvious content and examine the properties of the retrieved files carefully. One finding should lead to the additional server exposure.

### Investigation

I reviewed:

- Retrieved file contents.
- File properties and metadata.
- Any information that could point to another exposed resource on the server.

### Required Data

The milestone required me to find:

- Staff salaries.
- Shareholder details.

### Results

| Data | Finding |
|---|---|
| Staff salaries | To be documented from captured evidence |
| Shareholder details | To be documented from captured evidence |

### M3 Evidence

Evidence should show the finding that led from the retrieved files to the additional exposure, followed by proof of the salary and shareholder information.

---

# 📝 M4 — Penetration Testing Report

The final milestone was to consolidate the assessment into a professional report.

The report structure required by the project brief is:

### 01 — Executive Summary
Summary of the engagement, key findings, and overall risk.

### 02 — Scope and Methodology
Target, tools used, approach taken, and limitations.

### 03 — Findings and Proof of Exploitation
Each confirmed vulnerability with screenshots and supporting evidence.

### 04 — Risk Rating
Each vulnerability rated **Critical, High, Medium, or Low**, with justification.

### 05 — Recommendations and Remediation
Actionable recommendations for addressing each finding.

---

# 📸 Evidence Index

The evidence is arranged to follow the actual project workflow.

| Section | Evidence |
|---|---|
| **M1** | Reconnaissance, exposed entry point, authentication, input testing, restricted-area access, three patient PDFs |
| **M2** | Protection analysis, recovery process, successful access for all three files |
| **M3** | File properties/metadata, staff salary exposure, shareholder details |
| **M4** | Final penetration-testing report |

Sensitive information should be redacted where necessary before screenshots are published in a public repository.

---

# 🧠 Summary

This project took me through a complete black-box penetration-testing workflow: starting with reconnaissance, identifying exposed areas, gaining access to restricted information, recovering protected files, investigating additional exposure, and documenting the findings.

I kept the assessment focused on the defined target and used evidence from each stage to support the final report.

---

## 📚 Project Information

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

## 🔗 Related

- [← Back to NETWORKWALKS](../../README.md)
