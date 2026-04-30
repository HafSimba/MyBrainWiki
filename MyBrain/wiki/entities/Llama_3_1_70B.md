---
type: entity
status: active
updated: 2026-04-29
source_ids: [SRC-20260429-dimensionamento-hardware-ai]
tags: [llm, llama, 70b, agentic-ai, inference]
---

# Llama 3.1 70B

## Definizione
Modello open-weights di fascia alta (circa 70 miliardi di parametri) adatto a carichi agentici complessi con requisiti infrastrutturali elevati.

## Fatti rilevanti
- Parametri indicativi: ~70.6B.
- Pesi FP16: circa 140 GB VRAM.
- Nel worst-case analizzato (20 utenti concorrenti, 32K contesto), il requisito totale stimato supera 360 GB VRAM.

## Caratteristiche
- Alta capacita di reasoning, ma costo infrastrutturale significativo.
- KV cache dominante nei costi memoria in scenari agentici concorrenti.
- Richiede distribuzione multi-GPU con tensor parallelism.

## Evidenze
- Il report propone come baseline stabile un nodo con 8x H100 80GB (640 GB aggregati) e RAM host da almeno 512 GB, con raccomandazione verso 1 TB ([SRC-20260429-dimensionamento-hardware-ai](../sources/SRC-20260429-dimensionamento-hardware-ai.md)).

## Relazioni
- Entita correlata: [NVIDIA_H100](NVIDIA_H100.md).
- Entita correlata: [Llama_3_1_8B](Llama_3_1_8B.md).
- Concetto correlato: [Dimensionamento_Hardware_AI](../concepts/Dimensionamento_Hardware_AI.md).

## Contraddizioni e note
- Economicamente sostenibile solo quando il valore del reasoning aggiuntivo supera il delta CAPEX/OPEX rispetto ai modelli mini.
