# Дорожная карта VPS to VPN

**Обновлено:** 13 сентября 2026  
**Продукт:** VPS to VPN  
**Текущие сборки:** Windows v3.2.0 (Build 220). Android и Config Builder берутся из `version.json` на хостах обновлений.  
**Сайт:** [https://foxnext.net](https://foxnext.net)  
**Публичный GitHub:** [BlackFoxGroup/VPS-to-VPN](https://github.com/BlackFoxGroup/VPS-to-VPN)

Список того, что уже вышло, что ещё правим и что планируем. Опора: текущее дерево Go для Windows, сайт и сервис лицензий. Номер Android здесь не меняем, пока этого нет в release notes.

---

## Загрузки

| Продукт | Файл | GitHub | Сайт |
|---------|------|--------|------|
| Установщик Windows | `VPS-to-VPN-Setup.zip` | [скачать](https://github.com/BlackFoxGroup/VPS-to-VPN/releases/latest/download/VPS-to-VPN-Setup.zip) | [foxnext.net](https://foxnext.net/downloads/VPS%20to%20VPN-Setup.exe) |
| Portable Windows | `VPS to VPN-Portable.zip` | [скачать](https://github.com/BlackFoxGroup/VPS-to-VPN/releases/latest/download/VPS-to-VPN-Portable.zip) | — |
| Android arm64 | `VPS-to-VPN-Android-arm64-v8a-release.apk` | [скачать](https://github.com/BlackFoxGroup/VPS-to-VPN/releases/latest/download/VPS-to-VPN-Android-arm64-v8a-release.apk) | [foxnext.net](https://foxnext.net/downloads/VPS%20to%20VPN%20Android.apk) |
| Black Fox Config Builder | `Black-Fox-Config-Builder.apk` | — | [foxnext.net](https://foxnext.net/downloads/Black-Fox-Config-Builder.apk) |

Google Play: скоро.  
macOS: скоро.

---

## Сделано

- Консоль Windows v3.2.0 Build 220, приложение Android, Config Builder 1.1.3 Build 7
- Сайт и два хоста обновлений (`foxnext.net`, `blackfoxupdate.ir`)
- Политика конфиденциальности EN/FA
- Документы и бинарники на [BlackFoxGroup/VPS-to-VPN](https://github.com/BlackFoxGroup/VPS-to-VPN)
- Basic и Pro, лицензия AI Assistant Pro и ИИ-агент Black Fox Group в чате
- Central / SSH / Full Deploy, Tunnel (Pro), Exit (2 слота в Basic, до 6 в Pro)
- Девять типов mesh с failover, Configure Panel, установка WireGuard и 3X-UI
- DNS (Cloudflare, ArvanCloud), CDN на Windows Pro, Move Central на Windows и Android
- Онлайн-оплата, офлайн-коды, Reactivation по отпечатку устройства
- Config Builder: шесть вкладок, одиночное и массовое создание, удаление с панели
- Десять языков интерфейса
- README, ROADMAP и WHITEPAPER на EN, FA, RU, ZH

---

## В работе

- Сближение Android и Windows на длинных и краевых сценариях
- Понятнее UI во время Deploy и Move
- Стабильность SSH, синхронизации панели и проверки обновлений
- Текст сайта по фактическому поведению программ
- Разрыв между CDN на Windows и Pro на Android

---

## План

Ближайшее: Google Play, отдельный Backup/Restore, продолжение прерванного деплоя, понятнее ошибки.

Средний срок: macOS, больше полировки CDN, дополнительные DNS/CDN по запросу, аудит Move Central и reactivation.

Позже: больше региональных инструментов, автоматизация жизненного цикла клиентов панели, другие магазины при спросе.

---

## Пока не делаем

Потребительский VPN-клиент. Заявления, что Google Play или macOS уже вышли. Описание функций, которых нет в текущем исходнике.

---

## Связанные файлы

- [README.md](../README.md)
- [WHITEPAPER.ru.md](WHITEPAPER.ru.md)
- [ROADMAP.en.md](ROADMAP.en.md)

© Black Fox Security Team
