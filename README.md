# Vythea docs

How to use [Vythea](https://vythea.com): the AI agent with a window, a terminal, its own cloud and a wallet. Every page is a Markdown file you can read right here on GitHub, in nine languages.

**Start here:** [Getting started](en/getting-started.md)

## Languages

[English](en/getting-started.md) · [简体中文](zh/getting-started.md) · [日本語](ja/getting-started.md) · [한국어](ko/getting-started.md) · [Deutsch](de/getting-started.md) · [Español](es/getting-started.md) · [עברית](he/getting-started.md) · [العربية](ar/getting-started.md) · [Русский](ru/getting-started.md)

English is the source. A page not translated yet is read in English.

## Contents

### Getting started

- [Getting started](en/getting-started.md) — Make an account, install Vythea, sign it in and ask it something.

### Using Vythea

- [The app](en/app.md) — The Vythea window: sessions, models, settings, and what differs on Windows, Linux and macOS.
  - [The parts of the window](en/app/window/layout.md)
    - [First start](en/app/window/setup.md)
    - [The side panel](en/app/window/panel.md)
    - [The command palette](en/app/window/palette.md)
    - [Keyboard shortcuts](en/app/window/shortcuts.md)
    - [Settings](en/app/window/settings.md)
    - [Appearance](en/app/window/appearance.md)
    - [Voice](en/app/window/voice.md)
    - [Quick Entry](en/app/window/quick-entry.md)
    - [Tray, notifications and updates](en/app/window/tray.md)
  - [Asking first and modes](en/app/permissions.md)
  - [What the agent can do](en/app/tools.md)
  - [Sessions](en/app/sessions.md)
  - [Memory](en/app/memory.md)
  - [Skills and your own commands](en/app/skills.md)
  - [Artifacts and previews](en/app/artifacts.md)
  - [Scheduled jobs and loops](en/app/scheduled-jobs.md)
  - [Helpers and workflows](en/app/helpers.md)
- [The terminal](en/terminal.md) — vythea in a terminal: how to start it, its options, and every slash command.
  - [Commands and options](en/terminal/options.md)
  - [Every slash command](en/terminal/slash-commands.md)
  - [Keys in the terminal](en/terminal/keys.md)
  - [Scripts and one-shot runs](en/terminal/scripts.md)
  - [The screen](en/terminal/tui/screen.md)
    - [Approving tool calls](en/terminal/tui/approvals.md)
    - [Lists and pickers](en/terminal/tui/pickers.md)
    - [Selecting and copying](en/terminal/tui/selecting-and-copying.md)
    - [Scrolling](en/terminal/tui/scrolling.md)
    - [Pasting and pictures](en/terminal/tui/pasting-and-pictures.md)
    - [Title and notifications](en/terminal/tui/notifications.md)
    - [Colours and text](en/terminal/tui/look-and-feel.md)
    - [Terminals that work](en/terminal/tui/terminal-support.md)
- [The mobile app](en/mobile/overview.md) — Vythea on iPhone and Android: what it does, and where each part is explained.
  - [Signing in](en/mobile/signing-in.md)
  - [Chats](en/mobile/chats.md)
  - [Models](en/mobile/models.md)
  - [Working offline](en/mobile/offline.md)
    - [Adding a model](en/mobile/add-model.md)
  - [Web search and photos](en/mobile/search-and-photos.md)
  - [Live Activity and notifications](en/mobile/live-activity.md)
  - [Your computer](en/mobile/your-computer.md)
  - [Code sessions](en/mobile/code-sessions.md)
  - [Settings](en/mobile/settings.md)
- [Gateways](en/gateways.md) — Where Vythea gets its models: your Vythea account, OpenAI, OpenRouter, Ollama or any OpenAI-compatible server.
- [Hosted models and credit](en/hosted-models.md) — Vythea's own models: how credit works, what Pro changes, and making images, speech and video.
- [Local models](en/local-models/overview.md) — Running a model on your own computer: why you might, and what you need.
  - [Ollama](en/local-models/ollama.md)
  - [Other local servers](en/local-models/other-servers.md)
  - [Choosing a model](en/local-models/choosing-a-model.md)
  - [Working offline](en/local-models/offline.md)
  - [Serving your accounts to other tools](en/local-models/local-endpoint.md)

### Connect and extend

- [Telegram, Discord and Slack](en/chat-apps.md) — Talking to Vythea from a chat app on your phone, and getting scheduled jobs' reports there.
- [MCP servers](en/mcp.md) — Giving Vythea more tools from MCP servers: adding them, signing in, and choosing which tools it may use.
- [Plugins, hooks and more](en/plugins.md) — Project instructions, plugins, hooks, language servers, and running Vythea inside Zed or JetBrains.
- [Wallet](en/wallet.md) — The wallet the agent pays from: paying sites that ask to be paid, sending money, and the limits you set.

### Cloud and teams

- [Vythea Cloud](en/cloud.md) — Run a task on Vythea's servers, keep a service running, or host a web app with its own link, all from the chat.
  - [Tasks in the cloud](en/cloud/tasks.md)
  - [Services](en/cloud/services.md)
  - [Web apps with a link](en/cloud/web-apps.md)
  - [Looking after them](en/cloud/managing.md)
  - [A terminal in the browser](en/cloud/terminal.md)
  - [Telegram while your computer is off](en/cloud/telegram.md)
  - [What Vythea Cloud costs](en/cloud/costs.md)
  - [Limits](en/cloud/limits.md)
- [Teams](en/teams.md) — One credit pool for 2 to 5 people: seats, spending limits, the audit log, and who pays.

### Account and data

- [The dashboard](en/dashboard.md) — Your account on vythea.com: what each page of the dashboard shows and does.
- [VYTH](en/vyth.md) — VYTH, Vythea's token: your wallet, turning VYTH into credit, and staking it for daily AI.
- [Your data](en/data-and-privacy.md) — What Vythea keeps on your computer, what it sends where, and adding tools from MCP servers.

### Developers

- [Developers](en/developers/overview.md) — Using Vythea from your own programs: scripts, editors and other agents.
  - [Building on Vythea](en/developers/building-on-vythea.md)

### Help

- [Troubleshooting](en/troubleshooting.md) — Checking the setup with vythea doctor, what common errors mean, and where the logs are.

## Help with the docs

Fix a word, add a page or translate one: read [CONTRIBUTING.md](CONTRIBUTING.md), and [GLOSSARY.md](GLOSSARY.md) to translate. Run `node scripts/check.mjs` before you open a pull request.

Something missing or wrong in Vythea itself? Write to support@vythea.com.

The text is published under [CC BY 4.0](LICENSE).
