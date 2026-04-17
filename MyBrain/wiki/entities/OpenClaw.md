---
type: entity
status: active
updated: 2026-04-17
source_ids: [SRC-20260417-openclaw-docs, SRC-20260417-openclaw-ollama]
tags: [software, gateway, self-hosted]
---

# OpenClaw

## Profilo
Piattaforma open source (licenza MIT) che espone un gateway multi-canale per interagire con agenti AI tramite chat app, web UI e nodi mobili.

## Ruolo nel dominio
Agisce da livello di integrazione tra canali di messaggistica e runtime agentico, mantenendo sessioni, routing e configurazione in un punto unico.

## Fatti rilevanti
- Supporta canali multipli con un singolo processo gateway ([SRC-20260417-openclaw-docs](../sources/SRC-20260417-openclaw-docs.md)).
- Enfasi su esecuzione self-hosted e controllo dati locale ([fonte raw](../../raw/sources/2026-04-17--openclaw.md)).
- Include Control UI web e nodi iOS/Android per interazione remota ([fonte raw](../../raw/sources/2026-04-17--openclaw.md)).
- Integrazione con Ollama per bootstrap guidato tramite `ollama launch openclaw` ([SRC-20260417-openclaw-ollama](../sources/SRC-20260417-openclaw-ollama.md)).
- Supporto modalita headless (`--model ... --yes`) per automazioni CI/CD o script ([fonte raw](../../raw/sources/2026-04-17--openclaw-via-ollama.md)).

## Relazioni
- Concetto: [Gateway_Multi_Canale](../concepts/Gateway_Multi_Canale.md).
- Concetto: [Bootstrap_OpenClaw_via_Ollama](../concepts/Bootstrap_OpenClaw_via_Ollama.md).
- Entita: [Ollama](Ollama.md).

## Contraddizioni e note
- Nessuna contraddizione segnalata al primo ingest.
