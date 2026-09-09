# VPS to VPN — Roadmap

**Last updated:** 2026-09-09  
**Product:** VPS to VPN  
**Current releases:** Windows **v3.1.1 (Build 213)** · Android and Config Builder: see hub `version.json` (not updated in this pass)  
**Website:** [https://foxnext.net](https://foxnext.net)

This roadmap describes completed work, active work, and planned work for **VPS to VPN** (Black Fox Group). It is based on the current Windows Go codebase, website, and licensing service behavior. Android version numbers are left unchanged in this document.

---

## Downloads (full product names)

| Product | File | Link |
|---------|------|------|
| VPS to VPN (Windows) | `VPS to VPN-Setup.exe` | [Download](https://foxnext.net/downloads/VPS%20to%20VPN-Setup.exe) |
| VPS to VPN Android | `VPS to VPN Android.apk` | [Download](https://foxnext.net/downloads/VPS%20to%20VPN%20Android.apk) |
| Black Fox Config Builder | `Black-Fox-Config-Builder.apk` | [Download](https://foxnext.net/downloads/Black-Fox-Config-Builder.apk) |

Google Play publication for VPS to VPN Android: **Coming Soon**  
macOS edition: **Coming Soon**

---

## Completed

### Platform & releases

- Windows desktop installer and operations console — **VPS to VPN** v3.1.1 Build 213  
- Android operations app — **VPS to VPN Android** (version not changed in this pass)  
- Companion Android tool — **Black Fox Config Builder** v1.1.3 Build 7  
- Official site + dual update hosts (`foxnext.net`, `blackfoxupdate.ir`)  
- Privacy Policy pages (EN/FA) on foxnext.net  

### Core operations (Windows + Android)

- Basic Mode and Pro Mode  
- Central Server setup / Connect SSH / Full Deploy  
- Tunnel Server management (Pro)  
- Exit Server management (Basic: 2 slots · Pro: up to 6)  
- Nine mesh path types (Xray reverse / overlays + WireGuard last) with automatic failover  
- Configure Panel helpers  
- Core helpers: Install WireGuard / Install 3X-UI  

### Pro advanced features

- Domain / subdomain management with DNS automation (Cloudflare, ArvanCloud)  
- CDN automation on **Windows Pro** (ArvanCloud, Cloudflare, KeyCDN, Other)  
- **Move Central Server on Windows and Android (Pro)**  
  - Reconnects tunnel and exit servers to the new central  
  - Transfers 3X-UI panel clients automatically via snapshot restore  
  - Creates a local migration backup during the move  
- Migration-oriented backup path used by Move Central  

### Licensing

- Online payment verification (TX Hash / USDT)  
- Offline activation codes  
- **License Reactivation** on Registration screen  
  - After uninstall/reinstall on the **same device**, user presses **Reactivation** / **فعال‌سازی مجدد**  
  - App restores activation from the official reactivation service using the device machine fingerprint  
  - Users no longer need to permanently keep license codes only to recover after reinstall on the same device  

### Companion — Black Fox Config Builder

- Android companion **Black Fox Config Builder** v1.1.3 Build 7  
- Download: [Black-Fox-Config-Builder.apk](https://foxnext.net/downloads/Black-Fox-Config-Builder.apk)  
- Docs repo: [BlackFoxGroup/blackfox-config-builder](https://github.com/BlackFoxGroup/blackfox-config-builder)  
- Six tabs: Connection · Single · Bulk · List · Settings · Contact  
- Multi-inbound create (single + bulk)  
- Delete from panel / delete from list  
- Dual-server remote updates (`blackfoxupdate.ir` + `foxnext.net`)  
- Requires 3X-UI **≥ 3.3.0** · Android API 24+ · 10 languages  
- Build 6: dual-server remote feed · Build 7: current published Android release  

### Localization

- **10 languages:** English, Persian, Russian, Chinese, German, Uzbek, Turkish, Indonesian, Ukrainian, Hindi  
- Shared localization coverage across apps and website  

### Documentation & brand surfaces

- README (EN + full FA)  
- ROADMAP (EN + FA)  
- WHITEPAPER (EN + FA)  
- Website guides for Basic / Pro / Registration / Keys / Config Builder  

---

## In Progress

- Further Android ↔ Windows operational parity (UI depth and edge-case flows)  
- UX hardening for long-running deploy / move operations  
- Stability improvements around SSH, panel sync, and update checks  
- Website content synchronization with product behavior  
- Softening remaining differences between Windows CDN tooling and Android Pro scope  

---

## Planned

### Near term

- Google Play listing for **VPS to VPN Android** (Coming Soon → published)  
- Broader standalone Backup / Restore tooling beyond Move Central migration backups  
- Mid-workflow resume / recovery UI for interrupted deployments  
- Expanded operator diagnostics and clearer failure recovery messages  

### Medium term

- macOS edition of VPS to VPN (Coming Soon)  
- Deeper multi-CDN workflow polish on Windows  
- Additional DNS / CDN provider options where demand is clear  
- Stronger audit trails for Move Central and license reactivation events  

### Longer term

- Expanded multi-region operator tooling  
- Deeper panel automation and client lifecycle helpers  
- Additional platforms / packaging channels as demand grows  

---

## Explicit non-goals (for now)

- Turning the suite into a consumer VPN client for end users  
- Claiming Google Play or macOS as already released  
- Documenting features that are not present in current Windows/Android source  

---

## Related documents

- [README.md](../README.md)  
- [WHITEPAPER.en.md](WHITEPAPER.en.md)  
- [WHITEPAPER.fa.md](WHITEPAPER.fa.md)  
- [ROADMAP.fa.md](ROADMAP.fa.md)  
- Config Builder docs: [BlackFoxGroup/blackfox-config-builder](https://github.com/BlackFoxGroup/blackfox-config-builder)  

---

© Black Fox Security Team
