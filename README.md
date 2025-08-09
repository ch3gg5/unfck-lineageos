# 🛠️ unfck-lineageos

A curated collection of **Magisk** and **KernelSU (KSU)** modules to remove or replace embedded Google services in **LineageOS**, improving **privacy**, **security**, and true **de-Googling**.

LineageOS removes Google apps, but not all Google *services*. This project eliminates those hidden dependencies, replacing them with **privacy-respecting**, **open-source**, and **community-run** alternatives.

> 🛑 Your phone shouldn’t be a surveillance device. Let’s take back control.

---

## 🔧 What These Modules Change

### 🌐 Captive Portal Detection
Replaces Google’s default check (`connectivitycheck.gstatic.com`) with privacy-focused endpoints:

```shell
settings put global captive_portal_http_url "http://204.ecloud.global"
settings put global captive_portal_https_url "https://e.foundation/net_204/"
settings put global captive_portal_fallback_url "http://captiveportal.kuketz.de"
settings put global captive_portal_other_fallback_urls "http://captiveportal.kuketz.de"
```

> ✅ Powered by:
> - **[e.foundation](https://e.foundation)** – A nonprofit building open, private-by-design mobile OS that doesn’t log, track, or scan your data.
> - **[Kuketz Blog](https://www.kuketz-blog.de)** – Run by a renowned security researcher focused on privacy and transparency.

Stops your device from "phoning home" when connecting to Wi-Fi.

---

### ⏰ NTP Time Server
Switches time sync to the decentralized public pool:

```shell
NTP_SERVER=pool.ntp.org
```

No more reliance on Google’s time servers.

---

### 📡 SUPL (Location) Server
Replaces Google’s SUPL server with **Librem 5’s neutral host**:

```shell
SUPL_HOST=nip.ntfp.org
```

Improves privacy for A-GPS and network-assisted location, no more tracking via location services.

---

### 🌍 WebView Replacement
Replaces stock WebView with a **privacy-hardened alternative**:

We recommend:  
🔹 **[Cromite WebView](https://github.com/uazo/cromite)** – Lightweight, tracker-free Chromium fork.

Also compatible with:
- **Vanadium** (GrapheneOS)
- **Mulch** (DivestOS)

> ✅ Blocks telemetry, ads, and bloatware  
> ✅ Fully open-source  
> ✅ Works with modern web apps (banking, messaging, etc)

---

## 📦 Installation

1. ✅ Install [Magisk](https://github.com/topjohnwu/Magisk) or [KernelSU](https://github.com/tiann/KernelSU)
2. 🔽 Download modules from:  
   [👉 Latest Release on GitHub](https://github.com/ch3gg5/unfck-lineageos/releases/latest)
3. 🔽 Install a de-Googled WebView:  
   - [open_webview (Magisk Modules Alt Repo)](https://github.com/Magisk-Modules-Alt-Repo/open_webview)  
   Choose: **Cromite**, **Vanadium**, or **Mulch**
4. 🔁 Reboot your device

---

## 🛡️ Why This Matters

> *"Your data is **YOUR** data!"* - [e.foundation](https://e.foundation)

Even on LineageOS:
- Your phone pings Google for Wi-Fi checks
- Location uses Google’s SUPL servers
- WebView may include telemetry
- Time sync defaults to Google

This project closes those gaps.

✅ No tracking  
✅ No logging  
✅ No hidden dependencies

You stay in control

---

## 🙏 Credits

- [Atrate](https://github.com/Atrate) – *Magisk-Captive-Control*
- [PlqnK](https://github.com/PlqnK) – *magisk-supl-replacer*
- [Magisk Modules Alt Repo](https://github.com/Magisk-Modules-Alt-Repo) – *open_webview, updated supl replacer*
- [e.foundation](https://e.foundation) – Privacy-first OS & captive portal
- [Kuketz Blog](https://www.kuketz-blog.de) – Security research and fallback portal
- [Mental Outlaw](https://www.youtube.com/watch?v=E1U5qoiR1fM) – How to De-Google LineageOS

---

## 🤝 Contribute

Found a leak? Know a better endpoint? Want to automate this?

👉 Open an **issue** or **pull request**!  
Let’s make **de-Googling** seamless and accessible to all.

---

## 📜 License

This project is community-maintained and includes open-source components. Each module is under its original license. See individual repositories for details.
