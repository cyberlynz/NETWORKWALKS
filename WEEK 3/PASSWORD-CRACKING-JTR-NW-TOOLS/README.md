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

As part of my Week 03 NetworkWalks cybersecurity training, I completed two practical modules focused on password cracking:

- **W3-PM1 — Password Cracking with JTR**
- **W3-PM2 — Password Cracking with NetworkWalks Tools**

For this practical, I worked with the supplied password-protected PDF **`My Locked PDF1.pdf`**. My objective was to understand how a protected PDF hash can be extracted, processed by password-cracking tools, and used to recover the password in a controlled lab environment.

I also verified the recovered password by using it to open the protected PDF.

## 🎯 Objectives

During this practical, I aimed to:

- Understand the basic password-cracking workflow.
- Use **John the Ripper (JTR)** and **Johnny GUI**.
- Extract a crackable PDF hash.
- Use the **NetworkWalks Hash Calculator**.
- Use the **NetworkWalks Password Cracker**.
- Verify the recovered password against the protected PDF.
- Record what I learned from the practical.

---

# 🔴 W3-PM1 — Password Cracking with JTR

## Tools I Used

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

**Evidence:** `01-johnny-configuration.png`

### 2. Preparing the Protected PDF

I downloaded the supplied **`My Locked PDF1.pdf`** and confirmed that the document was password protected.

**Evidence:** `02-pdf-locked.png`

### 3. Extracting the PDF Hash

I used the PDF hash extraction process provided in the lab to obtain the hash required by the cracking tool.

The extracted value began with:

`$pdf$`

I copied the complete hash and saved it in a file named **`hash1.txt`**.

**Evidence:** `03-pdf-hash-extracted.png`  
**Evidence:** `04-hash1-txt.png`

### 4. Loading the Hash File in Johnny

I opened Johnny and used the **Open password file** option to load **`hash1.txt`**.

**Evidence:** `05-johnny-password-file.png`

### 5. Starting the Password Attack

I started a new password-cracking attack from Johnny.

At this stage, I observed that the time required for cracking can depend on factors such as password complexity and computer performance.

**Evidence:** `06-johnny-attack-running.png`

### 6. Checking the Recovered Password

After the attack completed, the lab demonstration showed the recovered password as:

**`password1`**

I then entered the recovered password into the protected PDF and confirmed that the document opened successfully.

**Evidence:** `07-jtr-password-recovered.png`  
**Evidence:** `08-pdf-opened-with-password.png`

---

# 🔵 W3-PM2 — Password Cracking with NetworkWalks Tools

## Tools I Used

- NetworkWalks Hash Calculator
- NetworkWalks Password Cracker
- Web browser
- Windows laptop
- `My Locked PDF1.pdf`

## My Practical Steps

### 1. Preparing the PDF

For the second practical, I used the same supplied **`My Locked PDF1.pdf`**.

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

### 1. I learned how the password-cracking workflow works

This practical helped me understand that the process starts by obtaining the information required by the cracking tool rather than simply trying to open the protected PDF directly.

### 2. I learned how PDF hashes are used

I learned how a protected PDF can have a crackable hash extracted from it and how that hash can then be supplied to a password-cracking tool.

### 3. I learned how to use John the Ripper and Johnny

Using both JTR and Johnny helped me understand the relationship between the underlying John the Ripper tool and its graphical interface.

### 4. I compared local and browser-based tools

The practical gave me experience with both a locally installed JTR workflow and the NetworkWalks browser-based tools. Both followed the same general process of obtaining the hash and attempting password recovery.

### 5. I observed the importance of password complexity

The practical showed me that password complexity can affect the time required to recover a password.

### 6. I understood why strong passwords are important

Recovering the lab password showed me why predictable passwords should not be used to protect sensitive documents.

---

# ✅ Results

| Practical | Tool | My Result |
|---|---|---|
| W3-PM1 | John the Ripper / Johnny | I recovered the PDF password |
| W3-PM2 | NetworkWalks Hash Calculator | I extracted the PDF hash |
| W3-PM2 | NetworkWalks Password Cracker | I recovered the PDF password |
| Verification | PDF reader | I successfully opened the protected PDF |

**Recovered lab password:** `password1`

> This is the password shown in the supplied NetworkWalks training material and demonstration. It should only be used with the provided lab file.

---

# 🔐 Security & Ethical Use

I performed this practical as part of a controlled cybersecurity training exercise.

I understand that password-cracking techniques should only be used against files, systems, or accounts that I own or have explicit authorization to test. The purpose of this exercise was to learn about password security and password-recovery techniques in an authorized lab environment.

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
