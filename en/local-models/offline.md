---
title: "Working offline"
description: "What Vythea can and cannot do with no internet connection."
---

With a [local model](overview.md), the agent runs with no internet at all.

| Works offline | Needs the internet |
|---|---|
| chatting with a model on this computer or your network | the Vythea gateway and other [hosted models](../hosted-models.md) |
| reading, writing and searching your files; running commands | signing in, and anything paid from your credit |
| sessions, [memory](../app/memory.md), [skills](../app/skills.md) | web search |
| fetching pages on this computer or the local network | fetching pages on the web |
| | images, speech, transcription and video |
| | [Vythea Cloud](../cloud.md) and [chat apps](../chat-apps.md) |

## When the connection drops

Once a request to the web cannot connect, web search and fetching say at once that they are unavailable for now, naming the host and why, rather than each waiting to fail. They try again after two minutes in a session you are watching, or as soon as a request gets through.

A hosted model fails, saying why in the chat. Pick a local model from the menu and carry on in the same session. To keep going on its own, name a local model with `/fallback`.

## Before you go offline

- Download the models you will want while you still have a connection.
- Check the setup without the network:

  ```sh
  vythea doctor --offline
  ```
