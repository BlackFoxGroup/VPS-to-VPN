# VPS to VPN 路线图

**更新日期：** 2026-09-13  
**产品：** VPS to VPN  
**当前版本：** Windows v3.1.1（Build 213）。Android 与 Config Builder 以更新主机上的 `version.json` 为准。  
**网站：** [https://foxnext.net](https://foxnext.net)  
**公开仓库：** [BlackFoxGroup/VPS-to-VPN](https://github.com/BlackFoxGroup/VPS-to-VPN)

下面按已交付、进行中、计划写。依据是当前 Windows Go 代码、官网和许可服务。Android 版本号除非发行说明另写，这里不改。

---

## 下载

| 产品 | 文件 | GitHub | 网站 |
|------|------|--------|------|
| Windows 安装包 | `VPS-to-VPN-Setup.zip` | [下载](https://github.com/BlackFoxGroup/VPS-to-VPN/releases/latest/download/VPS-to-VPN-Setup.zip) | [foxnext.net](https://foxnext.net/downloads/VPS%20to%20VPN-Setup.exe) |
| Windows 便携包 | `VPS to VPN-Portable.zip` | [下载](https://github.com/BlackFoxGroup/VPS-to-VPN/releases/latest/download/VPS.to.VPN-Portable.zip) | — |
| Android arm64 | `VPS-to-VPN-Android-arm64-v8a-release.apk` | [下载](https://github.com/BlackFoxGroup/VPS-to-VPN/releases/latest/download/VPS-to-VPN-Android-arm64-v8a-release.apk) | [foxnext.net](https://foxnext.net/downloads/VPS%20to%20VPN%20Android.apk) |
| Black Fox Config Builder | `Black-Fox-Config-Builder.apk` | — | [foxnext.net](https://foxnext.net/downloads/Black-Fox-Config-Builder.apk) |

Google Play：即将上线。macOS：即将上线。

---

## 已完成

Windows 控制台 3.1.1 Build 213、Android 运维应用、Config Builder 1.1.3 Build 7。官网与双更新主机。隐私页（中英对照站点上的 EN/FA）。公开文档和安装包在 [BlackFoxGroup/VPS-to-VPN](https://github.com/BlackFoxGroup/VPS-to-VPN)。

Basic / Pro，以及 AI Assistant Pro（聊天里的 Black Fox Group 智能体，改服务器前会确认）。Central、SSH、Full Deploy，Pro 的 Tunnel，Exit（Basic 2 槽，Pro 最多 6）。九种 mesh 与 failover。Configure Panel。安装 WireGuard / 3X-UI。

Pro：Cloudflare / ArvanCloud DNS；Windows 上的 CDN；Windows 与 Android 的 Move Central。许可：在线支付、离线码、同机重新激活。Config Builder 六个页签。界面十种语言。README / ROADMAP / WHITEPAPER 有英、波斯、俄、中。

---

## 进行中

拉近 Android 与 Windows 的长流程和边角。Deploy / Move 时界面更清楚。SSH、面板同步、检查更新更稳。网站文案跟程序实际行为对齐。Windows CDN 与 Android Pro 范围之间的差距。

---

## 计划

近期：Google Play、独立备份恢复、中断部署后续、更清楚的报错。  
中期：macOS、Windows CDN 再打磨、有需求再加 DNS/CDN 厂商、Move Central 与重新激活的审计。  
更后：更多区域运维工具、面板客户生命周期自动化、有需求再上其他渠道。

---

## 暂时不做

面向终端用户的消费级 VPN 客户端。宣称 Google Play 或 macOS 已经上线。把源码里没有的功能写成已发布。

---

## 相关

- [README.md](../README.md)
- [WHITEPAPER.zh.md](WHITEPAPER.zh.md)
- [ROADMAP.en.md](ROADMAP.en.md)

© Black Fox Security Team
