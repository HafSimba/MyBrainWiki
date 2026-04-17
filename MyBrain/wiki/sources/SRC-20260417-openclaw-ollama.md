---
type: source
status: active
updated: 2026-04-17
source_ids: [SRC-20260417-openclaw-ollama]
source_id: SRC-20260417-openclaw-ollama
raw_path: raw/sources/2026-04-17--openclaw-via-ollama.md
tags: [openclaw, ollama, bootstrap, gateway]
---

# SRC-20260417-openclaw-ollama

## TL;DR
La guida Ollama integra il bootstrap di OpenClaw in un solo comando, automatizzando installazione, setup sicurezza, scelta modello, onboarding del gateway e plugin web search/fetch.

## Punti chiave
- `ollama launch openclaw` avvia un flusso guidato che copre installazione, onboarding e avvio gateway ([fonte raw](../../raw/sources/2026-04-17--openclaw-via-ollama.md)).
- E raccomandata una context window di almeno 64k token per modelli locali ([fonte raw](../../raw/sources/2026-04-17--openclaw-via-ollama.md)).
- Il plugin web search/fetch e attivato automaticamente dal launch tramite Ollama ([fonte raw](../../raw/sources/2026-04-17--openclaw-via-ollama.md)).
- Modalita headless supportata con `--yes` e `--model`, utile per Docker/CI/CD/script ([fonte raw](../../raw/sources/2026-04-17--openclaw-via-ollama.md)).

## Evidenze estratte
- Sequenza automatica dichiarata: install, security notice, model selection, onboarding, gateway startup ([fonte raw](../../raw/sources/2026-04-17--openclaw-via-ollama.md)).
- Alias legacy: `ollama launch clawdbot` ancora supportato ([fonte raw](../../raw/sources/2026-04-17--openclaw-via-ollama.md)).
- Configurazione senza lancio via `ollama launch openclaw --config` ([fonte raw](../../raw/sources/2026-04-17--openclaw-via-ollama.md)).

## Impatti sulla wiki
- Creata pagina concetto [Bootstrap_OpenClaw_via_Ollama](../concepts/Bootstrap_OpenClaw_via_Ollama.md).
- Creata pagina entita [Ollama](../entities/Ollama.md).
- Aggiornata pagina entita [OpenClaw](../entities/OpenClaw.md).

## Contraddizioni e incertezze
- Nessuna contraddizione interna esplicita.
- Incertezza: non sono fornite misure quantitative su tempi di bootstrap e affidabilita in ambienti CI lunghi.

## Azioni successive
- Validare in locale il flusso `--model ... --yes` su un caso reale.
- Definire policy di sicurezza canali prima di esposizione remota.
- Confrontare modello cloud vs locale su costo/latenza/qualita.
