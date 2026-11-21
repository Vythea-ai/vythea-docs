---
title: "Troubleshooting"
description: "Checking the setup with vythea doctor, what common errors mean, and where the logs are."
---

## Check the setup

```sh
vythea doctor
```

It checks the version, your system, the data folder and the space left on its disk, the settings, where your keys are kept, the logs, the last crash, and whether the gateway answers. It ends with "No problems found." or says what is wrong. To check without using the network:

```sh
vythea doctor --offline
```

## When a message fails

A failed request says why in the chat, and in the window offers the fix. The usual reasons:

| It says | What to do |
|---|---|
| the key was refused | check the key under Settings > Accounts, or with `/connect` |
| out of credit | add credit on [Billing](https://vythea.com/dashboard/billing), switch to a gateway with your own key, or set a fallback model |
| a rate limit | wait the time it names; Vythea waits out short limits by itself |
| the provider is busy | try again, or pick another model |
| the conversation is too long | `/compact` summarises earlier turns; `/new` starts fresh |

`/fallback` names models to carry on with when yours is overloaded or out of credit:

```sh
/fallback
```

## Signing in

- If the browser does not open, the app offers to open the page again or copy its link.
- `/whoami` shows who is signed in on this computer; `/login` signs in again.
- [Devices](https://vythea.com/dashboard/devices) lists the computers signed in to your account.

## A model on your own server answers badly

If Vythea does not know a model's limits, set them in the environment:

```sh
VYTHEA_CONTEXT_WINDOW=32000 VYTHEA_MAX_OUTPUT=4096 vythea
```

`context_window` and `max_output` in `settings.json` do the same for good.

## Logs and crashes

Vythea keeps a log in `logs/` and crash reports in `crashes/`, in your [data folder](data-and-privacy.md). They stay on your computer. `vythea doctor` shows where they are and the last crash.

## Starting over

Run setup again to change your name, gateway, model or what is installed:

```sh
vythea setup
```

Uninstalling keeps your data folder, so your sessions and memory stay.

## Still stuck

Write to support@vythea.com with what you did, what it said, and the output of `vythea doctor`.
