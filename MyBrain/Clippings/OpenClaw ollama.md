---
title: "OpenClaw"
source: "https://docs.ollama.com/integrations/openclaw"
author:
published:
created: 2026-04-17
description:
tags:
  - "clippings"
---
OpenClaw is a personal AI assistant that runs on your own devices. It bridges messaging services (WhatsApp, Telegram, Slack, Discord, iMessage, and more) to AI coding agents through a centralized gateway.

## Quick start

```shellscript
ollama launch openclaw
```

Ollama handles everything automatically:

1. **Install** — If OpenClaw isn’t installed, Ollama prompts to install it via npm
2. **Security** — On the first launch, a security notice explains the risks of tool access
3. **Model** — Pick a model from the selector (local or cloud)
4. **Onboarding** — Ollama configures the provider, installs the gateway daemon, sets your model as the primary, and installs the web search and fetch plugin
5. **Gateway** — Starts in the background and opens the OpenClaw TUI

OpenClaw requires a larger context window. It is recommended to use a context window of at least 64k tokens if using local models. See [Context length](https://docs.ollama.com/context-length) for more information.

Previously known as Clawdbot. `ollama launch clawdbot` still works as an alias.

## Web search and fetch

OpenClaw ships with a web search and fetch plugin that gives local or cloud models the ability to search the web and extract readable page content.

```shellscript
ollama launch openclaw
```

Web search and fetch is enabled automatically when launching OpenClaw through Ollama. To install the plugin directly:

```shellscript
openclaw plugins install @ollama/openclaw-web-search
```

Web search for local models requires `ollama signin`.

## Configure without launching

To change the model without starting the gateway and TUI:

```shellscript
ollama launch openclaw --config
```

To use a specific model directly:

```shellscript
ollama launch openclaw --model kimi-k2.5:cloud
```

If the gateway is already running, it restarts automatically to pick up the new model.

## Recommended models

**Cloud models**:

- `kimi-k2.5:cloud` — Multimodal reasoning with subagents
- `qwen3.5:cloud` — Reasoning, coding, and agentic tool use with vision
- `glm-5.1:cloud` — Reasoning and code generation
- `minimax-m2.7:cloud` — Fast, efficient coding and real-world productivity

**Local models:**

- `gemma4` — Reasoning and code generation locally (~16 GB VRAM)
- `qwen3.5` — Reasoning, coding, and visual understanding locally (~11 GB VRAM)

More models at [ollama.com/search](https://ollama.com/search?c=cloud).

## Non-interactive (headless) mode

Run OpenClaw without interaction for use in Docker, CI/CD, or scripts:

```shellscript
ollama launch openclaw --model kimi-k2.5:cloud --yes
```

The `--yes` flag auto-pulls the model, skips selectors, and requires `--model` to be specified.

## Connect messaging apps

```shellscript
openclaw configure --section channels
```

Link WhatsApp, Telegram, Slack, Discord, or iMessage to chat with your local models from anywhere.

## Stopping the gateway

```shellscript
openclaw gateway stop
```