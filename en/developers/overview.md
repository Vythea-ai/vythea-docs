---
title: "Developers"
description: "Using Vythea from your own programs: scripts, editors and other agents."
---

Vythea runs on your computer, and your programs reach it through the `vythea` command. There are three ways in:

| You want to | Use | See |
|---|---|---|
| ask once from a script or a CI job, and read the answer | `vythea -p` | [Scripts and one-shot runs](../terminal/scripts.md) |
| have an editor use Vythea as its agent | `vythea acp` | [Zed and JetBrains](../plugins.md) |
| give another agent Vythea's browser, media and search tools | `vythea mcp serve` | [Vythea as an MCP server](../mcp.md) |

[Building on Vythea](building-on-vythea.md) says which to pick and what each one gives your program.

## Keys and the hosted models

There are no API keys to create for the hosted models. A program that uses Vythea through one of the commands above is paid from the credit of the account that computer is signed in to, at the prices on the [models page](https://vythea.com/dashboard/models). See [Hosted models and credit](../hosted-models.md).

To point Vythea at a server of your own instead, see [Gateways](../gateways.md), or [Running with nothing set up](../terminal/scripts.md) for a one-off run.
