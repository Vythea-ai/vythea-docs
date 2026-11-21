---
title: "Memory"
description: "What Vythea remembers between sessions, when it saves, where it keeps it, and how to see and change it."
---

Vythea keeps notes between sessions in plain files on your computer. You can read and change all of them.

## What it keeps

| Memory | Holds |
|---|---|
| **About you** (`USER.md`) | what Vythea knows about you |
| **Its notes** (`MEMORY.md`) | its own notes, for every chat |
| **Project** | notes on one project, kept in your data folder, never in the repository |
| **This chat** | notes for one chat alone; they go when the chat is deleted |
| **Soul** (`SOUL.md`) | who Vythea is, in your words; optional |

Once `SOUL.md` has something in it, it takes the place of Vythea's own first line in every request. A project's `AGENTS.md` is read as that project's instructions; see [Project instructions](../plugins.md).

Memory refuses keys and passwords, and text that tries to give Vythea orders.

## When it saves

By default, Vythea saves to memory only when you ask. You can choose, for each chat or for all of them:

| Choice | Saves |
|---|---|
| when asked | only when you ask it to remember something |
| ask | when it thinks something is worth keeping, after your yes |
| auto | on its own |

While it saves on its own, it can also look back every 10 messages for what to remember; `/memory-review` turns that on or off.

## Where it keeps it

| Choice | Keeps memory |
|---|---|
| auto | everywhere: about you, its notes, the project and the chat |
| project | for this project |
| chat | for this chat only |

With no project folder attached, "project" means the chat's own notes.

## Choosing in the terminal

`/remember` shows and changes when this chat saves and where. Followed by text, it keeps that text:

```sh
/remember I prefer tabs to spaces
/remember --project the tests need Docker running
/remember --chat call the draft v2
```

To start the terminal with a choice:

```sh
vythea --memory auto --memory-scope project
```

`--memory` takes `when-asked`, `ask` or `auto`; `--memory-scope` takes `auto`, `project` or `chat`.

## Private chats

A private chat loads only its own notes and saves to them only when asked. Nothing typed in it is kept in the terminal's prompt history.

```sh
vythea --private
```

## Seeing and changing it

- In the window, open Settings > Memory. Each entry can be edited or deleted, and `SOUL.md` can be written there.
- In the terminal, `/memory` shows what is kept. `/memory edit` opens a file in your editor, `/memory log` lists the changes, and `/memory restore` puts an earlier version back. Each takes `user`, `memory`, `project` or `soul`:

```sh
/memory edit user
/memory log project
```

You can also open the files in your [data folder](../data-and-privacy.md) and edit them yourself.
