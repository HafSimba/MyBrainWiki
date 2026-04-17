---
type: entity
status: active
updated: 2026-04-17
source_ids: [SRC-20260417-confronto-llm-benchmark]
tags: [benchmark, evaluation, llm]
---

# Chatbot Arena

## Profilo
Piattaforma di valutazione comparativa dei modelli conversazionali basata su confronti alla cieca tra due LLM e giudizio umano.

## Ruolo nel dominio
Nel vault rappresenta un riferimento per stimare performance percepita nel ragionamento complesso e nell'uso quotidiano, tramite punteggio Elo.

## Fatti rilevanti
- Metodo di valutazione: utenti confrontano due modelli senza conoscerne l'identita e scelgono la risposta migliore ([SRC-20260417-confronto-llm-benchmark](../sources/SRC-20260417-confronto-llm-benchmark.md)).
- Il punteggio Elo viene usato per stimare la forza relativa dei modelli in confronti diretti ([fonte raw](../../raw/sources/2026-04-17--confronto-migliori-llm-benchmark.md)).
- Nella fonte viene trattato come benchmark utile per il caso d'uso "ragionamento complesso" ([fonte raw](../../raw/sources/2026-04-17--confronto-migliori-llm-benchmark.md)).

## Relazioni
- Concetto: [Selezione_LLM_Per_Caso_d_Uso](../concepts/Selezione_LLM_Per_Caso_d_Uso.md).

## Contraddizioni e note
- Il giudizio crowd-based migliora il realismo d'uso ma puo includere preferenze soggettive e bias di popolazione.
