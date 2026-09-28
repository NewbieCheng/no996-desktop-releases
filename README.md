# 不加班智能团 Desktop · 公开发布

> 本仓库**仅提供安装包与 DSH 运行时组件**，不含源代码。  
> 海外镜像：[GitHub Releases](https://github.com/NewbieCheng/no996-desktop-releases/releases) · 国内镜像：[Gitee Releases](https://gitee.com/ZJCACE/no996-desktop-releases/releases)

当前版本：**v0.3.1-alpha**（2026-09-28，Windows + macOS）

## v0.3.1-alpha 更新摘要

- **修复：安装包主进程启动即崩** —— `@no996/module-sdk` 根入口不再带 React 成员（主进程经 Node `require` 取纯函数而安装包无 react-dom）；React 成员独立成 `@no996/module-sdk/ui` 子路径，Shell 与全部板块改引 `/ui`；新增根入口零 React 的回归断言与板块边界机检
- **升级：DSH 内核 `dsh-v0.1.7-rc.2`（`477b4f42`）**，运行时组件升至 **1.5.0**
- **实装：定时任务与时间上下文**、**桌面托盘后台运行**、**统一快捷键注册表**、**新手引导状态持久化**、**插件管理与实验性能力**
- **对齐：工具输出多字节代理对截断保护**

> 完整中英双语说明见 [v0.3.1-alpha Release](https://github.com/NewbieCheng/no996-desktop-releases/releases/tag/v0.3.1-alpha)；可直接覆盖安装 0.2.x / 0.1.x。

---

## 安装包（整包更新）

应用内「设置 → 通用 → 检查更新」读取 `latest` 标签下的 `latest.json`；也可手动下载下方安装包。

| 平台 | 文件 | 海外（GitHub） | 国内（Gitee） |
|------|------|----------------|---------------|
| Windows x64 | `no996-workbench-0.3.1-alpha-win-x64.exe` | [下载](https://github.com/NewbieCheng/no996-desktop-releases/releases/download/v0.3.1-alpha/no996-workbench-0.3.1-alpha-win-x64.exe) | 整包超过 Gitee 100 MB 上限，请用 GitHub 或应用内更新 |
| macOS Apple Silicon | `no996-workbench-0.3.1-alpha-mac-arm64.dmg` | [下载](https://github.com/NewbieCheng/no996-desktop-releases/releases/download/v0.3.1-alpha/no996-workbench-0.3.1-alpha-mac-arm64.dmg) | 同上，请用 GitHub |
| 更新清单 | `latest.json` / `release-history.json` | [latest](https://github.com/NewbieCheng/no996-desktop-releases/releases/download/latest/latest.json) · [v0.3.1-alpha](https://github.com/NewbieCheng/no996-desktop-releases/releases/download/v0.3.1-alpha/latest.json) | [latest](https://gitee.com/ZJCACE/no996-desktop-releases/releases/download/latest/latest.json) · [v0.3.1-alpha](https://gitee.com/ZJCACE/no996-desktop-releases/releases/download/v0.3.1-alpha/latest.json) |

### 平台安装指南

- **Windows 用户**：直接运行 `no996-workbench-0.3.1-alpha-win-x64.exe` 安装（支持 Windows 10/11 64 位）。
- **macOS 用户**：下载 `no996-workbench-0.3.1-alpha-mac-arm64.dmg` 双击打开，将「不加班工作台」拖入 `Applications`（应用程序）文件夹即可。适配 macOS 12+ 及 Apple Silicon（M1/M2/M3/M4 系列芯片）；首次启动自动下载 arm64 架构 DSH 智能内核组件。
- **覆盖升级**：已安装早期版本的用户可直接覆盖安装，原有账号登录态、工作区文件与会话历史完整保留。

Release 页面：

- GitHub：[v0.3.1-alpha](https://github.com/NewbieCheng/no996-desktop-releases/releases/tag/v0.3.1-alpha) · [latest](https://github.com/NewbieCheng/no996-desktop-releases/releases/tag/latest)
- Gitee：[v0.3.1-alpha](https://gitee.com/ZJCACE/no996-desktop-releases/releases/tag/v0.3.1-alpha) · [latest](https://gitee.com/ZJCACE/no996-desktop-releases/releases/tag/latest)

---

## DSH 运行时组件（首次启动下载）

安装包内**不包含** DSH 内核；首次启动按 manifest 自动下载。文件名固定，与 App 版本解耦（runtime **v1.5.0**）。

| 平台 | 文件 | 海外（GitHub） | 国内（Gitee） |
|------|------|----------------|---------------|
| Windows x64 | `dsh-runtime-win-x64.zip` | [下载](https://github.com/NewbieCheng/no996-desktop-releases/releases/download/runtime/dsh-runtime-win-x64.zip) | [下载](https://gitee.com/ZJCACE/no996-desktop-releases/releases/download/runtime/dsh-runtime-win-x64.zip) |
| macOS arm64 | `dsh-runtime-macos-arm64.zip` | [下载](https://github.com/NewbieCheng/no996-desktop-releases/releases/download/runtime/dsh-runtime-macos-arm64.zip) | [下载](https://gitee.com/ZJCACE/no996-desktop-releases/releases/download/runtime/dsh-runtime-macos-arm64.zip) |
| Office 扩展（可选） | `dsh-runtime-ext-libreoffice-{platform}.zip` | [runtime Release](https://github.com/NewbieCheng/no996-desktop-releases/releases/tag/runtime) | 同上 |
| 语音扩展（可选） | `dsh-runtime-ext-sherpa-{platform}.zip` | 同上 | 同上 |
| Manifest | `dsh-runtime-*.manifest.json` | [runtime Release](https://github.com/NewbieCheng/no996-desktop-releases/releases/tag/runtime) | [runtime Release](https://gitee.com/ZJCACE/no996-desktop-releases/releases/tag/runtime) |

Runtime Release 页面：

- GitHub：<https://github.com/NewbieCheng/no996-desktop-releases/releases/tag/runtime>
- Gitee：<https://gitee.com/ZJCACE/no996-desktop-releases/releases/tag/runtime>

---

## 可选板块（应用内插件市场）

安装包**不含**可选板块；应用内「插件市场」按需下载签名包，与 App 版本解耦（当前板块 **0.5.0**）。

| 板块 | 文件 | 前置 | 海外（GitHub） | 国内（Gitee） |
|------|------|------|----------------|---------------|
| 产品管理 | `product-0.5.0.no996-module.zip` | — | [下载](https://github.com/NewbieCheng/no996-desktop-releases/releases/download/modules/product-0.5.0.no996-module.zip) | [下载](https://gitee.com/ZJCACE/no996-desktop-releases/releases/download/modules/product-0.5.0.no996-module.zip) |
| 产品营销专家 | `product-marketing-0.5.0.no996-module.zip` | 产品管理 | [下载](https://github.com/NewbieCheng/no996-desktop-releases/releases/download/modules/product-marketing-0.5.0.no996-module.zip) | [下载](https://gitee.com/ZJCACE/no996-desktop-releases/releases/download/modules/product-marketing-0.5.0.no996-module.zip) |
| 朋友圈运营 | `moments-0.5.0.no996-module.zip` | 产品管理 | [下载](https://github.com/NewbieCheng/no996-desktop-releases/releases/download/modules/moments-0.5.0.no996-module.zip) | [下载](https://gitee.com/ZJCACE/no996-desktop-releases/releases/download/modules/moments-0.5.0.no996-module.zip) |
| 公众号写作 | `wechat-article-0.5.0.no996-module.zip` | — | [下载](https://github.com/NewbieCheng/no996-desktop-releases/releases/download/modules/wechat-article-0.5.0.no996-module.zip) | [下载](https://gitee.com/ZJCACE/no996-desktop-releases/releases/download/modules/wechat-article-0.5.0.no996-module.zip) |
| 合规专家 | `compliance-0.5.0.no996-module.zip` | 产品管理 | [下载](https://github.com/NewbieCheng/no996-desktop-releases/releases/download/modules/compliance-0.5.0.no996-module.zip) | [下载](https://gitee.com/ZJCACE/no996-desktop-releases/releases/download/modules/compliance-0.5.0.no996-module.zip) |
| AI真人口播 | `avatar-video-0.5.0.no996-module.zip` | 产品管理 | [下载](https://github.com/NewbieCheng/no996-desktop-releases/releases/download/modules/avatar-video-0.5.0.no996-module.zip) | [下载](https://gitee.com/ZJCACE/no996-desktop-releases/releases/download/modules/avatar-video-0.5.0.no996-module.zip) |
| 电商视觉 | `ecom-visual-0.5.0.no996-module.zip` | 产品管理 | [下载](https://github.com/NewbieCheng/no996-desktop-releases/releases/download/modules/ecom-visual-0.5.0.no996-module.zip) | [下载](https://gitee.com/ZJCACE/no996-desktop-releases/releases/download/modules/ecom-visual-0.5.0.no996-module.zip) |
| 宣传主视觉 | `promo-key-visual-0.5.0.no996-module.zip` | 产品管理 | [下载](https://github.com/NewbieCheng/no996-desktop-releases/releases/download/modules/promo-key-visual-0.5.0.no996-module.zip) | [下载](https://gitee.com/ZJCACE/no996-desktop-releases/releases/download/modules/promo-key-visual-0.5.0.no996-module.zip) |
| 目录 | `catalog.json` | — | [catalog](https://github.com/NewbieCheng/no996-desktop-releases/releases/download/modules/catalog.json) | [catalog](https://gitee.com/ZJCACE/no996-desktop-releases/releases/download/modules/catalog.json) |
| 板块开发起步模板 | `module-starter-0.2.0.zip` | — | [下载](https://github.com/NewbieCheng/no996-desktop-releases/releases/download/modules/module-starter-0.2.0.zip) | [下载](https://gitee.com/ZJCACE/no996-desktop-releases/releases/download/modules/module-starter-0.2.0.zip) |

板块 Release 页面：<https://github.com/NewbieCheng/no996-desktop-releases/releases/tag/modules>

手动安装不需要：应用内「设置 → 插件市场」会自动读取 `catalog.json`，先装前置再装所选板块。
`module-starter-*.zip` 是给第三方开发者的**源码起步包**（解压后改 id 即成新板块），不是安装项，不会出现在插件市场里。

---

## 许可

本软件为闭源商业软件，最终用户许可协议（EULA）详见安装包内的 `LICENSE.txt`。

Agent 运行时基于 DeepSeek Harness（DSH，MIT）构建；本产品为独立软件，与 DeepSeek 无隶属、背书或授权关系。第三方开源声明见安装包内 `legal/THIRD_PARTY_NOTICES.md`，也可在应用内「设置 → 版本信息」查看。

© 2026 不加班智能团

---

# No996 Workbench Desktop · Public Releases

> Installers and DSH runtime only — **no source code**.  
> Overseas: [GitHub Releases](https://github.com/NewbieCheng/no996-desktop-releases/releases) · China mirror: [Gitee Releases](https://gitee.com/ZJCACE/no996-desktop-releases/releases)

Current version: **v0.3.1-alpha** (2026-09-28, Windows + macOS)

## v0.3.1-alpha highlights

- **Fix: packaged Main process crashed on launch** —— the `@no996/module-sdk` root entry no longer pulls in React members (Main `require`s it via Node while the installer ships no react-dom); React members moved to the `@no996/module-sdk/ui` subpath and Shell plus every board import `/ui`. Adds a React-free root-entry regression and a module-boundary gate
- **DSH kernel upgraded to `dsh-v0.1.7-rc.2` (`477b4f42`)**, runtime component at **1.5.0**
- **Scheduled tasks & time context**, **desktop tray with background execution**, **unified shortcuts registry**, **onboarding state persistence**, **plugin manager & experimental bundles**
- **Surrogate-pair protective truncation** for tool output

> Full bilingual notes: [v0.3.1-alpha release](https://github.com/NewbieCheng/no996-desktop-releases/releases/tag/v0.3.1-alpha). Safe to install over 0.2.x / 0.1.x.

## Installers

| Platform | File | GitHub download |
|----------|------|-----------------|
| Windows x64 | `no996-workbench-0.3.1-alpha-win-x64.exe` | [download](https://github.com/NewbieCheng/no996-desktop-releases/releases/download/v0.3.1-alpha/no996-workbench-0.3.1-alpha-win-x64.exe) |
| macOS Apple Silicon | `no996-workbench-0.3.1-alpha-mac-arm64.dmg` | [download](https://github.com/NewbieCheng/no996-desktop-releases/releases/download/v0.3.1-alpha/no996-workbench-0.3.1-alpha-mac-arm64.dmg) |
| Update manifest | `latest.json` | https://github.com/NewbieCheng/no996-desktop-releases/releases/download/latest/latest.json |

Gitee mirrors `latest.json` + `release-history.json` + runtime; full exe/dmg are GitHub-only (100 MB Gitee limit).

### Platform installation notes

- **Windows users**: Run `no996-workbench-0.3.1-alpha-win-x64.exe` directly (Windows 10/11 x64).
- **macOS users**: Open `no996-workbench-0.3.1-alpha-mac-arm64.dmg` and drag "No996 Workbench" to `Applications`. Requires macOS 12+ on Apple Silicon (M1/M2/M3/M4); first launch automatically downloads the arm64 DSH kernel runtime bundle.
- **In-place upgrade**: Safe to install over earlier releases; user accounts, workspace files, and conversation history are preserved.

## DSH runtime (first launch)

Runtime **v1.5.0**, decoupled from the app version.

| Platform | GitHub | Gitee |
|----------|--------|-------|
| Windows x64 | [zip](https://github.com/NewbieCheng/no996-desktop-releases/releases/download/runtime/dsh-runtime-win-x64.zip) | [zip](https://gitee.com/ZJCACE/no996-desktop-releases/releases/download/runtime/dsh-runtime-win-x64.zip) |
| macOS arm64 | [zip](https://github.com/NewbieCheng/no996-desktop-releases/releases/download/runtime/dsh-runtime-macos-arm64.zip) | [zip](https://gitee.com/ZJCACE/no996-desktop-releases/releases/download/runtime/dsh-runtime-macos-arm64.zip) |

Gitee mirrors: `https://gitee.com/ZJCACE/no996-desktop-releases/releases/download/<tag>/<file>`

## Optional modules (in-app marketplace)

Optional boards are **not** bundled in the installer; the in-app marketplace downloads signed packages on demand (current **0.5.0**).

Catalog: <https://github.com/NewbieCheng/no996-desktop-releases/releases/download/modules/catalog.json>

Boards (`product` is the prerequisite of `product-marketing`, `moments`, `compliance`, `avatar-video`, `ecom-visual`, and `promo-key-visual`):

| Board | File | Prerequisite |
|-------|------|--------------|
| Product management | `product-0.5.0.no996-module.zip` | — |
| Product marketing | `product-marketing-0.5.0.no996-module.zip` | product |
| Moments operations | `moments-0.5.0.no996-module.zip` | product |
| WeChat article | `wechat-article-0.5.0.no996-module.zip` | — |
| Compliance review | `compliance-0.5.0.no996-module.zip` | product |
| AI talking-head video | `avatar-video-0.5.0.no996-module.zip` | product |
| E-commerce visuals | `ecom-visual-0.5.0.no996-module.zip` | product |
| Promo key visuals | `promo-key-visual-0.5.0.no996-module.zip` | product |
| Developer starter template | `module-starter-0.2.0.zip` | — |

Modules release: <https://github.com/NewbieCheng/no996-desktop-releases/releases/tag/modules>. No manual install is needed: Settings → Marketplace reads `catalog.json` and installs prerequisites first. `module-starter-*.zip` is a **source starter kit** for third-party developers (unzip and rename the id), not an installable board — it never appears in the marketplace.
