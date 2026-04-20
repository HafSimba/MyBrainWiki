---
type: source
status: active
updated: 2026-04-17
source_ids: [SRC-20260417-claude-code-memory]
source_id: SRC-20260417-claude-code-memory
raw_path: raw/sources/2026-04-17--how-claude-remembers-project.md
tags: [claude-code, memory, claude-md, auto-memory]
---

# SRC-20260417-claude-code-memory

## TL;DR
La fonte descrive come Claude Code mantenga continuita tra sessioni tramite due meccanismi complementari: istruzioni esplicite in `CLAUDE.md` e note automatiche (`auto memory`).

## Punti chiave
- Ogni sessione parte con context window fresca, ma memoria operativa viene recuperata da file dedicati caricati all'avvio ([fonte raw](../../raw/sources/2026-04-17--how-claude-remembers-project.md)).
- `CLAUDE.md` serve per regole e istruzioni scritte dall'utente/team, con scope multipli (project, user, org, local) ([fonte raw](../../raw/sources/2026-04-17--how-claude-remembers-project.md)).
- Auto memory salva learnings utili per working tree (comandi build, pattern di debug, preferenze), modificabili come normali file markdown ([fonte raw](../../raw/sources/2026-04-17--how-claude-remembers-project.md)).
- La qualita delle istruzioni dipende da specificita e concisione; file troppo lunghi riducono aderenza e consumano contesto ([fonte raw](../../raw/sources/2026-04-17--how-claude-remembers-project.md)).

## Evidenze estratte
- La fonte distingue chiaramente `CLAUDE.md` (guidance scritta da te) e auto memory (note scritte da Claude) ([fonte raw](../../raw/sources/2026-04-17--how-claude-remembers-project.md)).
- Viene indicato limite operativo consigliato: circa 200 linee per file `CLAUDE.md` ([fonte raw](../../raw/sources/2026-04-17--how-claude-remembers-project.md)).
- Sono documentati `/memory`, `claudeMdExcludes`, import `@path` e regole path-scoped in `.claude/rules/` per progetti grandi ([fonte raw](../../raw/sources/2026-04-17--how-claude-remembers-project.md)).

## Impatti sulla wiki
- Creata pagina concetto [Memoria_Persistente_Claude_Code](../concepts/Memoria_Persistente_Claude_Code.md).
- Aggiornata pagina entita [Claude_Code](../entities/Claude_Code.md).

## Contraddizioni e incertezze
- Nessuna contraddizione interna esplicita nella fonte.
- Incertezza: il documento non fornisce metriche quantitative su impatto reale delle strategie di memoria su velocita/qualita output.

## Azioni successive
- Definire standard locale su quando promuovere istruzioni in `CLAUDE.md` vs auto memory.
- Pianificare review periodica dei file di memoria per rimuovere istruzioni obsolete o in conflitto.
- Valutare adozione di `.claude/rules/` path-scoped su repository con moduli eterogenei.