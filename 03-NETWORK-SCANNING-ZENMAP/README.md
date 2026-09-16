<div align="center">

# 🌐 Network Scanning with Zenmap

**Practical network discovery and topology mapping using Zenmap and Nmap**
</div>

<p align="center">
  <img src="https://img.shields.io/badge/Skill-Network%20Scanning-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/Nmap-Zenmap-0070C0?style=flat-square&labelColor=000000" />
  <img src="https://img.shields.io/badge/NetworkWalks-B083-C00000?style=flat-square" />
  <img src="https://img.shields.io/badge/Week-02-E87500?style=flat-square&labelColor=000000" />
  <img src="https://img.shields.io/badge/GitHub-404040?style=flat-square&labelColor=0070C0&logo=github&logoColor=white" />
  <img src="https://img.shields.io/badge/Ethical%20Hacking-C00000?style=flat-square&labelColor=000000" />
</p>

---

## 📌 Project Overview

This project focuses on practical **network scanning with Zenmap**, the graphical interface for Nmap.

The objective is to identify the local IP address and LAN subnet, discover live hosts on the network, identify host IP and MAC addresses, and use Zenmap's **Topology** view to visualize the discovered network and save the result as a PDF.

The work follows the same structured, evidence-based documentation style used throughout the NetworkWalks internship.

---

## 🎯 Objectives

The main objectives of this project are to:

- Install and configure Zenmap.
- Identify the local IP address and LAN subnet.
- Perform a Ping Scan to discover live hosts.
- Record the IP addresses of discovered hosts.
- Identify MAC addresses where available.
- Use Zenmap Topology to visualize the network.
- Save the network topology as a PDF.
- Document the results with screenshots and supporting evidence.

---

# 🪜 Network Scanning Procedure

## Step 1. Download & Install Zenmap

Zenmap was installed on the Windows system for graphical Nmap scanning.

**Official Nmap download:** https://nmap.org/download.html

**Result:**

> Zenmap installation completed successfully and the application was ready for network scanning.

**Screenshot:**

> ![Zenmap](nmap1.PNG)

---

## Step 2. Find Local IP Address & LAN Subnet

Open **Command Prompt** and run:

```cmd
ipconfig
```

Use the output to identify the local IPv4 address and determine the LAN subnet.

**Result:**

```text
Local IP: 10.0.0.10
LAN Subnet: 255.255.255.0
```

**Screenshot:**

> ![ipconfig](ipconfig-screenshot.png)

---

## Step 3. Find Live Hosts in the IP Subnet

Open Zenmap, enter the local LAN subnet as the target, select **Ping Scan**, and run the scan.

Example Nmap command:

```text
nmap -sn 10.0.0.0/24
```

> Use the actual local subnet identified from your `ipconfig` output rather than the example subnet above.

**Result:**

> Add a short description of the live hosts discovered during the Ping Scan.

**Screenshot:**

> Add your Zenmap Ping Scan screenshot here.

---

## Step 4. Record the Number of Live Hosts

Record the total number of live hosts identified by the Ping Scan.

**Result:**

```text
 4 hosts are live (including my PC)
```

---

## Step 5. Record IP Addresses of Live Hosts

Document the IP addresses returned by the Ping Scan.

**Result:**

```text
10.0.0.1 
10.0.0.2 
10.0.0.3 
10.0.0.10
```

**Screenshot:**

> ![host](ping-screenshot.png)

---

## Step 6. Identify MAC Addresses

Use the scan results and, where necessary, Command Prompt to identify the MAC address of the local system.

```cmd
ipconfig /all
```

**Result:**

```text
 52:54:00:12:35:00
 08:00:27:4C:1D:4B
 52:54:00:12:35:00
 00:0C:29:C0:94:8F
```

**Screenshot:**

> ![MAC address](mac-screenshot.png)

---

## Step 7. Display & Save Network Topology

Zenmap was used to display the discovered network topology.

Procedure:

1. Open the **Topology** tab.
2. Enable the **Legend**.
3. Review the discovered hosts and network relationships.
4. Select **Save Graphic**.
5. Choose **PDF** as the output format.
6. Save the topology PDF.

**Result:**

> Add a short note confirming that the Zenmap topology was displayed and saved successfully as a PDF.

**Topology Screenshot:**

> ![Zenmap](topology-screenshot.png)

**Topology PDF:**

> Add or link your saved topology PDF here.

---

# 📊 Evidence Checklist

| ✅ Evidence | Status |
|---|---|
| Zenmap installation | ⬜ |
| `ipconfig` output | ⬜ |
| Ping Scan result | ⬜ |
| Number of live hosts | ⬜ |
| Live host IP addresses | ⬜ |
| MAC address information | ⬜ |
| Zenmap Topology view | ⬜ |
| Saved topology PDF | ⬜ |

---

# 💡 What I Learned

Through this project, I learned how to use Zenmap and Nmap for basic network discovery and visualization.

### 1. Network Identification

I learned how to use `ipconfig` to identify the local IPv4 address and understand the subnet used by the computer.

### 2. Host Discovery

I learned how a Ping Scan can be used to identify live hosts within a network range without performing a full port scan.

### 3. IP & MAC Information

I learned how to document the IP addresses of discovered hosts and use local network information to identify MAC addresses where available.

### 4. Network Topology

I learned how Zenmap's Topology view can provide a graphical representation of discovered hosts and their relationships.

### 5. Security Documentation

I learned that recording commands, scan results, screenshots, and supporting evidence makes a cybersecurity project easier to understand, review, and reproduce.

---

# 🔐 Security & Ethical Use

This project is for **educational and authorised security testing only**.

Network scanning should only be performed against systems and networks that are owned, provided for training, or explicitly authorised for testing. Scanning third-party networks without permission may be unlawful or disruptive.

---

# 🔗 Tools & Resources

- **Nmap / Zenmap:** https://nmap.org/download.html
- **Command Prompt:** Windows networking utility used to inspect local network configuration

---

# 👤 Author

**Collins**  
Cybersecurity Learner | NetworkWalks Batch B083

---

## 📌 Project Information

| Item | Details |
|---|---|
| Program Name | NetworkWalks Cybersecurity & Ethical Hacking |
| Batch | B083 |
| Week | 02 |
| Project | W2-PM5 |
| Project Title | Network Scanning with Zenmap |
| Author | Collins |
| Repository | GitHub |

---

[← Back to NETWORKWALKS Internship](https://github.com/cyberlynz/NETWORKWALKS)
