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
  <a href="https://foxnext.net">Website</a> ·
  <a href="https://t.me/blackFoxVPNN">Telegram</a> ·
  <a href="https://github.com/BlackFoxGroup/blackfox-vpn-installer">GitHub</a>
</p>

---

<a id="english"></a>

# English

## What this product is

**VPS to VPN** (Black Fox Group) is **not** a simple VPN client.

It is a Windows operations console that deploys and manages multi-server VPN infrastructure:

- Central / Tunnel / Exit / Node servers over SSH  
- Automated **3X-UI (Sanaei)** install and Configure Panel  
- Mesh links with **nine path types** (eight Xray-based + WireGuard last) and automatic failover  
- **Server Connection Manager** for link type, watchdog, and Link Monitor agents  
- Basic Mode and Pro Mode licensing  
- Move Central, domain/CDN helpers, bots, and license reactivation  

Designed for operators who need multi-location egress without deep Linux expertise.

### Current releases

| Platform | Product | Status | Download |
|----------|---------|--------|----------|
| Windows | **VPS to VPN** v3.1.1 | Available | [Setup.exe](https://foxnext.net/downloads/VPS%20to%20VPN-Setup.exe) |
| Android | **VPS to VPN Android** | Available | [APK](https://foxnext.net/downloads/VPS%20to%20VPN%20Android.apk) |
| Android | **Black Fox Config Builder** | Available | [APK](https://foxnext.net/downloads/Black-Fox-Config-Builder.apk) |
| Android | Google Play | Coming soon | — |
| macOS | Black Fox Vpn | Coming soon | — |

---

## Main capabilities

### Deploy and operate servers

- Connect SSH, Full Deploy, host preparation  
- Install and harden **3X-UI** on Central  
- Add **Exit**, **Tunnel**, and **Node** chain slots (Pro)  
- Configure Panel with multi-protocol client inbounds  
- Test Client with share links after configure  
- Refresh / repair mesh paths and topology status  

### Mesh link types (9)

WireGuard / GRE / QUIC are **no longer** primary mesh transports. Active path IDs:

| # | ID | Role |
|---|----|------|
| 1 | `xray_reverse_bridge` | Primary reverse bridge (SDN-style) |
| 2 | `xray_reverse_portal` | Reverse portal (Lattix-style) |
| 3 | `l2_vless_waterwall` | L2 + VLESS + WaterWall |
| 4 | `xray_federation` | Bridge ↔ portal federation |
| 5 | `reverse_stealth_wss` | Stealth-WSS reverse tunnel |
| 6 | `ssh_protected_backup` | SSH backup path |
| 7 | `obfuscated_overlay` | Obfuscated overlay |
| 8 | `vxlan_overlay` | VXLAN overlay |
| 9 | `wireguard` | Site-to-site WireGuard (UDP; last in picker) |

**Failover order:** bridge → portal → stealth-wss → ssh → obfuscated → vxlan  
(WireGuard fallback: SSH) 

Any live path keeps the topology **link line green** (server square health is separate).

### Server Connection Manager (Pro)

Unified Mesh tab that replaces the old Deploy/Repair split:

1. Select linked servers once  
2. **Change Link Type**  
3. **Apply Watchdog** (Link Monitor agents on both ends)  
4. Install backup paths / Optimize VPS / Link Monitor  

Also includes Topology view, Mesh Links status, and Active Link Monitor list.

### Configure Panel

- Per-server link strategy (no global xray/WG mode picker)  
- Client protocols: **VLESS**, **Trojan**, **VMess**, **Shadowsocks** (roles depend on link type)  
- Opens Test Client with collected share links  

### Modes

| Mode | Focus |
|------|--------|
| **Basic** | Central + limited Exit slots, faster setup |
| **Pro** | Full chain (Tunnel/Node), Mesh Manager, Domain/CDN (Windows), Move Central |

### Other features

- Move Central Server with panel client continuity  
- License Reactivation on the same device fingerprint  
- Dual update hosts (`foxnext.net` + `blackfoxupdate.ir`)  
- Multilingual UI (10 languages)  
- Companion **Black Fox Config Builder** (Android) for panel config creation  

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

## Privacy & support

- Privacy EN: https://foxnext.net/en/privacy.html  
- Privacy FA: https://foxnext.net/fa/privacy.html  
- Telegram: https://t.me/blackFoxVPNN  
- Email: support@foxnext.net  

Commercial licensing (Basic / Pro) is handled through official registration on [foxnext.net](https://foxnext.net).

Roadmap / whitepaper: [docs/ROADMAP.en.md](docs/ROADMAP.en.md) · [docs/WHITEPAPER.en.md](docs/WHITEPAPER.en.md)

---

<a id="فارسی"></a>

# فارسی

## این محصول چیست؟

**VPS to VPN** (گروه Black Fox) یک کلاینت VPN ساده نیست.

یک کنسول عملیات ویندوز است برای استقرار و مدیریت زیرساخت VPN چندسروری:

- سرورهای Central / Tunnel / Exit / Node از طریق SSH  
- نصب و پیکربندی خودکار **3X-UI (سنایی)** و Configure Panel  
- لینک‌های مش با **نه نوع مسیر** (هشت مسیر Xray + WireGuard آخر) و failover خودکار  
- **Server Connection Manager** برای نوع لینک، Watchdog و ایجنت Link Monitor  
- لایسنس Basic و Pro  
- Move Central، دامنه/CDN، ربات‌ها و فعال‌سازی مجدد لایسنس  

مناسب اپراتورهایی که بدون تخصص عمیق لینوکس به خروجی چندلوکیشن نیاز دارند.

### وضعیت انتشار

| پلتفرم | محصول | وضعیت | دانلود |
|--------|--------|--------|--------|
| ویندوز | **VPS to VPN** نسخه ۳٫۱٫۱ | منتشر شده | [Setup.exe](https://foxnext.net/downloads/VPS%20to%20VPN-Setup.exe) |
| اندروید | **VPS to VPN Android** | منتشر شده | [APK](https://foxnext.net/downloads/VPS%20to%20VPN%20Android.apk) |
| اندروید | **Black Fox Config Builder** | منتشر شده | [APK](https://foxnext.net/downloads/Black-Fox-Config-Builder.apk) |
| اندروید | Google Play | به‌زودی | — |
| macOS | Black Fox Vpn | به‌زودی | — |

---

## امکانات اصلی

### استقرار و عملیات سرور

- اتصال SSH، Full Deploy، آماده‌سازی میزبان  
- نصب و سخت‌سازی **3X-UI** روی Central  
- افزودن اسلات‌های **Exit**، **Tunnel** و **Node** (Pro)  
- Configure Panel با inbound چندپروتکلی کلاینت  
- Test Client با لینک‌های اشتراکی بعد از پیکربندی  
- به‌روزرسانی / تعمیر مسیرهای مش و وضعیت Topology  

### انواع لینک مش (۹ نوع)

WireGuard / GRE / QUIC دیگر مسیر اصلی مش نیستند. شناسه‌های فعال:

| # | شناسه | نقش |
|---|--------|-----|
| ۱ | `xray_reverse_bridge` | مسیر اصلی reverse bridge |
| ۲ | `xray_reverse_portal` | reverse portal |
| ۳ | `l2_vless_waterwall` | L2 + VLESS + WaterWall |
| ۴ | `xray_federation` | فدراسیون bridge ↔ portal |
| ۵ | `reverse_stealth_wss` | Reverse Tunnel Stealth-WSS |
| ۶ | `ssh_protected_backup` | مسیر پشتیبان SSH |
| ۷ | `obfuscated_overlay` | Overlay مبهم‌سازی‌شده |
| ۸ | `vxlan_overlay` | Overlay با VXLAN |
| ۹ | `wireguard` | WireGuard سایت‌به‌سایت (آخر لیست) |

**ترتیب failover:** bridge → portal → stealth-wss → ssh → obfuscated → vxlan  
(پشتیبان WireGuard: SSH) 

اگر هر پروتکل زنده‌ای روی مسیر باشد، **خط Topology سبز** می‌ماند (سلامت مربع سرور جداست).

### Server Connection Manager (Pro)

تب یکپارچهٔ مش به‌جای Deploy/Repair قبلی:

1. یک‌بار انتخاب سرورهای متصل  
2. **Change Link Type**  
3. **Apply Watchdog** (ایجنت Link Monitor روی دو سرور)  
4. نصب مسیرهای پشتیبان / Optimize VPS / Link Monitor  

همراه با Topology، وضعیت Mesh Links و فهرست Active Link Monitor.

### Configure Panel

- استراتژی لینک به‌ازای هر سرور (بدون انتخاب سراسری xray/WG)  
- پروتکل‌های کلاینت: **VLESS**، **Trojan**، **VMess**، **Shadowsocks**  
- باز شدن Test Client با لینک‌های جمع‌آوری‌شده  

### حالت‌ها

| حالت | تمرکز |
|------|--------|
| **Basic** | Central + Exit محدود، راه‌اندازی سریع‌تر |
| **Pro** | زنجیره کامل، Mesh Manager، Domain/CDN (ویندوز)، Move Central |

### سایر امکانات

- انتقال Central با حفظ کلاینت‌های پنل  
- فعال‌سازی مجدد لایسنس روی همان اثر انگشت دستگاه  
- دو میزبان آپدیت (`foxnext.net` و `blackfoxupdate.ir`)  
- رابط چندزبانه (۱۰ زبان)  
- ابزار همراه **Black Fox Config Builder** روی اندروید  

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

لایسنس تجاری (Basic / Pro) از طریق ثبت‌نام رسمی در [foxnext.net](https://foxnext.net) انجام می‌شود.

نقشه راه / وایت‌پیپر: [docs/ROADMAP.fa.md](docs/ROADMAP.fa.md) · [docs/WHITEPAPER.fa.md](docs/WHITEPAPER.fa.md)
