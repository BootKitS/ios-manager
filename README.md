<div align="center">

# iOS 设备管理工具 · iOS Manager

**Windows 上批量管理 iPhone 的免费工具：批量签名安装 IPA、批量激活 WebDriverAgent、批量导出 UDID、批量卸载应用。**

免费 · 免注册 · 解压即用 · 中文 / English

[**⬇️ 立即下载（官网）**](https://www.wtscript.com/zh/download?utm_source=github&utm_medium=readme#manager)
&nbsp;·&nbsp;
[使用教程](https://www.wtscript.com/zh/docs?utm_source=github&utm_medium=readme#prepare)
&nbsp;·&nbsp;
[English](README_EN.md)

![Platform](https://img.shields.io/badge/platform-Windows%2010%20%7C%2011-0078D6?logo=windows)
![iOS](https://img.shields.io/badge/iOS-13%2B%20%7C%2017%2B-black?logo=apple)
![Price](https://img.shields.io/badge/price-free-4EDEA3)
![Lang](https://img.shields.io/badge/UI-中文%20%7C%20English-4C7CFF)

</div>

<!--
  截图：把软件主界面截图存成 docs/screenshot.png 后，删掉这段注释的首尾两行即可显示。
  建议截一张连着多台设备、正在「全部安装」的画面，最能说明用途。

<p align="center"><img src="docs/screenshot_zh.png" alt="iOS 设备管理工具主界面：多台 iPhone 批量安装 IPA" width="820"></p>
-->
<p align="center"><img src="docs/screenshot_zh.png" alt="iOS 设备管理工具主界面：多台 iPhone 批量安装 IPA" width="820"></p>
---

## 它能做什么

手上有几台到几十台 iPhone，要给每台装同一个 App、每台用自己的证书签名、每台都激活开发者服务 —— 一台台用爱思助手、Xcode 点，非常耗时间。这个工具把这些事情变成「插上数据线，点一下全部」。

| 功能 | 说明 |
|---|---|
| 📱 **设备列表** | 自动识别 USB 连接的 iPhone / iPad，显示设备名、UDID、系统版本 |
| 📋 **UDID 一键复制 / 批量导出** | 点一下复制 UDID；所有已连接设备的 UDID 一次导出为 `.txt`，直接拿去申请证书 |
| ✍️ **按设备自动重签名** | 每台设备用自己的 `.p12` 证书和 `.mobileprovision` 描述文件签名，工具按 UDID 自动匹配 |
| 📦 **批量安装 IPA** | 选好 IPA，「全部安装」依次为每台设备签名并安装，进度实时显示 |
| 🔓 **越狱设备免签名** | 已越狱并装有 AppSync Unified 的设备，直接安装原始 IPA，不需要证书 |
| ⚙️ **批量激活** | 自动挂载开发者磁盘映像（DDI）并启动 WebDriverAgent，支持 iOS 17 及以上 |
| 🗑️ **批量卸载** | 输入 Bundle ID，从所有设备上一次性卸载同一个应用 |
| 💾 **记住设置** | 证书目录、IPA 位置、签名方式自动保存，下次打开不用重选 |

## 适合谁用

- 做 **iOS 自动化 / 群控 / 云控** 的团队，需要给大量设备装 WebDriverAgent 并激活
- **测试团队**，要把同一个测试包装到一批真机上
- 用 **企业证书 / 个人开发者证书** 给设备分发 App 的场景
- 有一批 **越狱设备** 需要批量装包

## 下载

> 👉 **[到官网下载最新版](https://www.wtscript.com/zh/download?utm_source=github&utm_medium=readme#manager)**（含版本说明和 SHA-256 校验值）

官网下载页同时提供配套的 **WebDriverAgent** 和 **云点iOS App** 安装包。

## 三步上手

1. **解压运行**：解压下载的压缩包，双击 `ios-manager.exe`。
2. **连接设备**：用数据线连接 iPhone，手机上点「信任」，在工具里点「刷新设备」。
3. **签名并安装**：点「签名设置」选证书目录（或选越狱免签名），再点「选择IPA」→「全部安装」。

证书目录的结构：每台设备一个以 UDID 命名的文件夹，里面放证书、描述文件和密码文件。

```
证书目录/
├── 00008110-001A2B3C4D5E6F7A/     ← 以设备 UDID 命名
│   ├── xxx.p12                     ← 证书
│   ├── xxx.mobileprovision         ← 描述文件
│   └── 密码.txt                    ← 证书密码（任意 .txt，文件名不限）
└── 00008030-000B1C2D3E4F5A6B/
    └── …
```

完整图文教程（含激活、开发者模式、常见问题）：**[wtscript.com/zh/docs](https://www.wtscript.com/zh/docs?utm_source=github&utm_medium=readme#prepare)**

## 系统要求

- Windows 10 / 11（64 位）
- iPhone / iPad：iOS 13 及以上；iOS 16 及以上需在手机上开启「开发者模式」
- 一根能传数据的数据线

## 常见问题

<details>
<summary><b>工具收费吗？需要注册吗？</b></summary>

完全免费，不需要注册，全部功能都能用。
</details>

<details>
<summary><b>Windows 提示「已保护你的电脑」怎么办？</b></summary>

点「更多信息」→「仍要运行」。
</details>

<details>
<summary><b>刷新后看不到设备？</b></summary>

确认手机已解锁，并在「要信任此电脑吗？」弹窗里点了「信任」。仍然没有的话，换一根数据线或换一个 USB 口再刷新。
</details>

<details>
<summary><b>提示「未找到设备的证书」？</b></summary>

检查证书目录里的文件夹名是否和这台设备的 UDID 完全一致，文件夹里要同时有 `.p12` 和 `.mobileprovision`。
</details>

<details>
<summary><b>激活失败？</b></summary>

激活前要先装好 WebDriverAgent；iOS 16 及以上要先开启开发者模式；保持手机解锁后重新插拔数据线再试。
</details>

更多问题见 [官网教程的「排查问题」](https://www.wtscript.com/zh/docs?utm_source=github&utm_medium=readme#troubleshooting)。

## iOS 群控 / 云控平台

这个工具是 **[云点iOS](https://www.wtscript.com/zh?utm_source=github&utm_medium=readme)** 的配套工具。云点iOS 是浏览器里就能用的 iOS 真机群控平台：零代码录制脚本、找图找色与文字识别、P2P 实时投屏、脚本一键下发到整组设备批量执行。

需要 **iOS 群控 / 云控系统、自动化脚本等定制开发**，欢迎联系：

- Telegram：[@WTScript](https://t.me/WTScript)
- QQ：3252528962
- 官网：[www.wtscript.com](https://www.wtscript.com/zh?utm_source=github&utm_medium=readme)

---

<sub>关键词：iOS 批量安装 IPA · iPhone 批量签名 · IPA 重签名工具 · 批量导出 UDID · WebDriverAgent 批量激活 · iOS 群控 · iOS 云控 · 爱思助手批量替代 · Windows iOS 管理工具 · zsign GUI · iOS 自动化</sub>

<sub>© 2026 WTScript. All rights reserved.</sub>
