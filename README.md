# 不加班智能团 Desktop · 公开发布

> 本仓库**仅提供安装包与 DSH 运行时组件**，不含源代码。  
> 海外镜像：[GitHub Releases](https://github.com/NewbieCheng/no996-desktop-releases/releases) · 国内镜像：[Gitee Releases](https://gitee.com/ZJCACE/no996-desktop-releases/releases)

当前版本：**v0.2.0**（2026-09-19，Windows + macOS）

## v0.2.0 更新摘要

- **新增可选板块「电商视觉」与「宣传主视觉」**：电商视觉走识别 → 确认 → 方案 → 任务四步产出商品图方案；宣传主视觉走输入 → 概念 → 提示词 → 任务四步产出宣发主视觉，两板块均接入产品库选品与统一任务轨
- **统一任务轨与板块逻辑下沉**：一次性生成的绑定收口为各板块 prepare 原子入口，任务中心跨模块展示进度并可点回来源页
- **真人口播打磨**：重生成链路、字幕与皮肤、多模态通道判定与用量 toast 优化
- **导航与首页体验**：功能地图 / 径向快捷与侧栏同源更新，开屏、首页布局与磁贴交互优化，五语言文案同步
- **双平台同步发布**：Windows 与 macOS（Apple Silicon）同版发布

> 完整中英双语说明见 [v0.2.0 Release](https://github.com/NewbieCheng/no996-desktop-releases/releases/tag/v0.2.0)；此前下载过 0.1.6 的用户可直接安装 0.2.0 覆盖。

---

## 安装包（整包更新）

应用内「设置 → 通用 → 检查更新」读取 `latest` 标签下的 `latest.json`；也可手动下载下方安装包。

| 平台 | 文件 | 海外（GitHub） | 国内（Gitee） |
|------|------|----------------|---------------|
| Windows x64 | `no996-workbench-0.2.0-win-x64.exe` | [下载](https://github.com/NewbieCheng/no996-desktop-releases/releases/download/v0.2.0/no996-workbench-0.2.0-win-x64.exe) | 整包超过 Gitee 100 MB 上限，请用 GitHub 或应用内更新 |
| macOS Apple Silicon | `no996-workbench-0.2.0-mac-arm64.dmg` | [下载](https://github.com/NewbieCheng/no996-desktop-releases/releases/download/v0.2.0/no996-workbench-0.2.0-mac-arm64.dmg) | 同上，请用 GitHub |
| 更新清单 | `latest.json` / `release-history.json` | [latest](https://github.com/NewbieCheng/no996-desktop-releases/releases/download/latest/latest.json) · [v0.2.0](https://github.com/NewbieCheng/no996-desktop-releases/releases/download/v0.2.0/latest.json) | [latest](https://gitee.com/ZJCACE/no996-desktop-releases/releases/download/latest/latest.json) · [v0.2.0](https://gitee.com/ZJCACE/no996-desktop-releases/releases/download/v0.2.0/latest.json) |

### 平台安装指南

- **Windows 用户**：直接运行 `no996-workbench-0.2.0-win-x64.exe` 安装（支持 Windows 10/11 64 位）。
- **macOS 用户**：下载 `no996-workbench-0.2.0-mac-arm64.dmg` 双击打开，将「不加班工作台」拖入 `Applications`（应用程序）文件夹即可。适配 macOS 12+ 及 Apple Silicon（M1/M2/M3/M4 系列芯片）；首次启动自动下载 arm64 架构 DSH 智能内核组件。
- **覆盖升级**：已安装早期版本的用户可直接覆盖安装，原有账号登录态、工作区文件与会话历史完整保留。

Release 页面：

- GitHub：[v0.2.0](https://github.com/NewbieCheng/no996-desktop-releases/releases/tag/v0.2.0) · [latest](https://github.com/NewbieCheng/no996-desktop-releases/releases/tag/latest)
- Gitee：[v0.2.0](https://gitee.com/ZJCACE/no996-desktop-releases/releases/tag/v0.2.0) · [latest](https://gitee.com/ZJCACE/no996-desktop-releases/releases/tag/latest)

---

## DSH 运行时组件（首次启动下载）

安装包内**不包含** DSH 内核；首次启动按 manifest 自动下载。文件名固定，与 App 版本解耦（runtime **v1.2.2**，本版**未更新**）。

| 平台 | 文件 | 海外（GitHub） | 国内（Gitee） |
|------|------|----------------|---------------|
| Windows x64 | `dsh-runtime-win-x64.zip` | [下载](https://github.com/NewbieCheng/no996-desktop-releases/releases/download/runtime/dsh-runtime-win-x64.zip) | [下载](https://gitee.com/ZJCACE/no996-desktop-releases/releases/download/runtime/dsh-runtime-win-x64.zip) |
| macOS arm64 | `dsh-runtime-macos-arm64.zip` | [下载](https://github.com/NewbieCheng/no996-desktop-releases/releases/download/runtime/dsh-runtime-macos-arm64.zip) | [下载](https://gitee.com/ZJCACE/no996-desktop-releases/releases/download/runtime/dsh-runtime-macos-arm64.zip) |
| Manifest | `dsh-runtime-*.manifest.json` | [runtime Release](https://github.com/NewbieCheng/no996-desktop-releases/releases/tag/runtime) | [runtime Release](https://gitee.com/ZJCACE/no996-desktop-releases/releases/tag/runtime) |

Runtime Release 页面：

- GitHub：<https://github.com/NewbieCheng/no996-desktop-releases/releases/tag/runtime>
- Gitee：<https://gitee.com/ZJCACE/no996-desktop-releases/releases/tag/runtime>

---

## 可选板块（应用内插件市场）

安装包**不含**可选板块；应用内「插件市场」按需下载签名包，与 App 版本解耦（板块版本 **0.2.0**）。

| 板块 | 文件 | 前置 | 海外（GitHub） | 国内（Gitee） |
|------|------|------|----------------|---------------|
| 产品管理 | `product-0.2.0.no996-module.zip` | — | [下载](https://github.com/NewbieCheng/no996-desktop-releases/releases/download/modules/product-0.2.0.no996-module.zip) | [下载](https://gitee.com/ZJCACE/no996-desktop-releases/releases/download/modules/product-0.2.0.no996-module.zip) |
| 产品营销专家 | `product-marketing-0.2.0.no996-module.zip` | 产品管理 | [下载](https://github.com/NewbieCheng/no996-desktop-releases/releases/download/modules/product-marketing-0.2.0.no996-module.zip) | [下载](https://gitee.com/ZJCACE/no996-desktop-releases/releases/download/modules/product-marketing-0.2.0.no996-module.zip) |
| 朋友圈运营 | `moments-0.2.0.no996-module.zip` | 产品管理 | [下载](https://github.com/NewbieCheng/no996-desktop-releases/releases/download/modules/moments-0.2.0.no996-module.zip) | [下载](https://gitee.com/ZJCACE/no996-desktop-releases/releases/download/modules/moments-0.2.0.no996-module.zip) |
| 公众号写作 | `wechat-article-0.2.0.no996-module.zip` | — | [下载](https://github.com/NewbieCheng/no996-desktop-releases/releases/download/modules/wechat-article-0.2.0.no996-module.zip) | [下载](https://gitee.com/ZJCACE/no996-desktop-releases/releases/download/modules/wechat-article-0.2.0.no996-module.zip) |
| 合规专家 | `compliance-0.2.0.no996-module.zip` | 产品管理 | [下载](https://github.com/NewbieCheng/no996-desktop-releases/releases/download/modules/compliance-0.2.0.no996-module.zip) | [下载](https://gitee.com/ZJCACE/no996-desktop-releases/releases/download/modules/compliance-0.2.0.no996-module.zip) |
| AI真人口播 | `avatar-video-0.2.0.no996-module.zip` | 产品管理 | [下载](https://github.com/NewbieCheng/no996-desktop-releases/releases/download/modules/avatar-video-0.2.0.no996-module.zip) | [下载](https://gitee.com/ZJCACE/no996-desktop-releases/releases/download/modules/avatar-video-0.2.0.no996-module.zip) |
| 电商视觉 | `ecom-visual-0.2.0.no996-module.zip` | 产品管理 | [下载](https://github.com/NewbieCheng/no996-desktop-releases/releases/download/modules/ecom-visual-0.2.0.no996-module.zip) | [下载](https://gitee.com/ZJCACE/no996-desktop-releases/releases/download/modules/ecom-visual-0.2.0.no996-module.zip) |
| 宣传主视觉 | `promo-key-visual-0.2.0.no996-module.zip` | 产品管理 | [下载](https://github.com/NewbieCheng/no996-desktop-releases/releases/download/modules/promo-key-visual-0.2.0.no996-module.zip) | [下载](https://gitee.com/ZJCACE/no996-desktop-releases/releases/download/modules/promo-key-visual-0.2.0.no996-module.zip) |
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

Current version: **v0.2.0** (2026-09-19, Windows + macOS)

## v0.2.0 highlights

- **Two new optional boards: e-commerce visuals and promo key visuals**: four-step pipelines (input → confirm → plan → tasks) wired to the product library and the unified task rail
- **Unified task rail with logic sunk into the modules**: one-shot generation binds atomically through each board's prepare entry; the task centre shows cross-module progress with jump-back to the source page
- **Talking-head polish**: regeneration chain, subtitles and skins, multimodal channel decision, and usage toasts
- **Navigation and home experience**: the feature map / radial shortcuts stay derived from the same sidebar source, plus splash, home layout, and tile improvements with all five locales synced
- **Both platforms ship together**: Windows and macOS (Apple Silicon) release at the same version

> Full bilingual notes: [v0.2.0 release](https://github.com/NewbieCheng/no996-desktop-releases/releases/tag/v0.2.0). Users on 0.1.6 can install 0.2.0 over the existing app.

## Installers

| Platform | File | GitHub download |
|----------|------|-----------------|
| Windows x64 | `no996-workbench-0.2.0-win-x64.exe` | [download](https://github.com/NewbieCheng/no996-desktop-releases/releases/download/v0.2.0/no996-workbench-0.2.0-win-x64.exe) |
| macOS Apple Silicon | `no996-workbench-0.2.0-mac-arm64.dmg` | [download](https://github.com/NewbieCheng/no996-desktop-releases/releases/download/v0.2.0/no996-workbench-0.2.0-mac-arm64.dmg) |
| Update manifest | `latest.json` | https://github.com/NewbieCheng/no996-desktop-releases/releases/download/latest/latest.json |

Gitee mirrors `latest.json` + `release-history.json` + runtime; full exe/dmg are GitHub-only (100 MB Gitee limit).

### Platform installation notes

- **Windows users**: Run `no996-workbench-0.2.0-win-x64.exe` directly (Windows 10/11 x64).
- **macOS users**: Open `no996-workbench-0.2.0-mac-arm64.dmg` and drag "No996 Workbench" to `Applications`. Requires macOS 12+ on Apple Silicon (M1/M2/M3/M4); first launch automatically downloads the arm64 DSH kernel runtime bundle.
- **In-place upgrade**: Safe to install over earlier releases (such as 0.1.6 Win or 0.1.5 Mac); user accounts, workspace files, and conversation history are preserved.

## DSH runtime (first launch)

Runtime **v1.2.2**, decoupled from the app version and **unchanged this release**.

| Platform | GitHub | Gitee |
|----------|--------|-------|
| Windows x64 | [zip](https://github.com/NewbieCheng/no996-desktop-releases/releases/download/runtime/dsh-runtime-win-x64.zip) | [zip](https://gitee.com/ZJCACE/no996-desktop-releases/releases/download/runtime/dsh-runtime-win-x64.zip) |
| macOS arm64 | [zip](https://github.com/NewbieCheng/no996-desktop-releases/releases/download/runtime/dsh-runtime-macos-arm64.zip) | [zip](https://gitee.com/ZJCACE/no996-desktop-releases/releases/download/runtime/dsh-runtime-macos-arm64.zip) |

Gitee mirrors: `https://gitee.com/ZJCACE/no996-desktop-releases/releases/download/<tag>/<file>`

## Optional modules (in-app marketplace)

Optional boards are **not** bundled in the installer; the in-app marketplace downloads signed packages on demand.

Catalog: <https://github.com/NewbieCheng/no996-desktop-releases/releases/download/modules/catalog.json>

Boards (`product` is the prerequisite of `product-marketing`, `moments`, `compliance`, `avatar-video`, `ecom-visual`, and `promo-key-visual`):

| Board | File | Prerequisite |
|-------|------|--------------|
| Product management | `product-0.2.0.no996-module.zip` | — |
| Product marketing | `product-marketing-0.2.0.no996-module.zip` | product |
| Moments operations | `moments-0.2.0.no996-module.zip` | product |
| WeChat article | `wechat-article-0.2.0.no996-module.zip` | — |
| Compliance review | `compliance-0.2.0.no996-module.zip` | product |
| AI talking-head video | `avatar-video-0.2.0.no996-module.zip` | product |
| E-commerce visuals | `ecom-visual-0.2.0.no996-module.zip` | product |
| Promo key visuals | `promo-key-visual-0.2.0.no996-module.zip` | product |
| Developer starter template | `module-starter-0.2.0.zip` | — |

Modules release: <https://github.com/NewbieCheng/no996-desktop-releases/releases/tag/modules>. No manual install is needed: Settings → Marketplace reads `catalog.json` and installs prerequisites first. `module-starter-*.zip` is a **source starter kit** for third-party developers (unzip and rename the id), not an installable board — it never appears in the marketplace.
