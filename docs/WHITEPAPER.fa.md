# وایت‌پیپر VPS to VPN

**آخرین به‌روزرسانی:** ۱۳ سپتامبر ۲۰۲۶  
**محصول‌ها:** VPS to VPN (ویندوز)، VPS to VPN Android، Black Fox Config Builder  
**نسخه ویندوز:** v3.1.1 (Build 213)  
**وب‌سایت:** [https://foxnext.net](https://foxnext.net)  
**گیت‌هاب عمومی:** [https://github.com/BlackFoxGroup/VPS-to-VPN](https://github.com/BlackFoxGroup/VPS-to-VPN)

---

## ۱. هدف

مجموعه VPS to VPN برای استقرار و عملیات سرور است. اپراتور روی شبکه محدود با آن زیرساخت VPN چندلوکیشن را روی این لایه‌ها بالا می‌آورد:

- پنل 3X-UI (سنایی)
- نه نوع مسیر مش (هشت مسیر Xray، WireGuard آخر) با failover خودکار
- Server Connection Manager برای نوع لینک زنده، Watchdog و Link Monitor

کار تکراری لینوکس، SSH، پنل، DNS و تونل از کار روزانه کم می‌شود.

---

## ۲. سطح محصول

| سطح | نام | نقش | دانلود |
|------|------|-----|--------|
| ویندوز | VPS to VPN | کنسول دسکتاپ | [Setup.exe در گیت‌هاب](https://github.com/BlackFoxGroup/VPS-to-VPN/releases/latest/download/VPS.to.VPN-Setup.exe)، [Portable.zip](https://github.com/BlackFoxGroup/VPS-to-VPN/releases/latest/download/VPS.to.VPN-Portable.zip) |
| اندروید | VPS to VPN Android | عملیات موبایل (Basic و Pro) | [APK در گیت‌هاب](https://github.com/BlackFoxGroup/VPS-to-VPN/releases/latest/download/VPS-to-VPN-Android-arm64-v8a-release.apk) |
| همراه اندروید | Black Fox Config Builder | ساخت کانفیگ کلاینت 3X-UI | [APK](https://foxnext.net/downloads/Black-Fox-Config-Builder.apk) |
| Google Play | VPS to VPN Android | فروشگاه | به‌زودی |
| مک | VPS to VPN | نسخه دسکتاپ بعدی | به‌زودی |

مستندات Config Builder: [BlackFoxGroup/blackfox-config-builder](https://github.com/BlackFoxGroup/blackfox-config-builder)

---

## ۳. مدل کار

### Basic Mode

استقرار کوچک‌تر و سریع‌تر: Central، SSH و Full Deploy، حداکثر دو Exit، کمک پنل، نصب WireGuard و 3X-UI.

### Pro Mode

زنجیره بزرگ‌تر: Central، Tunnel، تا شش Exit، نه نوع مش و failover، دامنه و DNS، CDN روی ویندوز، Move Central روی ویندوز و اندروید، بکاپ مهاجرت.

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

## ۴. انتقال Central

قبلاً جابه‌جایی نقش Central یعنی ساخت دوباره تونل، وصل دوباره Exit و برگرداندن دستی کلاینت پنل بود.

حالا Move Central در Pro روی ویندوز و اندروید این کار را می‌کند:

1. Operations را در Pro باز کنید
2. Move Central Server را بزنید
3. مشخصات Central جدید را بدهید
4. برنامه تونل و خروجی را دوباره وصل کند
5. کلاینت 3X-UI از snapshot مهاجرت برگردد
6. بکاپ محلی همان انتقال را نگه دارید

صفحه‌هایی که این را فقط ویندوز می‌نویسند کهنه است.

---

## ۵. لایسنس و فعال‌سازی مجدد

سه راه:

1. تأیید آنلاین پرداخت / TX Hash
2. کد آفلاین
3. فعال‌سازی مجدد بعد از نصب دوباره روی همان دستگاه

خیلی‌ها برنامه را پاک و دوباره نصب می‌کنند. مجبور کردن به نگهداری همیشگی کد برای همین کار، پشتیبانی را زیاد می‌کند.

در ثبت‌نام:

1. روی همان دستگاه دوباره نصب کنید
2. Registration را باز کنید
3. فعال‌سازی مجدد / Reactivation را بزنید

برنامه اثر انگشت ماشین را به سرویس رسمی می‌فرستد. اگر سابقه معتبر باشد دسترسی برمی‌گردد.

نکته‌ها:

- فقط دستگاهی که سرویس قبلاً ثبت کرده
- TX آنلاین و کد آفلاین سر جایشان هستند
- برگرداندن vault محلی ویندوز، اگر باشد، مکانیزم جداست
- لایسنس جدید ساخته نمی‌شود؛ همان سابقه دستگاه برمی‌گردد

قیمت روی سایت در آخرین بررسی: Basic ۱۹ USDT، Pro ۳۳ USDT. روی سایت چک کنید.

---

## ۶. دامنه، DNS و CDN

در Pro اتوماسیون DNS برای Cloudflare و ArvanCloud هست.

Pro ویندوز CDN هم دارد: ArvanCloud، Cloudflare، KeyCDN، Other.

Pro اندروید روی توپولوژی و Move Central می‌ماند. ابزار عمیق‌تر CDN هنوز روی ویندوز است.

---

## ۷. Black Fox Config Builder

این اپ اندروید کانفیگ کلاینت 3X-UI را روی گوشی می‌سازد. سرور مستقر نمی‌کند. اپراتور اول زیرساخت را با VPS to VPN می‌سازد، بعد Panel Login Info را اینجا می‌چسباند.

نسخه ۱٫۱٫۳ Build 7، بسته `com.blackfoxvpnn.configbuilder`، حداقل API 24، پنل 3X-UI از ۳٫۳٫۰.

تب‌ها: Connection، Single، Bulk، List، Settings، Contact.

Build 6 فید دو سرور را آورد. Build 7 نسخه فعلی اندروید است. ثبت لایسنس Installer داخل این اپ نیست.

---

## ۸. زبان

انگلیسی، فارسی، روسی، چینی، آلمانی، ازبکی، ترکی، اندونزیایی، اوکراینی، هندی.

---

## ۹. حریم خصوصی و آپدیت

- فارسی: [https://foxnext.net/fa/privacy.html](https://foxnext.net/fa/privacy.html)
- انگلیسی: [https://foxnext.net/en/privacy.html](https://foxnext.net/en/privacy.html)
- میزبان آپدیت: `foxnext.net` و `blackfoxupdate.ir`

صفحه منتشرشده حریم خصوصی مرجع است.

---

## ۱۰. حد این سند

این مجموعه کنسول عملیات است. Google Play و macOS هنوز منتشر نشده‌اند. چیزی که در سورس فعلی نیست اینجا به‌عنوان قابلیت آماده نوشته نمی‌شود.

---

## ۱۱. اسناد مرتبط

- [README.md](../README.md)
- [ROADMAP.fa.md](ROADMAP.fa.md)
- [WHITEPAPER.en.md](WHITEPAPER.en.md) · [WHITEPAPER.ru.md](WHITEPAPER.ru.md) · [WHITEPAPER.zh.md](WHITEPAPER.zh.md)

© Black Fox Security Team
