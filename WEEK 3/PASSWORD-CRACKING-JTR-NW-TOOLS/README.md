# 🔐 Password Cracking with JTR & NetworkWalks Tools

**NetworkWalks Cybersecurity & Ethical Hacking — Batch B083**  
**Week 03 | W3-PM1 & W3-PM2**

![Cybersecurity](https://img.shields.io/badge/Cybersecurity-Password%20Cracking-blue)
![John the Ripper](https://img.shields.io/badge/John%20the%20Ripper-JTR-C00000)
![NetworkWalks](https://img.shields.io/badge/NetworkWalks-B083-green)
![Windows](https://img.shields.io/badge/Platform-Windows%2010-0078D6)
![Ethical Hacking](https://img.shields.io/badge/Ethical%20Hacking-Lab-black)

---

## 📌 Introduction

During Week 03 of my NetworkWalks cybersecurity training, I worked on two practical exercises focused on password recovery:

- **W3-PM1 — Password Cracking with JTR**
- **W3-PM2 — Password Cracking with NetworkWalks Tools**

For the exercises, I worked with the supplied `My Locked PDF1.pdf`. I first examined how the protected PDF could be processed to obtain the information required for password recovery. I then used the assigned tools to perform the recovery process and checked the result by opening the document with the recovered password.

## 🎯 Objectives

By completing these practicals, I aimed to:

- Set up and use John the Ripper and Johnny.
- Extract a usable PDF hash from a protected document.
- Load a hash file into Johnny and initiate a password attack.
- Use the NetworkWalks Hash Calculator and Password Cracker.
- Confirm whether the recovered password successfully opened the PDF.
- Gain practical experience with password-security testing in an authorized lab.

---

# 🔴 W3-PM1 — Password Cracking with JTR

## Background

Before starting the practical, I reviewed how John the Ripper is used in password-security testing. I also learned that **Johnny** provides a graphical interface for working with John the Ripper.

The practical required me to recover the password of the supplied protected PDF using JTR and Johnny on a Windows PC.

### Tools I Used

- John the Ripper
- Johnny GUI
- Windows PC
- `My Locked PDF1.pdf`
- PDF hash extractor

## My Practical Steps

### 1. Installing John the Ripper and Johnny

I started by installing John the Ripper and Johnny on my Windows PC.

The lab provided the following resources:

- John the Ripper: https://www.openwall.com/john/
- Johnny GUI: https://openwall.info/wiki/john/johnny

After installing Johnny, I opened its configuration and selected the location of **`john.exe`** in the JTR `run` folder.

![Johnny configuration](./01-johnny-configuration.png)

### 2. Preparing the Protected PDF

I downloaded the supplied **`My Locked PDF1.pdf`** and confirmed that the document was password protected.

![Password-protected PDF](./02-pdf-locked.png)

### 3. Extracting the PDF Hash

I used the PDF hash extraction process provided in the lab to obtain the hash required by the cracking tool.

The extracted value began with:

`$pdf$`

I copied the complete hash and saved it in a file named **`hash1.txt`**.

![PDF hash extraction](./03-pdf-hash-extracted.png)

![Saved hash file](./04-hash1-txt.png)

### 4. Loading the Hash File in Johnny

I opened Johnny and used the **Open password file** option to load **`hash1.txt`**.

![Loading hash1 into Johnny](./05-johnny-password-file.png)

### 5. Starting the Password Attack

I started a new password-cracking attack from Johnny.

During this stage, I noted that the time required for cracking can vary depending on factors such as password complexity and computer performance.

![Johnny password attack](./06-johnny-attack-running.png)

### 6. Checking the Recovered Password

After the attack completed, the lab demonstration showed the recovered password as:

**`password1`**

I entered the recovered password into the protected PDF and confirmed that the document opened successfully.

![Password verification](./password-verification-steps.webp)

*I entered the recovered password and submitted it. The PDF then opened successfully and displayed the result.*

---

# 🔵 W3-PM2 — Password Cracking with NetworkWalks Tools

## Background

For the second practical, I worked with two NetworkWalks web-based tools: the **Hash Calculator** and **Password Cracker**.

Instead of using a locally installed cracking application, this exercise allowed me to follow the password-recovery process through a web browser. The main stages were obtaining the PDF hash, submitting it to the password-cracking tool, and checking the recovered password.

### Tools I Used

- NetworkWalks Hash Calculator
- NetworkWalks Password Cracker
- Web browser
- Windows laptop
- `My Locked PDF1.pdf`

## My Practical Steps

### 1. Preparing the PDF

For this practical, I used the supplied **`My Locked PDF1.pdf`**.

**Evidence:** `09-networkwalks-locked-pdf.png`

### 2. Using the NetworkWalks Hash Calculator

I opened the NetworkWalks Hash Calculator:

https://networkwalks.com/hash-calculator/

I uploaded the protected PDF and used the tool to obtain its PDF hash.

The returned hash began with:

`$pdf$`

I copied the complete hash for the next stage.

**Evidence:** `10-networkwalks-hash-calculator.png`

### 3. Opening the NetworkWalks Password Cracker

I then opened the NetworkWalks Password Cracker:

https://networkwalks.com/password-cracker/

### 4. Submitting the Hash

I pasted the extracted **`$pdf$...`** hash into the password-cracking interface and started the attack.

The tool tested password candidates until a matching password was found.

**Evidence:** `11-networkwalks-password-cracker.png`

### 5. Verifying the Result

The lab demonstration returned:

**PASSWORD CRACKED SUCCESSFULLY**

The recovered password was:

**`password1`**

I entered the password into the protected PDF and confirmed that I could open the document successfully.

**Evidence:** `12-password-cracked-successfully.png`  
**Evidence:** `13-pdf-opened-with-password.png`

---

# 🔄 My Password-Cracking Workflow

The overall process I followed was:

```text
My Locked PDF1.pdf
        │
        ▼
Extract PDF Hash
        │
        ▼
Copy / Save $pdf$... Hash
        │
        ├───────────────┐
        ▼               ▼
   JTR / Johnny     NW Hash Calculator
        │               │
        ▼               ▼
Password Attack    NW Password Cracker
        │               │
        └───────┬───────┘
                ▼
        Password Recovered
                │
                ▼
        Open Protected PDF
                │
                ▼
          Verify Access
```

---

# 🧠 What I Learned

This practical gave me hands-on experience with the different stages involved in password recovery.

- I learned how to prepare a protected PDF for the cracking process by obtaining its required hash.
- I became familiar with loading a hash file into Johnny and starting an attack with John the Ripper.
- I gained experience using the NetworkWalks Hash Calculator and Password Cracker through a web browser.
- I saw that different tools can follow the same general password-recovery process while providing different interfaces.
- I observed that password complexity and computer performance can affect the time required for an attack.
- I understood more clearly why predictable passwords can create security risks for protected documents.

---

# ✅ Results

I completed both practical modules and verified the result by opening the protected PDF with the recovered password.

| Practical | Tool | Result |
|---|---|---|
| W3-PM1 | John the Ripper / Johnny | PDF password recovered |
| W3-PM2 | NetworkWalks Hash Calculator | PDF hash extracted |
| W3-PM2 | NetworkWalks Password Cracker | PDF password recovered |
| Verification | PDF reader | Protected PDF opened successfully |

**Recovered lab password:** `password1`

> This is the password shown in the supplied NetworkWalks training material and demonstration. It should only be used with the provided lab file.

---

# 🔐 Security & Ethical Use

I performed this practical as part of a controlled cybersecurity training exercise.

The techniques covered in this project should only be used against files, systems, or accounts that I own or have explicit authorization to test. I carried out the exercise in the provided lab environment for learning and security-awareness purposes.

---

# 📚 References

- NetworkWalks — **W3-PM1: Password Cracking with JTR**
- NetworkWalks — **W3-PM2: Password Cracking with NetworkWalks Tools**
- NetworkWalks — **Week 3 Project Work**
- John the Ripper: https://www.openwall.com/john/
- Johnny: https://openwall.info/wiki/john/johnny
- NetworkWalks Hash Calculator: https://networkwalks.com/hash-calculator/
- NetworkWalks Password Cracker: https://networkwalks.com/password-cracker/

---

## 📋 Project Information

| Item | Details |
|---|---|
| Training Program | NetworkWalks Cybersecurity & Ethical Hacking |
| Batch | B083 |
| Week | 03 |
| Modules | W3-PM1 & W3-PM2 |
| Main Task | Password Cracking |
| Target File | `My Locked PDF1.pdf` |
| Platform | Windows PC / Web Browser |
| Author | Collins |
