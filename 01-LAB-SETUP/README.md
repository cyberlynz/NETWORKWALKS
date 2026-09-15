<div align="center">

# 🔐 Cybersecurity Lab Environment Setup

**NetworkWalks Cybersecurity Internship — Batch B083**  
**Week 01 | Project WK1-PM1**

![Cybersecurity](https://img.shields.io/badge/Cybersecurity-Lab-blue)
![VirtualBox](https://img.shields.io/badge/VirtualBox-Virtualization-orange)
![Kali Linux](https://img.shields.io/badge/Kali%20Linux-Attacking%20Machine-557C94)
![NetworkWalks](https://img.shields.io/badge/NetworkWalks-B083-green)

</div>

---

## 📌 Project Overview

This project documents the setup of a basic cybersecurity testing lab for practical security exercises during the NetworkWalks cybersecurity internship.

The lab uses **VirtualBox** to run **Kali Linux** as the attacking/testing machine. The virtual network is configured around the required **10.0.0.0/24** subnet, with Kali assigned **10.0.0.2/24** and internet access through the configured NAT Network.

The purpose of the environment is to provide an isolated and controlled platform for learning cybersecurity tools, networking, reconnaissance, vulnerability assessment, and penetration-testing techniques.

## 🎯 Objectives

- Set up a functional cybersecurity testing environment.
- Install and configure VirtualBox.
- Configure a NAT Network using the `10.0.0.0/24` subnet.
- Install/import Kali Linux as the primary testing machine.
- Configure the Kali Linux network settings.
- Enable required VM integration features such as clipboard and drag-and-drop.
- Create a shared `/downloads` folder for transferring files between the host and VM.
- Verify Kali network connectivity and internet access.
- Take a VM snapshot after successful configuration.

## 🧪 Purpose of the Lab

The lab provides a safe environment for cybersecurity practice. Testing activities should be performed only on systems that are owned by me, provided for training, or explicitly authorized for security testing.

## ⚙️ Lab Configuration

| Component | Configuration |
|---|---|
| Host OS | Windows 10 |
| Host RAM | 16 GB |
| Processor | AMD Ryzen |
| Hypervisor | VirtualBox 7.2 |
| Security OS | Kali Linux 2025.4 |
| Kali RAM | 3048 MB |
| Virtual Network | NAT Network |
| Network Address | `10.0.0.0/24` |
| Kali IP Address | `10.0.0.2/24` |
| Default Gateway | `10.0.0.1` |
| DNS Server | `8.8.8.8` |
| Future VM Range | `10.0.0.3–10.0.0.99` |

## 📸 Screenshots

### NAT Network Configuration

The VirtualBox NAT Network is configured with the required `10.0.0.0/24` IPv4 prefix and DHCP enabled.

![NAT Network Configuration](2-screenshot-network-settings-1.png)

### Kali Linux Network Adapter

The Kali Linux VM is connected to the configured `NatNetwork` using the VirtualBox network adapter.

![Kali Linux Network Adapter](3-screenshot-kali-linux.png)

### Kali Network Configuration Troubleshooting

The following screenshot shows the NetworkManager commands used to resolve the networking configuration issue. The connection was successfully deactivated and activated again.

![Kali Network Troubleshooting](4-screenshot-kali-network-settings.png)

### VirtualBox Manager

The VirtualBox Manager screenshot shows the Kali Linux virtual machine used for the lab.

![VirtualBox Manager](5-screenshot-kali-snapshot.png)

## 🛠️ Lab Setup Procedure

### Step 1 — Install 7-Zip

7-Zip was used to extract compressed virtual machine files where required.

### Step 2 — Install VirtualBox

VirtualBox was installed as the virtualization platform for the cybersecurity lab.

### Step 3 — Configure the NAT Network

A NAT Network was created in VirtualBox using the required subnet:

```text
10.0.0.0/24
```

### Step 4 — Import Kali Linux

The Kali Linux virtual machine was imported into VirtualBox and configured as the attacking/testing machine.

### Step 5 — Configure Kali Linux Network

Kali Linux was configured to use the required address:

```text
IP Address: 10.0.0.2/24
Gateway:    10.0.0.1
```

### Step 6 — Configure VM Integration Features

The required VirtualBox integration settings were enabled, including:

- Shared Clipboard
- Drag and Drop
- Shared Folder: `/downloads`

### Step 7 — Take a Snapshot

After completing the configuration and verifying the environment, a VirtualBox snapshot was taken so the working lab state can be restored when necessary.

## 🐛 Troubleshooting

For the VirtualBox/Kali networking issue covered in the NetworkWalks task instructions, the following commands were used:

```bash
sudo nmcli connection modify "Wired connection 1" ipv4.dad-timeout 0
sudo nmcli connection down "Wired connection 1"
sudo nmcli connection up "Wired connection 1"
```

## ✅ Lab Verification

| Check | Expected Result |
|---|---|
| NAT Network | `10.0.0.0/24` configured |
| Kali IP | `10.0.0.2/24` |
| Gateway | `10.0.0.1` |
| Internet Access | Available from Kali |
| Clipboard | Enabled |
| Drag and Drop | Enabled |
| Shared Folder | `/downloads` |
| Snapshot | Created after setup |

## 📚 What I Learned

This exercise helped me understand how to build a controlled virtual cybersecurity lab and how virtualization, network configuration, and VM integration settings work together.

I also gained practical experience with configuring a private subnet, assigning a static address to a Linux testing machine, troubleshooting NetworkManager connectivity, and maintaining a recoverable VM state with snapshots.

## 🔒 Security & Ethical Use

This laboratory environment is intended for authorized cybersecurity training and testing only. Any scanning, exploitation, or security assessment performed with the tools in this lab should be limited to systems where permission has been granted.

## 🧰 Tools & Technologies

- VirtualBox
- Kali Linux
- 7-Zip
- NetworkManager (`nmcli`)
- NAT Network

## 👤 Author

**Collins**  
NetworkWalks Cybersecurity Internship — Batch B083

## 📋 Project Information

| Item | Details |
|---|---|
| Training Program | NetworkWalks Cybersecurity Internship |
| Batch | B083 |
| Week | 01 |
| Project | WK1-PM1 |
| Project Title | Cybersecurity Lab Environment Setup |
| Author | Collins |

---

> **Note:** This documentation follows the structure and presentation style of the NetworkWalks sample project while documenting my own lab setup and learning experience.
