---
type: concept
status: active
updated: 2026-04-17
source_ids: [SRC-20260417-confronto-llm-benchmark, SRC-20260417-intelligenza-artificiale-wikipedia]
tags: [llm, benchmark, decision-making, ai]
---

# Selezione LLM Per Caso d'Uso

## Definizione
Approccio pratico alla scelta di modelli linguistici basato sul tipo di attivita da svolgere e sui benchmark piu pertinenti a quella attivita.

## Perche conta
Riduce scelte arbitrarie del modello e migliora affidabilita operativa: il miglior LLM dipende dal compito, non da un ranking unico.

## Regole operative
- Definisci prima il task primario (es. ricerca, coding, ragionamento complesso).
- Associa al task il benchmark piu rappresentativo.
- Confronta i migliori modelli sul benchmark specifico, non su metriche aggregate vaghe.
- Rivalida periodicamente perche i ranking cambiano nel tempo.

## Evidenze
- La fonte mappa esplicitamente task diversi su benchmark diversi (GPQA, SWE-bench, Chatbot Arena) ([SRC-20260417-confronto-llm-benchmark](../sources/SRC-20260417-confronto-llm-benchmark.md)).
- La fonte su IA ribadisce che differenti tecniche/obiettivi richiedono criteri diversi di valutazione ([SRC-20260417-intelligenza-artificiale-wikipedia](../sources/SRC-20260417-intelligenza-artificiale-wikipedia.md)).

## Collegamenti
- Entita correlata: [Chatbot_Arena](../entities/Chatbot_Arena.md).
- Concetto correlato: [IA_Definizioni_Classificazioni](IA_Definizioni_Classificazioni.md).

## Contraddizioni e limiti
- Un benchmark non misura tutte le dimensioni di qualita reale (robustezza, sicurezza, costo, UX).
