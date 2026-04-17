---
type: source
status: active
updated: 2026-04-17
source_ids: [SRC-20260417-openclaw-docs]
source_id: SRC-20260417-openclaw-docs
raw_path: raw/sources/2026-04-17--openclaw.md
tags: [openclaw, gateway, ai-agent, multi-channel]
---

# SRC-20260417-openclaw-docs

## TL;DR
OpenClaw e un gateway self-hosted multi-canale che collega app di messaggistica e superfici web/mobile ad agenti AI, con routing multi-agent, sessioni isolate e controllo locale.

## Punti chiave
- OpenClaw centralizza molteplici canali (Discord, Slack, Telegram, WhatsApp, Teams e altri) in un singolo processo gateway ([fonte raw](../../raw/sources/2026-04-17--openclaw.md)).
- Il progetto e orientato a deployment self-hosted e controllo dati locale ([fonte raw](../../raw/sources/2026-04-17--openclaw.md)).
- Sono presenti funzionalita agent-native: sessioni, routing multi-agent, memory e integrazione strumenti ([fonte raw](../../raw/sources/2026-04-17--openclaw.md)).
- Richiede Node 24 raccomandato (oppure Node 22 LTS 22.14+) e API key provider ([fonte raw](../../raw/sources/2026-04-17--openclaw.md)).

## Evidenze estratte
- "Self-hosted gateway" e "one Gateway process" come architettura di base ([fonte raw](../../raw/sources/2026-04-17--openclaw.md)).
- La Gateway viene descritta come "single source of truth for sessions, routing, and channel connections" ([fonte raw](../../raw/sources/2026-04-17--openclaw.md)).
- Configurazione opzionale in `~/.openclaw/openclaw.json` con allowlist per canali ([fonte raw](../../raw/sources/2026-04-17--openclaw.md)).

## Impatti sulla wiki
- Creata pagina entita [OpenClaw](../entities/OpenClaw.md).
- Creata pagina concetto [Gateway_Multi_Canale](../concepts/Gateway_Multi_Canale.md).

## Contraddizioni e incertezze
- Nessuna contraddizione interna rilevata nella pagina processata.
- Incertezza: non sono riportate metriche comparative quantitative (latenza, throughput, costo operativo).

## Azioni successive
- Cercare benchmark tecnici o case study con numeri operativi.
- Verificare maturita dei plugin canale necessari al tuo caso d'uso.
- Definire una policy security locale (token, allowlist, accesso remoto) prima del deployment.
