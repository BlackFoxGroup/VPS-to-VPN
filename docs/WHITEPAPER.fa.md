# وایت‌پیپر VPS to VPN

**آخرین به‌روزرسانی:** ۹ سپتامبر ۲۰۲۶  
**خانواده محصول:** VPS to VPN (ویندوز) · VPS to VPN Android · Black Fox Config Builder  
**نسخه‌های فعلی:** ویندوز **v3.1.1 (Build 213)** · اندروید / Config Builder در این گذر دست نخورده‌اند  
**وب‌سایت:** [https://foxnext.net](https://foxnext.net)  
**گیت‌هاب:** [https://github.com/BlackFoxGroup/blackfox-vpn-installer](https://github.com/BlackFoxGroup/blackfox-vpn-installer)

---

## ۱. هدف

VPS to VPN یک **مجموعه استقرار و عملیات سرور** است، نه یک کلاینت VPN مصرفی برای کاربر نهایی.

هدف این مجموعه کمک به اپراتورهایی است که در شبکه‌های محدود کار می‌کنند تا زیرساخت VPN چندلوکیشن را بر پایه این لایه‌ها راه‌اندازی و مدیریت کنند:

- **3X-UI (سنایی)** به‌عنوان لایه پنل  
- **نه نوع مسیر مش** (هشت مسیر Xray + WireGuard در آخر) با failover خودکار  
- **Server Connection Manager** برای نوع لینک زنده، Watchdog و Link Monitor  

هدف محصول این است که بخش بزرگی از کارهای تکراری لینوکس، SSH، پنل، DNS و تونل را از عملیات روزمره حذف کند.

---

## ۲. سطوح محصول

| سطح | نام کامل محصول | نقش | دانلود |
|------|-----------------|-----|--------|
| ویندوز | **VPS to VPN** | کنسول کامل عملیات دسکتاپ | [VPS to VPN-Setup.exe](https://foxnext.net/downloads/VPS%20to%20VPN-Setup.exe) |
| اندروید | **VPS to VPN Android** | اپ عملیاتی موبایل (Basic + Pro) | [VPS to VPN Android.apk](https://foxnext.net/downloads/VPS%20to%20VPN%20Android.apk) |
| ابزار همراه اندروید | **Black Fox Config Builder** | کمک‌کننده ساخت کانفیگ کلاینت روی پنل 3X-UI | [Black-Fox-Config-Builder.apk](https://foxnext.net/downloads/Black-Fox-Config-Builder.apk) |
| Google Play | فهرست VPS to VPN Android | کانال توزیع | **به‌زودی** |
| macOS | VPS to VPN | نسخه دسکتاپ آینده | **به‌زودی** |

مستندات اختصاصی Config Builder: [BlackFoxGroup/blackfox-config-builder](https://github.com/BlackFoxGroup/blackfox-config-builder)

---

## ۳. مدل عملیاتی

### Basic Mode

Basic Mode برای استقرارهای سریع‌تر و کوچک‌تر طراحی شده است:

- راه‌اندازی Central Server  
- اتصال SSH و Full Deploy  
- حداکثر دو Exit Server  
- ابزارهای پیکربندی پنل  
- کمک‌کننده‌های نصب WireGuard و 3X-UI  

### Pro Mode

Pro Mode برای زیرساخت‌های چندپرشی و بزرگ‌تر طراحی شده است:

- Central Server  
- Tunnel Server  
- حداکثر شش Exit Server  
- نه نوع مسیر مش به‌همراه failover  
- مدیریت Domain / DNS  
- اتوماسیون CDN روی ویندوز  
- **Move Central Server روی ویندوز و اندروید**  
- بکاپ مهاجرتی هنگام جابه‌جایی سرور مرکزی  

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

## ۴. انتقال Central Server

جابه‌جایی نقش مرکزی قبلاً یعنی بازسازی دستی تونل‌ها، اتصال مجدد Exitها و بازیابی دستی کلاینت‌های پنل.

**Move Central Server** این جابه‌جایی را در Pro Mode روی **ویندوز و اندروید** خودکار می‌کند.

جریان کار اپراتور:

۱. در Pro Mode بخش Operations را باز کنید  
۲. گزینه Move Central Server را انتخاب کنید  
۳. مشخصات سرور مرکزی جدید را وارد کنید  
۴. اجازه دهید مجموعه، نقش‌های Tunnel و Exit را به مرکزی جدید وصل کند  
۵. انتقال خودکار کلاینت‌های پنل 3X-UI از snapshot مهاجرتی انجام شود  
۶. بکاپ محلی ساخته‌شده در مسیر انتقال را نگه دارید  

این قابلیت روی اندروید هم فعال است و فقط مخصوص ویندوز نیست. هر مستندی که Move Central را فقط ویندوزی معرفی کند، قدیمی است.

---

## ۵. لایسنس و فعال‌سازی مجدد

لایسنس در عمل سه مسیر دارد:

۱. تأیید آنلاین از طریق پرداخت / TX Hash  
۲. کدهای فعال‌سازی آفلاین  
۳. **فعال‌سازی مجدد** پس از نصب مجدد روی همان دستگاه  

### چرا فعال‌سازی مجدد اضافه شد

اپراتورها اغلب برنامه را حذف و دوباره نصب می‌کنند. اجبار به نگهداری دائمی کد آفلاین فقط برای همین حالت رایج، اصطکاک و بار پشتیبانی ایجاد می‌کرد.

### رفتار فعلی فعال‌سازی مجدد

در صفحه ثبت‌نام:

۱. برنامه را روی **همان دستگاه** دوباره نصب کنید  
۲. وارد Registration شوید  
۳. دکمه **فعال‌سازی مجدد (Reactivation)** را بزنید  

برنامه با اثرانگشت دستگاه به سرویس رسمی فعال‌سازی مجدد مراجعه می‌کند. اگر سابقه فعال‌سازی معتبر برای همان دستگاه وجود داشته باشد، دسترسی بازیابی می‌شود و کاربر مجبور نیست برای همین مسیر بازیابی، کد لایسنس را دائماً نگه دارد و دوباره وارد کند.

توضیح‌های مهم:

- فعال‌سازی مجدد برای دستگاهی کار می‌کند که قبلاً فعال شده و رکورد آن در سرویس رسمی ثبت شده باشد  
- مسیرهای TX آنلاین و کد آفلاین همچنان موجودند  
- بازیابی محلی vault در ویندوز (در صورت وجود) مکانیزمی جداگانه روی خود دستگاه است و نباید با فعال‌سازی مجدد سمت سرویس اشتباه گرفته شود  
- فعال‌سازی مجدد لایسنس جدید نمی‌سازد؛ سابقه فعال‌سازی وابسته‌به‌دستگاه را بازیابی می‌کند  

مرجع قیمت فعلی روی وب‌سایت عمومی: Basic **۱۹ USDT** · Pro **۳۳ USDT** (روی سایت تأیید کنید).

---

## ۶. دامنه، DNS و CDN

در Pro Mode مدیریت Domain و Subdomain با اتوماسیون DNS برای این ارائه‌دهنده‌ها وجود دارد:

- Cloudflare  
- ArvanCloud  

در Pro ویندوز، عملیات CDN نیز برای این موارد در دسترس است:

- ArvanCloud  
- Cloudflare  
- KeyCDN  
- Other CDN  

در Pro اندروید تمرکز فعلی روی عملیات توپولوژی اصلی و Move Central است؛ سطح عمیق‌تر اتوماسیون CDN همچنان روی ویندوز قرار دارد.

---

## ۷. Black Fox Config Builder

**Black Fox Config Builder** ابزار همراه اندروید برای ساخت روزمره کانفیگ روی پنل 3X-UI از طریق گوشی است.

این برنامه سرور راه‌اندازی نمی‌کند. اپراتور ابتدا با VPS to VPN یا VPS to VPN Android زیرساخت Basic/Pro را می‌سازد، سپس اطلاعات **Panel Login Info** را در Config Builder وارد می‌کند.

### نسخه فعلی

| مورد | مقدار |
|------|--------|
| نام کامل محصول | Black Fox Config Builder |
| نسخه | **1.1.3 (Build 7)** |
| بسته | `com.blackfoxvpnn.configbuilder` |
| دانلود | [Black-Fox-Config-Builder.apk](https://foxnext.net/downloads/Black-Fox-Config-Builder.apk) |
| حداقل اندروید | API 24 |
| حداقل پنل | 3X-UI **۳.۳.۰ به بالا** |

### سطح برنامه (شش تب)

۱. **Connection** — آدرس پنل / کاربر / رمز / API Key اختیاری / Sub URI اختیاری  
۲. **Single** — یک کانفیگ با انتخاب چند Inbound، لینک VLESS و ساب، QR Code  
۳. **Bulk** — چند کانفیگ با پیشرفت و امکان توقف  
۴. **List** — کپی لینک، حذف از پنل، حذف از لیست  
۵. **Settings** — ۱۰ زبان، آپدیت دو میزبان، Force Update، لاگ فعالیت  
۶. **Contact** — وب‌سایت، ایمیل، گیت‌هاب، تلگرام  

### یادداشت بیلدهای منتشرشده

- **Build 6:** فید ریموت دو سرور (`blackfoxupdate.ir` و `foxnext.net`) برای version / wallet / news / APK  
- **Build 7:** نسخه فعلی منتشرشده اندروید با گردش‌کار کامل شش تب، ساخت multi-inbound، حذف از پنل و پوشش ۱۰ زبان  

Config Builder مسیر ثبت‌نام لایسنس / TX Unlock مربوط به Installer را داخل خود اپ پیاده‌سازی نمی‌کند.

---

## ۸. بومی‌سازی

اپلیکیشن‌های Black Fox Group و وب‌سایت از **۱۰ زبان** پشتیبانی می‌کنند:

انگلیسی، فارسی، روسی، چینی، آلمانی، ازبکی، ترکی، اندونزیایی، اوکراینی و هندی.

---

## ۹. حریم خصوصی و آپدیت

- سیاست حریم خصوصی فارسی: [https://foxnext.net/fa/privacy.html](https://foxnext.net/fa/privacy.html)  
- سیاست حریم خصوصی انگلیسی: [https://foxnext.net/en/privacy.html](https://foxnext.net/en/privacy.html)  
- میزبان‌های آپدیت: `foxnext.net` و `blackfoxupdate.ir`  

صفحات منتشرشده Privacy Policy منبع معتبر حریم خصوصی هستند.

---

## ۱۰. این مجموعه چیست و چه چیزی نیست

- کلاینت ساده VPN برای کاربر نهایی نیست  
- ادعای زنده بودن Google Play نیست  
- ادعای انتشار فعلی macOS نیست  
- محل ثبت امکانات پیاده‌سازی‌نشده نیست  

---

## ۱۱. اسناد مرتبط

- [README.md](../README.md)  
- [ROADMAP.fa.md](ROADMAP.fa.md)  
- [ROADMAP.en.md](ROADMAP.en.md)  
- [WHITEPAPER.en.md](WHITEPAPER.en.md)  
- مستندات Config Builder: [BlackFoxGroup/blackfox-config-builder](https://github.com/BlackFoxGroup/blackfox-config-builder)  

---

© Black Fox Security Team
