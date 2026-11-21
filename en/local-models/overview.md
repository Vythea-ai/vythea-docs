---
title: "Local models"
description: "Running a model on your own computer: why you might, and what you need."
---

Vythea can use a model running on your own computer instead of one in the cloud. Your messages, files and tool results then never leave the machine, nothing is paid per request, and the agent keeps working with no internet.

The trade is quality and speed. A model small enough for a laptop is well behind the hosted ones at long, many-step work, and it answers only as fast as your hardware lets it.

## What you need

- **A server that runs the model.** Vythea does not run models itself; it talks to a server on your computer over the same OpenAI-compatible API it uses for every [gateway](../gateways.md). [Ollama](ollama.md) is found by itself; [LM Studio, llama.cpp and others](other-servers.md) are added by their address.
- **A model that fits.** Memory is what decides: see [Choosing a model](choosing-a-model.md).
- **One that can call tools.** The agent reads, writes and runs things through tool calls. A model made only for chat can talk, but not act.

No account and no key are needed for a local model.

## In this section

- [Ollama](ollama.md): the quickest way to start
- [Other local servers](other-servers.md): LM Studio, llama.cpp, vLLM and anything OpenAI-compatible
- [Choosing a model](choosing-a-model.md): what fits your memory, and the context window
- [Working offline](offline.md): what still works with no internet
- [Serving your accounts to other tools](local-endpoint.md): the Local endpoint

The phone app runs small models on the device itself: see [Mobile models](../mobile/models.md).
