# Cursor Releases 存档

Cursor 编辑器 3.23–3.30 各版本的全平台安装包存档（GitHub Releases 附件），
以及 cursor-byok 上游版本的 Release 资产存档。

## 版本与发布日期

| 版本 | 发布日期 | 平台 |
|---|---|---|
| 3.30.14 | 2026-11-13 | Win x64/ARM64 (System/User), macOS Universal/x64/ARM64, Linux AppImage/deb/RPM x64/ARM64 |
| 3.30.8 | 2026-11-12 | 同上 |
| 3.29.15 | 2026-11-09 | 同上 |
| 3.29.9 | 2026-11-05 | 同上 |
| 3.28.7 | 2026-11-03 | 同上 |
| 3.28.5 | 2026-10-28 | 同上 |
| 3.27.22 | 2026-10-27 | 同上 |
| 3.27.14 | 2026-10-25 | 同上 |
| 3.27.12 | 2026-10-23 | 同上 |
| 3.27.6 | 2026-10-21 | 同上 |
| 3.26.16 | 2026-10-21 | 同上 |
| 3.26.13 | 2026-10-20 | 同上 |
| 3.25.9 | 2026-10-17 | 同上 |
| 3.25.6 | 2026-10-15 | 同上 |
| 3.24.18 | 2026-10-13 | 同上 |
| 3.24.12 | 2026-10-09 | 同上 |
| 3.24.9 | 2026-10-08 | 同上 |
| 3.24.7 | 2026-10-08 | 同上 |
| 3.23.23 | 2026-10-05 | 同上 |
| 3.23.12 | 2026-10-01 | 同上 |
| 3.23.10 | 2026-10-01 | 同上 |

## 更新日志

官方更新日志：<https://cursor.com/changelog>

| 日期 | 条目 |
|---|---|
| 2026-11-06 | [Voice Chat with Agents](https://cursor.com/changelog/voice-chat) |
| 2026-11-05 | [Build Live Apps](https://cursor.com/changelog/build-live-apps) |
| 2026-10-20 | [Agent SDK](https://cursor.com/changelog/agent-sdk) |
| 2026-10-16 | [Cloud Agent Canvases and Environments](https://cursor.com/changelog/cloud-agent-canvases-and-environments) |
| 2026-10-13 | [Origin App Marketplace](https://cursor.com/changelog/origin-app-marketplace) |
| 2026-10-06 | [Remote Control Local Agents](https://cursor.com/changelog/remote-control-local-agents) |
| 2026-09-23 | [Rollouts and Security Reviewer](https://cursor.com/changelog/rollouts-and-security-reviewer) |
| 2026-09-10 | [Projects](https://cursor.com/changelog/projects) |
| 2026-09-02 | [Self-hosted Machines](https://cursor.com/changelog/self-hosted-machines) |
| 2026-08-27 | [Start from Scratch](https://cursor.com/changelog/start-from-scratch) |

各 Release 的说明里附有发布日期 ±3 天内对应的更新日志链接。

## 数据来源

- 版本/日期/下载链接：Cursor 官方下载 API 与
  [oslook/cursor-ai-downloads](https://github.com/oslook/cursor-ai-downloads) 镜像
- Linux deb/RPM：官方 golden 端点 `api2.cursor.sh/updates/download/golden/...`
- 更新日志：`cursor.com/changelog`（原文存档于 `changelogs/`）

## 自动化

手动触发 `.github/workflows/archive.yml`（workflow_dispatch）即可下载并上传 Release 资产；
已存在的 Release 会跳过，资产用 `--clobber` 覆盖上传。
