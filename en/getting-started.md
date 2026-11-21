---
title: "Getting started"
description: "Make an account, install Vythea, sign it in and ask it something."
---

Vythea is an AI agent that stays open beside your work: a window, and the same agent in a terminal. It reads and writes files, runs commands (asking first), keeps notes about you on your disk, and talks to whichever models you choose.

## 1. Make an account

[Sign up](https://vythea.com/signup) on vythea.com. While Vythea is in alpha, downloads come with an account; it also carries your credit for hosted models, your plan and your teams.

## 2. Install it

Open [Download](https://vythea.com/dashboard/download) in the dashboard. It offers your own system first:

- **macOS** (13 or later, Apple silicon): copy the one-line command and paste it into Terminal. It puts in the window and the terminal and opens Vythea, with no warning to click through. Or open the .dmg and drag Vythea into Applications; the first time, macOS may say it cannot verify Vythea: close the message, open System Settings › Privacy & Security, click **Open Anyway** next to Vythea and confirm. You only do this once.
- **Windows** (11, x64): download the .zip, unpack it and run `vythea.exe setup` — or copy the one-line command and paste it into PowerShell, which does both.
- **Linux** (x64, glibc 2.31 or later): download the .tar.gz, unpack it and run `./vythea setup` — or paste the one-line command into a terminal.

Nothing needs administrator rights, and nothing goes outside your own account on the computer except, on a Mac, the app in Applications.

## 3. Set it up

`vythea setup` asks what to call you, signs you in, picks a gateway and a model, and puts the window, the terminal or both where you choose. Run it again any time to change the answers. On Windows and Linux the app then shows up in the start menu or application menu.

## 4. Sign it in

Signing in happens on vythea.com: the app opens it for you, or run `/login` in the terminal. The computer then shows under [Devices](https://vythea.com/dashboard/devices).

## 5. Ask it something

Type a message. Vythea answers with the model you picked, and asks before it runs a command or changes a file. Hosted models are paid from your credit; to use your own API keys instead, see [Gateways](gateways.md).
