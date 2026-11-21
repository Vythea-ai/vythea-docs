---
title: "What the agent can do"
description: "The tools Vythea uses: files, commands, web search, reading documents, attaching pictures and controlling apps."
---

Vythea works through tools. Each one it uses shows in the chat, and anything that changes your computer asks first: see [Asking first and modes](permissions.md).

## Files

- It reads, searches, writes and edits files in the project folder, and shows a diff before each change.
- It reads Word, Excel, PowerPoint and PDF files as text, OpenDocument files, and EPUB books chapter by chapter. Search can look inside documents too.
- Scratch work, such as a script to reproduce a bug, can go in the system's temp folder, out of your project.
- With no project folder attached, a chat works in Vythea's own folder.

## Commands

- It runs commands in the project folder, in bash where bash is installed.
- A command still running at its time limit carries on as a background job. `/jobs` lists them in the terminal, and the Jobs tab in the window shows them live.
- In the terminal, a line starting with `!` runs as a command yourself, without asking, and the model sees what it printed with your next message:

```sh
!git status
```

## Web search and pages

Vythea can read a web page and search the web. Switch search on with the Web switch in the window, or `/search` in the terminal.

By default, search goes through the gateway when it sells search (on the Vythea gateway, paid from your credit), and through DuckDuckGo when it cannot answer. The approval card says where a search goes and who pays. To use a search service of your own, open Settings > Search, or:

```sh
/search services
```

| Service | Needs |
|---|---|
| Brave, Tavily, Exa | an API key |
| SearXNG | your own server |
| DuckDuckGo | nothing; it may be slow or limited at busy times |

A chosen service is the only one used. To keep every search on DuckDuckGo, with no key and no cost:

```sh
/search keyless
```

## Pictures

The model sees pictures you attach and pictures its tools open. In the window, drop or paste them into the box. In the terminal, Ctrl+V attaches the picture on the clipboard, dragging a picture file in attaches it, or:

```sh
/image screenshot.png
```

## Files and folders by name

Type `@` and a path to attach a file, a range of lines or a folder. The box offers paths as you type.

## Controlling apps

On macOS, and on Linux under X11, Vythea can use desktop apps for you. It asks once for each app.

## Speaking and listening

- Replies can be read aloud as they stream, paid from your credit. In the terminal, `/voice` turns it on or off.
- In the window, voice input turns what you say into text at the cursor.

## Images, speech and video

Making images, speech and video, and turning audio into text, are covered in [Hosted models and credit](../hosted-models.md). A picture you attach can also be edited with `edit_image`, on the chat's own gateway.

## Reply style

`/style` lists the reply styles and picks one; you can also write your own.

```sh
/style concise
```
