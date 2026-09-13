# نقشه راه VPS to VPN

**آخرین به‌روزرسانی:** ۱۳ سپتامبر ۲۰۲۶  
**محصول:** VPS to VPN  
**نسخه فعلی:** ویندوز v3.1.1 (Build 213). اندروید و Config Builder از `version.json` روی میزبان آپدیت می‌آیند.  
**وب‌سایت:** [https://foxnext.net](https://foxnext.net)  
**گیت‌هاب عمومی:** [BlackFoxGroup/VPS-to-VPN](https://github.com/BlackFoxGroup/VPS-to-VPN)

این فهرست کار تمام‌شده، کار جاری و کار برنامه‌ریزی‌شده را نشان می‌دهد. مبنا کد Go ویندوز، سایت و سرویس لایسنس است. شماره نسخه اندروید را اینجا عوض نمی‌کنیم مگر در یادداشت انتشار گفته شود.

---

## دانلودها

| محصول | فایل | گیت‌هاب | سایت |
|--------|------|---------|------|
| نصب‌کننده ویندوز | `VPS-to-VPN-Setup.zip` | [دانلود](https://github.com/BlackFoxGroup/VPS-to-VPN/releases/latest/download/VPS-to-VPN-Setup.zip) | [foxnext.net](https://foxnext.net/downloads/VPS%20to%20VPN-Setup.exe) |
| نسخه قابل‌حمل ویندوز | `VPS to VPN-Portable.zip` | [دانلود](https://github.com/BlackFoxGroup/VPS-to-VPN/releases/latest/download/VPS.to.VPN-Portable.zip) | — |
| اندروید arm64 | `VPS-to-VPN-Android-arm64-v8a-release.apk` | [دانلود](https://github.com/BlackFoxGroup/VPS-to-VPN/releases/latest/download/VPS-to-VPN-Android-arm64-v8a-release.apk) | [foxnext.net](https://foxnext.net/downloads/VPS%20to%20VPN%20Android.apk) |
| Black Fox Config Builder | `Black-Fox-Config-Builder.apk` | — | [foxnext.net](https://foxnext.net/downloads/Black-Fox-Config-Builder.apk) |

Google Play برای اندروید: به‌زودی.  
نسخه macOS: به‌زودی.

---

## انجام‌شده

### پلتفرم و انتشار

- نصب‌کننده و کنسول ویندوز: VPS to VPN نسخه 3.1.1 Build 213
- اپ عملیات اندروید
- ابزار همراه Config Builder نسخه 1.1.3 Build 7
- سایت و دو میزبان آپدیت (`foxnext.net`، `blackfoxupdate.ir`)
- صفحات حریم خصوصی فارسی و انگلیسی
- اسناد و باینری عمومی روی [BlackFoxGroup/VPS-to-VPN](https://github.com/BlackFoxGroup/VPS-to-VPN)

### عملیات اصلی (ویندوز و اندروید)

- حالت Basic و Pro
- لایسنس AI Assistant Pro و ایجنت هوش مصنوعی گروه Black Fox در چت (قبل از تغییر سرور تأیید می‌گیرد)
- راه‌اندازی Central، Connect SSH، Full Deploy
- Tunnel Server در Pro
- Exit Server (Basic: دو اسلات؛ Pro: تا شش)
- نه نوع مسیر مش با failover خودکار
- ابزار Configure Panel
- نصب WireGuard و 3X-UI

### امکانات Pro

- DNS دامنه و ساب‌دامین (Cloudflare، ArvanCloud)
- CDN روی Pro ویندوز (ArvanCloud، Cloudflare، KeyCDN، Other)
- Move Central روی ویندوز و اندروید: وصل دوباره تونل و خروجی، برگرداندن کلاینت 3X-UI از snapshot، بکاپ محلی مهاجرت

### لایسنس

- تأیید پرداخت آنلاین (TX Hash / USDT)
- کد آفلاین
- فعال‌سازی مجدد در صفحه ثبت‌نام بعد از حذف و نصب روی همان دستگاه (اثر انگشت ماشین)

### Config Builder

شش تب، ساخت تکی و گروهی، حذف از پنل یا لیست، آپدیت دو سرور، نیاز به 3X-UI 3.3.0 به بالا و API 24.  
مستندات: [BlackFoxGroup/blackfox-config-builder](https://github.com/BlackFoxGroup/blackfox-config-builder)

### بومی‌سازی

ده زبان: انگلیسی، فارسی، روسی، چینی، آلمانی، ازبکی، ترکی، اندونزیایی، اوکراینی، هندی.

### اسناد

README، ROADMAP و WHITEPAPER به انگلیسی، فارسی، روسی و چینی.

---

## در حال انجام

- نزدیک‌کردن رفتار اندروید و ویندوز در جریان‌های طولانی یا حاشیه‌ای
- UI واضح‌تر هنگام Deploy و Move
- پایداری SSH، همگام‌سازی پنل و چک آپدیت
- هم‌خوانی متن سایت با رفتار واقعی برنامه
- کم کردن فاصله ابزار CDN ویندوز و دامنه Pro اندروید

---

## برنامه‌ریزی‌شده

### کوتاه‌مدت

- فهرست Google Play
- Backup و Restore جدا از snapshot مهاجرت
- ازسرگیری استقرار قطع‌شده
- پیام خطای واضح‌تر برای اپراتور

### میان‌مدت

- نسخه macOS
- پرداخت بیشتر جریان CDN روی ویندوز
- ارائه‌دهنده DNS/CDN بیشتر اگر تقاضا باشد
- لاگ ممیزی بهتر برای Move Central و فعال‌سازی مجدد

### بعدتر

- ابزار اپراتوری چندمنطقه‌ای بیشتر
- اتوماسیون بیشتر چرخه کلاینت پنل
- پلتفرم یا استور دیگر اگر تقاضا باشد

---

## فعلاً در هدف نیست

- کلاینت VPN مصرفی برای کاربر نهایی
- گفتن اینکه Google Play یا macOS منتشر شده
- نوشتن امکاناتی که در سورس فعلی نیست

---

## اسناد مرتبط

- [README.md](../README.md)
- [WHITEPAPER.fa.md](WHITEPAPER.fa.md)
- [ROADMAP.en.md](ROADMAP.en.md) · [ROADMAP.ru.md](ROADMAP.ru.md) · [ROADMAP.zh.md](ROADMAP.zh.md)

© Black Fox Security Team
