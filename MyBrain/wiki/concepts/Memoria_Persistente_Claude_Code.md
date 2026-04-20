---
type: concept
status: active
updated: 2026-04-17
source_ids: [SRC-20260417-claude-code-memory]
tags: [claude-code, memory, claude-md, auto-memory]
---

# Memoria Persistente Claude Code

## Definizione
Modello a due livelli per mantenere conoscenza tra sessioni: istruzioni intenzionali (`CLAUDE.md`) e apprendimento incrementale automatico (`auto memory`).

## Perche conta
Riduce la ripetizione di contesto nelle sessioni nuove e rende piu stabile il comportamento operativo di Claude Code su un progetto nel tempo.

## Regole operative
- Usa `CLAUDE.md` per regole stabili del progetto (build, convenzioni, architettura).
- Mantieni istruzioni specifiche e concise; evita file troppo lunghi o ambigui.
- Usa `.claude/rules/` per regole path-scoped quando il repository e grande o eterogeneo.
- Riesamina periodicamente auto memory e istruzioni con `/memory` per rimuovere conflitti e obsolescenze.

## Evidenze
- La fonte spiega che entrambe le memorie vengono caricate a inizio sessione e trattate come contesto, non enforcement hard ([SRC-20260417-claude-code-memory](../sources/SRC-20260417-claude-code-memory.md)).
- Sono indicati pattern pratici di organizzazione: scope multipli, import `@path`, esclusioni (`claudeMdExcludes`) e regole condizionali per path ([fonte raw](../../raw/sources/2026-04-17--how-claude-remembers-project.md)).

## Collegamenti
- Entita correlata: [Claude_Code](../entities/Claude_Code.md).
- Entita correlata: [Ollama](../entities/Ollama.md).
- Concetto correlato: [Bootstrap_Claude_Code_via_Ollama](Bootstrap_Claude_Code_via_Ollama.md).

## Contraddizioni e limiti
- Le istruzioni in memoria non sono una garanzia assoluta di compliance: conflitti e vaghezza riducono affidabilita.