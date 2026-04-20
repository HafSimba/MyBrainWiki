---
type: entity
status: active
updated: 2026-04-17
source_ids: [SRC-20260417-claude-code-ollama, SRC-20260417-claude-code-memory]
tags: [tool, cli, coding-agent, anthropic]
---

# Claude Code

## Profilo
Tool di coding agentico in ambiente terminale, sviluppato da Anthropic, progettato per operare direttamente sulla codebase locale.

## Ruolo nel dominio
Esegue task di sviluppo assistito (lettura/modifica/esecuzione codice) e automazioni ricorrenti, integrandosi con modelli esposti da Ollama.

## Fatti rilevanti
- La fonte indica capacita dirette di lettura, modifica ed esecuzione nella directory di lavoro ([SRC-20260417-claude-code-ollama](../sources/SRC-20260417-claude-code-ollama.md)).
- Puo usare modelli open/cloud via endpoint Anthropic-compatible di Ollama ([fonte raw](../../raw/sources/2026-04-17--claude-code.md)).
- Supporta scheduling interno con comando `/loop` per task periodici ([fonte raw](../../raw/sources/2026-04-17--claude-code.md)).
- Offre integrazione Telegram via plugin, con modello permessi esplicito per azioni sensibili ([fonte raw](../../raw/sources/2026-04-17--claude-code.md)).
- Integra memoria persistente tramite `CLAUDE.md` (istruzioni utente/team) e auto memory (note generate da Claude) ([SRC-20260417-claude-code-memory](../sources/SRC-20260417-claude-code-memory.md)).
- Espone comando `/memory` per ispezionare file di istruzioni e memoria automatica della sessione/progetto ([fonte raw](../../raw/sources/2026-04-17--how-claude-remembers-project.md)).

## Relazioni
- Entita: [Ollama](Ollama.md).
- Concetto: [Bootstrap_Claude_Code_via_Ollama](../concepts/Bootstrap_Claude_Code_via_Ollama.md).
- Concetto: [Memoria_Persistente_Claude_Code](../concepts/Memoria_Persistente_Claude_Code.md).
- Concetto correlato: [Bootstrap_OpenClaw_via_Ollama](../concepts/Bootstrap_OpenClaw_via_Ollama.md).

## Contraddizioni e note
- La fonte e orientata all'uso operativo; per valutazioni comparative servono benchmark indipendenti su task reali.