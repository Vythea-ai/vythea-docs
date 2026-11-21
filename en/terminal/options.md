---
title: "Commands and options"
description: "Everything vythea takes on the command line: its commands and its options."
---

`vythea --help` prints this list too.

## Commands

| Command | Does |
|---|---|
| `vythea` | open a conversation |
| `vythea -p "question"` | ask once, print the answer and exit; see [Scripts and one-shot runs](scripts.md) |
| `vythea gui` | open the window instead |
| `vythea serve` | answer chat apps and run scheduled jobs, with no window |
| `vythea setup` | name, sign in, provider, model, install |
| `vythea doctor` | check the setup, the disk and the gateway |
| `vythea cloud` | run a task on Vythea's servers (Pro); see [Vythea Cloud](../cloud.md) |
| `vythea wallet` | the wallet the agent pays from, and its limits; see [Wallet](../wallet.md) |
| `vythea mcp` | add, list, get or remove MCP servers; see [MCP servers](../mcp.md) |
| `vythea mcp serve` | offer the browser, media and search tools to another agent over MCP |
| `vythea acp` | serve an editor over the Agent Client Protocol |
| `vythea --uninstall` | take it off again |

## Options

| Option | Does |
|---|---|
| `-c`, `--continue` | resume this folder's most recent session |
| `-r`, `--resume [id]` | choose a session, or open the one with this id (the id `/where` shows) |
| `--worktree` | work in a git worktree of its own, on a branch made from HEAD, leaving your checkout alone |
| `--mode <mode>` | how much runs without asking: `default`, `accept-edits`, `plan`, `auto`, `dont-ask` or `bypass` |
| `--yes` | the same as `--mode bypass`: run tools without asking, except risky ones |
| `--plan` | the same as `--mode plan`: read and search only |
| `--model <id>` | this session's model, leaving the default as it is |
| `--gateway <name>` | the gateway that model is on |
| `--effort <level>` | how hard it thinks in this session, or `auto` |
| `--memory <when>` | when this session saves to memory: `when-asked`, `ask` or `auto` |
| `--memory-scope <where>` | where it keeps memory: `auto` (everywhere), `project` or `chat` |
| `--private` | a new private chat: only its own notes load, and it saves only when asked |
| `--offline` | with `doctor`: leave the network alone |
| `-h`, `--help` | the list of commands and options |
| `-V`, `--version` | which version this is |

The modes are explained in [Asking first and modes](../app/permissions.md), and memory in [Memory](../app/memory.md).

## Examples

```sh
vythea --mode accept-edits --worktree
vythea -r 16
vythea doctor --offline
```

With no mode option, the terminal starts in the mode the window starts sessions in.
