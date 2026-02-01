# 🎥 Vantix Setup Assistant (Pro Edition)

A high-performance, responsive setup wizard designed to onboard family members to a private Jellyfin server with zero friction. Optimized for **USBX/Merlion** hosting and **Zurg** backends.

## 🚀 Pro Features

### 📱 Intelligent Device Routing
The wizard uses a custom User-Agent detection script to serve two distinct experiences:
* **Mobile Mode:** Focuses on one-tap app connectivity and deep linking.
* **TV Mode (Chromecast/Firestick/SmartTV):** Prioritizes QR codes and ultra-short URLs to eliminate remote-control typing fatigue.

### ⚡ Magic "Deep Link" Setup
Includes a fail-safe "Connect" button for mobile users:
1.  **Protocol Launch:** Attempts to open the Jellyfin app and pre-fill the server URL using `jellyfin://`.
2.  **Smart Redirect:** If the app is missing, a JavaScript timer automatically forwards the user to the **iOS App Store** or **Google Play Store** based on their OS.

### 📡 Live Server Heartbeat
A built-in asynchronous health check pings the Merlion server in real-time:
* **Green Pulse:** "System Ready" – The server is online and accepting connections.
* **Red Pulse:** "Updating" – Alerts family if the server is down for maintenance, preventing "it's not working" support calls.

### 📺 TV Remote Optimization
* **Short-Link Integration:** Displays an `is.gd` shortcut to reduce 40+ character URLs down to 5-10 characters for D-pad entry.
* **Voice Guide:** Built-in instructions prompting users to use the Voice Remote (Alexa/Google Assistant) for app installation.

### 🛠️ Support Bridge
Integrated **Discord**, **Telegram**, and **WhatsApp** direct-action links with high-fidelity Font Awesome vector icons for immediate family support.

---

## 🛠️ Setup Instructions

1.  **Short URL:** Create a short link at `is.gd` pointing to your long Merlion address and update `const shortUrl`.
2.  **Socials:** Update the `social-links` section with your specific IDs:
    * **Discord:** `https://discord.com/users/YOUR_ID`
    * **Telegram:** `https://t.me/YOUR_USER`
    * **WhatsApp:** `https://wa.me/YOUR_NUMBER`
3.  **Deployment:** Upload the `index.html` to your web server (e.g., GitHub Pages, USBX web root, or Nginx).

---
*Created for the Vantix Media ecosystem.*
