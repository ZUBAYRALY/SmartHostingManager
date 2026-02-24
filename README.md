<div align="center">
  <h1>Smart Hosting Manager</h1>
  <p>An open-source, comprehensive GUI for deploying, monitoring, and managing multi-site hosting environments seamlessly.</p>
</div>

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Windows%20|%20Linux-blue?style=flat-square&logo=python" alt="Platform">
  <img src="https://img.shields.io/badge/License-Non--Commercial-red?style=flat-square" alt="License">
</p>

## About Smart Hosting Manager

**Smart Hosting Manager** is a modern, open-source application designed for managing servers. It acts as a control panel for local and remote servers, seamlessly handling domains, SSL certificates, PM2 processes, and automated deployments securely via SFTP and SSH. 

## ✨ Features

- **Multi-Site Management:** Switch between different active environments and hosting setups effortlessly.
- **Remote Server Integration:** Connect securely to remote Linux servers using SSH to execute commands and monitor stats. 
- **Automated Deployments:** Built-in SFTP capability to effortlessly compress and deploy backups and files automatically.
- **Status Dashboard:** Real-time visibility into your PM2 Backends, Caddy frontends, and SSL Certificates.
- **Developer & Control Panel:** Instantly tail remote server logs, reboot environments, apply SSL, and update frontend/backend instances.

## 📥 Installation & Setup

> **Note:** Smart Hosting Manager requires **Windows 10 / 11** or **Ubuntu (Linux)** to run. The source requires **Python 3.9+**.

### Running from Source
1. Clone the repository:
   ```bash
   git clone https://github.com/zubayraly/SmartHostingManager.git
   ```
2. Navigate to the project directory:
   ```bash
   cd SmartHostingManager
   ```
3. Install the required dependencies:
   ```bash
   pip install customtkinter paramiko
   ```
4. Run the application:
   ```bash
   python SmartHosting.py
   ```

### Pre-built Release
You can also download the pre-packaged executable version of Smart Hosting Manager from the **[Releases page](https://github.com/zubayraly/SmartHostingManager/releases)**.

## 📖 User Guide
For detailed instructions on how to use each feature and tab in Smart Hosting Manager, please see the **[User Guide](UserGuide.md)**.

## 📸 Screenshots

*(Replace these placeholders with your actual screenshots inside the `screenshots/` directory)*

### Dashboard
<img width="1151" height="833" alt="dashboard" src="https://github.com/user-attachments/assets/28c05df5-c450-4738-b15e-e129942bd0d9" />

### Control Panel
<img width="1151" height="833" alt="control panel" src="https://github.com/user-attachments/assets/b2266b9a-df5a-4ed1-80cf-0c4044148e37" />

### Developer
<img width="1151" height="833" alt="developer" src="https://github.com/user-attachments/assets/8b12dd36-cf2d-451c-b9ce-64f0c0de5c3e" />

### Domain & SSL
<img width="1151" height="833" alt="domain" src="https://github.com/user-attachments/assets/fa651129-457d-4eab-ae3c-bebe1f4c8628" />

### Backup & Restore
<img width="1151" height="833" alt="backup" src="https://github.com/user-attachments/assets/5b2dd631-d847-4f2b-bbaa-1d1c616fdf84" />

### Installer
<img width="1151" height="833" alt="installer" src="https://github.com/user-attachments/assets/c47a0ee5-4a9e-4a94-ac1c-32413d911ad3" />

## 🐛 Bug Reports & Feature Requests

Encountered a bug or have a cool idea? We'd love to hear it! 
Please open a new issue in the **[Issues tab](https://github.com/zubayraly/SmartHostingManager/issues)**. 

When reporting bugs, please include:
- Your OS and version
- Steps to reproduce the issue
- Screenshots or console logs (if applicable)

## 🛠 Built With

- **Python 3** - Primary language
- **CustomTkinter** - Complete customized UI toolkit for modern dark mode interfaces
- **Paramiko** - To handle robust SSH & SFTP connections

## ❤️ Support the Developer

If you enjoy using Smart Hosting Manager and would like to support its continued development, you can buy me a coffee! 

- **PayPal:** [Donate via PayPal](https://www.paypal.com/paypalme/zubayrop)
- **NayaPay:** `zubayr@nayapay`
- **USDT (Binance BEP20):** `0xeb0aa1a7b9704ef876c8c9f2cd65b8e989c25249`

<br>

## ⚖️ License

This project is strictly **free to use for personal or non-commercial purposes only**.

⛔ **Selling this software or modifying it to be sold is STRICTLY PROHIBITED.** ⛔

Any unauthorized commercialization or sale of this software will result in an immediate **lawsuit and legal action** against the offending party. Please see the `LICENSE` file for full terms.

<div align="center">
  <sub>Built with 🕊️🥀 by Zubayr Aly</sub>
</div>

