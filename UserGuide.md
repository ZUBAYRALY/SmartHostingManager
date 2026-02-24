# Smart Hosting Manager - Complete User Guide

Welcome to the **Smart Hosting Manager** User Guide! This document provides detailed, step-by-step instructions on how to set up, navigate, and utilize every feature across all tabs of the application.

---

## 1. Initial Setup & Profiles

Before you start managing your servers, you need to set up a profile for your project.

### Creating a New Profile
1. Launch the **Smart Hosting Manager** application.
2. In the top bar, click the **+ New** button next to the Profile dropdown.
3. Fill in the required details:
   - **Project:** Enter a unique name for your project (e.g., `MyStore`).
   - **Port:** Enter the local port your backend runs on (e.g., `4000`).
   - **Path:** Click the **📂 (Folder icon)** to select the root folder of your project on your local machine.
4. Click the **Save** button to store your profile. 
5. To load an existing project later, simply select it from the dropdown and click **Load**.

### Connecting to a Remote Server (Optional)
If you want to manage a remote Linux VPS (Virtual Private Server) instead of your local machine:
1. Navigate to the **Remote Server** section right below the profile bar.
2. Enter your server's **IP Address**, **Username** (e.g., `root`), and **Password**.
3. Click **Connect**.
4. Once connected, the status label will change to green (Connected), and all actions performed in the tool will now execute securely on your remote server via SSH/SFTP.

---

## 2. Dashboard

The Dashboard is the central hub for monitoring your server's health and system status.

**How to Use:**
- **Site Status:** Indicates whether your backend server (PM2) is currently `Running` or `Stopped`.
- **PM2 Uptime:** Shows how long your application has been running without interruption.
- **Caddy Status:** Displays the status of your reverse proxy/web server.
- **Prisma Studio:** Shows whether your database studio is active.
- **SSL Status:** Indicates if Let's Encrypt SSL is active for your domain.
- **Last Backup:** Displays the timestamp of the last successful backup generated.

*No direct actions are taken here; it is purely for real-time monitoring. The dashboard refreshes automatically.*

---

## 3. Control Panel

The Control Panel provides actionable controls to manage your server environment actively.

**Step-by-Step Usage:**
- **Manage Backend (PM2):** Use the **Start**, **Restart**, and **Stop** buttons to control your backend Node.js/Python background processes.
- **Auto-Reboot Policy:** Click **Enable Auto Reboot** to ensure PM2 automatically restarts your backend applications if the physical server reboots.
- **Delete Process:** Use the **Delete PM2** button to remove the app from the background process list entirely.
- **Caddy Web Server:** Click **Start Global Caddy** to initialize your web server routing, or stop it to pause all incoming web traffic.
- **Prisma Studio:** Toggle your database visualizer on and off using the provided switches.

---

## 4. Developer Tab

The Developer tab offers advanced tools designed for in-depth debugging and seamless code deployment.

**Using Developer Tools:**
- **Code Updates (Over-The-Air Deployments):** 
  1. Click **Update Source Code**.
  2. Select a `.zip` file of your new code from your local computer.
  3. The tool will automatically upload the ZIP via SFTP, back up the old codebase (skipping heavy files like `node_modules`), clear the old files, and extract the new ones gracefully.
- **Log Tailing:** Click **Tail Backend Logs** to stream live output (console logs & errors) from your application directly into the unified log window at the bottom of the tool.
- **SSH Console:** You can type custom CLI commands into the command input box and hit enter to execute them directly on your server without opening Putty or Terminal.

---

## 5. Domain & SSL

Effortlessly handle networking and routing configurations from the Domain & SSL tab.

**Setting Up a Live Domain:**
1. Ensure your domain's DNS `A Record` points to your Server's IP address.
2. Open the **Domain & SSL** tab.
3. Enter your **Domain Name** (e.g., `example.com`).
4. Enter your **Email Address** (Required by Let's Encrypt to generate a free SSL certificate).
5. (Optional) Check **"Is API Proxy Only?"** if you only want to route backend API traffic and do not want to host a frontend UI.
6. Click **Apply Domain & SSL Settings**.
7. The manager will automatically generate a Caddyfile, route your ports, and provision a secure HTTPS connection.

---

## 6. Backup & Restore

Ensure data integrity with the quick tools provided in the Backup & Restore tab.

**How to Backup:**
1. Click the **Create Full Backup** button.
2. The tool will instantly create a highly compressed `.zip` archive of your entire project directory.
3. It intelligently ignores unnecessary heavy folders like `node_modules`, `build/`, `.git/`, ensuring the backup is lightweight and fast.
4. *If connected remotely:* Click **Download Backup to PC** to fetch the generated backup from the remote server directly to your local workstation via SFTP.

---

## 7. Installer

The Installer tab automates setting up new pristine environments, making it perfect for brand-new VPS deployments.

**Installing Dependencies:**
- Simply click any of the available installation buttons to bootstrap your server:
  - **Quick Server Setup:** Installs essential Linux tools, Updates APT packages, and secures the server.
  - **Install Caddy:** Installs the Caddy web server globally.
  - **Install Docker/NodeJS:** Sets up necessary development runtimes.
  - **Install Umami:** Sets up a privacy-focused analytics dashboard.

---

## 8. Frequently Asked Questions (FAQ)

### Q1: Why does my SFTP upload fail halfway?
**A:** This usually happens due to network instability or incorrect folder permissions on the remote server. Ensure the user account you logged in with has `write` access to the target directory.

### Q2: My SSL Certificate says "Inactive" after applying the domain. What should I do?
**A:** Let's Encrypt requires your domain's DNS to propagate fully before issuing a certificate. Ensure your domain's `<A-Record>` points to your VPS IP address. Wait 5-10 minutes, restart Caddy from the Control Panel, and check the status again.

### Q3: How do I view error logs if my app crashes?
**A:** Go to the **Developer** tab and click **Tail Backend Logs**. If you are looking for specific PM2 crash errors, you can also type `pm2 logs` in the Developer SSH console input to read historical errors.

### Q4: Can I manage multiple projects at the same time?
**A:** Yes! Simply create a new profile for each project in the top profile bar. You can instantly switch between projects by selecting a different profile from the dropdown and clicking **Load**.

### Q5: Is it safe to leave "Auto Reboot" enabled?
**A:** Yes. Enabling Auto Reboot ensures that if your Windows server or Linux VPS restarts unexpectedly (due to updates or power loss), your PM2 applications will start running automatically upon boot.

### Q6: Can I run this tool strictly on my local Windows machine without a remote server?
**A:** Absolutely. By default, if you do not connect to a remote server, all commands, backups, and deployments execute locally right on your computer.
