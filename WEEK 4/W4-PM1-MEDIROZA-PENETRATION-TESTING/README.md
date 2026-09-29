<div align="center">

# 🏥 W4 — Mediroza General Hospital Penetration Testing

**NetworkWalks Cybersecurity & Ethical Hacking — Batch B083**  
**Week 04**

</div>

---

## Objectives

The project was divided into four milestones:

- **M1 — Initial Access:** Attack the website and retrieve 3 confidential patient PDF lab reports.
- **M2 — Data Extraction:** Crack the encryption on all 3 retrieved files.
- **M3 — Attack (cracking):** Find staff salaries and shareholder details of the hospital.
- **M4 — Pentest Report:** Write a professional penetration-testing report for the client.

---

## 1. Project Scope

| Item | Details |
|---|---|
| Client | Mediroza General Hospital |
| Target | `https://medirozahospital.com` |
| Testing Type | Black-box Pentest |
| Duration | 5 Days |

The assessment was authorised and limited to the target domain. Social engineering, denial of service, and testing outside the agreed scope were not permitted.

---

# 2. M1 — Initial Access

I began by carrying out reconnaissance against the target to identify exposed entry points and understand the application's accessible areas.

The project brief specifically directed me to examine authentication behaviour and how the application handled user input before attempting to reach the restricted area containing the patient reports.

### Reconnaissance

I first accessed:

`https://medirozahospital.com`

I reviewed the publicly accessible website and its available navigation.

The site exposed the following areas during the walkthrough:

- Home
- About
- Doctors
- Contact
- Patient Portal
- Staff Login

### Staff Login

I opened the **Staff Login** page and observed:

- Staff ID
- Password
- Sign in

The page also displayed **“Internal staff access only.”**

### Other Publicly Accessible Pages

I also reviewed the:

**Doctors** page, where information about the hospital's doctors was displayed.

**Contact and find us** page, where the site's address, phone number, email, and opening hours were displayed.

**Home** page, including the hospital introduction, **Book an appointment**, **Meet our doctors**, and **Our Departments**.

**About Mediroza** page, including information about the hospital, its values, and accreditation.

### M1 Evidence

Evidence for this milestone should show the reconnaissance results, identified entry point, authentication behaviour, input testing, restricted-area access, and the three retrieved patient PDFs.

---

# 3. M2 — Data Extraction

After obtaining the three files from M1, I moved to the second milestone.

The brief required me to analyse the protection used on each file, select appropriate tools and wordlists, and avoid assuming that the same method would work for all three files.

I therefore treated each file separately and changed the approach where necessary.

### File Analysis

| File | Protection / Encryption | Tool(s) | Wordlist | Result |
|---|---|---|---|---|
| PDF 1 | To be documented from evidence | To be documented | To be documented | To be documented |
| PDF 2 | To be documented from evidence | To be documented | To be documented | To be documented |
| PDF 3 | To be documented from evidence | To be documented | To be documented | To be documented |

### M2 Evidence

Evidence should show the protection identified for each PDF, the recovery process used, and successful access to all three files.

---

# 4. M3 — Attack: Critical Data Exposure

For M3, I reviewed everything collected from the earlier stages rather than treating the milestone as a completely separate task.

The brief specifically instructed me to examine the retrieved files and their properties carefully because one finding was expected to lead to another exposure on the server.

I was also permitted to use AI tools for data analysis and reporting.

### Required Investigation

I analysed:

- The information recovered from M2
- File properties and metadata
- Any information that could point to another exposed resource on the server

### Required Findings

The milestone required me to find:

- Staff salaries
- Shareholder details

### Data Summary

| Data | Result |
|---|---|
| Staff salaries | To be documented from evidence |
| Shareholder details | To be documented from evidence |

### M3 Evidence

Evidence should show the file property or other finding that led to the exposure, followed by proof of the exposed salary and shareholder information.

---

# 5. Findings and Risk Rating

The final report requires each identified vulnerability to be documented with supporting evidence and assigned a risk rating of **Critical, High, Medium, or Low**, with justification.

| Finding | Evidence | Risk |
|---|---|---|
| M1 — Initial access weakness | M1 evidence | To be assessed from evidence |
| M2 — File protection weakness | M2 evidence | To be assessed from evidence |
| M3 — Critical data exposure | M3 evidence | To be assessed from evidence |

I will only assign the final ratings after reviewing the actual evidence for each finding.

---

# 6. Recommendations and Remediation

For each confirmed vulnerability, the final report should include practical remediation steps addressing the underlying issue and reducing the possibility of the same exposure happening again.

The recommendations will be based on the confirmed findings rather than assumptions.

---

# 7. Final Report Structure

My completed M4 report will contain:

### Executive Summary
A concise summary of the engagement, confirmed findings, and overall risk.

### Scope and Methodology
The target, tools used, testing approach, and any limitations.

### Findings and Proof of Exploitation
Each confirmed vulnerability with the supporting screenshots and evidence.

### Risk Rating
A justified rating for each vulnerability.

### Recommendations and Remediation
Actions the client can take to address each confirmed issue.

---

# 8. Evidence Structure

The supporting evidence should follow the project workflow:

```
M1 — Initial Access
├── Reconnaissance
├── Exposed entry point
├── Authentication
├── Input testing
├── Restricted-area access
├── Patient PDF 1
├── Patient PDF 2
└── Patient PDF 3

M2 — Data Extraction
├── PDF 1 analysis
├── PDF 1 recovery
├── PDF 1 verification
├── PDF 2 analysis
├── PDF 2 recovery
├── PDF 2 verification
├── PDF 3 analysis
├── PDF 3 recovery
└── PDF 3 verification

M3 — Critical Data Exposure
├── File properties / metadata
├── Staff salaries
└── Shareholder details

M4 — Final Report
└── Completed penetration-testing report
```

---

## Conclusion

In this project, I followed the assessment from reconnaissance and initial access through file recovery, further investigation, and final reporting.

The main focus was not only finding weaknesses but also documenting the path from the initial entry point to the information exposed and supporting each finding with clear evidence.

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

