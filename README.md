# 🛠️ unfck-lineageos

A curated collection of **Magisk** and **KernelSU (KSU)** modules to remove or replace deeply embedded Google services in **LineageOS**, enhancing **privacy**, **security**, and true **de-Googling**.

LineageOS removes Google apps — but not all Google *services*. This project helps eliminate those hidden dependencies, replacing them with **privacy-respecting**, **open-source**, and **community-run** alternatives.

> 🛑 Your phone shouldn’t be a surveillance device. Let’s take back control.

---

## 🔧 What These Modules Change

### 🌐 Captive Portal Detection
Replaces Google’s default captive portal check (`connectivitycheck.gstatic.com`) with privacy-focused endpoints:

```shell
settings put global captive_portal_http_url "http://204.ecloud.global"
settings put global captive_portal_https_url "https://e.foundation/net_204/"
settings put global captive_portal_fallback_url "http://captiveportal.kuketz.de"
settings put global captive_portal_other_fallback_urls "http://captiveportal.kuketz.de"
```

> ✅ Powered by:
> - **[e.foundation](https://e.foundation)** – A nonprofit building open, private-by-design mobile OS that doesn’t log, track, or scan your data.
> - **[Kuketz Blog](https://www.kuketz-blog.de)** – Run by a renowned security researcher focused on privacy and transparency.

This prevents your device from "phoning home" to Google when connecting to Wi-Fi networks.

---

### ⏰ NTP Time Server
Switches the default time sync server to a decentralized, public pool:

```shell
NTP_SERVER=pool.ntp.org
```

No more reliance on Google’s time servers. Stay synchronized with the global NTP network.

---

### 📡 SUPL (Location) Server
Replaces Google’s SUPL (Secure User Plane Location) server with **Librem 5’s neutral host**:

```shell
SUPL_HOST=nip.ntfp.org
```

Improves privacy for A-GPS and network-assisted location lookups — no more tracking via location services.

---

### 🌍 WebView Replacement
Replaces the stock (often Google-dependent) WebView with a **privacy-hardened alternative**:

We recommend:  
🔹 **[Cromite WebView](https://github.com/uazo/cromite)** – A lightweight, tracker-free Chromium fork designed for privacy.

Also compatible with:
- **Vanadium** (GrapheneOS)
- **Mulch** (DivestOS)

> ✅ Blocks telemetry, ads, and bloatware.  
> ✅ Fully open-source.  
> ✅ Maintains compatibility with modern web apps (banking, messaging, etc).

---

## 📦 Installation

1. ✅ Install [Magisk](https://github.com/topjohnwu/Magisk) or [KernelSU](https://github.com/tiann/KernelSU).
2. 🔽 Download and install the **customized modules** from:
   - [👉 Latest Release on GitHub](https://github.com/ch3gg5/unfck-lineageos/releases/latest)
3. 🔽 Install a de-Googled WebView:
   - [open_webview (Magisk Modules Alt Repo)](https://github.com/Magisk-Modules-Alt-Repo/open_webview)
   - Choose your preferred engine: **Cromite**, **Vanadium**, or **Mulch**
4. 🔁 Reboot your device.

> ⚠️ After OTA updates, some settings may reset. Consider scripting the captive portal commands for reapplication.

---

## 🛡️ Why This Matters

> *"Your data is **YOUR** data!"* — [e.foundation](https://e.foundation)

Even on LineageOS:
- Your phone pings Google for Wi-Fi login checks.
- Location services use Google’s SUPL servers.
- WebView may still contain telemetry.
- Time sync often defaults to Google.

This project closes those gaps.

✅ **No tracking**  
✅ **No logging**  
✅ **No hidden dependencies**

You keep full control — just like it should be.

---

## 🙏 Credits

- [Atrate](https://github.com/Atrate) – *Magisk-Captive-Control*
- [PlqnK](https://github.com/PlqnK) – *magisk-supl-replacer*
- [Magisk Modules Alt Repo](https://github.com/Magisk-Modules-Alt-Repo) – *open_webview*
- [e.foundation](https://e.foundation) – Privacy-first mobile OS & captive portal
- [Kuketz Blog](https://www.kuketz-blog.de) – Trusted security research and captive portal fallback

---

## 🤝 Contribute

Found a leak? Know a better endpoint? Want to bundle this into a single automated module?

👉 Open an **issue** or **pull request**!  
Let’s make **de-Googling** seamless, reliable, and accessible to all.

---

## 📜 License

This project is community-maintained and aggregates open-source components. Each module is licensed under its original terms. Please refer to individual repositories for licensing details.

