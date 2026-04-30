---
type: entity
status: active
updated: 2026-04-29
source_ids: [SRC-20260429-dimensionamento-hardware-ai]
tags: [llm, llama, 8b, mini-agent, inference]
---

# Llama 3.1 8B

## Definizione
Variante compatta della famiglia Llama 3.1 (~8 miliardi di parametri), orientata a mini-agenti e automazioni con costi infrastrutturali contenuti.

## Fatti rilevanti
- Parametri indicativi: ~8.03B.
- Pesi FP16: circa 16 GB VRAM.
- Nel worst-case analizzato (20 utenti concorrenti, 32K contesto), il requisito totale stimato e poco oltre 100 GB VRAM.

## Caratteristiche
- Buon compromesso tra capacita e sostenibilita operativa.
- Puo essere servito con configurazioni hardware sensibilmente piu piccole del profilo 70B.
- Adatto a routing, task specializzati e automazioni non estreme in reasoning profondo.

## Evidenze
- Il report indica configurazioni come 2x H100 80GB o 2x A100 80GB, con RAM host tipica 128 GB e costi energetici mensili molto inferiori rispetto al 70B ([SRC-20260429-dimensionamento-hardware-ai](../sources/SRC-20260429-dimensionamento-hardware-ai.md)).

## Relazioni
- Entita correlata: [NVIDIA_A100](NVIDIA_A100.md).
- Entita correlata: [Llama_3_1_70B](Llama_3_1_70B.md).
- Concetto correlato: [Dimensionamento_Hardware_AI](../concepts/Dimensionamento_Hardware_AI.md).

## Contraddizioni e note
- In scenari con elevato bisogno di reasoning multi-step complesso, puo risultare insufficiente rispetto al 70B.
