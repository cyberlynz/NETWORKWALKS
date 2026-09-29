# W4 — Mediroza General Hospital Penetration Testing Report

**NetworkWalks Cybersecurity & Ethical Hacking — Batch B083**  
**Week 04 | Mediroza General Hospital**

---

## Introduction

For Week 04, I worked on a penetration testing and vulnerability assessment project for Mediroza General Hospital.

The exercise was a **black-box penetration test** carried out over **5 days** against:

`https://medirozahospital.com`

The project brief stated that written permission had been granted and that my testing had to remain within the target domain. Social engineering, denial-of-service testing and testing outside the agreed scope were not allowed.

The work was divided into four milestones:

1. **Initial Access**
2. **Data Extraction**
3. **Critical Data Exposure**
4. **Penetration Testing Report**

---

## Objectives

My main objective was to follow the project brief from the initial reconnaissance stage through exploitation, file recovery, further investigation and final reporting.

The specific tasks given to me were to:

- Gain access to the restricted area of the website.
- Retrieve three confidential patient PDF lab reports.
- Crack the encryption on all three files.
- Investigate the recovered information for a further critical exposure.
- Find the hospital employee salary information and shareholder details.
- Document my work and prepare the final penetration testing report.

---

# M1 — Initial Access

## What I Did

I started with reconnaissance on the target and looked at the publicly accessible parts of the website.

The project brief instructed me to:

- Conduct reconnaissance on the target.
- Identify exposed entry points.
- Analyse any authentication mechanisms I found.
- Look for weaknesses in how the application handles user input.
- Gain access to a restricted area of the site.

After gaining access to the restricted area, I was required to retrieve the three confidential patient PDF lab reports.

## Evidence

**Screenshot 1 — Reconnaissance**

`[INSERT SCREENSHOT HERE]`

I will use this screenshot to show the reconnaissance information I collected from the target.

**Screenshot 2 — Exposed Entry Point**

`[INSERT SCREENSHOT HERE]`

This screenshot will show the entry point I identified during the assessment.

**Screenshot 3 — Authentication**

`[INSERT SCREENSHOT HERE]`

This will show the authentication mechanism I examined.

**Screenshot 4 — Input Testing**

`[INSERT SCREENSHOT HERE]`

This will show the relevant request, response or application behaviour observed while testing input handling.

**Screenshot 5 — Restricted Area**

`[INSERT SCREENSHOT HERE]`

This will provide proof that I reached the restricted area.

**Screenshot 6 — Patient Report 1**

`[INSERT SCREENSHOT HERE]`

**Screenshot 7 — Patient Report 2**

`[INSERT SCREENSHOT HERE]`

**Screenshot 8 — Patient Report 3**

`[INSERT SCREENSHOT HERE]`

## M1 Result

The required result for this milestone was proof of access together with the three retrieved PDF files.

---

# M2 — Data Extraction

## What I Did

For the second milestone, I worked on the three PDF files I had retrieved.

The brief instructed me to:

- Analyse the encryption on each file.
- Select appropriate tools and wordlists to recover the contents.
- Avoid assuming that the same method would work for all three files.
- Try another method when one approach failed.

I treated each file separately and documented the recovery process and the final successful access.

## Evidence

**Screenshot 9 — PDF 1 Encryption Analysis**

`[INSERT SCREENSHOT HERE]`

**Screenshot 10 — PDF 1 Recovery**

`[INSERT SCREENSHOT HERE]`

**Screenshot 11 — PDF 1 Opened Successfully**

`[INSERT SCREENSHOT HERE]`

**Screenshot 12 — PDF 2 Encryption Analysis**

`[INSERT SCREENSHOT HERE]`

**Screenshot 13 — PDF 2 Recovery**

`[INSERT SCREENSHOT HERE]`

**Screenshot 14 — PDF 2 Opened Successfully**

`[INSERT SCREENSHOT HERE]`

**Screenshot 15 — PDF 3 Encryption Analysis**

`[INSERT SCREENSHOT HERE]`

**Screenshot 16 — PDF 3 Recovery**

`[INSERT SCREENSHOT HERE]`

**Screenshot 17 — PDF 3 Opened Successfully**

`[INSERT SCREENSHOT HERE]`

## M2 Result

The required result was the recovered contents of all three files with proof that I was able to access them successfully.

---

# M3 — Critical Data Exposure

## What I Did

For the third milestone, I went back through the information I had already collected and looked for anything else that could lead to a critical exposure on the server.

The brief specifically instructed me to:

- Analyse everything retrieved so far.
- Look beyond the obvious content.
- Examine file properties carefully.
- Follow the finding that pointed to another critical exposure.

I was also allowed to use AI tools for data analysis and reporting.

The tasks given to me were to find:

- The salaries of all hospital employees.
- The shareholder details of the hospital.

## Evidence

**Screenshot 18 — File Properties / Metadata**

`[INSERT SCREENSHOT HERE]`

This will show the file property or metadata that led me to the next finding.

**Screenshot 19 — Staff Salary Exposure**

`[INSERT SCREENSHOT HERE]`

This will show the evidence of the exposed staff salary information.

**Screenshot 20 — Shareholder Details Exposure**

`[INSERT SCREENSHOT HERE]`

This will show the evidence of the exposed shareholder information.

## M3 Result

The required result was full documented evidence of the exposure together with a readable summary of the confidential information uncovered.

---

# M4 — Penetration Testing Report

The final milestone was to put everything together into a detailed penetration testing report.

The required report structure was:

## 1. Executive Summary

A concise overview of the engagement, the main findings and the overall risk to the client.

## 2. Scope and Methodology

The target, tools used, approach taken and any limitations encountered during the assessment.

## 3. Findings and Proof of Exploitation

Each vulnerability should be documented with screenshots and supporting evidence from the different milestones.

## 4. Risk Rating

Each vulnerability should be rated:

- Critical
- High
- Medium
- Low

with a reason for the rating.

## 5. Recommendations and Remediation

Actionable steps that the client can take to fix each identified issue.

## Final Evidence

**Screenshot 21 — Final Report**

`[INSERT SCREENSHOT HERE]`

This will show the completed penetration testing report or proof of submission.

---

# Conclusion

This Week 04 project helped me understand how a black-box penetration test can move from the initial reconnaissance stage to gaining access, recovering protected files, investigating further exposure and finally documenting the findings.

I also understood why keeping proper evidence during the assessment is important. Each milestone had a specific deliverable, so I needed to make sure that my screenshots and notes supported what I had done.

Overall, the project gave me more practical experience with following a penetration testing workflow and documenting the results in a structured way.

---

## Ethical Use

This was an authorised training exercise conducted within the scope provided by NetworkWalks. The techniques used in this project should only be applied to systems where permission has been given by the owner.

---

## Project Information

| Item | Details |
|---|---|
| Training Program | NetworkWalks Cybersecurity & Ethical Hacking |
| Batch | B083 |
| Week | 04 |
| Project | Mediroza General Hospital Penetration Testing |
| Testing Type | Black-box Pentest |
| Duration | 5 Days |
| Target | `https://medirozahospital.com` |
| Author | Collins |
