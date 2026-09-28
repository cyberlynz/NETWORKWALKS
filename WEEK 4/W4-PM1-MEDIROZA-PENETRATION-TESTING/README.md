<div align="center">

# 🔴 W4-PM1 — Mediroza General Hospital Penetration Testing

**NetworkWalks Cybersecurity & Ethical Hacking — Batch B083**  
**Week 04 | Penetration Testing Project**

</div>

---

## Introduction

For Week 04, I worked on a **Penetration Testing & Vulnerability Assessment** project for **Mediroza General Hospital**.

**Target:** `https://medirozahospital.com`  
**Testing Type:** Black-box Pentest  
**Duration:** 5 Days

The project was conducted within the defined scope and with written authorization for testing. Testing was limited to the target domain, with no social engineering, denial-of-service testing, or testing outside the agreed scope.

---

## Project Objectives

The project was divided into four milestones:

| Milestone | Objective |
|---|---|
| **M1 — Initial Access** | Attack the website and retrieve 3 confidential patient PDF lab reports |
| **M2 — Data Extraction** | Crack the encryption on all 3 retrieved files |
| **M3 — Attack (cracking)** | Find staff salaries and shareholder details |
| **M4 — Pentest Report** | Write a professional penetration-testing report |

---

# M1 — Initial Access

### Objective

Attack the website and find the **3 confidential PDF lab reports of patients**.

### Approach

The project brief instructed me to:

1. Conduct reconnaissance on the target.
2. Identify exposed entry points.
3. Analyse the behaviour of any authentication mechanisms found.
4. Look for weaknesses in how the application handles user input.
5. Gain access to a restricted area of the site.

### Website Reconnaissance

I started by accessing:

`https://medirozahospital.com`

I reviewed the publicly accessible pages and navigation.

The main navigation showed:

- Home
- About
- Doctors
- Contact
- Patient Portal

A **Staff Login** link was also visible.

### Staff Login

I opened the **Staff Login** page, which contained:

- Staff ID
- Password
- Sign in button

The page stated **“Internal staff access only.”**

No successful login was shown in the walkthrough.

### Doctors Page

I opened the **Doctors** page and reviewed the information displayed about the hospital's doctors.

### Contact Page

I opened the **Contact and find us** page and reviewed the displayed:

- Address
- Phone number
- Email
- Opening hours

### Home Page

I returned to the homepage and reviewed the hospital introduction, including:

**“Compassionate care, advanced medicine.”**

I also observed the **Book an appointment**, **Meet our doctors**, and **Our Departments** sections.

### About Page

I opened the **About Mediroza** page and reviewed information about:

- The hospital
- Its values
- Accreditation

### M1 Deliverable

The required deliverable was:

**Proof of access and the 3 retrieved PDF files.**

The supplied walkthrough did not show the actual retrieval of the three PDFs.

---

# M2 — Data Extraction

### Objective

Crack the encryption on all **3 retrieved files**.

### Required Approach

I was instructed to:

1. Analyse the encryption on each file.
2. Select appropriate tools and wordlists to recover the contents.
3. Avoid assuming that one approach would work for all three files.
4. Try another approach when one method fails.

### Deliverable

**Recovered contents of all 3 files with proof of successful access.**

The supplied walkthrough did not show the actual file-cracking process.

---

# M3 — Critical Data Exposure

### Objective

Find the **critical data exposure on the client server**.

### Required Approach

I was instructed to:

1. Thoroughly analyse everything retrieved so far.
2. Examine all file properties carefully.
3. Use the finding that points to a further exposure on the server.
4. Use AI tools where appropriate for data analysis and reporting.

### Tasks

- Find the salaries of all hospital employees.
- Find the shareholder details of the hospital.

### Deliverable

**Full documented evidence of the exposure and a readable summary of the confidential data uncovered.**

The supplied walkthrough did not show the actual discovery of this information.

---

# M4 — Penetration Testing Report

### Objective

Prepare a detailed penetration-testing report covering:

### 1. Executive Summary
A concise overview of the engagement, key findings, and overall risk.

### 2. Scope and Methodology
Document the target, tools used, approach taken, and any limitations.

### 3. Findings and Proof of Exploitation
Document each vulnerability with screenshots and evidence for every milestone.

### 4. Risk Rating
Rate each vulnerability as **Critical, High, Medium, or Low**, with justification.

### 5. Recommendations and Remediation
Provide actionable steps to address each identified issue.

---

## Project Workflow

**Reconnaissance**  
↓  
**M1 — Initial Access**  
↓  
**Retrieve 3 confidential patient PDFs**  
↓  
**M2 — Crack all 3 files**  
↓  
**M3 — Identify the critical server exposure**  
↓  
**Find employee salaries and shareholder details**  
↓  
**M4 — Prepare the penetration-testing report**

---

## What I Learned

This project helped me understand how a black-box penetration test progresses from reconnaissance to exploitation, data analysis, and reporting. I also learned the importance of documenting evidence at each stage and staying within the defined testing scope.

---

## Project Information

| Item | Details |
|---|---|
| Training Program | NetworkWalks Cybersecurity & Ethical Hacking |
| Batch | B083 |
| Week | 04 |
| Project | Mediroza General Hospital Penetration Testing |
| Type | Black-box Pentest |
| Target | `https://medirozahospital.com` |
| Duration | 5 Days |
| Author | Collins |

