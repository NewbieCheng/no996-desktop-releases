# 不加班智能团 Desktop · 公开发布

> 本仓库**仅提供安装包与 DSH 运行时组件**，不含源代码。  
> 海外镜像：[GitHub Releases](https://github.com/NewbieCheng/no996-desktop-releases/releases) · 国内镜像：[Gitee Releases](https://gitee.com/ZJCACE/no996-desktop-releases/releases)

当前版本：**v0.1.6**（2026-09-16，仅 Windows；macOS 待定）

## v0.1.6 更新摘要

- **新增可选板块「AI真人口播」**：真人出镜视频走五步流水线产出 9:16 竖屏口播成片；7 个音色可试听、5 套成片皮肤、字幕自动挑系统中文字体，未装 FFmpeg 明确提示
- **真人口播双通道计费**：自备厂商直连免费 / 平台专线按次计费，界面显示每条通道当前扣多少积分与剩余余额，积分不足开跑前拦下；「重新生成」在素材未变时复用对口型中间片
- **设置 → 记忆与隐私**：记忆总闸、全局自动写入、逐板块注入与写入档集中一页；关闭总闸是真的关掉（内核不再挂载记忆插件），关闭前提示需重启内核
- **技能 × 板块关联**：技能页说明每个技能在哪些板块用得上，区分「对话可用」（可开关）与「生成固化」（模板锁定，不可改），标注来源并可一键恢复默认；会话内只暴露本板块技能
- **模型页重做**：平台专线 / 自定义 API 切换 + 语言 / 视频 / 图片 / 语音四类标签；新增专线模型列表弹窗；非文本模型不再显示上下文与推理档位
- **顶栏全局搜索**：Ctrl/⌘+K 打开，支持 `>` 指令 / `#` 板块 / `@` 对话三种前缀
- **主区多标签 dock**：多标签拖动重排 + 左右分屏；刷新保留激活标签
- **会话历史**：「简介 / 详细」视图、按工作区筛选、导出与删除、虚拟滚动；修复会话边跑边重开只显示最近一条
- **首页**：便签升级为带优先级的清单（旧便签自动迁移）、磁贴可就地增删与拖拽排序、新增「整理布局」
- **安全**：平台专线 Key 只在 Main 授权的会话回合内发放，直连内核拿不到；内核日志统一脱敏
- **修复**：Windows 打包因 `pnpm list` 触发 EMFILE；模型写错记忆参数不再弹会报错的审批卡

> 完整中英双语说明见 [v0.1.6 Release](https://github.com/NewbieCheng/no996-desktop-releases/releases/tag/v0.1.6)；此前下载过 0.1.5 的用户可直接安装 0.1.6 覆盖。

> **macOS 用户请注意**：0.1.6 只发布 Windows 安装包，macOS 仍停在 v0.1.5。
> 应用内「检查更新」会显示已是最新，不会提示本版——无需理会，等 macOS 版发布后正常更新即可。

---

## 安装包（整包更新）

应用内「设置 → 通用 → 检查更新」读取 `latest` 标签下的 `latest.json`；也可手动下载下方安装包。

| 平台 | 文件 | 海外（GitHub） | 国内（Gitee） |
|------|------|----------------|---------------|
| Windows x64 | `no996-workbench-0.1.6-win-x64.exe` | [下载](https://github.com/NewbieCheng/no996-desktop-releases/releases/download/v0.1.6/no996-workbench-0.1.6-win-x64.exe) | 整包超过 Gitee 100 MB 上限，请用 GitHub 或应用内更新 |
| macOS Apple Silicon | — | **本版暂缓发布**，仍为 [v0.1.5](https://github.com/NewbieCheng/no996-desktop-releases/releases/download/v0.1.5/no996-workbench-0.1.5-mac-arm64.dmg) | 同上，请用 GitHub |
| 更新清单 | `latest.json` / `release-history.json` | [latest](https://github.com/NewbieCheng/no996-desktop-releases/releases/download/latest/latest.json) · [v0.1.6](https://github.com/NewbieCheng/no996-desktop-releases/releases/download/v0.1.6/latest.json) | [latest](https://gitee.com/ZJCACE/no996-desktop-releases/releases/download/latest/latest.json) · [v0.1.6](https://gitee.com/ZJCACE/no996-desktop-releases/releases/download/v0.1.6/latest.json) |

Release 页面：

- GitHub：[v0.1.6](https://github.com/NewbieCheng/no996-desktop-releases/releases/tag/v0.1.6) · [latest](https://github.com/NewbieCheng/no996-desktop-releases/releases/tag/latest)
- Gitee：[v0.1.6](https://gitee.com/ZJCACE/no996-desktop-releases/releases/tag/v0.1.6) · [latest](https://gitee.com/ZJCACE/no996-desktop-releases/releases/tag/latest)

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

安装包**不含**可选板块；应用内「插件市场」按需下载签名包，与 App 版本解耦（板块版本 **0.1.0**）。

| 板块 | 文件 | 前置 | 海外（GitHub） | 国内（Gitee） |
|------|------|------|----------------|---------------|
| 产品管理 | `product-0.1.0.no996-module.zip` | — | [下载](https://github.com/NewbieCheng/no996-desktop-releases/releases/download/modules/product-0.1.0.no996-module.zip) | [下载](https://gitee.com/ZJCACE/no996-desktop-releases/releases/download/modules/product-0.1.0.no996-module.zip) |
| 产品营销专家 | `product-marketing-0.1.0.no996-module.zip` | 产品管理 | [下载](https://github.com/NewbieCheng/no996-desktop-releases/releases/download/modules/product-marketing-0.1.0.no996-module.zip) | [下载](https://gitee.com/ZJCACE/no996-desktop-releases/releases/download/modules/product-marketing-0.1.0.no996-module.zip) |
| 朋友圈运营 | `moments-0.1.0.no996-module.zip` | 产品管理 | [下载](https://github.com/NewbieCheng/no996-desktop-releases/releases/download/modules/moments-0.1.0.no996-module.zip) | [下载](https://gitee.com/ZJCACE/no996-desktop-releases/releases/download/modules/moments-0.1.0.no996-module.zip) |
| 公众号写作 | `wechat-article-0.1.0.no996-module.zip` | — | [下载](https://github.com/NewbieCheng/no996-desktop-releases/releases/download/modules/wechat-article-0.1.0.no996-module.zip) | [下载](https://gitee.com/ZJCACE/no996-desktop-releases/releases/download/modules/wechat-article-0.1.0.no996-module.zip) |
| 合规专家 | `compliance-0.1.0.no996-module.zip` | 产品管理 | [下载](https://github.com/NewbieCheng/no996-desktop-releases/releases/download/modules/compliance-0.1.0.no996-module.zip) | [下载](https://gitee.com/ZJCACE/no996-desktop-releases/releases/download/modules/compliance-0.1.0.no996-module.zip) |
| AI真人口播 | `avatar-video-0.1.0.no996-module.zip` | 产品管理 | [下载](https://github.com/NewbieCheng/no996-desktop-releases/releases/download/modules/avatar-video-0.1.0.no996-module.zip) | [下载](https://gitee.com/ZJCACE/no996-desktop-releases/releases/download/modules/avatar-video-0.1.0.no996-module.zip) |
| 目录 | `catalog.json` | — | [catalog](https://github.com/NewbieCheng/no996-desktop-releases/releases/download/modules/catalog.json) | [catalog](https://gitee.com/ZJCACE/no996-desktop-releases/releases/download/modules/catalog.json) |
| 板块开发起步模板 | `module-starter-0.1.0.zip` | — | [下载](https://github.com/NewbieCheng/no996-desktop-releases/releases/download/modules/module-starter-0.1.0.zip) | [下载](https://gitee.com/ZJCACE/no996-desktop-releases/releases/download/modules/module-starter-0.1.0.zip) |

板块 Release 页面：<https://github.com/NewbieCheng/no996-desktop-releases/releases/tag/modules>

手动安装不需要：应用内「设置 → 插件市场」会自动读取 `catalog.json`，先装前置再装所选板块。
`module-starter-*.zip` 是给第三方开发者的**源码起步包**（解压后改 id 即成新板块），不是安装项，不会出现在插件市场里。

---

## 许可

本软件为闭源商业软件，最终用户许可协议（EULA）详见安装包内的 `LICENSE.txt`。

© 2026 不加班智能团

---

# No996 Workbench Desktop · Public Releases

> Installers and DSH runtime only — **no source code**.  
> Overseas: [GitHub Releases](https://github.com/NewbieCheng/no996-desktop-releases/releases) · China mirror: [Gitee Releases](https://gitee.com/ZJCACE/no996-desktop-releases/releases)

Current version: **v0.1.6** (2026-09-16, Windows only; macOS pending)

## v0.1.6 highlights

- **New optional module: AI talking-head video**: a real on-camera clip becomes a 9:16 vertical talking-head video through a five-step pipeline; 7 previewable voices, 5 output skins, automatic Chinese system font, and a clear message when FFmpeg is missing
- **Dual-channel billing for talking-head video**: bring-your-own provider (free) or the platform line (billed per call), with each channel's current points cost and your remaining balance shown; insufficient balance is blocked before the run. "Regenerate" reuses the lip-sync intermediate when the source is unchanged
- **Settings → Memory & privacy**: the master switch, global auto-write, and per-module inject/write levels on one page; turning the master switch off really turns it off (the kernel no longer mounts the memory plugin) with a restart warning
- **Skill ↔ module bindings**: the skills page states which modules each skill is used in, distinguishing "available in chat" (switchable) from "pinned by generation" (locked by the module's template), labelled with its source and resettable to default; a session only exposes that module's skills
- **Models page reworked**: a platform-line / custom-API switch plus language, video, image, and speech tabs; a new dialog lists the line's candidate models; non-text models no longer show context or reasoning level
- **Global title-bar search**: Ctrl/⌘+K with `>` commands, `#` modules, and `@` conversations
- **Multi-tab main dock**: drag to reorder tabs and split into two panes; the active tab survives a reload
- **Conversation history**: brief/detailed views, workspace filtering, export and delete, virtualized scrolling; fixed the merge bug where reopening a running conversation showed only the latest turn
- **Home**: notes became a checklist with priorities (old notes migrate automatically), tiles edit in place with drag reordering, and a new "tidy layout"
- **Security**: platform line keys are released only inside a Main-authorized conversation turn, so a direct kernel connection cannot obtain one; kernel logs are redacted
- **Fixes**: Windows packing failed with EMFILE because of `pnpm list`; a malformed memory tool call no longer produces an approval card that fails on click

> Full bilingual notes: [v0.1.6 release](https://github.com/NewbieCheng/no996-desktop-releases/releases/tag/v0.1.6). Users on 0.1.5 can install 0.1.6 over the existing app.

> **macOS users**: 0.1.6 ships a Windows installer only and macOS stays on v0.1.5.
> The in-app update check will report that you are up to date and will not offer this version — nothing to do, just update normally once the macOS build ships.

## Installers

| Platform | File | GitHub download |
|----------|------|-----------------|
| Windows x64 | `no996-workbench-0.1.6-win-x64.exe` | [download](https://github.com/NewbieCheng/no996-desktop-releases/releases/download/v0.1.6/no996-workbench-0.1.6-win-x64.exe) |
| macOS Apple Silicon | — | **deferred this version**; still [v0.1.5](https://github.com/NewbieCheng/no996-desktop-releases/releases/download/v0.1.5/no996-workbench-0.1.5-mac-arm64.dmg) |
| Update manifest | `latest.json` | https://github.com/NewbieCheng/no996-desktop-releases/releases/download/latest/latest.json |

Gitee mirrors `latest.json` + `release-history.json` + runtime; full exe/dmg are GitHub-only (100 MB Gitee limit).

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

Boards (`product` is the prerequisite of `product-marketing`, `moments`, `compliance`, and `avatar-video`):

| Board | File | Prerequisite |
|-------|------|--------------|
| Product management | `product-0.1.0.no996-module.zip` | — |
| Product marketing | `product-marketing-0.1.0.no996-module.zip` | product |
| Moments operations | `moments-0.1.0.no996-module.zip` | product |
| WeChat article | `wechat-article-0.1.0.no996-module.zip` | — |
| Compliance review | `compliance-0.1.0.no996-module.zip` | product |
| AI talking-head video | `avatar-video-0.1.0.no996-module.zip` | product |
| Developer starter template | `module-starter-0.1.0.zip` | — |

Modules release: <https://github.com/NewbieCheng/no996-desktop-releases/releases/tag/modules>. No manual install is needed: Settings → Marketplace reads `catalog.json` and installs prerequisites first. `module-starter-*.zip` is a **source starter kit** for third-party developers (unzip and rename the id), not an installable board — it never appears in the marketplace.
