<div align="center">

# 🔐 Password Cracking with JTR & NetworkWalks Tools

**NetworkWalks Cybersecurity & Ethical Hacking — Batch B083**  
**Week 03 | Project Modules 1 & 2**

![Cybersecurity](https://img.shields.io/badge/Cybersecurity-Password%20Cracking-blue)
![John the Ripper](https://img.shields.io/badge/John%20the%20Ripper-JTR-C00000)
![NetworkWalks](https://img.shields.io/badge/NetworkWalks-B083-green)
![Windows](https://img.shields.io/badge/Platform-Windows%2010-0078D6)
![Ethical Hacking](https://img.shields.io/badge/Ethical%20Hacking-Lab-black)

</div>

---

## 📌 Project Overview

This project documents the **Week 03 essential password-cracking practicals** completed during my NetworkWalks cybersecurity training.

The week contains two required modules:

- **W3-PM1 — Password Cracking with JTR**
- **W3-PM2 — Password Cracking with NetworkWalks Tools**

The supplied lab uses a password-protected PDF named **`My Locked PDF1.pdf`**. The exercise demonstrates the workflow of extracting a crackable PDF hash, testing password candidates, recovering the password, and using the recovered password to open the protected PDF.

The Week 3 project sheet states that both essential modules must be completed.

## 🎯 Objectives

- Understand the purpose of password cracking in security testing.
- Use **John the Ripper (JTR)** and **Johnny GUI** to perform a controlled password-recovery exercise.
- Extract a PDF password hash for cracking.
- Use the **NetworkWalks Hash Calculator** to obtain the PDF hash.
- Use the **NetworkWalks Password Cracker** to test password candidates.
- Verify the recovered password by opening the protected PDF.
- Document practical results and lessons learned.

---

# 🔴 W3-PM1 — Password Cracking with JTR

## Background

John the Ripper (JTR) is presented in the lab material as a password-cracking tool used by security professionals to test password strength. The material also introduces **Johnny** as the graphical interface for John the Ripper.

The task is to recover the password of the supplied protected PDF using **JTR John** and **JTR Johnny** on a Windows PC.

### Tools Used

- John the Ripper
- Johnny GUI
- Windows PC
- `My Locked PDF1.pdf`
- PDF hash extractor

## 🪜 Methodology

### 1. Install John the Ripper and Johnny

The lab instructions provide download sources for John the Ripper and Johnny.

John the Ripper:  
https://www.openwall.com/john/

Johnny GUI:  
https://openwall.info/wiki/john/johnny

After installing Johnny, the configuration is opened and the location of **`john.exe`** from the JTR `run` folder is selected.

**Evidence:** `01-johnny-configuration.png`

### 2. Prepare the Protected PDF

The encrypted lab PDF **`My Locked PDF1.pdf`** is downloaded to the workstation.

**Evidence:** `02-pdf-locked.png`

### 3. Extract the PDF Hash

The lab instructs the student to use a PDF hash extractor to obtain the crackable hash.

The extracted value should begin with:

`$pdf$`

The complete hash is copied and saved to a text file named:

`hash1.txt`

**Evidence:** `03-pdf-hash-extracted.png`  
**Evidence:** `04-hash1-txt.png`

### 4. Load the Password File in Johnny

Johnny is reopened and the **Open password file** option is used to load `hash1.txt`.

**Evidence:** `05-johnny-password-file.png`

### 5. Start the Attack

A new attack is started from Johnny.

The lab notes that cracking time can depend on computer performance and password complexity.

**Evidence:** `06-johnny-attack-running.png`

### 6. Verify the Recovered Password

After the password is recovered, it is entered into the protected PDF.

The supplied lab demonstration shows the recovered password as:

`password1`

and the protected PDF opens successfully.

**Evidence:** `07-jtr-password-recovered.png`  
**Evidence:** `08-pdf-opened-with-password.png`

---

# 🔵 W3-PM2 — Password Cracking with NetworkWalks Tools

## Background

The second module demonstrates a browser-based workflow using two NetworkWalks tools:

1. **Hash Calculator**
2. **Password Cracker**

The lab explains the workflow as extracting the hash from the locked PDF and then running that hash through a cracking tool that tests different password candidates.

### Tools Used

- NetworkWalks Hash Calculator
- NetworkWalks Password Cracker
- Web browser
- Windows laptop
- `My Locked PDF1.pdf`

## 🪜 Methodology

### 1. Obtain the Encrypted PDF

Download the supplied:

`My Locked PDF1.pdf`

**Evidence:** `09-networkwalks-locked-pdf.png`

### 2. Open the Hash Calculator

NetworkWalks Hash Calculator:  
https://networkwalks.com/hash-calculator/

### 3. Upload the Protected PDF

Upload the locked PDF.

The tool returns a PDF hash beginning with:

`$pdf$`

The full hash is copied.

**Evidence:** `10-networkwalks-hash-calculator.png`

### 4. Open the Password Cracker

NetworkWalks Password Cracker:  
https://networkwalks.com/password-cracker/

### 5. Paste the Hash

Paste the complete `$pdf$...` hash into the password-cracking interface and start the attack.

The tool attempts candidate passwords until a matching password is found.

**Evidence:** `11-networkwalks-password-cracker.png`

### 6. Verify the Result

The lab demonstration reports:

**PASSWORD CRACKED SUCCESSFULLY**

Recovered password:

`password1`

The password is then entered into the encrypted PDF and the document opens successfully.

**Evidence:** `12-password-cracked-successfully.png`  
**Evidence:** `13-pdf-opened-with-password.png`

---

# 🔄 Password Cracking Workflow

The practical workflow can be summarized as:

```text
My Locked PDF1.pdf
        │
        ▼
Extract PDF Hash
        │
        ▼
Save / Copy $pdf$... Hash
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

### 1. Password cracking works against weak passwords

The lab showed how a protected file can be tested by obtaining its associated crackable hash and trying candidate passwords until a match is found.

### 2. Hash extraction is an important part of the workflow

The PDF itself is not simply treated as plain text. The exercise first extracts the information needed by the cracking tool.

### 3. JTR and Johnny provide different interfaces

**John the Ripper** provides the underlying password-cracking functionality, while **Johnny** provides a graphical interface that makes the workflow easier to operate.

### 4. Browser-based tools can support the same learning objective

The NetworkWalks tools demonstrate that the same general workflow can be completed through a web browser without installing the cracking tool locally.

### 5. Password complexity affects cracking time

The lab notes that the time required can vary according to computer performance and password complexity.

### 6. Password security matters

The successful recovery of the lab password demonstrates why common or predictable passwords should not be used to protect sensitive files.

---

# ✅ Results

| Module | Tool | Result |
|---|---|---|
| W3-PM1 | John the Ripper / Johnny | PDF password recovered |
| W3-PM2 | NetworkWalks Hash Calculator | PDF hash extracted |
| W3-PM2 | NetworkWalks Password Cracker | PDF password recovered |
| Verification | PDF reader | Protected PDF opened successfully |

**Recovered lab password:** `password1`

> This value is the password shown in the supplied NetworkWalks training material and demonstration. It should only be used for the provided lab file.

---

# 🔐 Security & Ethical Use

This project was performed as a controlled cybersecurity learning exercise.

Password cracking should only be performed against files, systems, or accounts that you own or have explicit authorization to test. The purpose of this lab is to understand password security, password recovery workflows, and defensive security awareness.

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
| Essential Project Modules | W3-PM1 & W3-PM2 |
| Main Task | Password Cracking |
| Target File | `My Locked PDF1.pdf` |
| Platform | Windows PC / Web Browser |
| Author | Collins |
