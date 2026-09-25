<div align="center">

# 🔷 HexStrike MCP Server Setup with Claude Desktop

**NetworkWalks Academy — Practice Lab**  
**Kali Linux Environment**

![Cybersecurity](https://img.shields.io/badge/Cybersecurity-HexStrike%20MCP-blue)
![Kali Linux](https://img.shields.io/badge/Platform-Kali%20Linux-black)
![Claude](https://img.shields.io/badge/AI-Claude-orange)
![MCP](https://img.shields.io/badge/MCP-Server-green)

</div>

---

## 📌 Introduction

For this NetworkWalks practice lab, I set up the **HexStrike MCP Server** in a **Kali Linux virtual machine** and connected it to **Claude Desktop**.

The lab focused on installing Claude Desktop, downloading and preparing the HexStrike MCP server, starting the HexStrike server, and configuring Claude Desktop so that it could communicate with the local HexStrike MCP server. The objective was to establish a working AI-assisted cybersecurity lab environment.

---

## 🎯 Objectives

The objectives of this practical were to:

- Set up the HexStrike MCP Server on Kali Linux.
- Install Claude Desktop in the Kali Linux environment.
- Download the HexStrike-AI project from GitHub.
- Create and activate a Python virtual environment.
- Install the required Python dependencies.
- Start the HexStrike MCP server.
- Configure Claude Desktop to use the local HexStrike MCP server.
- Verify that the server is running and available from Claude Desktop.

---

## 🛠️ Tools and Environment

| Tool / Component | Purpose |
|---|---|
| Kali Linux VM | Lab environment |
| Claude Desktop | AI interface used to connect to MCP |
| HexStrike-AI MCP Server | Local cybersecurity MCP server |
| GitHub | Source repository for Claude Desktop and HexStrike-AI |
| Python 3 | Virtual environment and server runtime |
| pip3 | Installation of Python dependencies |

The NetworkWalks guide identifies the lab environment as a **HexStrike-AI MCP server with Claude Desktop on a Kali Linux VM**.

---

# 🛡️ Practical Steps

### Step 1 — Prepare the Kali Linux Environment

I used my Kali Linux virtual machine as the lab environment for the practical.

The objective was to build the HexStrike MCP and Claude Desktop setup directly inside Kali Linux, following the environment specified in the NetworkWalks practice guide.

### Step 2 — Download and Install Claude Desktop

I downloaded the Claude Desktop package for Kali Linux using the GitHub project referenced by the lab guide:

https://github.com/aaddrick/claude-desktop-debian

The guide provides the following installation process.

#### Add the GPG key

```bash
curl -fsSL https://pkg.claude-desktop-debian.dev/KEY.gpg | sudo gpg --dearmor -o /usr/share/keyrings/claude-desktop.gpg
```

#### Add the repository

```bash
echo "deb [signed-by=/usr/share/keyrings/claude-desktop.gpg arch=amd64,arm64] https://pkg.claude-desktop-debian.dev stable main" | sudo tee /etc/apt/sources.list.d/claude-desktop.list
```

#### Update the package list and install Claude Desktop

```bash
sudo apt update
sudo apt install claude-desktop
```

These are the installation commands provided in the NetworkWalks guide.

### Step 3 — Open Claude Desktop and Sign In

After installation, I opened **Claude Desktop** inside Kali Linux and completed the sign-in process.

This step prepared the Claude Desktop application for the MCP integration described later in the lab.

### Step 4 — Download the HexStrike-AI MCP Server

I downloaded the HexStrike-AI project from the GitHub repository provided by the lab:

https://github.com/0x4m4/hexstrike-ai

I cloned the repository with:

```bash
git clone https://github.com/0x4m4/hexstrike-ai.git
cd hexstrike-ai
```

The lab specifically instructs using the GitHub project and these commands to obtain the HexStrike-AI server files.

### Step 5 — Create a Python Virtual Environment

Inside the HexStrike-AI directory, I created a dedicated Python virtual environment:

```bash
python3 -m venv hexstrike-env
```

I then activated the environment:

```bash
source hexstrike-env/bin/activate
```

Using a virtual environment kept the HexStrike Python dependencies isolated from the rest of the Kali Linux Python installation.

The virtual-environment commands are included in the NetworkWalks lab instructions.

### Step 6 — Install the Required Python Dependencies

With the virtual environment activated, I installed the project dependencies using:

```bash
pip3 install -r requirements.txt
```

This installed the Python packages required by the HexStrike-AI server.

The NetworkWalks guide specifies installing the dependencies from the project's `requirements.txt` file.

### Step 7 — Start the HexStrike MCP Server

I moved back into the HexStrike-AI project directory, activated the virtual environment, and started the server:

```bash
cd ~/hexstrike-ai
source hexstrike-env/bin/activate
python3 hexstrike_server.py
```

This started the HexStrike server locally. The lab later identifies the local server endpoint as **`http://localhost:8888`**.

### Step 8 — Configure the MCP Server in Claude Desktop

I opened the Claude Desktop MCP configuration and added the HexStrike server configuration supplied by the lab.

The configuration used:

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

This configuration tells Claude Desktop which Python interpreter to use, which HexStrike MCP script to launch, and which local HexStrike server endpoint to connect to.

### Step 9 — Verify the MCP Server Connection

After saving the MCP configuration, I checked Claude Desktop to confirm that the **hexstrike-ai** MCP server was available.

The final section of the lab guide shows Claude Desktop displaying the HexStrike MCP server as connected and also shows a Claude conversation interacting with the HexStrike environment. This served as the final verification stage of the setup.

---

## 🔎 Practical Outcome

The practical established the complete workflow:

```text
Kali Linux
   ↓
Claude Desktop
   ↓
HexStrike MCP Configuration
   ↓
hexstrike_mcp.py
   ↓
Local HexStrike Server
   ↓
http://localhost:8888
```

The important part of the setup was not only installing the software, but correctly connecting Claude Desktop to the local HexStrike MCP server through the configuration file.

---

## 🧠 What I Learned

- **Claude Desktop on Kali Linux:** I learned how to install Claude Desktop in a Kali Linux environment using the repository method supplied by the lab.

- **GitHub-Based Installation:** I learned how a cybersecurity lab can use GitHub repositories as the source for both the Claude Desktop package instructions and the HexStrike-AI project.

- **Python Virtual Environments:** I learned how to create and activate a dedicated Python virtual environment before installing project dependencies.

- **MCP Server Deployment:** I learned how to clone an MCP project, install its dependencies, and start the local server from the terminal.

- **MCP Configuration:** I learned how Claude Desktop uses an MCP configuration to define the executable, script, and server endpoint required for an MCP integration.

- **Local AI-Assisted Security Environment:** I learned how Claude Desktop can be connected to a local cybersecurity MCP server so that the AI interface can interact with the configured security environment.

---

## 🔐 Security & Ethical Use

I completed this practical as part of my authorized cybersecurity training.

The HexStrike environment should only be used against systems, files, applications, or networks that I own or have explicit permission to test. AI-assisted security tooling does not change the authorization requirements for cybersecurity activities.

---

## 📚 References

- NetworkWalks Academy — How to Setup HexStrike MCP Server (Practice Lab)
- Claude Desktop Debian project: https://github.com/aaddrick/claude-desktop-debian
- HexStrike-AI: https://github.com/0x4m4/hexstrike-ai

---

## 📋 Project Information

| Item | Details |
|---|---|
| Training Program | NetworkWalks Cybersecurity & Ethical Hacking |
| Lab | How to Setup HexStrike MCP Server |
| Environment | Kali Linux VM |
| AI Interface | Claude Desktop |
| MCP Server | HexStrike-AI |
| Server Endpoint | `http://localhost:8888` |
| Author | Collins |
