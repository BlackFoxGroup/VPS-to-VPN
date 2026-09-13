# Белая книга VPS to VPN

**Обновлено:** 13 сентября 2026  
**Продукты:** VPS to VPN (Windows), VPS to VPN Android, Black Fox Config Builder  
**Windows:** v3.2.0 (Build 220)  
**Сайт:** [https://foxnext.net](https://foxnext.net)  
**Публичный GitHub:** [https://github.com/BlackFoxGroup/VPS-to-VPN](https://github.com/BlackFoxGroup/VPS-to-VPN)

---

## 1. Зачем

VPS to VPN — набор для развёртывания и эксплуатации серверов. Операторы в ограниченных сетях поднимают VPN в нескольких локациях на 3X-UI (Sanaei), девяти типах mesh (восемь на Xray, WireGuard в конце) с failover и Server Connection Manager (тип линка, Watchdog, Link Monitor). Лицензия AI Assistant Pro даёт ИИ-агента Black Fox Group в чате: после активации можно поручить добавление серверов, установку панели, mesh, домен и диагностику; перед изменением хоста агент спрашивает.

Повседневная рутина Linux, SSH, панели, DNS и туннелей сокращается.

---

## 2. Поверхности

| Где | Имя | Роль | Скачать |
|-----|-----|------|---------|
| Windows | VPS to VPN | Десктопная консоль | [Setup.zip](https://github.com/BlackFoxGroup/VPS-to-VPN/releases/latest/download/VPS-to-VPN-Setup.zip), [Portable.zip](https://github.com/BlackFoxGroup/VPS-to-VPN/releases/latest/download/VPS-to-VPN-Portable.zip) |
| Android | VPS to VPN Android | Мобильные операции | [APK](https://github.com/BlackFoxGroup/VPS-to-VPN/releases/latest/download/VPS-to-VPN-Android-arm64-v8a-release.apk) |
| Android | Black Fox Config Builder | Конфиги клиентов 3X-UI | [APK](https://foxnext.net/downloads/Black-Fox-Config-Builder.apk) |
| Google Play | VPS to VPN Android | Магазин | скоро |
| macOS | VPS to VPN | Будущая сборка | скоро |

Документация Config Builder: [BlackFoxGroup/blackfox-config-builder](https://github.com/BlackFoxGroup/blackfox-config-builder)

---

## 3. Режимы

Basic: Central, SSH и Full Deploy, до двух Exit, помощники панели, установка WireGuard и 3X-UI.

Pro: Central, Tunnel, до шести Exit, девять mesh и failover, домен и DNS, CDN на Windows, Move Central на Windows и Android, бэкап миграции.

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

Раньше смена Central означала собирать туннели заново, перепривязывать Exit и руками возвращать клиентов панели.

Сейчас в Pro на Windows и Android: Operations, Move Central Server, данные нового Central, переподключение tunnel/exit, restore клиентов 3X-UI из снимка, локальный бэкап. Страницы, где это только Windows, устарели.

---

## 5. Лицензия

Три пути: онлайн (оплата / TX Hash), офлайн-код, Reactivation после переустановки на том же устройстве.

На Registration нажимают Reactivation / فعال‌سازی مجدد. Приложение шлёт отпечаток машины. Если запись есть, доступ возвращается.

Reactivation не создаёт новую лицензию. Локальный vault Windows, если он есть, это другой механизм. Цены на сайте в последней проверке: Basic 19 USDT, Pro 33 USDT.

---

## 6. Домен, DNS, CDN

Pro: DNS Cloudflare и ArvanCloud. Windows Pro ещё CDN (ArvanCloud, Cloudflare, KeyCDN, Other). Android Pro держит топологию и Move Central.

---

## 7. Config Builder

Приложение не деплоит серверы. Версия 1.1.3 Build 7, пакет `com.blackfoxvpnn.configbuilder`, API 24+, панель 3X-UI 3.3.0+. Вкладки: Connection, Single, Bulk, List, Settings, Contact. Регистрации лицензии Installer внутри нет.

---

## 8–10

Десять языков. Политика: [EN](https://foxnext.net/en/privacy.html), [FA](https://foxnext.net/fa/privacy.html). Хосты обновлений: `foxnext.net`, `blackfoxupdate.ir`. Google Play и macOS ещё не вышли.

---

## Связанные файлы

- [README.md](../README.md)
- [ROADMAP.ru.md](ROADMAP.ru.md)
- [WHITEPAPER.en.md](WHITEPAPER.en.md)

© Black Fox Security Team
