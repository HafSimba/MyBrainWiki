---
type: source
status: active
updated: 2026-04-17
source_ids: [SRC-20260417-claude-code-ollama]
source_id: SRC-20260417-claude-code-ollama
raw_path: raw/sources/2026-04-17--claude-code.md
tags: [claude-code, ollama, cli, automation]
---

# SRC-20260417-claude-code-ollama

## TL;DR
La fonte documenta come usare Claude Code con Ollama tramite API compatibile Anthropic, includendo setup rapido, esecuzione headless e automazioni periodiche con `/loop`.

## Punti chiave
- Claude Code e descritto come tool agentico di coding capace di leggere, modificare ed eseguire codice nella working directory ([fonte raw](../../raw/sources/2026-04-17--claude-code.md)).
- Ollama abilita l'uso di modelli open/cloud in Claude Code tramite endpoint compatibile Anthropic ([fonte raw](../../raw/sources/2026-04-17--claude-code.md)).
- Il bootstrap rapido passa da `ollama launch claude`, con opzione di modello esplicito per run dirette ([fonte raw](../../raw/sources/2026-04-17--claude-code.md)).
- In modalita headless, `--yes` automatizza pull/selezione e richiede `--model`, utile per CI/CD o script ([fonte raw](../../raw/sources/2026-04-17--claude-code.md)).

## Evidenze estratte
- Sono riportati modelli consigliati (cloud e non cloud) e link al catalogo dedicato ([fonte raw](../../raw/sources/2026-04-17--claude-code.md)).
- Il comando `/loop <interval> <prompt>` supporta automazioni ricorrenti dentro Claude Code ([fonte raw](../../raw/sources/2026-04-17--claude-code.md)).
- La configurazione manuale richiede variabili `ANTHROPIC_AUTH_TOKEN`, `ANTHROPIC_API_KEY`, `ANTHROPIC_BASE_URL` ([fonte raw](../../raw/sources/2026-04-17--claude-code.md)).
- E raccomandata una context window di almeno 64k token ([fonte raw](../../raw/sources/2026-04-17--claude-code.md)).

## Impatti sulla wiki
- Creata pagina concetto [Bootstrap_Claude_Code_via_Ollama](../concepts/Bootstrap_Claude_Code_via_Ollama.md).
- Creata pagina entita [Claude_Code](../entities/Claude_Code.md).
- Aggiornata pagina entita [Ollama](../entities/Ollama.md).

## Contraddizioni e incertezze
- Nessuna contraddizione interna esplicita nella fonte.
- Gap: assenti benchmark quantitativi su tempi/costi/qualita nei diversi modelli consigliati.

## Azioni successive
- Definire policy di permission per uso operativo (interactive vs headless).
- Creare matrice locale per scelta modello (latenza, costo, context, qualita su task reali).
- Testare workflow `/loop` su task periodici del brain.