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

Black Fox Group is the company that makes VPS to VPN. Official website: https://foxnext.net

VPS to VPN runs on Windows and Android. You connect to a VPS, install the 3X-UI Sanaei panel without Linux knowledge, and build a multi-location VPN.

Official downloads: https://foxnext.net/en/download.html

## What this product is

VPS to VPN (Black Fox Group) is a Windows operations console for multi-server VPN setups.

You use it to:

- Add Central, Tunnel, Exit, and Node hosts over SSH
- Install 3X-UI (Sanaei) and run Configure Panel
- Keep mesh paths up across nine link types (eight Xray-based, WireGuard last) with automatic failover
- Change link type, apply Watchdog, and run Link Monitor from Server Connection Manager
- Run Basic or Pro licensing
- Move Central, work with domain/CDN helpers, bots, and license reactivation
- Activate AI Assistant Pro and hand those jobs to the Black Fox Group AI agent in chat

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
| AI Assistant Pro | In-app Black Fox Group agent: you ask in chat and confirm before a server change |

### Other features

- Move Central Server while keeping panel clients
- License Reactivation on the same device fingerprint
- Dual update hosts (`foxnext.net` and `blackfoxupdate.ir`)
- UI in 10 languages
- Black Fox Config Builder (Android) for panel config creation

### AI Assistant Pro

AI Assistant Pro is a Black Fox Group license inside the app. After you activate it, you can leave most console work to the in-app AI agent: add Central, Tunnel, Exit, or Node, install 3X-UI, mesh, domain and CDN, diagnose and repair, and other tasks the program already does. You type the request in chat (or attach a note or photo). The agent confirms before it changes a server.

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

Basic, Pro, and AI Assistant Pro licenses are sold through registration on [foxnext.net](https://foxnext.net).

Public docs repo: [BlackFoxGroup/VPS-to-VPN](https://github.com/BlackFoxGroup/VPS-to-VPN)

Roadmap / whitepaper:

- [docs/ROADMAP.en.md](docs/ROADMAP.en.md) · [docs/WHITEPAPER.en.md](docs/WHITEPAPER.en.md)
- [docs/ROADMAP.fa.md](docs/ROADMAP.fa.md) · [docs/WHITEPAPER.fa.md](docs/WHITEPAPER.fa.md)
- [docs/ROADMAP.ru.md](docs/ROADMAP.ru.md) · [docs/WHITEPAPER.ru.md](docs/WHITEPAPER.ru.md)
- [docs/ROADMAP.zh.md](docs/ROADMAP.zh.md) · [docs/WHITEPAPER.zh.md](docs/WHITEPAPER.zh.md)

---

<a id="فارسی"></a>

# فارسی

شرکت Black Fox Group سازنده محصول VPS to VPN است. وب‌سایت رسمی: https://foxnext.net

برنامه روی ویندوز و اندروید اجرا می‌شود. به سرور VPS وصل می‌شوید، پنل 3X-UI سنایی را بدون دانش لینوکس نصب می‌کنید و یک VPN چندلوکیشن می‌سازید.

دانلود رسمی: https://foxnext.net/en/download.html

## این محصول چیست؟

محصول VPS to VPN (گروه Black Fox) یک کنسول عملیات ویندوز برای زیرساخت VPN چندسروری است.

با آن می‌توانید:

- سرورهای Central، Tunnel، Exit و Node را از SSH اضافه کنید
- پنل 3X-UI (سنایی) را نصب کنید و Configure Panel را اجرا کنید
- نه نوع مسیر مش را نگه دارید (هشت مسیر روی Xray، WireGuard آخر) با failover خودکار
- نوع لینک، Watchdog و Link Monitor را از Server Connection Manager عوض کنید
- لایسنس Basic یا Pro بگیرید
- Central را جابه‌جا کنید، دامنه و CDN را بزنید، ربات‌ها را وصل کنید و لایسنس را دوباره فعال کنید
- لایسنس AI Assistant Pro را فعال کنید و همان کارها را به ایجنت هوش مصنوعی گروه Black Fox در چت بسپارید

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
| AI Assistant Pro | ایجنت گروه Black Fox در چت؛ قبل از تغییر سرور تأیید می‌گیرد |

### سایر امکانات

- انتقال Central با حفظ کلاینت‌های پنل
- فعال‌سازی مجدد لایسنس روی همان اثر انگشت دستگاه
- دو میزبان آپدیت (`foxnext.net` و `blackfoxupdate.ir`)
- رابط به ۱۰ زبان
- ابزار Black Fox Config Builder روی اندروید

### AI Assistant Pro

لایسنس AI Assistant Pro داخل برنامه است. بعد از فعال‌سازی می‌توانید بیشتر کار کنسول را به ایجنت هوش مصنوعی گروه Black Fox بسپارید: افزودن Central، Tunnel، Exit یا Node، نصب 3X-UI، مش، دامنه و CDN، تشخیص و تعمیر، و بقیه کارهایی که خود برنامه بلد است. درخواست را در چت می‌نویسید (یا فایل و عکس می‌فرستید). قبل از تغییر سرور ایجنت تأیید می‌گیرد.

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

لایسنس Basic، Pro و AI Assistant Pro از ثبت‌نام در [foxnext.net](https://foxnext.net) فروخته می‌شود.

ریپوی عمومی اسناد: [BlackFoxGroup/VPS-to-VPN](https://github.com/BlackFoxGroup/VPS-to-VPN)

نقشه راه و وایت‌پیپر: [docs/ROADMAP.fa.md](docs/ROADMAP.fa.md) · [docs/WHITEPAPER.fa.md](docs/WHITEPAPER.fa.md)

---

<a id="русский"></a>

# Русский

Компания Black Fox Group выпускает VPS to VPN. Официальный сайт: https://foxnext.net

Программа работает на Windows и Android. Вы подключаетесь к VPS, ставите панель 3X-UI Sanaei без знания Linux и собираете VPN в нескольких локациях.

Официальные загрузки: https://foxnext.net/en/download.html

## Что это

VPS to VPN (Black Fox Group) — консоль для Windows, которой поднимают и ведут VPN на нескольких серверах.

С ней можно:

- добавить Central, Tunnel, Exit и Node по SSH
- поставить 3X-UI (Sanaei) и пройти Configure Panel
- держать mesh из девяти типов пути (восемь на Xray, WireGuard в конце списка) с автоматическим failover
- менять тип линка, включать Watchdog и Link Monitor в Server Connection Manager
- работать в Basic или Pro
- переносить Central, настраивать домен и CDN, ботов и повторную активацию лицензии
- включить AI Assistant Pro и поручить эти задачи ИИ-агенту Black Fox Group в чате

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

---

## Основные возможности

### Развёртывание и работа с серверами

- Connect SSH, Full Deploy, подготовка хоста
- Установка и усиление 3X-UI на Central
- Слоты Exit, Tunnel и Node (Pro)
- Configure Panel с несколькими клиентскими inbound
- Test Client со ссылками после настройки
- Обновление или ремонт mesh и статус Topology

### Типы mesh (9)

WireGuard, GRE и QUIC больше не первые транспорты mesh. Активные ID:

| # | ID | Роль |
|---|----|------|
| 1 | `xray_reverse_bridge` | Основной reverse bridge (в стиле SDN) |
| 2 | `xray_reverse_portal` | Reverse portal (в стиле Lattix) |
| 3 | `l2_vless_waterwall` | L2 + VLESS + WaterWall |
| 4 | `xray_federation` | Федерация bridge и portal |
| 5 | `reverse_stealth_wss` | Reverse-туннель Stealth-WSS |
| 6 | `ssh_protected_backup` | Резервный путь SSH |
| 7 | `obfuscated_overlay` | Обфусцированный overlay |
| 8 | `vxlan_overlay` | Overlay VXLAN |
| 9 | `wireguard` | Site-to-site WireGuard (UDP; в конце списка) |

Порядок failover: bridge, portal, stealth-wss, ssh, obfuscated, vxlan.  
Запасной путь WireGuard: SSH.

Если жив любой путь, линия Topology остаётся зелёной. Здоровье квадрата сервера — отдельный сигнал.

### Server Connection Manager (Pro)

Одна вкладка Mesh:

1. Один раз выбрать связанные серверы
2. Change Link Type
3. Apply Watchdog (агенты Link Monitor на обоих концах)
4. Резервные пути, Optimize VPS или Link Monitor

Там же Topology, статус Mesh Links и список Active Link Monitor.

### Configure Panel

- Стратегия линка на каждый сервер (без общего переключателя xray/WG)
- Клиентские протоколы: VLESS, Trojan, VMess, Shadowsocks (роли зависят от типа линка)
- Открывает Test Client со собранными ссылками

### Режимы

| Режим | Фокус |
|-------|--------|
| Basic | Central и ограниченный набор слотов Exit |
| Pro | Полная цепочка (Tunnel/Node), Mesh Manager, Domain/CDN на Windows, Move Central |
| AI Assistant Pro | ИИ-агент Black Fox Group в чате; перед изменением сервера спрашивает подтверждение |

### Прочее

- Move Central Server с сохранением клиентов панели
- License Reactivation по отпечатку того же устройства
- Два хоста обновлений (`foxnext.net` и `blackfoxupdate.ir`)
- Интерфейс на 10 языках
- Black Fox Config Builder (Android) для конфигов панели

### AI Assistant Pro

AI Assistant Pro — лицензия Black Fox Group внутри приложения. После активации большую часть работы консоли можно отдать ИИ-агенту: добавить Central, Tunnel, Exit или Node, поставить 3X-UI, mesh, домен и CDN, диагностика и ремонт, и другие уже существующие операции. Запрос пишете в чат (или прикладываете файл или фото). Перед изменением сервера агент спрашивает подтверждение.

---

## Архитектура

```text
Клиенты → Central (3X-UI)
              ↓  путь mesh (bridge / portal / …)
         Tunnel (необязательно)
              ↓
           Exit / Node
              ↓
         Выход в интернет
```

---

## Языки

английский, персидский, русский, китайский, немецкий, узбекский, турецкий, индонезийский, украинский, хинди.

---

## Конфиденциальность и поддержка

- Политика EN: https://foxnext.net/en/privacy.html
- Политика FA: https://foxnext.net/fa/privacy.html
- Telegram: https://t.me/blackFoxVPNN
- Почта: support@foxnext.net

Лицензии Basic, Pro и AI Assistant Pro продаются через регистрацию на [foxnext.net](https://foxnext.net).

Публичный репозиторий: [BlackFoxGroup/VPS-to-VPN](https://github.com/BlackFoxGroup/VPS-to-VPN)

Дорожная карта и белая книга: [docs/ROADMAP.ru.md](docs/ROADMAP.ru.md) · [docs/WHITEPAPER.ru.md](docs/WHITEPAPER.ru.md)

---

<a id="中文"></a>

# 中文

Black Fox Group 是开发 VPS to VPN 的公司。官网：https://foxnext.net

程序可在 Windows 和 Android 上使用。连上 VPS 后，不必懂 Linux 也能安装 3X-UI Sanaei 面板，并搭好多地点 VPN。

官方下载：https://foxnext.net/en/download.html

## 这是什么

VPS to VPN（Black Fox Group）是一套 Windows 运维控制台，用来部署和管理多台 VPN 服务器。

可以做这些事：

- 通过 SSH 添加 Central、Tunnel、Exit、Node
- 安装 3X-UI（Sanaei）并做 Configure Panel
- 维护九种 mesh 路径（八种基于 Xray，WireGuard 排在最后），并自动 failover
- 在 Server Connection Manager 里改链路类型、加 Watchdog 和 Link Monitor
- 使用 Basic 或 Pro 许可
- 迁移 Central、处理域名/CDN、机器人和许可重新激活
- 开通 AI Assistant Pro，把这些事交给聊天里的 Black Fox Group 智能体

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

---

## 主要能力

### 部署和运维

- Connect SSH、Full Deploy、主机准备
- 在 Central 上安装并加固 3X-UI
- 添加 Exit、Tunnel、Node 槽位（Pro）
- Configure Panel，多协议客户端 inbound
- 配置完成后用 Test Client 看分享链接
- 刷新或修复 mesh 路径和 Topology 状态

### Mesh 链路类型（9）

WireGuard、GRE、QUIC 已不再是首选 mesh 传输。当前路径 ID：

| # | ID | 作用 |
|---|----|------|
| 1 | `xray_reverse_bridge` | 主 reverse bridge（SDN 风格） |
| 2 | `xray_reverse_portal` | Reverse portal（Lattix 风格） |
| 3 | `l2_vless_waterwall` | L2 + VLESS + WaterWall |
| 4 | `xray_federation` | bridge 与 portal 联邦 |
| 5 | `reverse_stealth_wss` | Stealth-WSS 反向隧道 |
| 6 | `ssh_protected_backup` | SSH 备用路径 |
| 7 | `obfuscated_overlay` | 混淆 overlay |
| 8 | `vxlan_overlay` | VXLAN overlay |
| 9 | `wireguard` | 站点间 WireGuard（UDP；列表最后） |

故障切换顺序：bridge、portal、stealth-wss、ssh、obfuscated、vxlan。  
WireGuard 的后备是 SSH。

只要有一条活路径，Topology 连线保持绿色。服务器方块的健康是另一套信号。

### Server Connection Manager（Pro）

一个 Mesh 页：

1. 先选好已连接的服务器
2. Change Link Type
3. Apply Watchdog（两端的 Link Monitor 代理）
4. 备用路径、Optimize VPS 或 Link Monitor

同一页还有 Topology、Mesh Links 状态和 Active Link Monitor 列表。

### Configure Panel

- 每台服务器各自的链路策略（没有全局 xray/WG 开关）
- 客户端协议：VLESS、Trojan、VMess、Shadowsocks（角色随链路类型变化）
- 打开 Test Client 并带上收集到的分享链接

### 模式

| 模式 | 侧重 |
|------|------|
| Basic | Central 和有限的 Exit 槽 |
| Pro | 完整链路（Tunnel/Node）、Mesh Manager、Windows 上的 Domain/CDN、Move Central |
| AI Assistant Pro | 聊天里的 Black Fox Group 智能体；改服务器前先确认 |

### 其他

- Move Central 时保留面板客户
- 同一台设备指纹上的 License Reactivation
- 双更新主机（`foxnext.net` 和 `blackfoxupdate.ir`）
- 界面十种语言
- Android 上的 Black Fox Config Builder，用来做面板配置

### AI Assistant Pro

AI Assistant Pro 是应用内的 Black Fox Group 许可。开通后，可以把控制台里大部分工作交给智能体：添加 Central、Tunnel、Exit、Node，安装 3X-UI，mesh，域名和 CDN，诊断和修复，以及程序本身已有的其他操作。在聊天里写需求（或附上文件、照片）。改服务器前智能体会先确认。

---

## 架构

```text
客户端 → Central (3X-UI)
              ↓  mesh 路径 (bridge / portal / …)
         Tunnel（可选）
              ↓
           Exit / Node
              ↓
         出口上网
```

---

## 语言

英语、波斯语、俄语、中文、德语、乌兹别克语、土耳其语、印尼语、乌克兰语、印地语。

---

## 隐私与支持

- 英文隐私：https://foxnext.net/en/privacy.html
- 波斯文隐私：https://foxnext.net/fa/privacy.html
- Telegram：https://t.me/blackFoxVPNN
- 邮箱：support@foxnext.net

Basic、Pro 和 AI Assistant Pro 许可通过 [foxnext.net](https://foxnext.net) 注册出售。

公开仓库：[BlackFoxGroup/VPS-to-VPN](https://github.com/BlackFoxGroup/VPS-to-VPN)

路线图与白皮书：[docs/ROADMAP.zh.md](docs/ROADMAP.zh.md) · [docs/WHITEPAPER.zh.md](docs/WHITEPAPER.zh.md)
