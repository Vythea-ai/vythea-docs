---
title: "Telegram while your computer is off"
description: "Have Vythea Cloud answer your Telegram chat when this computer is off."
---

If Vythea answers you on Telegram (see [Telegram, Discord and Slack](../chat-apps.md)), it does so from your computer. Switch on the relay and Vythea Cloud answers in its place whenever that computer has been off for three minutes.

```sh
vythea cloud relay on
```

- Each message from your paired chat becomes a cloud task, all on one thread, and the answer comes back to the chat.
- As soon as your computer is back and listening, the cloud lets go.
- Each answer is paid from your credit, as any task: see [Costs](costs.md).
- The cloud cannot see your computer's files.

Only Telegram is relayed.

To switch it off:

```sh
vythea cloud relay off
```
