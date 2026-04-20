---
type: source
status: active
updated: 2026-04-17
source_ids: [SRC-20260417-a-z-index-linux-command-line]
source_id: SRC-20260417-a-z-index-linux-command-line
raw_path: raw/sources/2026-04-17--a-z-index-linux-command-line.md
tags: [linux, bash, cli, reference]
---

# SRC-20260417-a-z-index-linux-command-line

## TL;DR
La fonte e un indice A-Z della command line Linux (bash + utility) con descrizioni sintetiche e link di approfondimento per sintassi e uso pratico.

## Punti chiave
- L'indice copre un insieme ampio di comandi per file system, processi, rete, permessi, utenti, package management e automazione shell ([fonte raw](../../raw/sources/2026-04-17--a-z-index-linux-command-line.md)).
- La fonte distingue i comandi built-in di bash (marcati con simbolo) dagli altri comandi e core utils disponibili anche in shell alternative ([fonte raw](../../raw/sources/2026-04-17--a-z-index-linux-command-line.md)).
- Ogni voce rinvia a una pagina dedicata, utile come punto di accesso rapido a sintassi ed esempi ([fonte raw](../../raw/sources/2026-04-17--a-z-index-linux-command-line.md)).

## Evidenze estratte
- Sono presenti comandi essenziali di navigazione e manipolazione file (`cd`, `ls`, `cp`, `mv`, `rm`, `find`) e comandi di analisi testo (`grep`, `sed`, `awk`) ([fonte raw](../../raw/sources/2026-04-17--a-z-index-linux-command-line.md)).
- Sono presenti comandi per processi e diagnostica (`ps`, `top`, `kill`, `strace`) e rete (`ssh`, `scp`, `ping`, `traceroute`, `netstat`) ([fonte raw](../../raw/sources/2026-04-17--a-z-index-linux-command-line.md)).
- Sono inclusi riferimenti a manuali esterni (`man7`, GNU CoreUtils) per approfondimenti ufficiali ([fonte raw](../../raw/sources/2026-04-17--a-z-index-linux-command-line.md)).

## Impatti sulla wiki
- Creata pagina concetto [Indice_Comandi_Bash_Linux](../concepts/Indice_Comandi_Bash_Linux.md).
- Creata pagina entita [Bash](../entities/Bash.md).

## Contraddizioni e incertezze
- Nessuna contraddizione interna esplicita.
- La fonte e una reference: non fornisce policy di sicurezza operative specifiche per ambiente.

## Azioni successive
- Creare una shortlist dei comandi Linux ad alto valore per il tuo workflow quotidiano.
- Aggiungere note di sicurezza per comandi distruttivi o privilegiati (`sudo`, `rm`, `dd`, `chmod`, `chown`).
- Collegare equivalenze Linux/Windows per attivita ricorrenti in contesti multi-OS.