# VPS to VPN — Whitepaper

**Last updated:** 2026-09-09  
**Product family:** VPS to VPN (Windows) · VPS to VPN Android · Black Fox Config Builder  
**Current releases:** Windows **v3.1.1 (Build 213)** · Android / Config Builder: unchanged in this pass  
**Website:** [https://foxnext.net](https://foxnext.net)  
**GitHub:** [https://github.com/BlackFoxGroup/blackfox-vpn-installer](https://github.com/BlackFoxGroup/blackfox-vpn-installer)

---

## 1. Purpose

VPS to VPN is a **server deployment and operations suite**, not a consumer VPN client.

It exists to help operators in constrained networks deploy and manage multi-location VPN infrastructure built on:

- **3X-UI (Sanaei)** as the panel layer  
- **Nine mesh path types** (eight Xray-based + WireGuard last) with automatic failover  
- **Server Connection Manager** for live link type, watchdog, and Link Monitor  

The product goal is to remove most of the repetitive Linux, SSH, panel, DNS, and tunnel work from day-to-day operations.

---

## 2. Product surfaces

| Surface | Full product name | Role | Download |
|---------|-------------------|------|----------|
| Windows | **VPS to VPN** | Full desktop operations console | [VPS to VPN-Setup.exe](https://foxnext.net/downloads/VPS%20to%20VPN-Setup.exe) |
| Android | **VPS to VPN Android** | Mobile operations app (Basic + Pro) | [VPS to VPN Android.apk](https://foxnext.net/downloads/VPS%20to%20VPN%20Android.apk) |
| Android companion | **Black Fox Config Builder** | Mobile helper to create 3X-UI client configs | [Black-Fox-Config-Builder.apk](https://foxnext.net/downloads/Black-Fox-Config-Builder.apk) |
| Google Play | VPS to VPN Android listing | Distribution channel | **Coming Soon** |
| macOS | VPS to VPN | Future desktop edition | **Coming Soon** |

Dedicated Config Builder documentation: [BlackFoxGroup/blackfox-config-builder](https://github.com/BlackFoxGroup/blackfox-config-builder)

---

## 3. Operating model

### Basic Mode

Basic Mode targets faster, smaller deployments:

- Central Server setup  
- SSH connect and Full Deploy  
- Up to two Exit servers  
- Panel configuration helpers  
- Core install helpers for WireGuard and 3X-UI  

### Pro Mode

Pro Mode targets larger multi-hop infrastructures:

- Central Server  
- Tunnel Server  
- Up to six Exit servers  
- Nine mesh path types + failover  
- Domain / DNS management  
- CDN automation on Windows  
- **Move Central Server on Windows and Android**  
- Migration backup during central relocation  

```text
Central Server
      ↓
Tunnel Server
      ↓
Exit Server
      ↓
Client Infrastructure
```

---

## 4. Move Central Server

Relocating the central role used to mean rebuilding tunnels, re-binding exits, and manually restoring panel clients.

**Move Central Server** automates that relocation in Pro Mode on **both Windows and Android**.

Operator flow:

1. Open Operations in Pro Mode  
2. Choose Move Central Server  
3. Enter the new central server details  
4. Let the suite reconnect tunnel and exit roles to the new central  
5. Allow automated transfer of 3X-UI panel clients from the migration snapshot  
6. Keep the local migration backup created during the move  

This is an active Android feature as well as a Windows feature. Documentation that lists Move Central as Windows-only is outdated.

---

## 5. Licensing and Reactivation

Licensing supports three practical paths:

1. Online verification through payment / TX Hash  
2. Offline activation codes  
3. **Reactivation** after reinstall on the same device  

### Why Reactivation exists

Operators often uninstall and reinstall the app. Requiring permanent storage of offline codes for that common case creates friction and support load.

### Current reactivation behavior

On the Registration screen:

1. Reinstall the app on the **same device**  
2. Open Registration  
3. Press **Reactivation** (English) / **فعال‌سازی مجدد** (Persian)  

The app uses the device’s machine fingerprint to query the official reactivation service. If a valid prior activation record exists for that device, access is restored without forcing the user to keep and re-enter a stored license code for that recovery path.

Important clarifications:

- Reactivation is for previously activated devices recorded by the official service  
- Online TX and offline codes remain available  
- Local Windows vault restore (if present) is a separate local-device mechanism and must not be confused with server reactivation  
- Reactivation does not invent a new license; it restores a known device-bound activation record  

Current public website pricing reference: Basic **19 USDT** · Pro **33 USDT** (confirm on site).

---

## 6. Domains, DNS, and CDN

Pro Mode includes domain/subdomain management with DNS automation for:

- Cloudflare  
- ArvanCloud  

Windows Pro additionally exposes CDN operations for:

- ArvanCloud  
- Cloudflare  
- KeyCDN  
- Other CDN  

Android Pro currently focuses on core topology operations and Move Central; Windows remains the deeper CDN automation surface.

---

## 7. Black Fox Config Builder

**Black Fox Config Builder** is the Android companion for day-to-day 3X-UI config creation on a phone.

It does **not** deploy servers. Operators still use VPS to VPN / VPS to VPN Android for Basic/Pro infrastructure, then paste **Panel Login Info** into Config Builder.

### Current release

| Item | Value |
|------|-------|
| Full product name | Black Fox Config Builder |
| Version | **1.1.3 (Build 7)** |
| Package | `com.blackfoxvpnn.configbuilder` |
| Download | [Black-Fox-Config-Builder.apk](https://foxnext.net/downloads/Black-Fox-Config-Builder.apk) |
| Min Android | API 24 |
| Min panel | 3X-UI **3.3.0+** |

### App surface (six tabs)

1. **Connection** — Panel URL / user / pass / optional API Key / optional Sub URI  
2. **Single** — One config with multi-inbound select, VLESS + sub links, QR codes  
3. **Bulk** — Many configs with progress and stop  
4. **List** — Copy link, delete from panel, delete from list  
5. **Settings** — 10 languages, dual-host updates, force update, activity log  
6. **Contact** — Website, email, GitHub, Telegram  

### Published build notes

- **Build 6:** Dual-server remote feed (`blackfoxupdate.ir` + `foxnext.net`) for version / wallet / news / APK  
- **Build 7:** Current published Android release with the full six-tab workflow, multi-inbound creation, delete-from-panel, and 10-language coverage  

Config Builder does **not** implement Installer license registration / TX unlock inside the app.

---

## 8. Localization

BlackFox Group applications and the website support **10 languages**:

English, Persian, Russian, Chinese, German, Uzbek, Turkish, Indonesian, Ukrainian, Hindi.

---

## 9. Privacy and updates

- Privacy Policy EN: [https://foxnext.net/en/privacy.html](https://foxnext.net/en/privacy.html)  
- Privacy Policy FA: [https://foxnext.net/fa/privacy.html](https://foxnext.net/fa/privacy.html)  
- Update hosts: `foxnext.net` and `blackfoxupdate.ir`  

Treat the published Privacy Policy pages as the authoritative source.

---

## 10. What this suite is not

- Not a simple end-user VPN client  
- Not a claim that Google Play is already live  
- Not a claim that macOS is already shipping  
- Not a documentation surface for unimplemented features  

---

## 11. Related documents

- [README.md](../README.md)  
- [ROADMAP.en.md](ROADMAP.en.md)  
- [ROADMAP.fa.md](ROADMAP.fa.md)  
- [WHITEPAPER.fa.md](WHITEPAPER.fa.md)  
- Config Builder docs: [BlackFoxGroup/blackfox-config-builder](https://github.com/BlackFoxGroup/blackfox-config-builder)  

---

© Black Fox Security Team
