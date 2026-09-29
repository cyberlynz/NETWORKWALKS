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

I carried out the work within the scope and rules provided for the NetworkWalks project.

---

## 🔎 Assessment Overview

I approached the project in stages, beginning with reconnaissance and moving through initial access, recovery of the protected files, further analysis of the recovered information, and final reporting.

The public-facing walkthrough included reviewing the target homepage, navigation, Staff Login, Doctors, Contact, and About pages. The later stages focus on the three protected PDF reports and the additional information that can be reached from the earlier findings.

### Project Flow

```
Reconnaissance
    ↓
M1 — Initial Access
    ↓
3 Confidential Patient PDF Reports
    ↓
M2 — Data Extraction
    ↓
Recovered Contents
    ↓
M3 — Critical Data Exposure
    ↓
Staff Salaries + Shareholder Details
    ↓
M4 — Penetration Testing Report
```

---

## 📂 Project Sections

| Section | Purpose |
|---|---|
| [M1 — Initial Access](./M1-INITIAL-ACCESS/README.md) | Reconnaissance, entry points, authentication/input testing, restricted access and the three PDFs |
| [M2 — Data Extraction](./M2-DATA-EXTRACTION/README.md) | Analyse and recover the three protected files |
| [M3 — Critical Data Exposure](./M3-ATTACK-CRITICAL-DATA-EXPOSURE/README.md) | Trace the additional exposure and document the required confidential information |
| [M4 — Pentest Report](./M4-PENTEST-REPORT/README.md) | Consolidate the assessment into the required professional report |
| [Evidence](./evidence/README.md) | Screenshot/evidence index for M1–M4 |

---

## 📸 Evidence

I am keeping evidence in the same order as the assessment so that each screenshot can be linked directly to the step it supports.

For sensitive patient, employee, or shareholder information, only the minimum information needed to demonstrate the finding should be shown.

---

## 🧠 Summary

This project gave me practical experience following a black-box penetration-testing workflow. I started by understanding what was publicly exposed on the target, then worked through the project milestones to identify restricted information, recover the protected files, investigate the additional exposure, and document the results.

I also learned that the quality of a penetration test depends on keeping clear evidence and relating each finding back to the steps used to reach it.

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

---

[← Back to NETWORKWALKS](../../README.md)
