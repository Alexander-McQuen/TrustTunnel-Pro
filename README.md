# TrustTunnel Pro 🚀🛡️

Welcome to **TrustTunnel Pro**! This project provides an ultra-fast, secure, and Anti-DPI VPN solution. It includes a fully automated Server Setup Script (based on the official TrustTunnel core) and a custom-built Windows Client with an easy-to-use graphical interface.

به **TrustTunnel Pro** خوش آمدید! این پروژه یک راهکار کامل برای دور زدن فیلترینگ شدید (Anti-DPI) است که شامل یک اسکریپت نصب خودکارِ سرور و یک کلاینت اختصاصی ویندوز با رابط کاربری گرافیکی (GUI) می‌شود.

---

## ✨ Features (امکانات)
* 🚀 **Modern Protocols:** Supports **HTTP/2** and **QUIC** (HTTP/3) for maximum speed.
* 🛡️ **Anti-DPI:** Disguises VPN traffic as normal web traffic to bypass heavy censorship.
* 🔒 **Auto SSL:** Automatically generates and renews Let's Encrypt SSL certificates.
* 💻 **Custom Windows Client:** A beautiful, portable GUI for Windows users.
* ⚡ **1-Click Server Setup:** Fully automated server installation script.

---

## 🛠️ 1. Server Setup (نصب سرور - لینوکس)

**Prerequisites (پیش‌نیازها):**
- A Linux Ubuntu Server (Ubuntu 20.04 or 22.04 recommended).
- A valid Domain/Subdomain pointing to your Server's IP (e.g., `vpn.yourdomain.com`).

**Quick Install Command (دستور نصب سریع):**
To install the server, copy and paste this single command into your server's terminal (run as root or with sudo):
برای نصب کامل سرور، کافیست دستور زیر را کپی کرده و در ترمینال سرور اوبونتوی خود اجرا کنید:

```bashe
curl -L -o setup.sh https://raw.githubusercontent.com/Alexander-McQuen/TrustTunnel-Pro/main/setup.sh && sed -i 's/\r$//' setup.sh && chmod +x setup.sh && sudo ./setup.sh
```

**What this script does (این اسکریپت چه کار می‌کند؟):**
1. Secures your server and opens necessary ports (22 for SSH, 80, and 443 for VPN/SSL).
2. Downloads the official TrustTunnel Core.
3. Runs the Setup Wizard to automatically get an SSL certificate and create your username/password.
4. Creates a background service so your VPN stays online 24/7.

---

## 💻 2. Windows Client Setup (کلاینت اختصاصی ویندوز)

We have built a custom, user-friendly Windows client so you don't have to deal with the command line!
ما یک کلاینت گرافیکی اختصاصی برای ویندوز ساخته‌ایم تا نیازی به استفاده از محیط‌های متنی نداشته باشید!

**How to use (نحوه استفاده):**
1. Go to the Releases section of this repository.
2. Download the `TrustTunnel_Windows_v1.0.zip` file.
3. **Extract (Unzip)** the downloaded file. 
4. Make sure all 3 files (`TrustTunnel_Pro.exe`, `trusttunnel_client.exe`, and `wintun.dll`) are in the **same folder**.
5. Right-click on `TrustTunnel_Pro.exe` and select **"Run as Administrator"**.
6. Enter your Server IP, Port (443), Domain (SNI), Username, and Password, then click **CONNECT**!

*(نکته: حتماً فایل را از حالت فشرده خارج کنید و هر ۳ فایل را در یک پوشه نگه دارید. برنامه را با دسترسی ادمینستراتور اجرا کنید).*

---

## 📱 3. Android / iOS Setup (سایر دستگاه‌ها)

You can also connect to this server using the official TrustTunnel apps available for Android.
- **Port:** 443
- **SNI / Domain:** your-domain.com
- **Protocol:** HTTP2 or QUIC
- Enable **"Allow Insecure"** or **"Skip Cert Verification"** if your app requires it.

---

## 🔧 Troubleshooting (عیب‌یابی سرور)

If you want to check your server's live logs and see if clients are connecting successfully, run this command on your server:
برای مشاهده لاگ‌های زنده سرور و بررسی وضعیت اتصالات، این دستور را در ترمینال سرور وارد کنید:

sudo journalctl -u trusttunnel -f

---

*Made with ❤️ for a free and open internet.*
