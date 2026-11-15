# Cursor Releases 存档

Cursor 编辑器 3.23–3.30 各版本的全平台安装包存档（GitHub Releases 附件），
以及 cursor-byok 上游版本的 Release 资产存档。

## 版本与发布日期

| 版本 | 发布日期 | 平台 | 对应更新日志 |
|---|---|---|---|
| 3.30.14 | 2026-11-13 | 全平台 | — |
| 3.30.8 | 2026-11-12 | 全平台 | — |
| 3.29.15 | 2026-11-09 | 全平台 | [Voice Chat with Agents（2026-11-06）](https://cursor.com/changelog/voice-chat) |
| 3.29.9 | 2026-11-05 | 全平台 | [Build Live Apps in Cursor（2026-11-05）](https://cursor.com/changelog/build-live-apps)；[Voice Chat with Agents（2026-11-06）](https://cursor.com/changelog/voice-chat) |
| 3.28.7 | 2026-11-03 | 全平台 | [Build Live Apps in Cursor（2026-11-05）](https://cursor.com/changelog/build-live-apps)；[Voice Chat with Agents（2026-11-06）](https://cursor.com/changelog/voice-chat) |
| 3.28.5 | 2026-10-28 | 全平台 | — |
| 3.27.22 | 2026-10-27 | 全平台 | — |
| 3.27.14 | 2026-10-25 | 全平台 | — |
| 3.27.12 | 2026-10-23 | 全平台 | [Agent SDK（2026-10-20）](https://cursor.com/changelog/agent-sdk) |
| 3.27.6 | 2026-10-21 | 全平台 | [Agent SDK（2026-10-20）](https://cursor.com/changelog/agent-sdk) |
| 3.26.16 | 2026-10-21 | 全平台 | [Agent SDK（2026-10-20）](https://cursor.com/changelog/agent-sdk) |
| 3.26.13 | 2026-10-20 | 全平台 | [Agent SDK（2026-10-20）](https://cursor.com/changelog/agent-sdk) |
| 3.25.9 | 2026-10-17 | 全平台 | [Cloud Agent Canvases and Environment Improvements（2026-10-16）](https://cursor.com/changelog/cloud-agent-canvases-and-environments)；[Agent SDK（2026-10-20）](https://cursor.com/changelog/agent-sdk) |
| 3.25.6 | 2026-10-15 | 全平台 | [Origin App Marketplace（2026-10-13）](https://cursor.com/changelog/origin-app-marketplace)；[Cloud Agent Canvases and Environment Improvements（2026-10-16）](https://cursor.com/changelog/cloud-agent-canvases-and-environments) |
| 3.24.18 | 2026-10-13 | 全平台 | [Origin App Marketplace（2026-10-13）](https://cursor.com/changelog/origin-app-marketplace)；[Cloud Agent Canvases and Environment Improvements（2026-10-16）](https://cursor.com/changelog/cloud-agent-canvases-and-environments) |
| 3.24.12 | 2026-10-09 | 全平台 | [Remote control for local agents（2026-10-06）](https://cursor.com/changelog/remote-control-local-agents) |
| 3.24.9 | 2026-10-08 | 全平台 | [Remote control for local agents（2026-10-06）](https://cursor.com/changelog/remote-control-local-agents) |
| 3.24.7 | 2026-10-08 | 全平台 | [Remote control for local agents（2026-10-06）](https://cursor.com/changelog/remote-control-local-agents) |
| 3.23.23 | 2026-10-05 | 全平台 | [Remote control for local agents（2026-10-06）](https://cursor.com/changelog/remote-control-local-agents) |
| 3.23.12 | 2026-10-01 | 全平台 | — |
| 3.23.10 | 2026-10-01 | 全平台 | — |

各 Release 的说明中附有对应更新日志的完整正文。

## 数据来源

- 版本/日期/下载链接：Cursor 官方下载 API 与
  [oslook/cursor-ai-downloads](https://github.com/oslook/cursor-ai-downloads) 镜像
- Linux deb/RPM：官方 golden 端点 `api2.cursor.sh/updates/download/golden/...`
- 更新日志：`cursor.com/changelog`（原文存档于 `changelogs/`）

## 自动化

手动触发 `.github/workflows/archive.yml`（workflow_dispatch）即可下载并上传 Release 资产；
已存在的 Release 会跳过，资产用 `--clobber` 覆盖上传。
