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

### Voice Chat with Agents（2026-11-06）

# Voice Chat with Agents

> 

# Voice Chat with Agents

You can now talk with your agents in a realtime voice call. Describe a change out loud, ask what an agent is working on, and hear updates as the work moves forward.

Voice chat works in the Agents Window, the IDE, on web, and in Cursor for iOS.

## #Start a call

When the agent is idle and the chat input is empty, click the waveform button labeled Start voice chat. It sits where Send usually is, next to the microphone button for dictation.

On iOS, you can also say "Hey Siri, call Cursor" to start a call with a new agent, and mute or hang up from the Lock Screen with a Live Activity.

## #Talk while the agent works

The voice agent listens, replies, and hands coding work to the agent in your chat. While that agent runs, you can keep the conversation going. Ask what changed in a diff, check on a run, search earlier messages and calls with this agent, or switch between workers in a Project that has them.

The coding agent speaks for itself too. It shares short progress notes while it works and a brief answer when it's done, so you usually hear a short update instead of the full written reply.

## #Powered by Grok Voice

Voice chat runs on Grok Voice. Pick from many voices in Voice settings, including Ara, Eve, Leo, Rex, and Sal. With Privacy Mode on, voice chat runs with zero data retention.

## #Voice chat and dictation

Voice chat is separate from dictation, which earlier releases called Voice Mode. Dictation still turns your speech into text in the chat input, and Cmd+Shift+Space still toggles it in the IDE. Voice chat is a two-way conversation where the agent answers out loud.

Update Cursor to try voice chat. Learn more in our docs.

### Build Live Apps in Cursor（2026-11-05）

# Build Live Apps in Cursor

> 

# Build Live Apps in Cursor

Agents have lowered the cost of writing code, but most apps and tools that users build never make it off of localhost.

Now, you can build live apps directly in Cursor and share them with a link. Describe what you want to create and Cursor will handle the rest: build the app, set up a database, configure auth, and deploy it.

With this release, anyone in your org can now build useful tools for their work and share them with teammates. Update Cursor to try it out.

## #How it works

To get started, kick off a cloud agent and tell it explicitly that you want to build an app.

Cursor will scaffold the web app, spin up a Postgres database if needed, set up authentication behind Cursor SSO, and provision hosting. If the app needs to connect to your systems, like a data warehouse, Cursor will ask for the secrets it needs.

When you go to publish your app, you pick a unique domain and Cursor gets you back a live link.

At Cursor, users across sales, operations, legal, finance, and engineering are building internal apps. Some of the most useful ones are:

- Internal ops tools for event registration, account assignments, and desk seating

- Multimedia presentations for customers that combine slides, videos, and interactive demos

- Training, enablement, and onboarding experiences for new hires

- Live dashboards and tools for sales teams to understand their pipeline and opportunities

- Portals to manage engineering services

Cursor can deploy apps from new or existing repos across Cursor Origin and GitHub. Support for other git providers like GitLab is coming soon.

## #Controls and guardrails

When you publish an app, Cursor will run deterministic and agentic security checks to catch common issues, like secrets written in app files or exposed credentials. If a check fails, the agent tells you what it needs to fix. Nothing goes live until the checks pass and you explicitly publish the app.

Team admins can see every app and secret on the team. They can also add their own rules to the security review, approve publishes the review blocked, and unpublish any app.

## #Share with your team

Once the checks pass, Cursor deploys the app to the URL you chose. You can then share your app with specific people, groups, or your entire team, all behind Cursor sign-in. On individual plans, you can also share apps publicly.

You can also provision a Cursor API key if you want a script or Grok Bot to use your app.

## #Get started

This capability is now available on all paid plans with cloud agents enabled. Learn more by reading our docs.

### Agent SDK（2026-10-20）

# Agent SDK

> 

# Agent SDK

The Agent SDK is available today. It allows you to define an agent as a folder of code, test it with evals, and deploy it to Cursor or your own infrastructure.

Run npx @cursor/agent-sdk init ./my-bot, then agent-sdk dev to start the bot locally with a playground. Pass --template to start from a security reviewer, an owners-policy approver, a PR autofixer, or a Linear or Jira triager.

## #Deploy agents wherever you need them

When you're ready to put an agent into use, you can deploy it to Cursor by running agent-sdk deploy from the project directory. The command builds the agent, gives it a URL, and starts it on our infrastructure. You can manage secrets and integrations from the dashboard, while continuing to use the same logs, evals, and playground available locally.

## #Agents as code

An agent is a project. instructions.md is the prompt. Each file in tools/ is one typed action the model can call. skills/ holds procedures the model loads on demand, mcp-connections/ adds tools from MCP servers, and channels/ defines where the bot receives and answers messages. agent-sdk validate checks the project and agent-sdk info prints what was discovered.

## #Channels

Agents wake on pull request, comment, and CI events from GitHub, GitLab, and Bitbucket; on mentions and DMs in Slack; on webhooks from any provider; and on a cron schedule. GitHub events pull through your Cursor account, so no public webhook URL is required. Slack is well-supported out of the box.

Each conversation keeps its own session and a complete record of every message and tool call. Follow-ups on a pull request or Slack thread resume the same session.

## #Evals

An eval sends a fixed message to the bot and asserts on what it did: which tools ran, with what input, and the shape of the reply. Run agent-sdk eval locally or in CI.

agent-sdk github replay <pr-url> turns a real pull request into signed webhook payloads and sends them to the bot, so GitHub-driven bots can be tested without waiting for a push. Add --dry-run --fixtures-dir fixtures/ to save the payloads as eval fixtures.

## #Get started

The Agent SDK is generally available today. Read the docs and get started.

### Cloud Agent Canvases and Environment Improvements（2026-10-16）

# Cloud Agent Canvases and Environment Improvements

> 

# Cloud Agent Canvases and Environment Improvements

## #Canvases from cloud agents

Cloud agents can now build interactive canvases as part of their work. Share a finished canvas with your team by sending its link.

Learn more about sharing canvases.

## #Environments API

The Environments API is now available in beta. Use it to programmatically create and manage the cloud environments your agents run in.

## #Larger, faster environments

Cloud agent environments now support up to 300 repositories. Large environments also load 5x faster.

### Origin App Marketplace（2026-10-13）

# Origin App Marketplace

> 

# Origin App Marketplace

Origin now integrates with over 20 apps for deployments, CI, code review, security, monitoring, and project management, from partners including Cloudflare, Linear, Sentry, and Socket Security.

Starting today, the marketplace is also open to public submissions, so any team building developer tools can publish an app for Origin.

## #Apps for your stack

The marketplace now includes apps for:

- Deployments: Cloudflare, Netlify, Render, Spacelift, and Vercel

- CI: Buildkite, CircleCI, CloudBees, Depot, EngFlow, Namespace, and RWX

- Code review: CodeRabbit, Greptile, and Tenki

- Security: Artemis Security, Semgrep, Socket Security, and Upwind

- Monitoring: Sentry

- Project management: Linear

[图: Origin App Marketplace listing apps across deployments, CI, code review, security, monitoring, and project management]

## #Publish to Marketplace

To submit an app:

- Create an app in your namespace. It stays private to your namespace while you build.

- Build against the Origin API. Apps authenticate with an app JWT and installation access tokens, receive webhook events, and write back check runs, pull request comments, and reviews.

- Make the app public, then submit it from the app's page with a slug, suggested tags, and a demo video. The video should show install, uninstall, and your core product flows.

- We review the submission and list the app once it's approved.

[图: Submitting an app to the Origin App Marketplace]

## #Get started

Try the apps in the Origin App Marketplace today.

Want to build an Origin app? Start with the publishing guide and the Origin API reference.

The Origin Apps plugin can also answer questions from the live Origin API docs and plan a port to Origin for an app you already run.

### Remote control for local agents（2026-10-06）

# Remote control for local agents

> 

# Remote control for local agents

You can now see and reply to the local agents running on your computer from the Cursor iOS app.

## #Get started

Remote Control is on by default for everyone except Enterprise organizations.

Download the Cursor iOS app and sign in. Computers on your account appear in the app automatically. Tap your computer in the app and approve your pairing request in the Cursor desktop app. Your local agents appear in a list. Tap one to see what it's doing or send it a message.

[图: Remote Control for local agents in the Cursor iOS app]

## #Agents keep running on your computer

Remote control doesn't move your agents anywhere. It keeps running on your computer, and the app connects to it. Your computer needs to stay on and online for remote control to work.

## #Keep your computer awake

To stop your computer from sleeping while you're away, turn on "Keep this computer awake" under Remote Control in Cursor's desktop settings. Your computer needs to be plugged in with the lid open.

## #For Enterprise teams

Remote control is on by default, except for Enterprise organizations. Enterprise admins can turn it on in Org settings > Security and identity > Remote control.

Remote control doesn't require cloud agents to work.

Remote control is available today in the Cursor iOS app.

### Rollouts and Security Review（2026-09-23）

# Rollouts and Security Review

> 

# Rollouts and Security Review

Today we're launching two Cursor bots for the last mile of shipping code. Rollouts watches every change as it deploys and reports its health per environment. Security Review reports exploitable bugs on every pull request.

Both are available today on Teams and Enterprise plans.

## #Rollouts

Rollouts attaches a monitor to every pull request and watches the change as it deploys, reporting change health per environment: verified healthy, regression detected, or inconclusive. It's the Cursor version of Firetiger Change Monitors, rebuilt with the Bot Development Kit.

Enable it from the dashboard and connect source control, your deploy system, and your telemetry provider. Rollouts starts watching on the next pull request.

#### #Monitoring plans

When a pull request opens, Rollouts reads the diff and the systems it touches, then writes a monitoring plan as a PR comment. The plan lists the risks it identified, the effect the change is meant to have, the signals it will check, and any gaps in instrumentation that would make the change hard to verify. Edit the plan in the PR and Rollouts uses your version.

#### #Deploy tracking

Rollouts wakes on deploy events for the change's commit and runs the plan against your logs, metrics, and traces. It tracks each environment separately, so a change can be verified in staging and still flagged in production. Rollouts checks the change's intended effect alongside error and latency signals, and reports back on the PR when it reaches a verdict.

#### #Regressions

When Rollouts detects a regression, it names the change it suspects and notifies the author. Depending on configuration, it can also open a revert PR for review or hand the finding to a cloud agent for a fix. Rollouts does not merge or roll back on its own today.

#### #Integrations

Rollouts connects to Origin or GitHub for source control, to your continuous delivery system for deploy events, and to Datadog and other telemetry providers for signals. Feature flag integration is coming soon.

## #Security Review

Security Review is available today. It reads every pull request in the context of the codebase and posts one review comment reporting exploitable bugs. Style and quality stay with Bugbot.

[图: Security Review comment on a pull request reporting an exploitable bug with a severity and proposed fix]

Enable it from the dashboard for the repositories you want reviewed. Draft PRs are skipped.

#### #What it reports

Security Review looks for injection across SQL, command, and template surfaces, along with authentication and authorization bypasses, including checks that a refactor stopped running. It also flags secrets and credentials committed to source, SSRF and unvalidated redirects, unsafe deserialization, and dependency changes that introduce known vulnerabilities. It traces where user input enters and what it passes through.

#### #Findings

Each finding carries a severity, the attack path, and a proposed fix. Dismiss one with a reason and Security Review won't raise it again on that PR.

#### #Team rules

Add rules for your codebase, such as which client external calls must go through or which tables are never queried from a request handler, and Security Review enforces them on every PR.

## #Get started

Rollouts and Security Reviewer are available today on Teams and Enterprise plans. Enable either bot from the automations tab.

For the next 10 days, we're including usage credits so teams can try Rollouts on real changes. Teams and Enterprise customers receive credits for roughly 50 and 500 changes, respectively.

### Cursor Projects（2026-09-10）

# Cursor Projects

> 

# Cursor Projects

Today we're launching Projects in Cursor. Projects lets you take on larger bodies of work, such as a feature, a migration, or a full app. It maintains context over months of work, delegates tasks to thousands of subagents, and performs recurring work without being prompted.

Access Projects from the left-hand nav. The coordinator agent in a project doesn't write code itself; it plans the work, delegates it to agents that implement it, and brings the finished work back to you to check. Coordinators create and manage agents on your behalf, running as many in parallel as the work needs.

## #Powered by Cloud Agents

A Project runs on its own computer in the cloud, so closing your laptop doesn't stop it. When something needs testing on your machine, the coordinator spins up a local agent to run it there.

## #Shared context

You shouldn't have to onboard an agent every time you start a task. Each Project maintains a set of files that sync across every cloud and local machine its agents use. Agents add research and artifacts, along with what they learn about the codebase and how you prefer work to be done. If one agent figures out how to test a service, for example, every future agent can use those instructions. The shared context grows with the Project, making the coordinator more effective over time.

## #Subscriptions

Tell the coordinator agent to watch a Slack channel, run on a schedule, or follow all your PRs. This way it can take action based on signals it detects, without waiting for your prompt.

Connect Slack and point it at a bug-report channel, and it starts delegating each time a bug comes in.

Projects are available in beta and rolling out to all users starting today.

### Self-hosted machines（2026-09-02）

# Self-hosted machines

> 

# Self-hosted machines

Cursor supports self-hosted machines, which let you keep tool execution entirely in your own network.

Your codebase, build outputs, and secrets all stay on internal machines running in your infrastructure, while the agent handles tool calls locally.

[图: Run on menu showing Remote Machines with self-hosted options lambda-test, cloud-demo, and jacks-desktop]

## #Dynamic pool scheduling

My Machines connects a single laptop or VM to your account for personal workflows.

Team pools are named queues of workers for a team or enterprise. Capacity can grow as requests arrive and shrink when workers disconnect, so your self-hosted machines can scale with demand. Pools are not tied to one repository: name the pool, and any available worker can claim the request.

Pools can also hibernate idle machines, then restore within a reconnect window when a follow-up arrives, so you don't keep expensive capacity warm just for the next prompt.

[图: Cloud Agents dashboard listing Self-hosted Machines pools with active and idle worker counts]

## #Run on your sandboxes

Cloud agents can now execute on infrastructure you already use, including from AWS Lambda, Coder, Cloudflare, Daytona, Modal, Namespace, Vercel, and E2B.

## #Computer use on Linux and Mac

Self-hosted workers now support computer use on Linux and Mac. With the right desktop packages, an agent can click, type, take screenshots, and drive the browser. You can watch its desktop or take control from Cursor.

### Start from scratch, without a repo（2026-08-27）

# Start from scratch, without a repo

> 

# Start from scratch, without a repo

Cloud Agents no longer require a connected GitHub or other third-party SCM provider to get started. Prompt from the get-go, then save your work to a Cursor Origin repo.

## #Get started

Select Start from scratch in the repo picker, then prompt the agent. In the background, Cursor creates an Origin repo for you.

[图: Start from scratch in the repo picker]

## #Turn it into a real repo, whenever you want

Once the agent's build is to your liking, click the Create repo button to save your work in an Origin repo. Choose a custom name or pick one of the suggested ones, then set the visibility to private or internal. You'll get a fully scaffolded Origin repo, ready to share or keep building on. Navigate to the Codebase tab to find your repo and access your project.

## #A live preview, right in the browser

Cursor now port-forwards your cloud agent's live environment straight to your browser, so you can preview it and use tools like design mode.

## #Publish your work

Connect a Vercel account and hit publish to get a live URL for what you built.

A Vercel account is required to use the publish feature.

Get started today.

## 数据来源

- 版本/日期/下载链接：Cursor 官方下载 API 与
  [oslook/cursor-ai-downloads](https://github.com/oslook/cursor-ai-downloads) 镜像
- Linux deb/RPM：官方 golden 端点 `api2.cursor.sh/updates/download/golden/...`
- 更新日志：`cursor.com/changelog`（原文存档于 `changelogs/`）

## 自动化

手动触发 `.github/workflows/archive.yml`（workflow_dispatch）即可下载并上传 Release 资产；
已存在的 Release 会跳过，资产用 `--clobber` 覆盖上传。
