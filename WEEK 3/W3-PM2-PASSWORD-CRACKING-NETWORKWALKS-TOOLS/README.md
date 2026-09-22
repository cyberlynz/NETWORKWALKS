<div align="center">

# 🔵 W3-PM2 — Password Cracking with NetworkWalks Tools

**NetworkWalks Cybersecurity & Ethical Hacking — Batch B083**  
**Week 03 | Project Module 2**

![Cybersecurity](https://img.shields.io/badge/Cybersecurity-Password%20Cracking-blue)
![NetworkWalks](https://img.shields.io/badge/NetworkWalks-B083-green)
![Web Tools](https://img.shields.io/badge/Tools-Web%20Based-orange)
![Ethical Hacking](https://img.shields.io/badge/Ethical%20Hacking-Lab-black)

</div>

---

## 📌 Introduction

For **Week 03 | Project Module 2**, I completed a practical on **Password Cracking with NetworkWalks Tools**.

The task was to recover the password of **password-protected PDF files** using two NetworkWalks browser-based tools:

- **NetworkWalks Hash Calculator**
- **NetworkWalks Password Cracker**

I first extracted the PDF hash, copied the complete **`$pdf$`** hash, submitted it to the Password Cracker, and then verified the recovered password by opening the protected PDF.

---

## 🎯 Objectives

The objectives of this practical were to:

- Understand the basic password-recovery process for a protected PDF.
- Extract a PDF hash using the NetworkWalks Hash Calculator.
- Copy the complete hash beginning with **`$pdf$`**.
- Submit the hash to the NetworkWalks Password Cracker.
- Run a dictionary attack and observe the cracking process.
- Verify the recovered password by opening the protected PDF.

---

## 🛠️ Tools Used

| Tool | Purpose |
|---|---|
| NetworkWalks Hash Calculator | Extract the PDF hash |
| NetworkWalks Password Cracker | Recover the password from the hash |
| Web Browser | Access the NetworkWalks web tools |
| Windows Laptop | Lab platform |
| Password-protected PDF files | Target files |

I used both NetworkWalks tools directly through my web browser, so I did not need to install them locally.

---

# 🛡️ Practical Steps

### Step 1 — Download the Password-Protected PDF

I downloaded the supplied **password-protected PDF files** from the NetworkWalks password-cracking lab page.

**Lab page:**  
https://networkwalks.com/project-task-lab-password-cracking-with-networkwalks-tools/

I used the supplied protected PDFs as the targets for this practical.

### Step 2 — Open the NetworkWalks Hash Calculator

I opened the NetworkWalks Hash Calculator in my browser.

**Tool:**  
https://networkwalks.com/hash-calculator/

### Step 3 — Upload the Password-Protected PDF

I uploaded the protected PDF to the Hash Calculator.

After processing the file, the tool produced a PDF hash beginning with **`$pdf$`**. This gave me the hash I needed for the next stage.

**Evidence — Step 3:**

![Step 3 — PDF Hash Extracted](./evidence/01-hash-extracted.png)

I repeated this hash-extraction process for each of the other supplied PDF files.

### Step 4 — Copy the Complete Hash

I copied the complete hash value, starting from **`$pdf$`**, without leaving out any part of the extracted value.

I made sure to copy the entire hash because the Password Cracker requires the complete value for the attack.

I repeated this step for each PDF after extracting its corresponding hash.

### Step 5 — Open the NetworkWalks Password Cracker

I opened the NetworkWalks Password Cracker in my browser.

**Tool:**  
https://networkwalks.com/password-cracker/

### Step 6 — Submit the Hash and Start the Attack

I pasted the extracted PDF hash into the Password Cracker and started the attack.

At this stage, I allowed the tool to test different password candidates against the submitted hash.

**Evidence — Step 6:**

![Step 6 — Hash Submitted to Password Cracker](./evidence/02-password-cracker-hash.png)

I repeated the same process using the hash extracted from each of the other supplied PDFs.

### Step 7 — Wait for the Password to Be Recovered

I waited for the Password Cracker to complete the attack and observed the password-recovery process.

The password was successfully recovered during the attack.

**Evidence — Step 7:**

![Step 7 — Password Recovered](./evidence/03-password-cracked.png)

The password-recovery process was repeated for the other supplied PDF files.

### Step 8 — Enter the Recovered Password & Verify the PDF

The recovered password for the demonstrated PDF was:

**`password1`**

I entered the recovered password into the protected PDF, and the PDF opened successfully. This confirmed that the recovered password was correct and completed the practical.

**Evidence — Step 8:**

![Step 8 — Password Entered and PDF Opened](./evidence/04-pdf-verified.png)

I also verified the recovered passwords for the other supplied PDF files by entering them into their respective protected PDFs and confirming that they opened successfully.

> **Note:** The same password-cracking steps were replicated for the **other supplied PDF files**. The screenshots in this README demonstrate the process for one PDF, while the same workflow was performed for the remaining PDFs.

---

## 🧠 What I Learned

- **PDF Hash Extraction:** I learned how to extract a PDF hash from a password-protected file using the NetworkWalks Hash Calculator. This helped me understand the first step required before attempting password recovery.

- **Working with PDF Hashes:** I learned the importance of copying the complete hash, including the **`$pdf$`** prefix, because the full hash is required by the Password Cracker for the attack.

- **Dictionary Attacks:** I learned how a password-cracking tool can test different password combinations against a recovered hash until a matching password is found. This helped me understand how dictionary-based password attacks work in practice.

- **Repeating the Process:** I learned that the same password-recovery workflow can be applied to multiple protected PDF files by extracting and submitting the appropriate hash for each file.

- **Password Strength:** I learned that simple and predictable passwords can be easier to recover through cracking attempts. This reinforced the importance of using strong and less predictable passwords to protect files.

- **Password Verification:** I learned that recovering a password is not the final step. I also need to verify the result by entering the recovered password and confirming that the protected PDF opens successfully.

---

## ✅ Results

| Stage | Result |
|---|---|
| Protected PDF Processing | Successful |
| PDF Hash Extraction | Successful |
| Complete Hash Submission | Successful |
| Password Cracking | Successful |
| Recovered Password | `password1` |
| PDF Verification | Successful |
| Process Replicated for Other PDFs | Successful |

---

## 🔐 Security & Ethical Use

I completed this practical as part of my authorized cybersecurity training.

I understand that password-recovery and cracking techniques should only be used against files, systems, or accounts that I own or have explicit permission to test.

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
| Target | Password-protected PDF files |
| Platform | Windows Laptop / Web Browser |
| Author | Collins |
