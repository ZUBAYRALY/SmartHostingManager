# Smart Hosting Manager - User Guide

Welcome to the **Smart Hosting Manager** User Guide! This document provides detailed instructions on how to navigate and utilize the features across all tabs of the application.

## Table of Contents

1. [Dashboard](#1-dashboard)
2. [Control Panel](#2-control-panel)
3. [Developer](#3-developer)
4. [Domain & SSL](#4-domain--ssl)
5. [Backup & Restore](#5-backup--restore)
6. [Installer](#6-installer)

---

## 1. Dashboard
The Dashboard is the central hub for monitoring your server's health and system status. 

**📸 Screenshot Required:** `screenshots/dashboard.png` *(Show the active connection, system uptime, and status labels)*

**Key Features:**
- **Real-time Status:** Live status indicators for PM2 (Backend), Caddy (Frontend), and Prisma Studio.
- **Domain Overview:** Displays the currently active domain configurations and SSL validities.
- **Backup Timestamps:** Instantly see when your last system backup was successfully created.

---

## 2. Control Panel
The Control Panel provides actionable controls to manage your server environment actively.

**📸 Screenshot Required:** `screenshots/control_panel.png` *(Show the quick action buttons and service toggles)*

**Key Features:**
- **Manage Services:** Quick actions to Start, Stop, or Restart PM2 instances and backend services.
- **Auto-Reboot:** Enable or disable auto-reboot policies to ensure applications start automatically on server boot.
- **Caddy Integration:** Global toggles to jump-start or halt your Caddy web server directly from the GUI.

---

## 3. Developer
The Developer tab offers advanced tools designed for in-depth debugging and seamless code deployment.

**📸 Screenshot Required:** `screenshots/developer.png` *(Show the terminal input, log tailing, or code update interface)*

**Key Features:**
- **Log Tailing:** Stream backend logs directly from the remote server seamlessly into the GUI.
- **SSH Console:** Run direct SSH commands without needing an external terminal emulator.
- **Project Upgrades:** Effortlessly deploy project updates by uploading ZIP archives directly to the remote server.

---

## 4. Domain & SSL
Effortlessly handle networking and routing configurations from the Domain & SSL tab.

**📸 Screenshot Required:** `screenshots/domain_ssl.png` *(Show the domain input fields and SSL port mappings)*

**Key Features:**
- **Domain Assignment:** Assign new custom domains (or localhost) to your projects effortlessly.
- **Caddy Configuration:** Dynamically generated and applied Caddyfile routing rules for API and static files.
- **Automated SSL:** Automatically provisions Let's Encrypt SSL certificates when valid domains are assigned.

---

## 5. Backup & Restore
Ensure data integrity with the quick tools provided in the Backup & Restore tab.

**📸 Screenshot Required:** `screenshots/backup_restore.png` *(Show the manual backup creator and recent backup list)*

**Key Features:**
- **Optimized Backups:** Perform one-click complete backups that intelligently ignore heavy `node_modules` or `.git` folders.
- **ZIP Compression:** Uses high-speed deflate algorithms to preserve space.
- **SFTP Fetching:** Allows effortless downloading of remote backups directly to your local workstation.

---

## 6. Installer
The Installer tab automates setting up new projects, environments, and dependencies.

**📸 Screenshot Required:** `screenshots/installer.png` *(Show the installation wizard toggles or module lists)*

**Key Features:**
- **Dependency Automation:** Automates the bootstrapping of essential environment packages and system dependencies.
- **Third-Party Services:** Easy installation scripts for auxiliary tools like Docker, Caddy, or Umami Analytics.
- **Guided Setup:** Smooth workflow to transition from a bare-bones OS to a production-ready application environment.

---
> **Note to Contributors:** When adding screenshots, save them directly to the `screenshots/` directory inside the repository, and ensure they match the exact filenames (`dashboard.png`, `control_panel.png`, etc.) referenced above.
