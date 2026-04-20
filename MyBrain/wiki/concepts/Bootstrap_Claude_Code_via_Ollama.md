---
type: concept
status: active
updated: 2026-04-17
source_ids: [SRC-20260417-claude-code-ollama]
tags: [bootstrap, claude-code, ollama, automation]
---

# Bootstrap Claude Code via Ollama

## Definizione
Procedura operativa per eseguire Claude Code su modelli gestiti da Ollama usando il bridge API compatibile Anthropic.

## Perche conta
Riduce attrito di setup per coding agentico su terminale, rendendo possibile un flusso unico per uso interattivo e automazioni headless.

## Regole operative
- Per setup rapido usa `ollama launch claude`.
- In automazione usa `ollama launch claude --model <modello> --yes -- <argomenti-claude>`.
- In configurazione manuale imposta le variabili Anthropic compatibili con endpoint Ollama.
- Evita `--dangerously-skip-permissions` fuori da ambienti isolati e controllati.

## Evidenze
- La fonte descrive quick setup, run con modello esplicito e headless mode con `--yes` ([SRC-20260417-claude-code-ollama](../sources/SRC-20260417-claude-code-ollama.md)).
- Sono documentati bridge API, plugin Telegram e automazione periodica con `/loop` ([fonte raw](../../raw/sources/2026-04-17--claude-code.md)).

## Collegamenti
- Entita correlata: [Claude_Code](../entities/Claude_Code.md).
- Entita correlata: [Ollama](../entities/Ollama.md).
- Concetto correlato: [Bootstrap_OpenClaw_via_Ollama](Bootstrap_OpenClaw_via_Ollama.md).

## Contraddizioni e limiti
- Il documento privilegia setup e comandi, ma non offre test comparativi di affidabilita/costo tra modelli.