# VPS to VPN whitepaper

**Last updated:** 2026-09-13  
**Products:** VPS to VPN (Windows), VPS to VPN Android, Black Fox Config Builder  
**Current Windows release:** v3.2.0 (Build 220)  
**Website:** [https://foxnext.net](https://foxnext.net)  
**Public GitHub:** [https://github.com/BlackFoxGroup/VPS-to-VPN](https://github.com/BlackFoxGroup/VPS-to-VPN)

---

## 1. Purpose

VPS to VPN is a server deploy and operations suite. Operators on restricted networks use it to stand up multi-location VPN infrastructure on:

- 3X-UI (Sanaei) as the panel
- Nine mesh path types (eight Xray-based, WireGuard last) with automatic failover
- Server Connection Manager for live link type, watchdog, and Link Monitor
- AI Assistant Pro: the Black Fox Group in-app agent. After activation, operators can ask in chat to add servers, install the panel, run mesh or domain work, and diagnose. The agent confirms before it changes a host.

The point is to cut the repeated Linux, SSH, panel, DNS, and tunnel work from daily ops.

---

## 2. Surfaces

| Surface | Name | Role | Download |
|---------|------|------|----------|
| Windows | VPS to VPN | Desktop operations console | [Setup.zip (GitHub)](https://github.com/BlackFoxGroup/VPS-to-VPN/releases/latest/download/VPS-to-VPN-Setup.zip), [Portable.zip](https://github.com/BlackFoxGroup/VPS-to-VPN/releases/latest/download/VPS-to-VPN-Portable.zip) |
| Android | VPS to VPN Android | Mobile operations (Basic and Pro) | [APK (GitHub)](https://github.com/BlackFoxGroup/VPS-to-VPN/releases/latest/download/VPS-to-VPN-Android-arm64-v8a-release.apk) |
| Android companion | Black Fox Config Builder | Phone helper for 3X-UI client configs | [APK](https://foxnext.net/downloads/Black-Fox-Config-Builder.apk) |
| Google Play | VPS to VPN Android | Store listing | Coming soon |
| macOS | VPS to VPN | Future desktop build | Coming soon |

Config Builder docs: [BlackFoxGroup/blackfox-config-builder](https://github.com/BlackFoxGroup/blackfox-config-builder)

---

## 3. Operating model

### Basic Mode

Smaller, faster setups:

- Central Server
- SSH connect and Full Deploy
- Up to two Exit servers
- Panel helpers
- WireGuard and 3X-UI install helpers

### Pro Mode

Larger multi-hop setups:

- Central, Tunnel, up to six Exit servers
- Nine mesh types plus failover
- Domain and DNS management
- CDN automation on Windows
- Move Central Server on Windows and Android
- Migration backup during a central move

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

Moving the central role used to mean rebuilding tunnels, rebinding exits, and restoring panel clients by hand.

Move Central Server does that relocation in Pro Mode on Windows and Android:

1. Open Operations in Pro Mode
2. Choose Move Central Server
3. Enter the new central
4. Let the suite reconnect tunnel and exit roles
5. Let it restore 3X-UI clients from the migration snapshot
6. Keep the local backup written during the move

Older pages that list this as Windows-only are wrong.

---

## 5. Licensing and reactivation

Three paths:

1. Online check through payment / TX Hash
2. Offline activation codes
3. Reactivation after reinstall on the same device

Operators often uninstall and reinstall. Forcing them to keep offline codes forever for that case creates extra support work.

On Registration:

1. Reinstall on the same device
2. Open Registration
3. Press Reactivation / فعال‌سازی مجدد

The app sends the machine fingerprint to the official reactivation service. If that device already has a valid record, access comes back without typing a stored code.

Notes:

- Reactivation only covers devices the official service already recorded
- Online TX and offline codes stay available
- A local Windows vault restore, if present, is a different mechanism
- Reactivation restores a known device-bound record; it does not mint a new license

Site price reference at last check: Basic 19 USDT, Pro 33 USDT. Confirm on the site.

---

## 6. Domains, DNS, and CDN

Pro includes domain/subdomain DNS automation for Cloudflare and ArvanCloud.

Windows Pro also has CDN operations for ArvanCloud, Cloudflare, KeyCDN, and Other.

Android Pro stays on topology and Move Central. Windows still has the deeper CDN tools.

---

## 7. Black Fox Config Builder

This Android app creates 3X-UI client configs on a phone. It does not deploy servers. Operators still use VPS to VPN or VPS to VPN Android for the hosts, then paste Panel Login Info into Config Builder.

| Item | Value |
|------|-------|
| Version | 1.1.3 (Build 7) |
| Package | `com.blackfoxvpnn.configbuilder` |
| Download | [Black-Fox-Config-Builder.apk](https://foxnext.net/downloads/Black-Fox-Config-Builder.apk) |
| Min Android | API 24 |
| Min panel | 3X-UI 3.3.0+ |

Tabs: Connection, Single, Bulk, List, Settings, Contact.

Build 6 added the dual-server remote feed (`blackfoxupdate.ir` and `foxnext.net`). Build 7 is the current published Android release.

Config Builder does not run Installer license registration or TX unlock.

---

## 8. Localization

English, Persian, Russian, Chinese, German, Uzbek, Turkish, Indonesian, Ukrainian, Hindi.

---

## 9. Privacy and updates

- EN: [https://foxnext.net/en/privacy.html](https://foxnext.net/en/privacy.html)
- FA: [https://foxnext.net/fa/privacy.html](https://foxnext.net/fa/privacy.html)
- Update hosts: `foxnext.net` and `blackfoxupdate.ir`

The published privacy pages are the source of truth.

---

## 10. Limits of this document

This suite is an operations console. Google Play and macOS are not released yet. Features that are not in the current Windows or Android source are not documented here as if they shipped.

---

## 11. Related

- [README.md](../README.md)
- [ROADMAP.en.md](ROADMAP.en.md)
- [WHITEPAPER.fa.md](WHITEPAPER.fa.md) · [WHITEPAPER.ru.md](WHITEPAPER.ru.md) · [WHITEPAPER.zh.md](WHITEPAPER.zh.md)

© Black Fox Security Team
