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
