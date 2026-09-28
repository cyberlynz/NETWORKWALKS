<div align="center">

# 🔴 Week 04 — Mediroza General Hospital Penetration Testing

**NetworkWalks Cybersecurity & Ethical Hacking — Batch B083**  
**Week 04 | Penetration Testing Project**

![Cybersecurity](https://img.shields.io/badge/Cybersecurity-Penetration%20Testing-blue)
![NetworkWalks](https://img.shields.io/badge/NetworkWalks-B083-green)
![Black Box](https://img.shields.io/badge/Testing-Black--Box-orange)
![Ethical Hacking](https://img.shields.io/badge/Ethical%20Hacking-Lab-black)

</div>

---

## 📌 Introduction

During Week 04 of my NetworkWalks cybersecurity training, I worked on a **Penetration Testing & Vulnerability Assessment** project for **Mediroza General Hospital**.

**Target:** `https://medirozahospital.com`  
**Testing Type:** Black-box Pentest  
**Duration:** 5 Days

The project had written authorization for testing. The scope was limited to the target domain, with no social engineering, denial-of-service testing, or testing outside the agreed scope.

## 🎯 Objectives

The project was divided into four milestones:

- **M1 — Initial Access:** Attack the website and retrieve 3 confidential patient PDF lab reports.
- **M2 — Data Extraction:** Crack the encryption on all 3 retrieved files.
- **M3 — Attack (cracking):** Find staff salaries and shareholder details of the hospital.
- **M4 — Pentest Report:** Write a professional penetration-testing report for the client.

---

# 🔎 M1 — Initial Access

## Objective

The first milestone was to attack the website and find the **3 confidential PDF lab reports of patients**.

### My Approach

I started with reconnaissance of the target and reviewed the publicly accessible areas of the website.

### 1. Opening the Target Website

I accessed:

`https://medirozahospital.com`

I reviewed the homepage and the available navigation.

The site showed:

- Home
- About
- Doctors
- Contact
- Patient Portal
- Staff Login

### 2. Checking Staff Login

I opened the **Staff Login** page.

The page contained:

- Staff ID
- Password
- Sign in

It also showed the message:

**Internal staff access only.**

### 3. Checking the Doctors Page

I opened the **Doctors** page and reviewed the information displayed about the hospital's doctors.

### 4. Checking the Contact Page

I opened the **Contact and find us** page and reviewed the available:

- Address
- Phone number
- Email
- Opening hours

### 5. Returning to the Home Page

I returned to the homepage and reviewed the main content, including:

- Book an appointment
- Meet our doctors
- Our Departments

The page also displayed the introduction:

**“Compassionate care, advanced medicine.”**

### 6. Checking the About Page

I opened the **About Mediroza** page and reviewed the sections covering:

- The hospital
- Its values
- Accreditation

### M1 Deliverable

The required deliverable for M1 was:

**Proof of access and the 3 retrieved PDF files.**

---

# 🔐 M2 — Data Extraction

## Objective

The second milestone was to **crack the encryption on all 3 retrieved files**.

### My Required Process

For this stage, I was required to:

1. Analyse the encryption on each file.
2. Select appropriate tools and wordlists to recover the contents.
3. Avoid assuming that one approach would work for all 3 files.
4. Try another approach when one method failed.

### M2 Deliverable

**Recovered contents of all 3 files with proof of successful access.**

---

# 🕵️ M3 — Critical Data Exposure

## Objective

The third milestone was to **find the critical data exposure on the client server**.

### My Required Process

I was required to:

1. Analyse everything retrieved so far.
2. Examine the file properties carefully.
3. Follow the finding that pointed to another critical exposure on the server.
4. Use AI tools for data analysis and reporting where appropriate.

### Tasks

I was required to find:

- The salaries of all hospital employees.
- The shareholder details of the hospital.

### M3 Deliverable

**Full documented evidence of the exposure and a readable summary of the confidential data uncovered.**

---

# 📝 M4 — Penetration Testing Report

## Objective

The final milestone was to prepare the penetration-testing report.

The required structure was:

### 1. Executive Summary
A concise overview of the engagement, key findings, and overall risk.

### 2. Scope and Methodology
Document the target, tools used, approach taken, and any limitations.

### 3. Findings and Proof of Exploitation
Document each vulnerability with screenshots and evidence for every milestone.

### 4. Risk Rating
Rate each vulnerability as:

- Critical
- High
- Medium
- Low

with justification.

### 5. Recommendations and Remediation
Provide actionable steps to fix each identified issue.

---

## 🧠 What I Learned

This project helped me understand the structure of a black-box penetration test, starting with reconnaissance and moving through access, data extraction, further analysis, and final reporting. I also learned the importance of collecting clear evidence throughout the assessment and working strictly within the defined scope.

---

## 📋 Project Information

| Item | Details |
|---|---|
| Training Program | NetworkWalks Cybersecurity & Ethical Hacking |
| Batch | B083 |
| Week | 04 |
| Project | Mediroza General Hospital Penetration Testing |
| Type | Penetration Testing & Vulnerability Assessment |
| Testing Type | Black-box Pentest |
| Target | `https://medirozahospital.com` |
| Duration | 5 Days |
| Author | Collins |

