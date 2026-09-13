<p align="center">
  <img src="docs/assets/logo.jpg" alt="Black Fox VPN Logo" width="96">
</p>

<h1 align="center">VPS to VPN</h1>

<p align="center">
  <strong>Server Installer &amp; Manager · Black Fox Group</strong><br>
  Windows desktop console · 3X-UI (Sanaei) · Xray reverse mesh paths
</p>

<p align="center">
  <a href="#english">English</a> ·
  <a href="#فارسی">فارسی</a> ·
  <a href="#русский">Русский</a> ·
  <a href="#中文">中文</a> ·
  <a href="https://foxnext.net">Website</a> ·
  <a href="https://t.me/blackFoxVPNN">Telegram</a> ·
  <a href="https://github.com/BlackFoxGroup/VPS-to-VPN">GitHub</a>
</p>

---

<a id="english"></a>

# English

## What this product is

VPS to VPN (Black Fox Group) is a Windows operations console for multi-server VPN setups.

You use it to:

- Add Central, Tunnel, Exit, and Node hosts over SSH
- Install 3X-UI (Sanaei) and run Configure Panel
- Keep mesh paths up across nine link types (eight Xray-based, WireGuard last) with automatic failover
- Change link type, apply Watchdog, and run Link Monitor from Server Connection Manager
- Run Basic or Pro licensing
- Move Central, work with domain/CDN helpers, bots, and license reactivation

It is aimed at operators who want several egress locations and do not want to do every Linux step by hand.

### Current releases

| Platform | Product | Status | Download |
|----------|---------|--------|----------|
| Windows | VPS to VPN v3.1.1 installer | Available | [Setup.zip (GitHub)](https://github.com/BlackFoxGroup/VPS-to-VPN/releases/latest/download/VPS-to-VPN-Setup.zip) · [foxnext.net](https://foxnext.net/downloads/VPS%20to%20VPN-Setup.exe) |
| Windows | VPS to VPN portable | Available | [Portable.zip (GitHub)](https://github.com/BlackFoxGroup/VPS-to-VPN/releases/latest/download/VPS.to.VPN-Portable.zip) |
| Android | VPS to VPN Android (arm64) | Available | [APK (GitHub)](https://github.com/BlackFoxGroup/VPS-to-VPN/releases/latest/download/VPS-to-VPN-Android-arm64-v8a-release.apk) · [foxnext.net](https://foxnext.net/downloads/VPS%20to%20VPN%20Android.apk) |
| Android | Black Fox Config Builder | Available | [APK](https://foxnext.net/downloads/Black-Fox-Config-Builder.apk) |
| Android | Google Play | Coming soon | — |
| macOS | VPS to VPN | Coming soon | — |

Release files on GitHub: [BlackFoxGroup/VPS-to-VPN/releases](https://github.com/BlackFoxGroup/VPS-to-VPN/releases)

---

## Main capabilities

### Deploy and operate servers

- Connect SSH, Full Deploy, host preparation
- Install and harden 3X-UI on Central
- Add Exit, Tunnel, and Node chain slots (Pro)
- Configure Panel with multi-protocol client inbounds
- Test Client with share links after configure
- Refresh or repair mesh paths and topology status

### Mesh link types (9)

WireGuard, GRE, and QUIC are no longer the first mesh transports. Active path IDs:

| # | ID | Role |
|---|----|------|
| 1 | `xray_reverse_bridge` | Primary reverse bridge (SDN-style) |
| 2 | `xray_reverse_portal` | Reverse portal (Lattix-style) |
| 3 | `l2_vless_waterwall` | L2 + VLESS + WaterWall |
| 4 | `xray_federation` | Bridge and portal federation |
| 5 | `reverse_stealth_wss` | Stealth-WSS reverse tunnel |
| 6 | `ssh_protected_backup` | SSH backup path |
| 7 | `obfuscated_overlay` | Obfuscated overlay |
| 8 | `vxlan_overlay` | VXLAN overlay |
| 9 | `wireguard` | Site-to-site WireGuard (UDP; last in picker) |

Failover order: bridge, portal, stealth-wss, ssh, obfuscated, vxlan.  
WireGuard fallback: SSH.

If any live path is up, the topology link line stays green. Server-square health is a separate signal.

### Server Connection Manager (Pro)

One Mesh tab:

1. Select linked servers once
2. Change Link Type
3. Apply Watchdog (Link Monitor agents on both ends)
4. Install backup paths, Optimize VPS, or Link Monitor

The same tab has Topology, Mesh Links status, and the Active Link Monitor list.

### Configure Panel

- Link strategy per server (no global xray/WG mode picker)
- Client protocols: VLESS, Trojan, VMess, Shadowsocks (roles depend on link type)
- Opens Test Client with collected share links

### Modes

| Mode | Focus |
|------|--------|
| Basic | Central plus a limited set of Exit slots |
| Pro | Full chain (Tunnel/Node), Mesh Manager, Domain/CDN on Windows, Move Central |

### Other features

- Move Central Server while keeping panel clients
- License Reactivation on the same device fingerprint
- Dual update hosts (`foxnext.net` and `blackfoxupdate.ir`)
- UI in 10 languages
- Black Fox Config Builder (Android) for panel config creation

---

## Architecture

```text
Clients → Central (3X-UI)
              ↓  mesh path (bridge / portal / …)
         Tunnel (optional)
              ↓
           Exit / Node
              ↓
         Internet egress
```

---

## Languages

English, Persian, Russian, Chinese, German, Uzbek, Turkish, Indonesian, Ukrainian, Hindi.

---

## Privacy and support

- Privacy EN: https://foxnext.net/en/privacy.html
- Privacy FA: https://foxnext.net/fa/privacy.html
- Telegram: https://t.me/blackFoxVPNN
- Email: support@foxnext.net

Basic and Pro licenses are sold through registration on [foxnext.net](https://foxnext.net).

Public docs repo: [BlackFoxGroup/VPS-to-VPN](https://github.com/BlackFoxGroup/VPS-to-VPN)

Roadmap / whitepaper:

- [docs/ROADMAP.en.md](docs/ROADMAP.en.md) · [docs/WHITEPAPER.en.md](docs/WHITEPAPER.en.md)
- [docs/ROADMAP.fa.md](docs/ROADMAP.fa.md) · [docs/WHITEPAPER.fa.md](docs/WHITEPAPER.fa.md)
- [docs/ROADMAP.ru.md](docs/ROADMAP.ru.md) · [docs/WHITEPAPER.ru.md](docs/WHITEPAPER.ru.md)
- [docs/ROADMAP.zh.md](docs/ROADMAP.zh.md) · [docs/WHITEPAPER.zh.md](docs/WHITEPAPER.zh.md)

---

<a id="فارسی"></a>

# فارسی

## این محصول چیست؟

محصول VPS to VPN (گروه Black Fox) یک کنسول عملیات ویندوز برای زیرساخت VPN چندسروری است.

با آن می‌توانید:

- سرورهای Central، Tunnel، Exit و Node را از SSH اضافه کنید
- پنل 3X-UI (سنایی) را نصب کنید و Configure Panel را اجرا کنید
- نه نوع مسیر مش را نگه دارید (هشت مسیر روی Xray، WireGuard آخر) با failover خودکار
- نوع لینک، Watchdog و Link Monitor را از Server Connection Manager عوض کنید
- لایسنس Basic یا Pro بگیرید
- Central را جابه‌جا کنید، دامنه و CDN را بزنید، ربات‌ها را وصل کنید و لایسنس را دوباره فعال کنید

برای کسی است که چند خروجی جغرافیایی می‌خواهد و نمی‌خواهد هر کار لینوکس را دستی تکرار کند.

### وضعیت انتشار

| پلتفرم | محصول | وضعیت | دانلود |
|--------|--------|--------|--------|
| ویندوز | نصب‌کننده VPS to VPN نسخه ۳٫۱٫۱ | منتشر شده | [Setup.zip در گیت‌هاب](https://github.com/BlackFoxGroup/VPS-to-VPN/releases/latest/download/VPS-to-VPN-Setup.zip) · [foxnext.net](https://foxnext.net/downloads/VPS%20to%20VPN-Setup.exe) |
| ویندوز | نسخه قابل‌حمل | منتشر شده | [Portable.zip در گیت‌هاب](https://github.com/BlackFoxGroup/VPS-to-VPN/releases/latest/download/VPS.to.VPN-Portable.zip) |
| اندروید | VPS to VPN Android (arm64) | منتشر شده | [APK در گیت‌هاب](https://github.com/BlackFoxGroup/VPS-to-VPN/releases/latest/download/VPS-to-VPN-Android-arm64-v8a-release.apk) · [foxnext.net](https://foxnext.net/downloads/VPS%20to%20VPN%20Android.apk) |
| اندروید | Black Fox Config Builder | منتشر شده | [APK](https://foxnext.net/downloads/Black-Fox-Config-Builder.apk) |
| اندروید | Google Play | به‌زودی | — |
| مک | VPS to VPN | به‌زودی | — |

فایل‌های انتشار در گیت‌هاب: [BlackFoxGroup/VPS-to-VPN/releases](https://github.com/BlackFoxGroup/VPS-to-VPN/releases)

---

## امکانات اصلی

### استقرار و عملیات سرور

- اتصال SSH، Full Deploy، آماده‌سازی میزبان
- نصب و سخت‌سازی 3X-UI روی Central
- افزودن اسلات Exit، Tunnel و Node (Pro)
- Configure Panel با inbound چندپروتکلی کلاینت
- Test Client با لینک‌های اشتراکی بعد از پیکربندی
- تازه‌کردن یا تعمیر مسیر مش و وضعیت Topology

### انواع لینک مش (۹ نوع)

دیگر WireGuard و GRE و QUIC مسیر اول مش نیستند. شناسه‌های فعال:

| # | شناسه | نقش |
|---|--------|-----|
| ۱ | `xray_reverse_bridge` | مسیر اصلی reverse bridge |
| ۲ | `xray_reverse_portal` | reverse portal |
| ۳ | `l2_vless_waterwall` | L2 + VLESS + WaterWall |
| ۴ | `xray_federation` | فدراسیون bridge و portal |
| ۵ | `reverse_stealth_wss` | Reverse Tunnel Stealth-WSS |
| ۶ | `ssh_protected_backup` | مسیر پشتیبان SSH |
| ۷ | `obfuscated_overlay` | Overlay مبهم‌سازی‌شده |
| ۸ | `vxlan_overlay` | Overlay با VXLAN |
| ۹ | `wireguard` | WireGuard سایت‌به‌سایت (آخر لیست) |

ترتیب failover: bridge، portal، stealth-wss، ssh، obfuscated، vxlan.  
پشتیبان WireGuard: SSH.

اگر هر مسیر زنده‌ای بالا باشد خط Topology سبز می‌ماند. سلامت مربع سرور جداست.

### Server Connection Manager (Pro)

یک تب مش:

1. یک‌بار سرورهای متصل را انتخاب کنید
2. Change Link Type
3. Apply Watchdog (ایجنت Link Monitor روی دو سرور)
4. مسیر پشتیبان، Optimize VPS یا Link Monitor

همان تب Topology، وضعیت Mesh Links و فهرست Active Link Monitor را دارد.

### Configure Panel

- استراتژی لینک برای هر سرور (بدون انتخاب سراسری xray یا WG)
- پروتکل کلاینت: VLESS، Trojan، VMess، Shadowsocks
- باز شدن Test Client با لینک‌های جمع‌آوری‌شده

### حالت‌ها

| حالت | تمرکز |
|------|--------|
| Basic | Central و تعداد محدود Exit |
| Pro | زنجیره کامل، Mesh Manager، Domain/CDN روی ویندوز، Move Central |

### سایر امکانات

- انتقال Central با حفظ کلاینت‌های پنل
- فعال‌سازی مجدد لایسنس روی همان اثر انگشت دستگاه
- دو میزبان آپدیت (`foxnext.net` و `blackfoxupdate.ir`)
- رابط به ۱۰ زبان
- ابزار Black Fox Config Builder روی اندروید

---

## معماری

```text
کلاینت‌ها → Central (3X-UI)
                 ↓  مسیر مش (bridge / portal / …)
            Tunnel (اختیاری)
                 ↓
              Exit / Node
                 ↓
            خروجی اینترنت
```

---

## زبان‌ها

انگلیسی، فارسی، روسی، چینی، آلمانی، ازبکی، ترکی، اندونزیایی، اوکراینی، هندی.

---

## حریم خصوصی و پشتیبانی

- حریم خصوصی فارسی: https://foxnext.net/fa/privacy.html
- حریم خصوصی انگلیسی: https://foxnext.net/en/privacy.html
- تلگرام: https://t.me/blackFoxVPNN
- ایمیل: support@foxnext.net

لایسنس Basic و Pro از ثبت‌نام در [foxnext.net](https://foxnext.net) فروخته می‌شود.

ریپوی عمومی اسناد: [BlackFoxGroup/VPS-to-VPN](https://github.com/BlackFoxGroup/VPS-to-VPN)

نقشه راه و وایت‌پیپر: [docs/ROADMAP.fa.md](docs/ROADMAP.fa.md) · [docs/WHITEPAPER.fa.md](docs/WHITEPAPER.fa.md)

---

<a id="русский"></a>

# Русский

## Что это

VPS to VPN (Black Fox Group) — консоль для Windows, которой поднимают и ведут VPN на нескольких серверах.

С ней можно:

- добавить Central, Tunnel, Exit и Node по SSH
- поставить 3X-UI (Sanaei) и пройти Configure Panel
- держать mesh из девяти типов пути (восемь на Xray, WireGuard в конце списка) с автоматическим failover
- менять тип линка, включать Watchdog и Link Monitor в Server Connection Manager
- работать в Basic или Pro
- переносить Central, настраивать домен и CDN, ботов и повторную активацию лицензии

Рассчитана на операторов, которым нужны несколько точек выхода и которые не хотят каждый шаг в Linux делать вручную.

### Текущие сборки

| Платформа | Продукт | Статус | Скачать |
|-----------|---------|--------|---------|
| Windows | установщик VPS to VPN v3.1.1 | доступен | [Setup.zip (GitHub)](https://github.com/BlackFoxGroup/VPS-to-VPN/releases/latest/download/VPS-to-VPN-Setup.zip) · [foxnext.net](https://foxnext.net/downloads/VPS%20to%20VPN-Setup.exe) |
| Windows | portable | доступен | [Portable.zip (GitHub)](https://github.com/BlackFoxGroup/VPS-to-VPN/releases/latest/download/VPS.to.VPN-Portable.zip) |
| Android | VPS to VPN Android (arm64) | доступен | [APK (GitHub)](https://github.com/BlackFoxGroup/VPS-to-VPN/releases/latest/download/VPS-to-VPN-Android-arm64-v8a-release.apk) · [foxnext.net](https://foxnext.net/downloads/VPS%20to%20VPN%20Android.apk) |
| Android | Black Fox Config Builder | доступен | [APK](https://foxnext.net/downloads/Black-Fox-Config-Builder.apk) |
| Android | Google Play | скоро | — |
| macOS | VPS to VPN | скоро | — |

Файлы релизов: [BlackFoxGroup/VPS-to-VPN/releases](https://github.com/BlackFoxGroup/VPS-to-VPN/releases)

Документы: [docs/ROADMAP.ru.md](docs/ROADMAP.ru.md) · [docs/WHITEPAPER.ru.md](docs/WHITEPAPER.ru.md)

---

<a id="中文"></a>

# 中文

## 这是什么

VPS to VPN（Black Fox Group）是一套 Windows 运维控制台，用来部署和管理多台 VPN 服务器。

可以做这些事：

- 通过 SSH 添加 Central、Tunnel、Exit、Node
- 安装 3X-UI（Sanaei）并做 Configure Panel
- 维护九种 mesh 路径（八种基于 Xray，WireGuard 排在最后），并自动 failover
- 在 Server Connection Manager 里改链路类型、加 Watchdog 和 Link Monitor
- 使用 Basic 或 Pro 许可
- 迁移 Central、处理域名/CDN、机器人和许可重新激活

面向需要多出口、又不想把每一步 Linux 都手搓一遍的运维。

### 当前版本

| 平台 | 产品 | 状态 | 下载 |
|------|------|------|------|
| Windows | VPS to VPN v3.1.1 安装包 | 已发布 | [Setup.zip（GitHub）](https://github.com/BlackFoxGroup/VPS-to-VPN/releases/latest/download/VPS-to-VPN-Setup.zip) · [foxnext.net](https://foxnext.net/downloads/VPS%20to%20VPN-Setup.exe) |
| Windows | 便携版 | 已发布 | [Portable.zip（GitHub）](https://github.com/BlackFoxGroup/VPS-to-VPN/releases/latest/download/VPS.to.VPN-Portable.zip) |
| Android | VPS to VPN Android（arm64） | 已发布 | [APK（GitHub）](https://github.com/BlackFoxGroup/VPS-to-VPN/releases/latest/download/VPS-to-VPN-Android-arm64-v8a-release.apk) · [foxnext.net](https://foxnext.net/downloads/VPS%20to%20VPN%20Android.apk) |
| Android | Black Fox Config Builder | 已发布 | [APK](https://foxnext.net/downloads/Black-Fox-Config-Builder.apk) |
| Android | Google Play | 即将上线 | — |
| macOS | VPS to VPN | 即将上线 | — |

发布页：[BlackFoxGroup/VPS-to-VPN/releases](https://github.com/BlackFoxGroup/VPS-to-VPN/releases)

文档：[docs/ROADMAP.zh.md](docs/ROADMAP.zh.md) · [docs/WHITEPAPER.zh.md](docs/WHITEPAPER.zh.md)
