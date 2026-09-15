# 🌐 Network Scanning with Zenmap

**NetworkWalks Cybersecurity & Ethical Hacking — Batch B083**  
**Week 02 | Project Module 5 (W2-PM5)**

## 📌 Project Overview

This project covers practical **network scanning with Zenmap**, the official graphical user interface for Nmap. The exercise focuses on identifying the local IP address and LAN subnet, discovering live hosts, identifying their IP and MAC addresses, and saving the network topology as a PDF.

## 🎯 Tasks

### 01 — Download & Install Zenmap

Download and install Zenmap from the official Nmap website on a Windows PC.

**Official download:** https://nmap.org/download.html

**Result:**

> Add a short note describing your Zenmap installation result here.

**Screenshot:**

> Add your Zenmap installation screenshot here.

---

### 02 — Find Local IP Address & LAN Subnet

Open Command Prompt and run:

```cmd
ipconfig
```

Use the output to identify the computer's local IP address and LAN subnet.

**Result:**

- Local IP: `Add your result`
- LAN Subnet: `Add your result`

**Screenshot:**

> Add your `ipconfig` screenshot here.

---

### 03 — Find Live Hosts in the IP Subnet

Open Zenmap, enter your local LAN subnet as the target, select **Ping Scan**, and run the scan.

Example command shown in the guide:

```text
nmap -sn 10.0.0.0/24
```

Use your own local subnet rather than the example subnet if it is different.

**Result:**

> Add a short note describing the live hosts discovered in your subnet.

**Screenshot:**

> Add your Zenmap Ping Scan screenshot here.

---

### 04 — Number of Live Hosts

Record the total number of live hosts discovered by the Ping Scan.

**Result:**

- Live hosts: `Add your result`

**Screenshot:**

> Add your screenshot showing the live host count here.

---

### 05 — IP Addresses of Live Hosts

Record the IP addresses of all live hosts discovered during the scan.

**Result:**

```text
Add live host IP addresses here
```

**Screenshot:**

> Add your screenshot showing the live host IP addresses here.

---

### 06 — MAC Addresses of Live Hosts

Record the MAC addresses of the live hosts. Use `ipconfig /all` where necessary to identify the local machine's MAC address.

```cmd
ipconfig /all
```

**Result:**

```text
Add MAC addresses here
```

**Screenshot:**

> Add your screenshot showing the MAC addresses here.

---

### 07 — Display & Save Network Topology

In Zenmap:

1. Open the **Topology** tab.
2. Turn on the **Legend**.
3. Review the topology and host relationships.
4. Select **Save Graphic**.
5. Choose **PDF** as the file type.
6. Save the topology PDF to the desktop.

**Result:**

> Add a short note confirming that the Zenmap network topology was displayed and saved as a PDF.

**Topology Screenshot:**

> Add your Zenmap topology screenshot here.

**Topology PDF:**

> Add or link your saved topology PDF here.

---

## 🧠 What I Learned

- How Zenmap provides a graphical interface for performing Nmap network scans.
- How to use `ipconfig` to identify a local IP address and LAN subnet.
- How a Ping Scan can be used to discover live hosts on a network.
- How to identify the IP and MAC addresses associated with discovered hosts.
- How to use Zenmap's Topology view to visualize discovered hosts and save the result as a PDF.
- The importance of performing network scanning only on networks and systems where scanning is authorised.

## 🔒 Security & Ethical Use

This project is for educational and authorised security testing only. Network scanning should be performed only on systems and networks that are owned, provided for training, or explicitly authorised for testing.

## 📌 Project Information

| Item | Details |
|---|---|
| Training Program | NetworkWalks Cybersecurity & Ethical Hacking |
| Batch | B083 |
| Week | 02 |
| Project | W2-PM5 |
| Project Title | Network Scanning with Zenmap |
| Author | Collins |

---

[← Back to NETWORKWALKS Internship](https://github.com/cyberlynz/NETWORKWALKS)
