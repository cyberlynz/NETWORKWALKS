# 🔵 W3-PM2 — Password Cracking with NetworkWalks Tools

**NetworkWalks Cybersecurity & Ethical Hacking — Batch B083**  
**Week 03 | Project Module 2**

![Cybersecurity](https://img.shields.io/badge/Cybersecurity-Password%20Cracking-blue)
![NetworkWalks](https://img.shields.io/badge/NetworkWalks-B083-green)
![Web Tools](https://img.shields.io/badge/Tools-Web%20Based-orange)
![Ethical Hacking](https://img.shields.io/badge/Ethical%20Hacking-Lab-black)

---

## 📌 Introduction

During Week 03, I completed **W3-PM2 — Password Cracking with NetworkWalks Tools**.

The practical focused on recovering the password of the supplied protected PDF file, **`My Locked PDF1.pdf`**, using two NetworkWalks web-based tools:

- **NetworkWalks Hash Calculator**
- **NetworkWalks Password Cracker**

Both tools were used through a web browser, so no local password-cracking application was required for this module.

## 🎯 Objectives

The objectives of this practical were to:

- Understand the basic password-recovery workflow for a protected PDF.
- Extract the PDF hash using the NetworkWalks Hash Calculator.
- Copy the complete hash value beginning with `$pdf$`.
- Submit the hash to the NetworkWalks Password Cracker.
- Observe the password-cracking process and verify the recovered password.
- Open the protected PDF using the recovered password.

---

## 🛠️ Tools Used

| Tool | Purpose |
|---|---|
| NetworkWalks Hash Calculator | Extract the PDF hash |
| NetworkWalks Password Cracker | Recover the password from the hash |
| Web Browser | Access the NetworkWalks tools |
| Windows Laptop | Lab platform |
| `My Locked PDF1.pdf` | Supplied protected PDF |

---

# 🧪 My Practical Steps

### Step 1 — Download the Encrypted PDF

I downloaded the supplied **`My Locked PDF1.pdf`** from the NetworkWalks lab page.

**Lab page:**  
https://networkwalks.com/project-task-lab-password-cracking-with-networkwalks-tools/

### Step 2 — Open the NetworkWalks Hash Calculator

I opened the NetworkWalks Hash Calculator in a web browser.

**Tool:**  
https://networkwalks.com/hash-calculator/

### Step 3 — Upload the Locked PDF

I uploaded the protected PDF to the Hash Calculator.

The tool processed the file and returned a PDF hash beginning with:

`$pdf$...`

### Step 4 — Copy the Complete Hash

I copied the full hash value, starting from **`$pdf$`**, making sure that no part of the hash was omitted.

### Step 5 — Open the NetworkWalks Password Cracker

I opened the NetworkWalks Password Cracker in the browser.

**Tool:**  
https://networkwalks.com/password-cracker/

### Step 6 — Submit the Hash and Start the Attack

I pasted the extracted PDF hash into the Password Cracker and started the attack.

The tool tested password candidates until a matching password was found.

### Step 7 — Wait for the Result

I waited for the tool to finish processing.

The cracking time depends on the complexity of the password and the tool's processing time.

### Step 8 — Enter the Recovered Password

After the password was recovered, I opened the locked PDF and entered the cracked password.

For the supplied lab demonstration, the recovered password was:

**`password1`**

### Step 9 — Verify the PDF

The PDF opened successfully after entering the recovered password, confirming that the password-recovery process was completed.

---

## 🖼️ Practical Evidence

The evidence below shows the main stages of the NetworkWalks Tools practical:

1. Protected PDF / Hash Calculator stage
2. Extracted PDF hash
3. Successful password recovery and PDF verification

![W3-PM2 NetworkWalks Tools Evidence](./evidence/pm2-networkwalks-evidence.jpg)

---

## 🔄 Workflow

```text
Protected PDF
     │
     ▼
NetworkWalks Hash Calculator
     │
     ▼
Extract $pdf$ Hash
     │
     ▼
Copy Complete Hash
     │
     ▼
NetworkWalks Password Cracker
     │
     ▼
Start Attack
     │
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

## 🧠 What I Learned

This practical helped me understand the password-recovery process from start to finish.

- I learned how a protected PDF can be processed to obtain a usable hash.
- I practiced extracting and copying a complete PDF hash.
- I gained experience using web-based password-security tools.
- I learned that password complexity can affect the time required to recover a password.
- I verified the result by opening the protected PDF with the recovered password.

---

## ✅ Results

| Stage | Result |
|---|---|
| PDF Hash Extraction | Successful |
| Hash Submission | Successful |
| Password Recovery | Successful |
| PDF Verification | Successful |
| Recovered Lab Password | `password1` |

> **Note:** The same process was repeated for the other protected PDF files used in the training exercise.

---

## 🔐 Security & Ethical Use

This practical was completed as part of an authorized cybersecurity training exercise.

Password-recovery and cracking techniques should only be used against files, systems, or accounts that are owned by the tester or where explicit permission has been granted.

---

## 📚 References

- NetworkWalks — W3-PM2: Password Cracking with NetworkWalks Tools
- NetworkWalks Hash Calculator: https://networkwalks.com/hash-calculator/
- NetworkWalks Password Cracker: https://networkwalks.com/password-cracker/
- NetworkWalks Password Cracking Lab: https://networkwalks.com/project-task-lab-password-cracking-with-networkwalks-tools/

---

## 📋 Project Information

| Item | Details |
|---|---|
| Training Program | NetworkWalks Cybersecurity & Ethical Hacking |
| Batch | B083 |
| Week | 03 |
| Module | W3-PM2 |
| Main Task | Password Cracking with NetworkWalks Tools |
| Target File | `My Locked PDF1.pdf` |
| Platform | Windows Laptop / Web Browser |
| Author | Collins |
