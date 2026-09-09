# نقشه راه VPS to VPN

**آخرین به‌روزرسانی:** ۹ سپتامبر ۲۰۲۶  
**محصول:** VPS to VPN  
**نسخه‌های فعلی:** ویندوز **v3.1.1 (Build 213)** · اندروید و Config Builder در این گذر دست نخورده‌اند  
**وب‌سایت:** [https://foxnext.net](https://foxnext.net)

این نقشه راه وضعیت واقعی کارهای انجام‌شده، کارهای در حال پیشرفت و کارهای برنامه‌ریزی‌شده را برای **VPS to VPN** (گروه Black Fox) شرح می‌دهد. مبنای آن کد فعلی Go ویندوز، وب‌سایت رسمی و رفتار سرویس لایسنس است. نسخهٔ اندروید در این گذر عوض نشده است.

---

## دانلودها (با نام کامل محصول)

| محصول | نام فایل | لینک |
|--------|----------|------|
| VPS to VPN (ویندوز) | `VPS to VPN-Setup.exe` | [دانلود](https://foxnext.net/downloads/VPS%20to%20VPN-Setup.exe) |
| VPS to VPN Android | `VPS to VPN Android.apk` | [دانلود](https://foxnext.net/downloads/VPS%20to%20VPN%20Android.apk) |
| Black Fox Config Builder | `Black-Fox-Config-Builder.apk` | [دانلود](https://foxnext.net/downloads/Black-Fox-Config-Builder.apk) |

انتشار VPS to VPN Android در Google Play: **به‌زودی**  
نسخه macOS: **به‌زودی**

---

## انجام‌شده

### پلتفرم و انتشار

- نصب‌کننده و کنسول عملیاتی دسکتاپ ویندوز — **VPS to VPN** نسخه 3.1.1 Build 213  
- اپ عملیاتی اندروید — **VPS to VPN Android** (نسخه در این گذر عوض نشده)  
- ابزار همراه اندروید — **Black Fox Config Builder** نسخه 1.1.3 Build 7  
- وب‌سایت رسمی و دو میزبان آپدیت (`foxnext.net` و `blackfoxupdate.ir`)  
- صفحات سیاست حریم خصوصی فارسی و انگلیسی روی foxnext.net  

### عملیات اصلی (ویندوز و اندروید)

- حالت‌های Basic و Pro  
- راه‌اندازی Central Server / Connect SSH / Full Deploy  
- مدیریت Tunnel Server در Pro  
- مدیریت Exit Server (Basic: دو اسلات · Pro: تا شش خروجی)  
- نه نوع مسیر مش (Xray reverse / overlay به‌علاوه WireGuard در آخر) با failover خودکار  
- ابزارهای Configure Panel  
- کمک‌کننده‌های نصب WireGuard و 3X-UI  

### امکانات پیشرفته Pro

- مدیریت Domain و Subdomain با اتوماسیون DNS (Cloudflare و ArvanCloud)  
- اتوماسیون CDN در **Pro ویندوز** (ArvanCloud، Cloudflare، KeyCDN، Other)  
- **Move Central Server روی ویندوز و اندروید (Pro)**  
  - اتصال مجدد Tunnel Serverها و Exit Serverها به مرکزی جدید  
  - انتقال خودکار کلاینت‌های پنل 3X-UI از طریق snapshot و restore  
  - ساخت بکاپ محلی در مسیر انتقال  
- مسیر بکاپ مهاجرتی که توسط Move Central استفاده می‌شود  

### لایسنس

- تأیید پرداخت آنلاین (TX Hash / USDT)  
- کدهای فعال‌سازی آفلاین  
- **فعال‌سازی مجدد لایسنس** در صفحه ثبت‌نام  
  - پس از حذف و نصب مجدد برنامه روی **همان دستگاه**، کاربر فقط دکمه **فعال‌سازی مجدد (Reactivation)** را می‌زند  
  - برنامه با اثرانگشت دستگاه، سابقه فعال‌سازی را از سرویس رسمی بازیابی می‌کند  
  - دیگر لازم نیست کاربر کد لایسنس را فقط برای بازیابی پس از نصب مجدد روی همان دستگاه دائماً نگهداری کند  

### ابزار همراه — Black Fox Config Builder

- ابزار همراه اندروید **Black Fox Config Builder** نسخه 1.1.3 Build 7  
- دانلود: [Black-Fox-Config-Builder.apk](https://foxnext.net/downloads/Black-Fox-Config-Builder.apk)  
- ریپوی مستندات: [BlackFoxGroup/blackfox-config-builder](https://github.com/BlackFoxGroup/blackfox-config-builder)  
- شش تب: Connection · Single · Bulk · List · Settings · Contact  
- ساخت با انتخاب چند Inbound (تکی و گروهی)  
- حذف از پنل / حذف از لیست  
- آپدیت ریموت دو سرور (`blackfoxupdate.ir` و `foxnext.net`)  
- نیاز به 3X-UI **≥ 3.3.0** · اندروید API 24 به بالا · ۱۰ زبان  
- Build 6: فید ریموت دو سرور · Build 7: نسخه فعلی منتشرشده اندروید  

### بومی‌سازی

- پشتیبانی از **۱۰ زبان:** انگلیسی، فارسی، روسی، چینی، آلمانی، ازبکی، ترکی، اندونزیایی، اوکراینی و هندی  
- پوشش مشترک بومی‌سازی در اپ‌ها و وب‌سایت  

### مستندات و سطوح برند

- README انگلیسی همراه با بخش کامل فارسی  
- ROADMAP انگلیسی و فارسی  
- WHITEPAPER انگلیسی و فارسی  
- راهنماهای وب‌سایت برای Basic / Pro / Registration / Keys / Config Builder  

---

## در حال انجام

- نزدیک‌تر کردن عمق عملیاتی اندروید و ویندوز (جزئیات UI و جریان‌های حاشیه‌ای)  
- سخت‌کردن تجربه کاربری برای عملیات طولانی Deploy و Move  
- بهبود پایداری SSH، همگام‌سازی پنل و بررسی آپدیت  
- همگام‌سازی محتوای وب‌سایت با رفتار واقعی محصول  
- کاهش تفاوت‌های باقی‌مانده بین ابزار CDN ویندوز و دامنه Pro اندروید  

---

## برنامه‌ریزی‌شده

### کوتاه‌مدت

- انتشار رسمی **VPS to VPN Android** در Google Play (از Coming Soon به منتشرشده)  
- ابزار Backup / Restore مستقل‌تر فراتر از بکاپ مهاجرت Move Central  
- رابط ازسرگیری میانی برای استقرارهای قطع‌شده  
- تشخیص‌پذیری بهتر خطا و پیام‌های بازیابی واضح‌تر برای اپراتور  

### میان‌مدت

- نسخه macOS از VPS to VPN (به‌زودی)  
- پرداخت عمیق‌تر جریان‌های چند CDN روی ویندوز  
- افزودن ارائه‌دهنده DNS / CDN بیشتر در صورت تقاضای روشن  
- ردپای ممیزی قوی‌تر برای Move Central و فعال‌سازی مجدد لایسنس  

### بلندمدت

- ابزارهای اپراتوری چندمنطقه‌ای گسترده‌تر  
- اتوماسیون عمیق‌تر پنل و چرخه عمر کلاینت  
- پلتفرم‌ها و کانال‌های بسته‌بندی بیشتر بر اساس تقاضا  

---

## چیزهایی که فعلاً هدف نیستند

- تبدیل این مجموعه به کلاینت VPN مصرفی برای کاربر نهایی  
- ادعای انتشار Google Play یا macOS قبل از آماده بودن واقعی  
- مستند کردن امکاناتی که در سورس فعلی ویندوز/اندروید وجود ندارد  

---

## اسناد مرتبط

- [README.md](../README.md)  
- [WHITEPAPER.fa.md](WHITEPAPER.fa.md)  
- [WHITEPAPER.en.md](WHITEPAPER.en.md)  
- [ROADMAP.en.md](ROADMAP.en.md)  
- مستندات Config Builder: [BlackFoxGroup/blackfox-config-builder](https://github.com/BlackFoxGroup/blackfox-config-builder)  

---

© Black Fox Security Team
