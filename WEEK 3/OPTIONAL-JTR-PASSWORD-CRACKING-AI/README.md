<div align="center">

# 🔴 Optional Module — JTR Password Cracking with AI

**NetworkWalks Cybersecurity & Ethical Hacking**  
**HexStrike-AI MCP + Claude Desktop + John the Ripper**

![Cybersecurity](https://img.shields.io/badge/Cybersecurity-Password%20Cracking-red)
![Kali Linux](https://img.shields.io/badge/Platform-Kali%20Linux-black)
![John the Ripper](https://img.shields.io/badge/Tool-John%20the%20Ripper-orange)
![AI](https://img.shields.io/badge/AI-HexStrike%20%2B%20Claude-blue)

</div>

---

## 📌 Introduction

For this optional NetworkWalks lab, I performed an **AI-assisted PDF password-cracking exercise** using **John the Ripper (JTR)** through a **HexStrike-AI MCP server with Claude Desktop on Kali Linux**.

The task was to crack the password of the supplied **`networkwalks_flag1.pdf`** target. The lab required the HexStrike-AI MCP environment to be prepared first, followed by checking the JTR installation, calculating the PDF hash, and using JTR with the **`rockyou.txt`** wordlist. fileciteturn46file1L8-L20

---

## 🎯 Objectives

The objectives of this practical were to:

- Use the HexStrike-AI MCP environment with Claude Desktop.
- Confirm that John the Ripper was installed and identify its version.
- Locate the supplied target PDF in Kali Linux.
- Calculate the hash value of the protected PDF.
- Use JTR through HexStrike MCP to perform a password-recovery attempt.
- Use the `rockyou.txt` wordlist as the dictionary source.
- Confirm that the password was successfully recovered.

---

## 🛠️ Tools and Environment

| Tool / Component | Purpose |
|---|---|
| Kali Linux VM | Lab environment |
| Claude Desktop | AI interface |
| HexStrike-AI MCP | AI-to-security-tool integration |
| John the Ripper (JTR) | Password-recovery tool |
| `rockyou.txt` | Dictionary wordlist |
| Protected PDF | Authorized lab target |

The lab manual states that the environment should consist of the **HexStrike-AI MCP server with Claude Desktop on a Kali Linux VM**, and it identifies the target file as `hash3.networkwalks_flag1.pdf` in the attachment to the lab manual. fileciteturn46file1L18-L20

---

# 🛡️ Practical Steps

### Step 1 — Copy the Target PDF to the Kali Linux Desktop

I copied the supplied target PDF file to the **Kali Linux Desktop** so that it could be accessed locally by the HexStrike/JTR workflow.

The NetworkWalks lab starts with this file-preparation step. fileciteturn46file1L21-L25

### Step 2 — Open Claude Desktop

I opened **Claude Desktop** on Kali Linux.

The lab uses Claude as the AI interface for interacting with the HexStrike MCP environment. The first prompt checks whether John the Ripper is installed and requests its version.

### Step 3 — Check the John the Ripper Installation

I entered the following prompt into Claude Desktop:

```text
Check if John the Ripper is installed in this Hexstrike MCP and show me its version
```

This allowed me to confirm that JTR was available through the HexStrike MCP environment before continuing.

The prompt shown in the NetworkWalks manual is specifically intended to verify the JTR installation and version. fileciteturn46file1L25-L29

### Step 4 — Calculate the PDF Hash

I then asked Claude to calculate the hash of the target PDF using:

```text
Please calculate the hash value of this PDF file:
/home/kali/Desktop/hash3.networkwalks_flag1.pdf
```

This step produced the hash information required for the password-recovery stage.

The lab manual gives the target path and this exact hash-calculation prompt. fileciteturn46file1L31-L33

### Step 5 — Request the JTR Password-Cracking Operation

After obtaining the hash information, I used the following AI prompt:

```text
Please use JTR tool in this hexstrike MCP server to crack the password of this PDF file.
Use the rockyou.txt wordlist dictionary.
```

This instructed the HexStrike MCP environment to use John the Ripper with the **rockyou.txt** dictionary against the authorized lab PDF.

The NetworkWalks manual provides this prompt and specifies the use of the `rockyou.txt` wordlist. fileciteturn46file1L34-L36

### Step 6 — Observe the AI-Assisted Cracking Process

I allowed the JTR operation to run through the HexStrike MCP environment.

During this stage, Claude acted as the AI interface while HexStrike MCP provided the connection to the underlying cybersecurity tool. The objective was to use the supplied dictionary to identify the password associated with the protected PDF.

### Step 7 — Review the Recovered Password

The lab manual shows a successful password-recovery response from the AI interface, confirming that the PDF password had been cracked.

The screenshot on **page 5** also shows the recovered password together with details such as the target file, hash format, time taken, and the wordlist used. fileciteturn46file1L38-L42

### Step 8 — Confirm the Password-Recovery Result

I treated the recovered password as the final output of the JTR operation and confirmed the cracking stage had completed successfully.

The manual's final evidence page follows the successful cracking result and provides additional references and tips. fileciteturn46file1L39-L44

---

## 🔎 Practical Workflow

The practical can be summarized as:

```text
Target PDF
   ↓
Kali Linux Desktop
   ↓
Claude Desktop
   ↓
HexStrike-AI MCP
   ↓
Check JTR Installation
   ↓
Calculate PDF Hash
   ↓
JTR + rockyou.txt
   ↓
Password Recovered
```

This workflow demonstrates how an AI interface can be used to coordinate a traditional password-recovery tool through an MCP-based security environment.

---

## 🧠 What I Learned

- **JTR Verification:** I learned how to check that John the Ripper is installed and available before starting a password-recovery task.

- **PDF Hash Preparation:** I learned that a protected PDF must first be processed to obtain the hash information required for the cracking stage.

- **AI-Assisted Tool Execution:** I learned how Claude Desktop can be used as an interface for requesting security-tool operations through HexStrike MCP.

- **Dictionary-Based Password Recovery:** I learned how a password-recovery operation can use the `rockyou.txt` dictionary to test candidate passwords against a protected file.

- **MCP Workflow:** I learned how the MCP layer can connect an AI interface with a local security tool and make the workflow more interactive.

- **Verification of Results:** I learned the importance of reviewing the tool's output after an operation to confirm whether the password-recovery attempt was successful.

---

## 🔐 Security & Ethical Use

I completed this practical as part of an authorized cybersecurity training lab.

John the Ripper, HexStrike-AI, and dictionary-based password-recovery techniques should only be used against files, systems, and accounts that I own or have explicit authorization to test.

---

## 📚 References

- NetworkWalks — LAB PRACTICE: JTR Password Cracking Lab Module (AI-version)
- NetworkWalks — How to Setup HexStrike MCP Server (Practice Lab)
- John the Ripper: https://www.openwall.com/john/
- HexStrike-AI: https://github.com/0x4m4/hexstrike-ai

---

## 📋 Project Information

| Item | Details |
|---|---|
| Training Program | NetworkWalks Cybersecurity & Ethical Hacking |
| Lab Type | Optional Module |
| Main Task | JTR Password Cracking with AI |
| Environment | Kali Linux VM |
| AI Interface | Claude Desktop |
| MCP Server | HexStrike-AI |
| Password-Cracking Tool | John the Ripper |
| Wordlist | `rockyou.txt` |
| Target | NetworkWalks protected PDF |
| Author | Collins |
