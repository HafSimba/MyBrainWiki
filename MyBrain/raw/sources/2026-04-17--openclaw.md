---
title: "OpenClaw"
source: "https://docs.openclaw.ai/"
author:
published:
created: 2026-04-17
description:
tags:
  - "clippings"
---
## OpenClaw 🦞

> *“EXFOLIATE! EXFOLIATE!”* — A space lobster, probably

**Any OS gateway for AI agents across Discord, Google Chat, iMessage, Matrix, Microsoft Teams, Signal, Slack, Telegram, WhatsApp, Zalo, and more.**  
Send a message, get an agent response from your pocket. Run one Gateway across built-in channels, bundled channel plugins, WebChat, and mobile nodes.

## [Get Started](https://docs.openclaw.ai/start/getting-started)

Install OpenClaw and bring up the Gateway in minutes.

## [Run Onboarding](https://docs.openclaw.ai/start/wizard)

Guided setup with `openclaw onboard` and pairing flows.

## [Open the Control UI](https://docs.openclaw.ai/web/control-ui)

Launch the browser dashboard for chat, config, and sessions.

## What is OpenClaw?

OpenClaw is a **self-hosted gateway** that connects your favorite chat apps and channel surfaces — built-in channels plus bundled or external channel plugins such as Discord, Google Chat, iMessage, Matrix, Microsoft Teams, Signal, Slack, Telegram, WhatsApp, Zalo, and more — to AI coding agents like Pi. You run a single Gateway process on your own machine (or a server), and it becomes the bridge between your messaging apps and an always-available AI assistant.

**Who is it for?** Developers and power users who want a personal AI assistant they can message from anywhere — without giving up control of their data or relying on a hosted service.

**What makes it different?**

- **Self-hosted**: runs on your hardware, your rules
- **Multi-channel**: one Gateway serves built-in channels plus bundled or external channel plugins simultaneously
- **Agent-native**: built for coding agents with tool use, sessions, memory, and multi-agent routing
- **Open source**: MIT licensed, community-driven

**What do you need?** Node 24 (recommended), or Node 22 LTS (`22.14+`) for compatibility, an API key from your chosen provider, and 5 minutes. For best quality and security, use the strongest latest-generation model available.

## How it works

<svg aria-roledescription="flowchart-v2" role="graphics-document document" viewBox="0 0 753.1000366210938 510" style="max-width: 753.1000366210938px;" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns="http://www.w3.org/2000/svg" width="100%" id="mermaid-_r_8_-1776411614140"><style>#mermaid-_r_8_-1776411614140{font-family:inherit;font-size:16px;fill:#ccc;}#mermaid-_r_8_-1776411614140.error-icon{fill:#a44141;}#mermaid-_r_8_-1776411614140.error-text{fill:#ddd;stroke:#ddd;}#mermaid-_r_8_-1776411614140.edge-thickness-normal{stroke-width:1px;}#mermaid-_r_8_-1776411614140.edge-thickness-thick{stroke-width:3.5px;}#mermaid-_r_8_-1776411614140.edge-pattern-solid{stroke-dasharray:0;}#mermaid-_r_8_-1776411614140.edge-thickness-invisible{stroke-width:0;fill:none;}#mermaid-_r_8_-1776411614140.edge-pattern-dashed{stroke-dasharray:3;}#mermaid-_r_8_-1776411614140.edge-pattern-dotted{stroke-dasharray:2;}#mermaid-_r_8_-1776411614140.marker{fill:lightgrey;stroke:lightgrey;}#mermaid-_r_8_-1776411614140.marker.cross{stroke:lightgrey;}#mermaid-_r_8_-1776411614140 svg{font-family:inherit;font-size:16px;}#mermaid-_r_8_-1776411614140 p{margin:0;}#mermaid-_r_8_-1776411614140.label{font-family:inherit;color:#ccc;}#mermaid-_r_8_-1776411614140.cluster-label text{fill:#F9FFFE;}#mermaid-_r_8_-1776411614140.cluster-label span{color:#F9FFFE;}#mermaid-_r_8_-1776411614140.cluster-label span p{background-color:transparent;}#mermaid-_r_8_-1776411614140.label text,#mermaid-_r_8_-1776411614140 span{fill:#ccc;color:#ccc;}#mermaid-_r_8_-1776411614140.node rect,#mermaid-_r_8_-1776411614140.node circle,#mermaid-_r_8_-1776411614140.node ellipse,#mermaid-_r_8_-1776411614140.node polygon,#mermaid-_r_8_-1776411614140.node path{fill:#1f2020;stroke:#ccc;stroke-width:1px;}#mermaid-_r_8_-1776411614140.rough-node.label text,#mermaid-_r_8_-1776411614140.node.label text,#mermaid-_r_8_-1776411614140.image-shape.label,#mermaid-_r_8_-1776411614140.icon-shape.label{text-anchor:middle;}#mermaid-_r_8_-1776411614140.node.katex path{fill:#000;stroke:#000;stroke-width:1px;}#mermaid-_r_8_-1776411614140.rough-node.label,#mermaid-_r_8_-1776411614140.node.label,#mermaid-_r_8_-1776411614140.image-shape.label,#mermaid-_r_8_-1776411614140.icon-shape.label{text-align:center;}#mermaid-_r_8_-1776411614140.node.clickable{cursor:pointer;}#mermaid-_r_8_-1776411614140.root.anchor path{fill:lightgrey!important;stroke-width:0;stroke:lightgrey;}#mermaid-_r_8_-1776411614140.arrowheadPath{fill:lightgrey;}#mermaid-_r_8_-1776411614140.edgePath.path{stroke:lightgrey;stroke-width:2.0px;}#mermaid-_r_8_-1776411614140.flowchart-link{stroke:lightgrey;fill:none;}#mermaid-_r_8_-1776411614140.edgeLabel{background-color:hsl(0, 0%, 34.4117647059%);text-align:center;}#mermaid-_r_8_-1776411614140.edgeLabel p{background-color:hsl(0, 0%, 34.4117647059%);}#mermaid-_r_8_-1776411614140.edgeLabel rect{opacity:0.5;background-color:hsl(0, 0%, 34.4117647059%);fill:hsl(0, 0%, 34.4117647059%);}#mermaid-_r_8_-1776411614140.labelBkg{background-color:rgba(87.75, 87.75, 87.75, 0.5);}#mermaid-_r_8_-1776411614140.cluster rect{fill:hsl(180, 1.5873015873%, 28.3529411765%);stroke:rgba(255, 255, 255, 0.25);stroke-width:1px;}#mermaid-_r_8_-1776411614140.cluster text{fill:#F9FFFE;}#mermaid-_r_8_-1776411614140.cluster span{color:#F9FFFE;}#mermaid-_r_8_-1776411614140 div.mermaidTooltip{position:absolute;text-align:center;max-width:200px;padding:2px;font-family:inherit;font-size:12px;background:hsl(20, 1.5873015873%, 12.3529411765%);border:1px solid rgba(255, 255, 255, 0.25);border-radius:2px;pointer-events:none;z-index:100;}#mermaid-_r_8_-1776411614140.flowchartTitleText{text-anchor:middle;font-size:18px;fill:#ccc;}#mermaid-_r_8_-1776411614140 rect.text{fill:none;stroke-width:0;}#mermaid-_r_8_-1776411614140.icon-shape,#mermaid-_r_8_-1776411614140.image-shape{background-color:hsl(0, 0%, 34.4117647059%);text-align:center;}#mermaid-_r_8_-1776411614140.icon-shape p,#mermaid-_r_8_-1776411614140.image-shape p{background-color:hsl(0, 0%, 34.4117647059%);padding:2px;}#mermaid-_r_8_-1776411614140.icon-shape rect,#mermaid-_r_8_-1776411614140.image-shape rect{opacity:0.5;background-color:hsl(0, 0%, 34.4117647059%);fill:hsl(0, 0%, 34.4117647059%);}#mermaid-_r_8_-1776411614140:root{--mermaid-font-family:inherit;}</style><g><marker orient="auto" markerHeight="8" markerWidth="8" markerUnits="userSpaceOnUse" refY="5" refX="5" viewBox="0 0 10 10" id="mermaid-_r_8_-1776411614140_flowchart-v2-pointEnd"><path style="stroke-width: 1; stroke-dasharray: 1, 0;" d="M 0 0 L 10 5 L 0 10 z"></path></marker><marker orient="auto" markerHeight="8" markerWidth="8" markerUnits="userSpaceOnUse" refY="5" refX="4.5" viewBox="0 0 10 10" id="mermaid-_r_8_-1776411614140_flowchart-v2-pointStart"><path style="stroke-width: 1; stroke-dasharray: 1, 0;" d="M 0 5 L 10 10 L 10 0 z"></path></marker><marker orient="auto" markerHeight="11" markerWidth="11" markerUnits="userSpaceOnUse" refY="5" refX="11" viewBox="0 0 10 10" id="mermaid-_r_8_-1776411614140_flowchart-v2-circleEnd"><circle style="stroke-width: 1; stroke-dasharray: 1, 0;" r="5" cy="5" cx="5"></circle></marker><marker orient="auto" markerHeight="11" markerWidth="11" markerUnits="userSpaceOnUse" refY="5" refX="-1" viewBox="0 0 10 10" id="mermaid-_r_8_-1776411614140_flowchart-v2-circleStart"><circle style="stroke-width: 1; stroke-dasharray: 1, 0;" r="5" cy="5" cx="5"></circle></marker><marker orient="auto" markerHeight="11" markerWidth="11" markerUnits="userSpaceOnUse" refY="5.2" refX="12" viewBox="0 0 11 11" id="mermaid-_r_8_-1776411614140_flowchart-v2-crossEnd"><path style="stroke-width: 2; stroke-dasharray: 1, 0;" d="M 1,1 l 9,9 M 10,1 l -9,9"></path></marker><marker orient="auto" markerHeight="11" markerWidth="11" markerUnits="userSpaceOnUse" refY="5.2" refX="-1" viewBox="0 0 11 11" id="mermaid-_r_8_-1776411614140_flowchart-v2-crossStart"><path style="stroke-width: 2; stroke-dasharray: 1, 0;" d="M 1,1 l 9,9 M 10,1 l -9,9"></path></marker><g><g></g><g><path marker-end="url(#mermaid-_r_8_-1776411614140_flowchart-v2-pointEnd)" style="" id="L_A_B_0" d="M255.875,243L260.042,243C264.208,243,272.542,243,280.208,243C287.875,243,294.875,243,298.375,243L301.875,243"></path><path marker-end="url(#mermaid-_r_8_-1776411614140_flowchart-v2-pointEnd)" style="" id="L_B_C_1" d="M382.12,216L395.117,185.833C408.113,155.667,434.107,95.333,460.677,65.167C487.248,35,514.396,35,527.97,35L541.544,35"></path><path marker-end="url(#mermaid-_r_8_-1776411614140_flowchart-v2-pointEnd)" style="" id="L_B_D_2" d="M393.752,216L404.81,203.167C415.868,190.333,437.984,164.667,466.736,151.833C495.488,139,530.875,139,548.569,139L566.263,139"></path><path marker-end="url(#mermaid-_r_8_-1776411614140_flowchart-v2-pointEnd)" style="" id="L_B_E_3" d="M435.1,243L439.267,243C443.433,243,451.767,243,464.564,243C477.36,243,494.621,243,503.251,243L511.881,243"></path><path marker-end="url(#mermaid-_r_8_-1776411614140_flowchart-v2-pointEnd)" style="" id="L_B_F_4" d="M393.752,270L404.81,282.833C415.868,295.667,437.984,321.333,461.792,334.167C485.6,347,511.1,347,523.85,347L536.6,347"></path><path marker-end="url(#mermaid-_r_8_-1776411614140_flowchart-v2-pointEnd)" style="" id="L_B_G_5" d="M381.485,270L394.588,302.167C407.69,334.333,433.895,398.667,450.498,430.833C467.1,463,474.1,463,477.6,463L481.1,463"></path></g><g><g><g transform="translate(0, 0)"></g></g><g><g transform="translate(0, 0)"></g></g><g><g transform="translate(0, 0)"></g></g><g><g transform="translate(0, 0)"></g></g><g><g transform="translate(0, 0)"></g></g><g><g transform="translate(0, 0)"></g></g></g><g><g transform="translate(131.9375, 243)" id="flowchart-A-12"><rect height="54" width="247.875" y="-27" x="-123.9375" style=""></rect><g transform="translate(-93.9375, -12)" style=""><rect></rect><foreignObject height="24" width="187.875"><p>Chat apps + plugins</p></foreignObject></g></g><g transform="translate(370.4875030517578, 243)" id="flowchart-B-13"><rect height="54" width="129.2249984741211" y="-27" x="-64.61249923706055" style=""></rect><g transform="translate(-34.61249923706055, -12)" style=""><rect></rect><foreignObject height="24" width="69.2249984741211"><p>Gateway</p></foreignObject></g></g><g transform="translate(615.1000061035156, 35)" id="flowchart-C-15"><rect height="54" width="139.1125030517578" y="-27" x="-69.5562515258789" style=""></rect><g transform="translate(-39.556251525878906, -12)" style=""><rect></rect><foreignObject height="24" width="79.11250305175781"><p>Pi agent</p></foreignObject></g></g><g transform="translate(615.1000061035156, 139)" id="flowchart-D-17"><rect height="54" width="89.67500114440918" y="-27" x="-44.83750057220459" style=""></rect><g transform="translate(-14.83750057220459, -12)" style=""><rect></rect><foreignObject height="24" width="29.67500114440918"><p>CLI</p></foreignObject></g></g><g transform="translate(615.1000061035156, 243)" id="flowchart-E-19"><rect height="54" width="198.4375" y="-27" x="-99.21875" style=""></rect><g transform="translate(-69.21875, -12)" style=""><rect></rect><foreignObject height="24" width="138.4375"><p>Web Control UI</p></foreignObject></g></g><g transform="translate(615.1000061035156, 347)" id="flowchart-F-21"><rect height="54" width="149" y="-27" x="-74.5" style=""></rect><g transform="translate(-44.5, -12)" style=""><rect></rect><foreignObject height="24" width="89"><p>macOS app</p></foreignObject></g></g><g transform="translate(615.1000061035156, 463)" id="flowchart-G-23"><rect height="78" width="260" y="-39" x="-130" style=""></rect><g transform="translate(-100, -24)" style=""><rect></rect><foreignObject height="48" width="200"><p>iOS and Android nodes</p></foreignObject></g></g></g></g></g></svg>

The Gateway is the single source of truth for sessions, routing, and channel connections.

## Key capabilities

## Multi-channel gateway

Discord, iMessage, Signal, Slack, Telegram, WhatsApp, WebChat, and more with a single Gateway process.

## Plugin channels

Bundled plugins add Matrix, Nostr, Twitch, Zalo, and more in normal current releases.

## Multi-agent routing

Isolated sessions per agent, workspace, or sender.

## Media support

Send and receive images, audio, and documents.

## Web Control UI

Browser dashboard for chat, config, sessions, and nodes.

## Mobile nodes

Pair iOS and Android nodes for Canvas, camera, and voice-enabled workflows.

## Quick start

Need the full install and dev setup? See [Getting Started](https://docs.openclaw.ai/start/getting-started).

## Dashboard

Open the browser Control UI after the Gateway starts.

- Local default: [http://127.0.0.1:18789/](http://127.0.0.1:18789/)
- Remote access: [Web surfaces](https://docs.openclaw.ai/web) and [Tailscale](https://docs.openclaw.ai/gateway/tailscale)

![OpenClaw](https://mintcdn.com/clawdhub/FaXdIfo7gPK_jSWb/whatsapp-openclaw.jpg?w=2500&fit=max&auto=format&n=FaXdIfo7gPK_jSWb&q=85&s=7050f3dda374e9a1adedf3cd08357338)

## Configuration (optional)

Config lives at `~/.openclaw/openclaw.json`.

- If you **do nothing**, OpenClaw uses the bundled Pi binary in RPC mode with per-sender sessions.
- If you want to lock it down, start with `channels.whatsapp.allowFrom` and (for groups) mention rules.

Example:

```json5
{
  channels: {
    whatsapp: {
      allowFrom: ["+15555550123"],
      groups: { "*": { requireMention: true } },
    },
  },
  messages: { groupChat: { mentionPatterns: ["@openclaw"] } },
}
```

## Start here

## [Docs hubs](https://docs.openclaw.ai/start/hubs)

All docs and guides, organized by use case.

## [Configuration](https://docs.openclaw.ai/gateway/configuration)

Core Gateway settings, tokens, and provider config.

## [Remote access](https://docs.openclaw.ai/gateway/remote)

SSH and tailnet access patterns.

## [Channels](https://docs.openclaw.ai/channels/telegram)

Channel-specific setup for Feishu, Microsoft Teams, WhatsApp, Telegram, Discord, and more.

## [Nodes](https://docs.openclaw.ai/nodes)

iOS and Android nodes with pairing, Canvas, camera, and device actions.

## [Help](https://docs.openclaw.ai/help)

Common fixes and troubleshooting entry point.

## Learn more

## [Full feature list](https://docs.openclaw.ai/concepts/features)

Complete channel, routing, and media capabilities.

## [Multi-agent routing](https://docs.openclaw.ai/concepts/multi-agent)

Workspace isolation and per-agent sessions.

## [Security](https://docs.openclaw.ai/gateway/security)

Tokens, allowlists, and safety controls.

## [Troubleshooting](https://docs.openclaw.ai/gateway/troubleshooting)

Gateway diagnostics and common errors.

## [About and credits](https://docs.openclaw.ai/reference/credits)

Project origins, contributors, and license.