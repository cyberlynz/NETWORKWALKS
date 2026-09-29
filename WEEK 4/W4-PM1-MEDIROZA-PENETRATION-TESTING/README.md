<div align="center">

# 🔴 W4-PM1 — Mediroza General Hospital Penetration Testing

**NetworkWalks Cybersecurity & Ethical Hacking — Batch B083**  
**Week 04 | Penetration Testing Project**

![Cybersecurity](https://img.shields.io/badge/Cybersecurity-Penetration%20Testing-blue)
![NetworkWalks](https://img.shields.io/badge/NetworkWalks-B083-green)
![Black Box](https://img.shields.io/badge/Testing-Black--Box-orange)
![Ethical Hacking](https://img.shields.io/badge/Ethical%20Hacking-Lab-black)

</div>

---

## 📌 Introduction

For Week 04, I worked on a **Penetration Testing and Vulnerability Assessment** project for **Mediroza General Hospital**.

The exercise was a **5-day black-box penetration test** against:

`https://medirozahospital.com`

The project came with written permission to carry out the testing. I was also required to stay within the target domain, avoid social engineering and denial-of-service testing, and not test anything outside the agreed scope.

My work was divided into four milestones: gaining initial access, extracting the contents of the recovered files, investigating a further data exposure, and preparing the final penetration testing report.

> **Evidence folder:** [Open Evidence](./evidence/README.md)

---

## 🎯 Objectives

The main objective of this project was to carry out the assigned black-box penetration test on Mediroza General Hospital, demonstrate the impact of the weaknesses I found, document the evidence, and prepare a final penetration testing report.

---

## 📋 Scope and Rules

| Item | Details |
|---|---|
| Client | Mediroza General Hospital |
| Target | `https://medirozahospital.com` |
| Testing Type | Black-box Pentest |
| Project Type | Penetration Testing & Vulnerability Assessment |
| Duration | 5 Days |
| Authorization | Written permission granted |
| Scope | Target domain only |
| Restrictions | No social engineering, no denial of service, no testing outside scope |

---

# 🔎 M1 — Initial Access

For the first milestone, I was required to attack the website and retrieve **three confidential patient PDF lab reports**.

### My Approach

I started by looking at the target from a black-box point of view. The first part was reconnaissance and checking what was exposed by the application.

The project instructions required me to:

- Conduct reconnaissance on the target.
- Identify exposed entry points.
- Analyse any authentication mechanisms I found.
- Look for weaknesses in how the application handles user input.
- Gain access to a restricted area of the site.

Once access was obtained, I needed to retrieve the three patient PDF lab reports.

### Evidence to Capture

**Evidence 01 — Target reconnaissance**

> `[SCREENSHOT PLACEHOLDER]`  
> Capture the reconnaissance result showing information relevant to the target.

**Evidence 02 — Exposed entry point**

> `[SCREENSHOT PLACEHOLDER]`  
> Show the entry point or exposed area that led to further testing.

**Evidence 03 — Authentication mechanism**

> `[SCREENSHOT PLACEHOLDER]`  
> Capture the login or authentication page/response that was examined.

**Evidence 04 — Input handling**

> `[SCREENSHOT PLACEHOLDER]`  
> Show the relevant request, response, or application behaviour used during input testing.

**Evidence 05 — Restricted area access**

> `[SCREENSHOT PLACEHOLDER]`  
> Show proof that the restricted area was reached.

**Evidence 06–08 — Three retrieved PDF files**

> `[SCREENSHOT PLACEHOLDER]`  
> Add one screenshot for each of the three recovered patient PDF files.

### M1 Deliverable

The required deliverable for M1 was **proof of access and the three retrieved PDF files**.

---

# 🔐 M2 — Data Extraction

For M2, I was required to **crack the encryption on all three retrieved PDF files** and recover their contents.

### My Approach

I first analysed the protection used on each file instead of assuming that the same method would work for all three.

The project instructions required me to:

- Analyse the encryption on each file.
- Select suitable tools and wordlists.
- Try another method when the first one failed.
- Prove that I successfully recovered the contents.

### Evidence to Capture

**Evidence 09 — PDF 1 encryption analysis**

> `[SCREENSHOT PLACEHOLDER]`  
> Show the protection/encryption details identified for PDF 1.

**Evidence 10 — PDF 1 password recovery**

> `[SCREENSHOT PLACEHOLDER]`  
> Show the tool or terminal output proving successful recovery for PDF 1.

**Evidence 11 — PDF 1 successfully opened**

> `[SCREENSHOT PLACEHOLDER]`  
> Show the recovered PDF opened successfully.

**Evidence 12 — PDF 2 encryption analysis**

> `[SCREENSHOT PLACEHOLDER]`

**Evidence 13 — PDF 2 password recovery**

> `[SCREENSHOT PLACEHOLDER]`

**Evidence 14 — PDF 2 successfully opened**

> `[SCREENSHOT PLACEHOLDER]`

**Evidence 15 — PDF 3 encryption analysis**

> `[SCREENSHOT PLACEHOLDER]`

**Evidence 16 — PDF 3 password recovery**

> `[SCREENSHOT PLACEHOLDER]`

**Evidence 17 — PDF 3 successfully opened**

> `[SCREENSHOT PLACEHOLDER]`

### M2 Deliverable

The required deliverable was **the recovered contents of all three files with proof of successful access**.

---

# 🕵️ M3 — Critical Data Exposure

For M3, I had to go through the information I had already recovered and look for anything that could lead to another critical exposure on the server.

### My Approach

I was instructed to examine the recovered files carefully, including their properties and metadata, rather than only reading the visible contents.

The two specific tasks were to find:

- The salaries of all hospital employees.
- The shareholder details of the hospital.

The project also stated that AI tools were permitted and encouraged for data analysis and reporting.

### Evidence to Capture

**Evidence 18 — File properties / metadata**

> `[SCREENSHOT PLACEHOLDER]`  
> Show the file property or metadata that points to the further exposure.

**Evidence 19 — Staff salary exposure**

> `[SCREENSHOT PLACEHOLDER]`  
> Show the evidence that demonstrates exposure of staff salary information.

**Evidence 20 — Shareholder details exposure**

> `[SCREENSHOT PLACEHOLDER]`  
> Show the evidence that demonstrates exposure of shareholder information.

### M3 Deliverable

The required deliverable was **full documented evidence of the exposure and a readable summary of the confidential information uncovered**.

> **Note:** When adding screenshots to this public repository, sensitive patient, staff, or shareholder information should be redacted or masked where appropriate. Keep the evidence focused on proving the finding.

---

# 📝 M4 — Penetration Testing Report

The final milestone was to prepare the detailed penetration testing report.

I was expected to structure the report around the following sections:

### 1. Executive Summary

A short summary of the engagement, the main findings, and the overall risk identified during the assessment.

### 2. Scope and Methodology

This section should explain the target, tools used, approach followed, and any limitations encountered during the test.

### 3. Findings and Proof of Exploitation

Each finding should be documented with the relevant screenshots and supporting evidence from the milestones.

### 4. Risk Rating

Each identified vulnerability should be rated as:

- Critical
- High
- Medium
- Low

The rating should include a clear reason for the level assigned.

### 5. Recommendations and Remediation

Each finding should have practical steps that the client can take to fix or reduce the risk.

### Evidence to Capture

**Evidence 21 — Final report**

> `[SCREENSHOT PLACEHOLDER]`  
> Add a screenshot showing the completed final report or the final report submission.

---

## 🧠 What I Learned

This project gave me a practical way to follow a penetration test from the beginning to the reporting stage.

I had to think about the target from a black-box perspective, identify possible entry points, test the application, recover protected files, inspect the information I found, and then document the results properly.

One thing I took from the project is that finding one weakness can sometimes lead to another issue, so I need to pay attention to details in the evidence I collect and not stop at the first successful access.

I also learned that evidence collection is important throughout the assessment because the final report depends on being able to clearly show what I found and how I proved it.

---

## 🔐 Ethical Use

This work was carried out as part of the authorised NetworkWalks training project. The provided brief states that testing was authorised and limited to the specified target and rules.

These techniques should only be used where there is explicit permission from the system owner.

---

## 📚 Project Reference

The project brief supplied for Week 04 defines:

- The Mediroza General Hospital target.
- The black-box testing scope.
- The four project milestones.
- The required deliverables for each milestone.
- The final penetration testing report structure.

---

## 📋 Project Information

| Item | Details |
|---|---|
| Training Program | NetworkWalks Cybersecurity & Ethical Hacking |
| Batch | B083 |
| Week | 04 |
| Module | W4-PM1 |
| Project | Mediroza General Hospital Penetration Testing |
| Testing Type | Black-box Pentest |
| Target | `https://medirozahospital.com` |
| Duration | 5 Days |
| Author | Collins |

---
