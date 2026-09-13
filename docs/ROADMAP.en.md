# VPS to VPN roadmap

**Last updated:** 2026-09-13  
**Product:** VPS to VPN  
**Current releases:** Windows v3.1.1 (Build 213). Android and Config Builder follow `version.json` on the update hosts.  
**Website:** [https://foxnext.net](https://foxnext.net)  
**Public GitHub:** [BlackFoxGroup/VPS-to-VPN](https://github.com/BlackFoxGroup/VPS-to-VPN)

This list tracks what already shipped, what we are still changing, and what is planned. It follows the current Windows Go tree, the site, and the license service. Android version numbers here stay as they were unless a release note says otherwise.

---

## Downloads

| Product | File | GitHub | Site |
|---------|------|--------|------|
| VPS to VPN (Windows installer) | `VPS-to-VPN-Setup.zip` | [download](https://github.com/BlackFoxGroup/VPS-to-VPN/releases/latest/download/VPS-to-VPN-Setup.zip) | [foxnext.net](https://foxnext.net/downloads/VPS%20to%20VPN-Setup.exe) |
| VPS to VPN (Windows portable) | `VPS to VPN-Portable.zip` | [download](https://github.com/BlackFoxGroup/VPS-to-VPN/releases/latest/download/VPS.to.VPN-Portable.zip) | — |
| VPS to VPN Android (arm64) | `VPS-to-VPN-Android-arm64-v8a-release.apk` | [download](https://github.com/BlackFoxGroup/VPS-to-VPN/releases/latest/download/VPS-to-VPN-Android-arm64-v8a-release.apk) | [foxnext.net](https://foxnext.net/downloads/VPS%20to%20VPN%20Android.apk) |
| Black Fox Config Builder | `Black-Fox-Config-Builder.apk` | — | [foxnext.net](https://foxnext.net/downloads/Black-Fox-Config-Builder.apk) |

Google Play for VPS to VPN Android: coming soon.  
macOS edition: coming soon.

---

## Done

### Platform and releases

- Windows installer and operations console: VPS to VPN v3.1.1 Build 213
- Android operations app: VPS to VPN Android
- Companion: Black Fox Config Builder v1.1.3 Build 7
- Site plus two update hosts (`foxnext.net`, `blackfoxupdate.ir`)
- Privacy pages (EN/FA) on foxnext.net
- Public docs and binaries on [BlackFoxGroup/VPS-to-VPN](https://github.com/BlackFoxGroup/VPS-to-VPN)

### Core operations (Windows and Android)

- Basic Mode and Pro Mode
- AI Assistant Pro: in-app Black Fox Group agent for day-to-day ops (chat, then confirm before changes)
- Central setup, Connect SSH, Full Deploy
- Tunnel Server (Pro)
- Exit Server (Basic: 2 slots; Pro: up to 6)
- Nine mesh path types with automatic failover
- Configure Panel helpers
- Install WireGuard / Install 3X-UI helpers

### Pro extras

- Domain and subdomain DNS automation (Cloudflare, ArvanCloud)
- CDN automation on Windows Pro (ArvanCloud, Cloudflare, KeyCDN, Other)
- Move Central Server on Windows and Android (Pro): reconnects tunnel and exit hosts, restores 3X-UI clients from a snapshot, writes a local migration backup

### Licensing

- Online payment check (TX Hash / USDT)
- Offline activation codes
- License Reactivation on the Registration screen after uninstall/reinstall on the same device (machine fingerprint)

### Companion: Black Fox Config Builder

- Six tabs: Connection, Single, Bulk, List, Settings, Contact
- Single and bulk inbound create
- Delete from panel or from the local list
- Dual-server updates
- Needs 3X-UI 3.3.0 or newer, Android API 24+, 10 languages
- Docs: [BlackFoxGroup/blackfox-config-builder](https://github.com/BlackFoxGroup/blackfox-config-builder)

### Localization

Ten languages: English, Persian, Russian, Chinese, German, Uzbek, Turkish, Indonesian, Ukrainian, Hindi.

### Docs

README, ROADMAP, and WHITEPAPER in English, Persian, Russian, and Chinese. Site guides for Basic, Pro, Registration, Keys, and Config Builder.

---

## In progress

- Closer Android and Windows behavior on long or odd flows
- Clearer UI while deploy or move jobs run
- SSH, panel sync, and update-check stability
- Site copy matching what the apps actually do
- Remaining gaps between Windows CDN tools and Android Pro

---

## Planned

### Near term

- Google Play listing for VPS to VPN Android
- Backup and restore that is not only the Move Central snapshot
- Resume or recover a deploy that stopped mid-way
- Clearer operator errors and recovery text

### Medium term

- macOS edition
- More CDN polish on Windows
- Extra DNS/CDN providers if operators ask for them
- Better audit logs for Move Central and reactivation

### Later

- More multi-region operator tools
- More panel automation around client lifecycle
- Other platforms or stores if there is demand

---

## Out of scope for now

- A consumer VPN client for end users
- Saying Google Play or macOS already shipped
- Writing up features that are not in the current Windows or Android source

---

## Related

- [README.md](../README.md)
- [WHITEPAPER.en.md](WHITEPAPER.en.md)
- [ROADMAP.fa.md](ROADMAP.fa.md) · [ROADMAP.ru.md](ROADMAP.ru.md) · [ROADMAP.zh.md](ROADMAP.zh.md)

© Black Fox Security Team
