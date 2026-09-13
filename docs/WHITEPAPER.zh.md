# VPS to VPN 白皮书

**更新日期：** 2026-09-13  
**产品：** VPS to VPN（Windows）、VPS to VPN Android、Black Fox Config Builder  
**Windows 版本：** v3.1.1（Build 213）  
**网站：** [https://foxnext.net](https://foxnext.net)  
**公开仓库：** [https://github.com/BlackFoxGroup/VPS-to-VPN](https://github.com/BlackFoxGroup/VPS-to-VPN)

---

## 1. 用途

VPS to VPN 是一套服务器部署和运维工具。受限网络里的运维用它搭多地点 VPN，底层是 3X-UI（Sanaei）、九种 mesh（八种 Xray，WireGuard 最后）加自动 failover，以及 Server Connection Manager（链路类型、Watchdog、Link Monitor）。

日常重复的 Linux、SSH、面板、DNS、隧道工作会少很多。

---

## 2. 产品面

| 端 | 名称 | 作用 | 下载 |
|----|------|------|------|
| Windows | VPS to VPN | 桌面运维控制台 | [Setup.zip](https://github.com/BlackFoxGroup/VPS-to-VPN/releases/latest/download/VPS-to-VPN-Setup.zip)、[Portable.zip](https://github.com/BlackFoxGroup/VPS-to-VPN/releases/latest/download/VPS.to.VPN-Portable.zip) |
| Android | VPS to VPN Android | 手机运维（Basic / Pro） | [APK](https://github.com/BlackFoxGroup/VPS-to-VPN/releases/latest/download/VPS-to-VPN-Android-arm64-v8a-release.apk) |
| Android | Black Fox Config Builder | 在手机上做 3X-UI 客户配置 | [APK](https://foxnext.net/downloads/Black-Fox-Config-Builder.apk) |
| Google Play | VPS to VPN Android | 商店 | 即将上线 |
| macOS | VPS to VPN | 后续桌面版 | 即将上线 |

Config Builder 文档：[BlackFoxGroup/blackfox-config-builder](https://github.com/BlackFoxGroup/blackfox-config-builder)

---

## 3. 模式

Basic：Central、SSH 与 Full Deploy、最多两个 Exit、面板辅助、安装 WireGuard 和 3X-UI。

Pro：Central、Tunnel、最多六个 Exit、九种 mesh 与 failover、域名与 DNS、Windows 上的 CDN、两端的 Move Central、迁移备份。

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

## 4. 迁移 Central

以前换 Central 要重做隧道、重绑 Exit、手工恢复面板客户。现在 Pro 在 Windows 和 Android 上都有 Move Central：Operations 里填新机，重连 tunnel/exit，从快照恢复 3X-UI 客户，并留下本地备份。只写 Windows 的旧页面已经不对。

---

## 5. 许可

三条路：在线支付 / TX Hash、离线码、同一台设备重装后的重新激活。在注册页按 Reactivation / فعال‌سازی مجدد，程序用机器指纹问官方服务。有记录就恢复访问，不新开一张许可。网站上次核对价格：Basic 19 USDT，Pro 33 USDT。

---

## 6. 域名、DNS、CDN

Pro 有 Cloudflare、ArvanCloud 的 DNS。Windows Pro 另有 CDN（ArvanCloud、Cloudflare、KeyCDN、Other）。Android Pro 侧重拓扑和 Move Central。

---

## 7. Config Builder

不部署服务器。1.1.3 Build 7，包名 `com.blackfoxvpnn.configbuilder`，API 24+，面板 3.3.0+。六个页签。不在应用内做 Installer 许可注册。

---

## 8–10

十种语言。隐私：[英文](https://foxnext.net/en/privacy.html)、[波斯文](https://foxnext.net/fa/privacy.html)。更新主机：`foxnext.net`、`blackfoxupdate.ir`。Google Play 和 macOS 尚未上线。

---

## 相关

- [README.md](../README.md)
- [ROADMAP.zh.md](ROADMAP.zh.md)
- [WHITEPAPER.en.md](WHITEPAPER.en.md)

© Black Fox Security Team
