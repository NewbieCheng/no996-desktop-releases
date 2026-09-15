# 不加班智能团 Desktop · 公开发布

> 本仓库**仅提供安装包与 DSH 运行时组件**，不含源代码。  
> 海外镜像：[GitHub Releases](https://github.com/NewbieCheng/no996-desktop-releases/releases) · 国内镜像：[Gitee Releases](https://gitee.com/ZJCACE/no996-desktop-releases/releases)

当前版本：**v0.1.5**（2026-09-15）

## v0.1.5 更新摘要

- **开发者模式与本地免签安装**：设置 → 插件市场 → 板块 可开启开发者模式，拖入 `.zip` 或用「从 zip 安装 / 选择已解压目录」安装未签名板块；除验签外，条目数 / 单文件 / 总解压上限、路径逃逸、符号链接、重复与大小写冲突路径、清单形状都与官方安装逐条相同
- **板块卸载**：插件市场 → 本机扩展 区分内置 / 已装 / 开发源；已装与开发源可卸载，内置只显示徽标；开发源卸载删 `modules/<id>/dist` 构建产物并记入 `disabledIds`；仍被依赖时拒绝删除并列出依赖方
- **Runtime 卸载**：设置 → 版本信息 →「智能内核 Runtime」新增卸载按钮，先停内核再删下载与缓存 zip，状态回到「需下载」
- **官方 Agent 预设锁定**：「官方拓展」分组带官方徽标、不提供删除按钮
- **补齐本版包含的上一批修复**：Windows 安装包黑屏「内核启动失败」、内核残留写锁启动失败、Gitee 镜像同步超时不再中断发布链、工作区上下文头与来源感知「回到对话」，详见 0.1.4 小节

> 完整中英双语说明见 [v0.1.5 Release](https://github.com/NewbieCheng/no996-desktop-releases/releases/tag/v0.1.5)；此前下载过 0.1.3 / 0.1.4 的用户可直接安装 0.1.5 覆盖。

---

## 安装包（整包更新）

应用内「设置 → 通用 → 检查更新」读取 `latest` 标签下的 `latest.json`；也可手动下载下方安装包。

| 平台 | 文件 | 海外（GitHub） | 国内（Gitee） |
|------|------|----------------|---------------|
| Windows x64 | `no996-workbench-0.1.5-win-x64.exe` | [下载](https://github.com/NewbieCheng/no996-desktop-releases/releases/download/v0.1.5/no996-workbench-0.1.5-win-x64.exe) | 整包超过 Gitee 100 MB 上限，请用 GitHub 或应用内更新 |
| macOS Apple Silicon | `no996-workbench-0.1.5-mac-arm64.dmg` | [下载](https://github.com/NewbieCheng/no996-desktop-releases/releases/download/v0.1.5/no996-workbench-0.1.5-mac-arm64.dmg) | 同上，请用 GitHub |
| 更新清单 | `latest.json` / `release-history.json` | [latest](https://github.com/NewbieCheng/no996-desktop-releases/releases/download/latest/latest.json) · [v0.1.5](https://github.com/NewbieCheng/no996-desktop-releases/releases/download/v0.1.5/latest.json) | [latest](https://gitee.com/ZJCACE/no996-desktop-releases/releases/download/latest/latest.json) · [v0.1.5](https://gitee.com/ZJCACE/no996-desktop-releases/releases/download/v0.1.5/latest.json) |

Release 页面：

- GitHub：[v0.1.5](https://github.com/NewbieCheng/no996-desktop-releases/releases/tag/v0.1.5) · [latest](https://github.com/NewbieCheng/no996-desktop-releases/releases/tag/latest)
- Gitee：[v0.1.5](https://gitee.com/ZJCACE/no996-desktop-releases/releases/tag/v0.1.5) · [latest](https://gitee.com/ZJCACE/no996-desktop-releases/releases/tag/latest)

---

## DSH 运行时组件（首次启动下载）

安装包内**不包含** DSH 内核；首次启动按 manifest 自动下载。文件名固定，与 App 版本解耦（runtime **v1.2.2**）。

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
| 目录 | `catalog.json` | — | [catalog](https://github.com/NewbieCheng/no996-desktop-releases/releases/download/modules/catalog.json) | [catalog](https://gitee.com/ZJCACE/no996-desktop-releases/releases/download/modules/catalog.json) |

板块 Release 页面：<https://github.com/NewbieCheng/no996-desktop-releases/releases/tag/modules>

手动安装不需要：应用内「设置 → 插件市场」会自动读取 `catalog.json`，先装前置再装所选板块。

---

## 许可

本软件为闭源商业软件，最终用户许可协议（EULA）详见安装包内的 `LICENSE.txt`。

© 2026 不加班智能团

---

# No996 Workbench Desktop · Public Releases

> Installers and DSH runtime only — **no source code**.  
> Overseas: [GitHub Releases](https://github.com/NewbieCheng/no996-desktop-releases/releases) · China mirror: [Gitee Releases](https://gitee.com/ZJCACE/no996-desktop-releases/releases)

Current version: **v0.1.5** (2026-09-15)

## v0.1.5 highlights

- **Developer mode and local unsigned install**: Settings → Marketplace → Modules turns on developer mode; drop a `.zip` onto the section or use "install from zip / choose an unpacked directory". Beyond skipping the signature check, entry count, per-file and total uncompressed limits, path escape, symlinks, duplicate and case-conflicting paths, and the manifest fields are enforced exactly as for an official install
- **Module uninstall**: Marketplace → Local extensions distinguishes built-in, installed, and dev-source modules; installed and dev-source ones uninstall, built-ins show only a badge; uninstalling a dev-source module deletes the `modules/<id>/dist` build output and records the id in `disabledIds`; a module still required by another is refused with its dependents listed
- **Runtime uninstall**: Settings → Version info → the "Kernel Runtime" row gained an uninstall button; it stops the kernel first, then removes the downloaded install and cached zip and returns to "needs download"
- **Bundled Agent presets are locked**: an "official extensions" group with an official badge and no delete button
- **Includes the previous batch of fixes**: the Windows installer opening to a black "kernel start failed" window, kernel start failing on a leftover writer lock, a Gitee mirror timeout no longer aborting the release chain, and the workspace context header with origin-aware "back to conversation" — see the 0.1.4 section

> Full bilingual notes: [v0.1.5 release](https://github.com/NewbieCheng/no996-desktop-releases/releases/tag/v0.1.5). Users on 0.1.3 / 0.1.4 can install 0.1.5 over the existing app.

## Installers

| Platform | File | GitHub download |
|----------|------|-----------------|
| Windows x64 | `no996-workbench-0.1.5-win-x64.exe` | [download](https://github.com/NewbieCheng/no996-desktop-releases/releases/download/v0.1.5/no996-workbench-0.1.5-win-x64.exe) |
| macOS Apple Silicon | `no996-workbench-0.1.5-mac-arm64.dmg` | [download](https://github.com/NewbieCheng/no996-desktop-releases/releases/download/v0.1.5/no996-workbench-0.1.5-mac-arm64.dmg) |
| Update manifest | `latest.json` | https://github.com/NewbieCheng/no996-desktop-releases/releases/download/latest/latest.json |

Gitee mirrors `latest.json` + `release-history.json` + runtime; full exe/dmg are GitHub-only (100 MB Gitee limit).

## DSH runtime (first launch)

Runtime **v1.2.2**, decoupled from the app version.

| Platform | GitHub | Gitee |
|----------|--------|-------|
| Windows x64 | [zip](https://github.com/NewbieCheng/no996-desktop-releases/releases/download/runtime/dsh-runtime-win-x64.zip) | [zip](https://gitee.com/ZJCACE/no996-desktop-releases/releases/download/runtime/dsh-runtime-win-x64.zip) |
| macOS arm64 | [zip](https://github.com/NewbieCheng/no996-desktop-releases/releases/download/runtime/dsh-runtime-macos-arm64.zip) | [zip](https://gitee.com/ZJCACE/no996-desktop-releases/releases/download/runtime/dsh-runtime-macos-arm64.zip) |

Gitee mirrors: `https://gitee.com/ZJCACE/no996-desktop-releases/releases/download/<tag>/<file>`

## Optional modules (in-app marketplace)

Optional boards are **not** bundled in the installer; the in-app marketplace downloads signed packages on demand.

Catalog: <https://github.com/NewbieCheng/no996-desktop-releases/releases/download/modules/catalog.json>

Boards (`product` is the prerequisite of `product-marketing`, `moments`, and `compliance`):

| Board | File | Prerequisite |
|-------|------|--------------|
| Product management | `product-0.1.0.no996-module.zip` | — |
| Product marketing | `product-marketing-0.1.0.no996-module.zip` | product |
| Moments operations | `moments-0.1.0.no996-module.zip` | product |
| WeChat article | `wechat-article-0.1.0.no996-module.zip` | — |
| Compliance review | `compliance-0.1.0.no996-module.zip` | product |

Modules release: <https://github.com/NewbieCheng/no996-desktop-releases/releases/tag/modules>. No manual install is needed: Settings → Marketplace reads `catalog.json` and installs prerequisites first.
