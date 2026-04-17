---
type: entity
status: active
updated: 2026-04-17
source_ids: [SRC-20260417-openclaw-ollama]
tags: [runtime, model-orchestrator, local-ai]
---

# Ollama

## Profilo
Piattaforma/runtime per eseguire e orchestrare modelli locali o cloud, usata qui come layer di bootstrap e gestione modello per OpenClaw.

## Ruolo nel dominio
Fornisce comando unificato di lancio e configurazione (`ollama launch openclaw`) per ridurre la complessita di setup dell'assistente multi-canale.

## Fatti rilevanti
- Gestisce onboarding OpenClaw e installazione componenti gateway nel flusso launch ([SRC-20260417-openclaw-ollama](../sources/SRC-20260417-openclaw-ollama.md)).
- Supporta modalita non interattiva con `--yes` e modello esplicito per automazione ([fonte raw](../../raw/sources/2026-04-17--openclaw-via-ollama.md)).
- Richiede autenticazione (`ollama signin`) per web search su modelli locali ([fonte raw](../../raw/sources/2026-04-17--openclaw-via-ollama.md)).

## Relazioni
- Entita: [OpenClaw](OpenClaw.md).
- Concetto: [Bootstrap_OpenClaw_via_Ollama](../concepts/Bootstrap_OpenClaw_via_Ollama.md).

## Contraddizioni e note
- Nessuna contraddizione rilevata in questa fonte.
