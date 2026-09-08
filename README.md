# 不加班智能团 Desktop · 公开发布

> 本仓库**仅提供安装包与 DSH 运行时组件**，不含源代码。  
> 海外镜像：[GitHub Releases](https://github.com/NewbieCheng/no996-desktop-releases/releases) · 国内镜像：[Gitee Releases](https://gitee.com/ZJCACE/no996-desktop-releases/releases)

当前版本：**v0.1.3**（2026-09-08）

## v0.1.3 更新摘要

- 修复：macOS Apple Silicon 首次启动 DSH Runtime 中 `fs-ext` 被误打成 x86_64，导致 Harness 退出（code=1）
- 新增：runtime 打包后对全部 `.node` 做架构校验
- 改进：重发 `dsh-runtime-macos-arm64.zip`（runtime 版本仍为 **1.0.0**，同名覆盖）；Gitee `runtime` Release 已同步
- 说明：已安装用户可删除 `~/Library/Application Support/no996/runtime/dsh/`（Windows：`%APPDATA%\no996\runtime\dsh\`）后重启拉取新 runtime

---

## 安装包（整包更新）

应用内「检查更新」读取 `latest` 标签下的 `latest.json`；也可手动下载下方安装包。

| 平台 | 文件 | 海外（GitHub） | 国内（Gitee） |
|------|------|----------------|---------------|
| Windows x64 | `no996-workbench-0.1.3-win-x64.exe` | [下载](https://github.com/NewbieCheng/no996-desktop-releases/releases/download/v0.1.3/no996-workbench-0.1.3-win-x64.exe) | 整包超过 Gitee 100 MB 上限，请用 GitHub 或应用内更新 |
| macOS Apple Silicon | `no996-workbench-0.1.3-mac-arm64.dmg` | [下载](https://github.com/NewbieCheng/no996-desktop-releases/releases/download/v0.1.3/no996-workbench-0.1.3-mac-arm64.dmg) | 同上，请用 GitHub |
| 更新清单 | `latest.json` / `release-history.json` | [latest](https://github.com/NewbieCheng/no996-desktop-releases/releases/download/latest/latest.json) · [v0.1.3](https://github.com/NewbieCheng/no996-desktop-releases/releases/download/v0.1.3/latest.json) | [latest](https://gitee.com/ZJCACE/no996-desktop-releases/releases/download/latest/latest.json) · [v0.1.3](https://gitee.com/ZJCACE/no996-desktop-releases/releases/download/v0.1.3/latest.json) |

Release 页面：

- GitHub：[v0.1.3](https://github.com/NewbieCheng/no996-desktop-releases/releases/tag/v0.1.3) · [latest](https://github.com/NewbieCheng/no996-desktop-releases/releases/tag/latest)
- Gitee：[v0.1.3](https://gitee.com/ZJCACE/no996-desktop-releases/releases/tag/v0.1.3) · [latest](https://gitee.com/ZJCACE/no996-desktop-releases/releases/tag/latest)

---

## DSH 运行时组件（首次启动下载）

安装包内**不包含** DSH 内核；首次启动按 manifest 自动下载。文件名固定，与 App 版本解耦（runtime **v1.0.0**）。

| 平台 | 文件 | 海外（GitHub） | 国内（Gitee） |
|------|------|----------------|---------------|
| Windows x64 | `dsh-runtime-win-x64.zip` | [下载](https://github.com/NewbieCheng/no996-desktop-releases/releases/download/runtime/dsh-runtime-win-x64.zip) | [下载](https://gitee.com/ZJCACE/no996-desktop-releases/releases/download/runtime/dsh-runtime-win-x64.zip) |
| macOS arm64 | `dsh-runtime-macos-arm64.zip` | [下载](https://github.com/NewbieCheng/no996-desktop-releases/releases/download/runtime/dsh-runtime-macos-arm64.zip) | [下载](https://gitee.com/ZJCACE/no996-desktop-releases/releases/download/runtime/dsh-runtime-macos-arm64.zip) |
| Manifest | `dsh-runtime-*.manifest.json` | [runtime Release](https://github.com/NewbieCheng/no996-desktop-releases/releases/tag/runtime) | [runtime Release](https://gitee.com/ZJCACE/no996-desktop-releases/releases/tag/runtime) |

Runtime Release 页面：

- GitHub：<https://github.com/NewbieCheng/no996-desktop-releases/releases/tag/runtime>
- Gitee：<https://gitee.com/ZJCACE/no996-desktop-releases/releases/tag/runtime>

---

## 许可

本软件为闭源商业软件，最终用户许可协议（EULA）详见安装包内的 `LICENSE.txt`。

© 2026 不加班智能团

---

# No996 Workbench Desktop · Public Releases

> Installers and DSH runtime only — **no source code**.  
> Overseas: [GitHub Releases](https://github.com/NewbieCheng/no996-desktop-releases/releases) · China mirror: [Gitee Releases](https://gitee.com/ZJCACE/no996-desktop-releases/releases)

Current version: **v0.1.3** (2026-09-08)

## v0.1.3 highlights

- Fix: macOS Apple Silicon first-run DSH Runtime `fs-ext` was built as x86_64, crashing Harness (exit code 1)
- Add: post-pack native `.node` arch verification
- Republished `dsh-runtime-macos-arm64.zip` (runtime **v1.0.0**, same filename); Gitee `runtime` release synced
- If you cached the bad runtime: delete `runtime/dsh/` and restart, or install app **≥ 0.1.3**

## Installers

| Platform | GitHub download |
|----------|-----------------|
| Windows x64 | https://github.com/NewbieCheng/no996-desktop-releases/releases/download/v0.1.3/no996-workbench-0.1.3-win-x64.exe |
| macOS Apple Silicon | https://github.com/NewbieCheng/no996-desktop-releases/releases/download/v0.1.3/no996-workbench-0.1.3-mac-arm64.dmg |
| Update manifest | https://github.com/NewbieCheng/no996-desktop-releases/releases/download/latest/latest.json |

## DSH runtime (first launch)

| Platform | GitHub | Gitee |
|----------|--------|-------|
| Windows x64 | [zip](https://github.com/NewbieCheng/no996-desktop-releases/releases/download/runtime/dsh-runtime-win-x64.zip) | [zip](https://gitee.com/ZJCACE/no996-desktop-releases/releases/download/runtime/dsh-runtime-win-x64.zip) |
| macOS arm64 | [zip](https://github.com/NewbieCheng/no996-desktop-releases/releases/download/runtime/dsh-runtime-macos-arm64.zip) | [zip](https://gitee.com/ZJCACE/no996-desktop-releases/releases/download/runtime/dsh-runtime-macos-arm64.zip) |

Gitee mirrors: `https://gitee.com/ZJCACE/no996-desktop-releases/releases/download/<tag>/<file>`
