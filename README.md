# 🛡️ Instagram-Creator

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.7+-blue?style=for-the-badge&logo=python&logoColor=white" alt="Python Version">
  <img src="https://img.shields.io/badge/License-Educational-green?style=for-the-badge" alt="License">
  <img src="https://img.shields.io/badge/Maintained%3F-Yes-orange?style=for-the-badge" alt="Maintained">
  <img src="https://img.shields.io/badge/Instagram-Creator-E4405F?style=for-the-badge&logo=instagram&logoColor=white" alt="Purpose">
</p>

---

### 🚀 Overview
**Fidra-Instagram-Accounts-Creator** is a high-performance, automated tool designed to streamline the creation of Instagram accounts using advanced techniques like Gmail dot-variations and IMAP verification. It mimics human behavior to bypass detection while providing a seamless automation experience.

> [!WARNING]  
> **DISCLAIMER:** This tool is for **EDUCATIONAL PURPOSES ONLY**. Creating fake accounts violates Instagram's ToS. Use at your own risk.

---

## 📑 Table of Contents
1. [Key Features](#-key-features)
2. [Prerequisites](#-prerequisites)
3. [Installation](#-installation)
4. [Configuration](#-configuration)
5. [Usage](#-usage)
6. [Output & Storage](#-output--storage)
7. [How It Works](#-how-it-works)
8. [Anti-Detection](#-anti-detection-features)
9. [Troubleshooting](#-troubleshooting)
10. [Support](#-support--contact)

---

## ✨ Key Features

| Feature | Description |
| :--- | :--- |
| **🤖 Automated Creation** | Fully automated account registration with random credentials. |
| **📧 Dot-Email Tech** | Generate thousands of unique emails from a single Gmail inbox. |
| **📩 IMAP Integration** | Automatically fetches verification codes directly from Gmail. |
| **🖼️ Auto-Customization** | Sets random profile pictures and uploads initial posts. |
| **⚡ Multi-Credential** | Rotates through multiple Gmail accounts to maximize throughput. |
| **📡 Proxy Support** | Integrated support for rotating proxies to prevent IP bans. |
| **📱 Telegram Alerts** | Real-time notifications for every successful account created. |

---

## 🛠️ Prerequisites

### System Requirements
- **Python:** v3.7 or higher
- **Internet:** Stable connection (Residential proxies recommended)
- **Gmail:** Accounts with **2-Step Verification** and **App Passwords** enabled.

### Gmail Setup (Critical)
1. Enable **2-Step Verification** in Google Account Security.
2. Generate an **App Password** (Select "Mail" and your device).
3. Copy the 16-character code.

---

## 💾 Installation

```bash
# Clone the repository
git clone https://github.com/x1877/Instagram-Creator
cd Instagram-Creator
# Install dependencies
pip install -r requirements.txt
```

---

## ⚙️ Configuration

### 1. Gmail Credentials (`credentials.txt`)
Create `credentials.txt` in the root folder. Format: `email:app_password`
```text
your_email@gmail.com:abcd efgh ijkl mnop
```

### 2. Bot Settings (`settings.json`)
```json
{
    "max_wait": 60,
    "interval": 2,
    "max_retries": 3,
    "retry_delay": 2,
}
```

### 3. Telegram Notifications (`bot.json`)
```json
{
    "bot_token": "1234567890:ABC...",
    "chat_id": "123456789"
}
```

### 4. Proxy Configuration (`proxies.txt`)
Create `proxies.txt` in the root folder to bypass IP blocks.
Format: `http://username:password@ip:port`
```text
http://user123:pass456@142.202.220.242:29167
```

---

## 🎮 Usage

```bash
python main.py
```

### 🟢 Example Success Output
When an account is created successfully, you will see a detailed breakdown in your console:

```text
[+] Using credential: example@gmail.com
[+] Remaining credentials: 3
[ ] Sending verification email to e.xample@gmail.com...
⏳ Waiting for code: 15s / 60s...
✅ Code received: 123456
🎉 Account created successfully!

👤 Username: john_doe_2024
🔑 Password: Password@123
📧 Email: e.xample@gmail.com
📸 Profile Picture: Done
📝 Post Uploaded: Done
```

---

## 📁 Output & Storage

Every account created is automatically logged and saved in multiple formats for your convenience.

### 📍 Storage Locations

| File Path | Description | Data Format |
| :--- | :--- | :--- |
| `📂 accounts/accounts_userpass.txt` | Quick login list | `username:password` |
| `📂 accounts/accounts_full.json` | Detailed account data | `JSON Object` |
| `📂 accounts/accounts_emailpass.txt`| Account + Email recovery | `email:password` |
| `📂 sessions/usersession.txt` | Active session identifiers| `username:sessionid` |
| `📂 sessions/session.txt` | Raw session list | `sessionid` |

### 📱 Telegram Notification Example
If configured, you will receive a message like this:
```text
🎉 New Instagram Account Created!

👤 Username: @fakee
📧 Email: fake@gmail.com
🔑 Password: Password@123
🆔 SessionID: 123456789...
⏰ Created: 2026-05-01 10:30
📊 Account Rank: #5
```

---

## 🔍 How It Works

### The Dot-Email Technique
Gmail ignores periods in usernames. For example:
- `user@gmail.com` == `u.ser@gmail.com` == `us.er@gmail.com`
Instagram sees these as unique, allowing you to register hundreds of accounts to a single Gmail mailbox.

### Account Creation Flow
1. **Init:** Load credentials & verify IMAP access.
2. **Setup:** Generate unique dot-email & random user agent.
3. **Register:** Send IG signup request.
4. **Verify:** Monitor Gmail for 6-digit code via IMAP.
5. **Profile:** Set avatar, upload post, and follow targets.
6. **Notify:** Send details to Telegram & save to local DB.

---

## 🛡️ Anti-Detection Features
- **Browser Impersonation:** Uses `curl_cffi` to mimic Chrome 110.
- **Human Delays:** Random wait times between clicks and requests.
- **Dynamic Headers:** Rotates user agents and cleaning session cookies.
- **Proxy Rotation:** Distributes requests across multiple IP addresses.

---

## 📁 Project Structure

```text
📁 instagram-account-generator/
├── 📜 main.py               # Application Core
├── 📜 credentials.txt       # Gmail List
├── 📜 proxies.txt           # Proxy Configuration
├── 📜 settings.json        # Bot Settings
├── 📜 bot.json             # Telegram Config
├── 📂 Avatars/              # Profile Pictures
├── 📂 Posts/                # Post Images
├── 📂 accounts/             # Generated Data
└── 📂 sessions/             # Auth Sessions
```

---

## 🤝 Support & Contact

**Author:** [@x1877](https://github.com/x1877)  
**Telegram:** [@x187m](https://t.me/x187m) 

---
<p align="center">
 instag : 197.1.1
</p>
