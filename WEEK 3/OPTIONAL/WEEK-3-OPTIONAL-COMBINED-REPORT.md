# Week 3 Optional Practical Report — HexStrike MCP, Claude Desktop and JTR Password Recovery

**NetworkWalks Cybersecurity & Ethical Hacking**  
**Environment:** Kali Linux Virtual Machine  
**Author:** Collins  
**Week:** 3  
**Lab Type:** Optional Practical

---

## 1. Introduction

As part of my Week 3 practical activities with NetworkWalks, I worked on an optional exercise that combined **HexStrike-AI MCP**, **Claude Desktop**, and **John the Ripper (JTR)** in a Kali Linux virtual machine.

I first prepared the HexStrike MCP environment and connected it to Claude Desktop. After confirming that the MCP server was working, I used the environment to interact with John the Ripper for an authorized PDF password-recovery exercise.

The purpose of combining the two activities was to understand how an AI interface can communicate with a local cybersecurity tool through MCP and how that setup can be applied to a controlled password-recovery task.

---

## 2. Objectives

The main objectives of this practical were to:

- Set up HexStrike-AI MCP on Kali Linux.
- Install and configure Claude Desktop.
- Create and activate a Python virtual environment for HexStrike.
- Install the required dependencies.
- Start the local HexStrike server.
- Connect Claude Desktop to the HexStrike MCP server.
- Verify the MCP connection.
- Confirm that John the Ripper was installed and available.
- Prepare the supplied protected PDF for password recovery.
- Calculate the PDF hash.
- Perform a dictionary-based password-recovery attempt using JTR and the `rockyou.txt` wordlist.
- Review and verify the result.

---

## 3. Tools and Environment

| Tool / Component | Purpose |
|---|---|
| Kali Linux | Virtual lab environment |
| Claude Desktop | AI interface |
| HexStrike-AI MCP | MCP-based security-tool integration |
| Python 3 | HexStrike runtime and virtual environment |
| pip3 | Python dependency installation |
| John the Ripper | Password-recovery tool |
| `rockyou.txt` | Dictionary wordlist |
| Protected PDF | Authorized lab target |
| GitHub | Source code and installation resources |

---

# 4. Practical Procedure

## 4.1 Preparing the Kali Linux Environment

I used my Kali Linux virtual machine as the environment for the practical. I carried out the setup directly inside the VM so that the required applications, Python environment, MCP server, and password-recovery tools could operate together.

**Screenshot 1 — Kali Linux lab environment**  
> **[INSERT SCREENSHOT HERE]**  
> *Evidence: Kali Linux desktop or terminal showing the environment being prepared.*

---

## 4.2 Installing Claude Desktop

I installed Claude Desktop in Kali Linux using the repository installation method provided in the NetworkWalks lab instructions.

I first added the repository signing key:

```bash
curl -fsSL https://pkg.claude-desktop-debian.dev/KEY.gpg | sudo gpg --dearmor -o /usr/share/keyrings/claude-desktop.gpg
```

I then added the Claude Desktop repository:

```bash
echo "deb [signed-by=/usr/share/keyrings/claude-desktop.gpg arch=amd64,arm64] https://pkg.claude-desktop-debian.dev stable main" | sudo tee /etc/apt/sources.list.d/claude-desktop.list
```

After that, I updated the package list and installed Claude Desktop:

```bash
sudo apt update
sudo apt install claude-desktop
```

Once the installation was complete, I opened Claude Desktop and signed in.

**Screenshot 2 — Claude Desktop installation**  
> **[INSERT SCREENSHOT HERE]**  
> *Evidence: terminal showing the installation process or confirmation that Claude Desktop was installed.*

**Screenshot 3 — Claude Desktop opened**  
> **[INSERT SCREENSHOT HERE]**  
> *Evidence: Claude Desktop running on Kali Linux.*

---

## 4.3 Downloading HexStrike-AI

Next, I downloaded the HexStrike-AI project from GitHub. I cloned the repository and changed into the project directory:

```bash
git clone https://github.com/0x4m4/hexstrike-ai.git
cd hexstrike-ai
```

This gave me the HexStrike-AI project files required for the MCP setup.

**Screenshot 4 — HexStrike-AI repository cloned**  
> **[INSERT SCREENSHOT HERE]**  
> *Evidence: terminal showing the repository being cloned and the project directory being accessed.*

---

## 4.4 Creating the Python Virtual Environment

Inside the HexStrike-AI directory, I created a dedicated Python virtual environment:

```bash
python3 -m venv hexstrike-env
```

I activated the environment with:

```bash
source hexstrike-env/bin/activate
```

Using a separate virtual environment allowed me to keep the HexStrike Python dependencies isolated from the rest of the Kali Linux Python installation.

**Screenshot 5 — Python virtual environment**  
> **[INSERT SCREENSHOT HERE]**  
> *Evidence: terminal showing the virtual environment being created and activated.*

---

## 4.5 Installing HexStrike Dependencies

With the virtual environment active, I installed the project dependencies using:

```bash
pip3 install -r requirements.txt
```

This installed the Python packages required by the HexStrike-AI project.

**Screenshot 6 — Dependencies installed**  
> **[INSERT SCREENSHOT HERE]**  
> *Evidence: terminal showing successful installation of the required Python packages.*

---

## 4.6 Starting the HexStrike MCP Server

After preparing the environment, I started the HexStrike server from the project directory:

```bash
cd ~/hexstrike-ai
source hexstrike-env/bin/activate
python3 hexstrike_server.py
```

The local HexStrike server was configured to operate through:

```
http://localhost:8888
```

At this point, the server was running locally and ready for the Claude Desktop integration.

**Screenshot 7 — HexStrike server running**  
> **[INSERT SCREENSHOT HERE]**  
> *Evidence: terminal showing the HexStrike server running successfully.*

---

## 4.7 Configuring Claude Desktop for HexStrike MCP

I then configured Claude Desktop to communicate with the local HexStrike MCP server.

The MCP configuration I used was:

```json
{
  "mcpServers": {
    "hexstrike-ai": {
      "command": "/home/kali/hexstrike-ai/hexstrike-env/bin/python",
      "args": [
        "/home/kali/hexstrike-ai/hexstrike_mcp.py",
        "--server",
        "http://localhost:8888"
      ]
    }
  }
}
```

This configuration defined the Python interpreter, the HexStrike MCP script, and the local server endpoint.

**Screenshot 8 — MCP configuration**  
> **[INSERT SCREENSHOT HERE]**  
> *Evidence: Claude Desktop MCP configuration containing the HexStrike server entry.*

---

## 4.8 Verifying the HexStrike MCP Connection

After saving the configuration, I checked Claude Desktop to verify that the **hexstrike-ai** MCP server was available.

This confirmed that Claude Desktop could communicate with my locally running HexStrike environment.

**Screenshot 9 — HexStrike MCP connected**  
> **[INSERT SCREENSHOT HERE]**  
> *Evidence: Claude Desktop showing the HexStrike MCP connection as available or connected.*

---

# 5. JTR Password-Recovery Exercise

Once the HexStrike environment was working, I continued with the second part of the optional practical: using John the Ripper through the MCP environment for an authorized PDF password-recovery exercise.

## 5.1 Preparing the Target PDF

I copied the supplied protected PDF to the Kali Linux Desktop so that it could be accessed locally by the HexStrike/JTR workflow.

The target used in the practical was the supplied NetworkWalks PDF:

```
/home/kali/Desktop/hash3.networkwalks_flag1.pdf
```

**Screenshot 10 — Target PDF on Kali Desktop**  
> **[INSERT SCREENSHOT HERE]**  
> *Evidence: the supplied PDF visible in the Kali Linux Desktop or file manager.*

---

## 5.2 Checking John the Ripper

Before attempting password recovery, I first verified that John the Ripper was installed and available through the HexStrike MCP environment.

I used the following prompt in Claude Desktop:

```
Check if John the Ripper is installed in this Hexstrike MCP and show me its version
```

This allowed me to confirm the JTR installation and version before proceeding.

**Screenshot 11 — John the Ripper version check**  
> **[INSERT SCREENSHOT HERE]**  
> *Evidence: Claude Desktop response showing that JTR is available and displaying the version.*

---

## 5.3 Calculating the PDF Hash

I then asked Claude to calculate the hash information for the protected PDF using:

```
Please calculate the hash value of this PDF file:
/home/kali/Desktop/hash3.networkwalks_flag1.pdf
```

The resulting hash information was required for the password-recovery process.

**Screenshot 12 — PDF hash extraction**  
> **[INSERT SCREENSHOT HERE]**  
> *Evidence: Claude Desktop showing the extracted PDF hash information.*

---

## 5.4 Performing the JTR Password-Recovery Attempt

After obtaining the hash information, I requested the password-recovery operation through the HexStrike MCP environment.

I used:

```
Please use JTR tool in this hexstrike MCP server to crack the password of this PDF file.
Use the rockyou.txt wordlist dictionary.
```

This instructed the environment to use John the Ripper with the `rockyou.txt` dictionary against the authorized lab target.

**Screenshot 13 — JTR operation initiated**  
> **[INSERT SCREENSHOT HERE]**  
> *Evidence: Claude Desktop showing the JTR request and the tool execution beginning.*

---

## 5.5 Reviewing the Cracking Process

I monitored the response from the HexStrike/JTR workflow while the dictionary-based password-recovery process was running.

At this stage, Claude Desktop acted as the interface, HexStrike MCP handled the connection to the local security tooling, and John the Ripper performed the password-recovery operation.

**Screenshot 14 — JTR processing/output**  
> **[INSERT SCREENSHOT HERE]**  
> *Evidence: tool output showing the JTR process, progress, or intermediate results.*

---

## 5.6 Reviewing the Recovered Password

The JTR operation returned a password-recovery result for the supplied lab PDF.

I reviewed the final response to verify the recovered password and the associated operation details, including the target, hash format, wordlist, and execution information.

**Screenshot 15 — Recovered password/result**  
> **[INSERT SCREENSHOT HERE]**  
> *Evidence: final Claude/JTR response showing the recovered password and relevant result details.*

---

# 6. Practical Workflow

The complete workflow I followed was:

```
Kali Linux
   ↓
Claude Desktop Installation
   ↓
HexStrike-AI Download
   ↓
Python Virtual Environment
   ↓
Dependencies Installed
   ↓
HexStrike Server Started
   ↓
Claude Desktop MCP Configuration
   ↓
MCP Connection Verified
   ↓
John the Ripper Verified
   ↓
Protected PDF Prepared
   ↓
PDF Hash Extracted
   ↓
JTR + rockyou.txt
   ↓
Password-Recovery Result
```

**Screenshot 16 — Complete workflow evidence**  
> **[INSERT SCREENSHOT HERE]**  
> *Evidence: a final screenshot or collection showing the completed setup and practical result.*

---

# 7. Results

The practical demonstrated the integration of an AI interface with a local cybersecurity MCP environment.

I was able to:

- Install and run Claude Desktop on Kali Linux.
- Download and prepare the HexStrike-AI environment.
- Create a dedicated Python virtual environment.
- Install the required dependencies.
- Start the local HexStrike server.
- Configure Claude Desktop to communicate with the MCP server.
- Verify the HexStrike MCP connection.
- Confirm John the Ripper availability.
- Extract the required PDF hash information.
- Run an authorized dictionary-based password-recovery task using JTR and `rockyou.txt`.
- Review the final password-recovery output.

---

# 8. What I Learned

### HexStrike MCP Setup

I learned how to deploy a local MCP-based security environment and connect it to an AI interface. The configuration process showed me that the MCP connection depends on correctly defining the executable, script, and local server endpoint.

### Python Virtual Environments

I gained more practical experience with Python virtual environments and learned why isolating project dependencies is useful when working with security tools and Python-based projects.

### AI-Assisted Security Tooling

I learned how Claude Desktop can act as an interface for interacting with locally configured cybersecurity tools through MCP.

### John the Ripper

I strengthened my understanding of John the Ripper and how it can be used for authorized password-recovery testing with a dictionary such as `rockyou.txt`.

### Hash Preparation

I learned that password-recovery workflows involving protected files require the appropriate hash representation before the cracking stage can begin.

### Evidence Collection

I also learned the importance of documenting each stage of a practical with screenshots. Capturing the setup, configuration, tool execution, and final result provides clear evidence of the work performed.

---

# 9. Security and Ethical Considerations

I carried out this practical as part of an authorized cybersecurity training exercise.

The techniques used in this lab should only be applied to files, systems, applications, or networks that I own or have explicit permission to test. The use of AI-assisted tooling does not remove the requirement for authorization when performing security testing or password-recovery activities.

---

# 10. Conclusion

This Week 3 optional practical gave me hands-on experience combining **Kali Linux, Claude Desktop, HexStrike-AI MCP, and John the Ripper** into one workflow.

I first built and verified the MCP environment, then used that environment to carry out an authorized password-recovery exercise against the supplied NetworkWalks PDF. The practical helped me understand both the technical setup of MCP-based security tooling and the workflow involved in using JTR for controlled password-recovery testing.

Overall, the exercise improved my practical understanding of AI-assisted cybersecurity tooling, Linux-based security environments, Python project setup, MCP configuration, and password-recovery techniques.

---

# 11. References

- NetworkWalks Academy — HexStrike MCP Server Setup Practice Lab
- NetworkWalks Academy — JTR Password Cracking Lab Module (AI Version)
- HexStrike-AI — https://github.com/0x4m4/hexstrike-ai
- Claude Desktop Debian — https://github.com/aaddrick/claude-desktop-debian
- John the Ripper — https://www.openwall.com/john/

---

## 12. Project Information

| Item | Details |
|---|---|
| Training Program | NetworkWalks Cybersecurity & Ethical Hacking |
| Week | Week 3 |
| Lab Type | Optional Practical |
| Environment | Kali Linux VM |
| AI Interface | Claude Desktop |
| MCP Server | HexStrike-AI |
| Password-Recovery Tool | John the Ripper |
| Wordlist | `rockyou.txt` |
| Target | NetworkWalks protected PDF |
| Author | Collins |
