# 🛠️ Homelab Setup Log — 00_setup.md

## 🗓️ Date Started: May 11, 2025

## 🔍 Purpose
Establish a local home server system using a mini-PC to self-host tools and services for learning, productivity, and sovereignty. This document covers initial configuration, OS installation, networking, and base tooling.

---

## 💻 Hardware Specs

| Component        | Details                             |
|------------------|--------------------------------------|
| Device           | [Mini-PC model]                      |
| CPU              | [e.g., Intel N5105]                  |
| RAM              | [e.g., 8GB DDR4]                     |
| Storage          | [e.g., 512GB NVMe SSD]              |
| Network          | [Ethernet / WiFi]                    |
| Power Source     | [UPS/Wall power/etc.]                |

---

## 📦 OS + Core Stack

| Component      | Version            | Notes |
|----------------|---------------------|-------|
| OS             | [e.g., Ubuntu 22.04 Server] | Minimal install + OpenSSH |
| Shell          | Bash/Zsh            | Aliases configured |
| Package Manager| apt / snap          | Updated & clean |
| Firewall       | ufw                 | Defaults + allow SSH |
| SSH Access     | Enabled             | Key-based auth |

---

## 🧱 Base Setup Steps

# Mini-PC Setup Log

## [Date] Initial Boot
- Booted Windows mini-PC.
- Connected to [Wi-Fi/Ethernet].
- Installed Windows updates: [Pending/In Progress/Complete].
- Removed bloatware: [List if any].
- Installed tools: [Git, VS Code, Terminal, etc.]

## Notes:
- System feels [Fast/Laggy/Decent]
- Any driver issues: [None/Yes - Details]





### ✅ 1. Flash & Install OS
- Used [Rufus/BalenaEtcher/etc.] to flash ISO to USB
- Installed OS via mini-PC monitor/keyboard
- Set hostname: `homelab-core`
- Created user: `daniel` with sudo

### ✅ 2. Secure Access
- Set static IP via Netplan (for consistent LAN access)
- Installed `openssh-server`
- Configured SSH with public key auth
- Disabled password login in `/etc/ssh/sshd_config`

### ✅ 3. System Tweaks
- Installed baseline tools:
  ```bash
  sudo apt update && sudo apt install -y git curl htop ufw fail2ban net-tools
