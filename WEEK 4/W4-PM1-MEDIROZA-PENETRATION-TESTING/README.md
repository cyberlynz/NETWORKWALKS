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

For **Week 04**, the project is a **Penetration Testing & Vulnerability Assessment** exercise against **Mediroza General Hospital**.

The project is a **full black-box penetration test** with a **5-day** timeline. The target is:

`https://medirozahospital.com`

The project brief states that written authorization has been provided for the security testing and that testing is limited to the target domain. Social engineering, denial of service, and testing outside the agreed scope are not allowed.

This write-up documents the project brief, milestone requirements, and the reconnaissance walkthrough reviewed for the project.

> **Important:** The supplied walkthrough explains the project and demonstrates initial website inspection. It does not show the actual exploitation, retrieval of the three PDFs, file cracking, discovery of salary/shareholder information, or completion of the final penetration-testing report. Those results are therefore not claimed as completed in this README.

---

## 🎯 Project Objectives

The project is divided into four milestones:

| Milestone | Objective |
|---|---|
| **M1 — Initial Access** | Attack the website and retrieve 3 confidential patient PDF lab reports |
| **M2 — Data Extraction** | Crack the encryption on all 3 retrieved files |
| **M3 — Attack (cracking)** | Find staff salaries and shareholder details of the hospital |
| **M4 — Pentest Report** | Write a professional penetration-testing report for the client |

---

## 🛡️ Scope, Rules & Authorization

### Scope

The assignment requires a **full black-box penetration test** to identify vulnerabilities, exploit them to demonstrate real impact, and document the findings in a professional report.

### Rules

Testing is limited to:

- The target domain only
- No social engineering
- No denial of service
- No testing outside the agreed scope

### Authorization

The project brief states that the client has provided **written authorization** to conduct security testing on its web infrastructure.

### Timeline

- **Duration:** 5 days
- Work independently
- Do not discuss findings with other participants until the reveal session

---

# 🔎 Milestone 1 — Initial Access

## Objective

**Attack the website and find the 3 confidential PDF lab reports of patients.**

**Written Permission: GRANTED**

### Required Approach

The M1 brief gives the following guidance:

1. Conduct reconnaissance on the target.
2. Identify exposed entry points.
3. Analyse the behaviour of any authentication mechanisms found.
4. Look for weaknesses in how the application handles user input.
5. Gain unauthorised access to a restricted area of the site.

### Deliverable

**Proof of access and the 3 retrieved PDF files.**

---

## 🌐 Website Reconnaissance Walkthrough

As part of the supplied walkthrough, I inspected the publicly accessible Mediroza General Hospital website before moving into the later project milestones.

### Step 1 — Open the Target Website

I accessed:

`https://medirozahospital.com`

The homepage displayed the hospital's main navigation and introductory content.

### Step 2 — Inspect the Main Navigation

The visible navigation included:

- Home
- About
- Doctors
- Contact
- Patient Portal

A **Staff Login** link was also visible.

### Step 3 — Inspect the Staff Login Page

The **Staff Login** page was opened.

The page contained:

- Staff ID field
- Password field
- Sign in button

The page also indicated:

**Internal staff access only.**

The walkthrough did not show a successful login.

### Step 4 — Inspect the Doctors Page

The **Doctors** page was opened.

The page displayed the hospital's doctors and their information.

### Step 5 — Inspect the Contact Page

The **Contact and find us** page was opened.

The page displayed contact information including:

- Address
- Phone number
- Email
- Opening hours

### Step 6 — Return to the Home Page

The homepage was revisited.

The page included the hospital introduction:

**“Compassionate care, advanced medicine.”**

It also displayed options such as:

- Book an appointment
- Meet our doctors

and an **Our Departments** section.

### Step 7 — Inspect the About Page

The **About Mediroza** page was opened.

The page contained information about the hospital, including sections covering:

- The hospital
- Its values
- Accreditation

---

# 🔐 Milestone 2 — Data Extraction

## Objective

**Crack the encryption on all 3 retrieved files.**

**Written Permission: GRANTED**

### Required Approach

The M2 brief instructs the tester to:

1. Analyse the encryption on each file.
2. Select appropriate tools and wordlists to recover the contents.
3. Do not assume a single approach will work for all 3 files.
4. Think carefully when one method fails and try another.

### Deliverable

**Recovered contents of all 3 files with proof of successful access.**

---

# 🕵️ Milestone 3 — Critical Data Exposure

## Objective

**Find the critical data exposure on the client server.**

**Written Permission: GRANTED**

### Required Approach

The M3 brief instructs the tester to:

1. Conduct a thorough analysis of everything retrieved so far.
2. Look beyond the obvious content and examine all file properties carefully.
3. Use the finding that points to a further critical exposure on the server.
4. AI tools are permitted and encouraged for data analysis and reporting.

### Tasks

The project requires finding:

- The salaries of all hospital employees.
- The shareholder details of the hospital.

### Deliverable

**Full documented evidence of the exposure and a readable summary of the confidential data uncovered.**

---

# 📝 Milestone 4 — Penetration Testing Report

## Objective

**Write a detailed penetration-testing report.**

The required report structure contains five sections.

### 01 — Executive Summary

A concise overview covering:

- The engagement
- Key findings
- Overall risk to the client

### 02 — Scope and Methodology

Document:

- Target
- Tools used
- Approach taken
- Any limitations encountered

### 03 — Findings and Proof of Exploitation

For each vulnerability:

- Document the vulnerability
- Include screenshots
- Include evidence for every milestone

### 04 — Risk Rating

Rate each vulnerability as:

- Critical
- High
- Medium
- Low

with justification.

### 05 — Recommendations and Remediation

Provide actionable steps for the client to fix each identified issue.

### Final Deliverable

A **complete professional penetration-testing report** submitted to the instructor.

---

## 📚 Project Workflow Summary

The Week 04 project follows this sequence:

**Project Scope & Authorization**  
↓  
**M1 — Initial Access**  
↓  
**Retrieve 3 confidential patient PDF reports**  
↓  
**M2 — Crack the encryption on all 3 files**  
↓  
**M3 — Analyse retrieved information and identify the critical server exposure**  
↓  
**Find employee salaries and shareholder details**  
↓  
**M4 — Document the findings in a professional penetration-testing report**

---

## 🧠 What I Learned from the Project Brief and Walkthrough

- I learned how a black-box penetration-testing project is structured from reconnaissance through reporting.
- I learned that the initial stage focuses on reconnaissance, exposed entry points, authentication behaviour, input handling, and access to restricted areas.
- I learned that the second milestone requires analysing each retrieved file individually and being prepared to use different approaches.
- I learned that the third milestone requires looking beyond the obvious information and examining file properties carefully.
- I learned that the final report must include scope, methodology, findings, proof of exploitation, risk ratings, and remediation recommendations.
- I also learned the importance of staying within the defined target and testing rules throughout the engagement.

---

## 🔐 Security & Ethical Use

This project is conducted in a controlled environment for educational purposes.

The project brief states that the target has been authorised for security testing by NetworkWalks. These techniques must not be applied to any system without explicit written permission from the owner.

---

## 📋 Project Information

| Item | Details |
|---|---|
| Training Program | NetworkWalks Cybersecurity & Ethical Hacking |
| Batch | B083 |
| Week | 04 |
| Project | Mediroza General Hospital Penetration Testing |
| Project Type | Penetration Testing & Vulnerability Assessment |
| Testing Type | Black-box Pentest |
| Target | https://medirozahospital.com |
| Client | Mediroza General Hospital |
| Duration | 5 Days |
| Author | Collins |

---

## 📚 Source Material

- NetworkWalks — Week 04 Penetration Testing Project: **Mediroza General Hospital**
- Target: `https://medirozahospital.com`
