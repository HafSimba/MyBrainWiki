---
type: entity
status: active
updated: 2026-04-17
source_ids: [SRC-20260417-a-z-index-windows-cmd-commands]
tags: [windows, shell, cli, amministrazione]
---

# CMD Windows

## Profilo
Interprete storico a riga di comando di Windows, usato per eseguire comandi interni della shell e utility esterne.

## Ruolo nel dominio
Fornisce un ambiente operativo per amministrazione, diagnostica, automazione batch e gestione di file/rete su host Windows.

## Fatti rilevanti
- La fonte classifica un ampio insieme di comandi CMD con link specifici per sintassi e descrizioni operative ([SRC-20260417-a-z-index-windows-cmd-commands](../sources/SRC-20260417-a-z-index-windows-cmd-commands.md)).
- I comandi marcati come interni sono disponibili solo dentro la shell CMD ([fonte raw](../../raw/sources/2026-04-17--a-z-index-windows-cmd-commands.md)).
- I comandi esterni possono essere richiamati anche da PowerShell e da Start-Run ([fonte raw](../../raw/sources/2026-04-17--a-z-index-windows-cmd-commands.md)).

## Relazioni
- Concetto: [Indice_Comandi_CMD_Windows](../concepts/Indice_Comandi_CMD_Windows.md).
- Entita correlata: [Claude_Code](Claude_Code.md).

## Contraddizioni e note
- La fonte e principalmente una reference: per uso in produzione servono policy aggiuntive su sicurezza, auditing e rollback.