---
type: concept
status: active
updated: 2026-04-24
source_ids: [SRC-20260417-confronto-llm-benchmark, SRC-20260417-intelligenza-artificiale-wikipedia, SRC-20260424-gpt-5-5]
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
- GPT-5.5 (2026-04) conferma il pattern: model selection dipende dal task specifico; coding eccelle su Terminal-Bench 82.7%, mentre Claude Opus 4.7 rimane superiore su SWE-Bench Pro 64.3% vs 58.6% ([SRC-20260424-gpt-5-5](../sources/SRC-20260424-gpt-5-5.md)).

## Aggiornamento benchmark GPT-5.5 (2026-04)
| Task | Miglior modello | Score | Note |
|---|---|---|---|
| Agentic coding | GPT-5.5 | 82.7% Terminal-Bench | State-of-the-art |
| Real-world issue resolution | Claude Opus 4.7 | 64.3% SWE-Bench Pro | Superiore, ma con caveat memorization |
| Knowledge work | GPT-5.5 | 84.9% GDPval | Leadership |
| Computer use | GPT-5.5 / Claude | ~78% OSWorld | Pareggio |
| Cybersecurity | GPT-5.5 | 81.8% CyberGym | Leadership |
| Math hard (Tier 4) | GPT-5.5 | 35.4% FrontierMath | 2x Claude Opus 4.7 |

## Collegamento entità
- Entita correlata: [Chatbot_Arena](../entities/Chatbot_Arena.md).
- Entita correlata: [GPT_5_5](../entities/GPT_5_5.md).
- Entita correlata: [OpenAI](../entities/OpenAI.md).

## Collegamenti
- Entita correlata: [Chatbot_Arena](../entities/Chatbot_Arena.md).
- Concetto correlato: [IA_Definizioni_Classificazioni](IA_Definizioni_Classificazioni.md).

## Contraddizioni e limiti
- Un benchmark non misura tutte le dimensioni di qualita reale (robustezza, sicurezza, costo, UX).
