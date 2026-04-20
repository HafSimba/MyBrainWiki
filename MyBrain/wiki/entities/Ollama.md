---
type: entity
status: active
updated: 2026-04-17
source_ids: [SRC-20260417-openclaw-ollama, SRC-20260417-claude-code-ollama]
tags: [runtime, model-orchestrator, local-ai]
---

# Ollama

## Profilo
Piattaforma/runtime per eseguire e orchestrare modelli locali o cloud, usata qui come layer di bootstrap e gestione modello per OpenClaw e Claude Code.

## Ruolo nel dominio
Fornisce comandi unificati di lancio e configurazione (`ollama launch ...`) per ridurre la complessita di setup di tool agentici multi-canale e CLI coding.

## Fatti rilevanti
- Gestisce onboarding OpenClaw e installazione componenti gateway nel flusso launch ([SRC-20260417-openclaw-ollama](../sources/SRC-20260417-openclaw-ollama.md)).
- Supporta modalita non interattiva con `--yes` e modello esplicito per automazione ([fonte raw](../../raw/sources/2026-04-17--openclaw-via-ollama.md)).
- Richiede autenticazione (`ollama signin`) per web search su modelli locali ([fonte raw](../../raw/sources/2026-04-17--openclaw-via-ollama.md)).
- Espone endpoint Anthropic-compatible usato da Claude Code via variabili `ANTHROPIC_*` ([SRC-20260417-claude-code-ollama](../sources/SRC-20260417-claude-code-ollama.md)).
- Supporta bootstrap diretto di Claude Code con `ollama launch claude` anche in headless mode ([fonte raw](../../raw/sources/2026-04-17--claude-code.md)).

## Relazioni
- Entita: [OpenClaw](OpenClaw.md).
- Entita: [Claude_Code](Claude_Code.md).
- Concetto: [Bootstrap_OpenClaw_via_Ollama](../concepts/Bootstrap_OpenClaw_via_Ollama.md).
- Concetto: [Bootstrap_Claude_Code_via_Ollama](../concepts/Bootstrap_Claude_Code_via_Ollama.md).

## Contraddizioni e note
- Nessuna contraddizione rilevata in questa fonte.
