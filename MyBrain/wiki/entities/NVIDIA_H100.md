---
type: entity
status: active
updated: 2026-04-29
source_ids: [SRC-20260429-dimensionamento-hardware-ai]
tags: [nvidia, gpu, datacenter, inference, thermal]
---

# NVIDIA H100

## Definizione
Acceleratore GPU datacenter di classe enterprise (architettura Hopper) usato come riferimento per inferenza LLM ad alte prestazioni.

## Fatti rilevanti
- Memoria tipica discussa nel report: 80 GB HBM3 per GPU.
- Larghezza di banda riportata: ~3.35 TB/s.
- TDP indicativo: ~700 W per scheda in configurazioni di picco.

## Caratteristiche
- Forte vantaggio su throughput per carichi 70B rispetto alla generazione precedente.
- Interconnessione NVLink utile per tensor parallelism multi-GPU.
- Supporto a precisioni moderne (incluso FP8) con buon compromesso accuracy/performance.

## Evidenze
- Nel dimensionamento worst-case 70B (20 utenti, contesto 32K), il documento propone 8x H100 80GB come configurazione stabile di riferimento ([SRC-20260429-dimensionamento-hardware-ai](../sources/SRC-20260429-dimensionamento-hardware-ai.md)).

## Relazioni
- Entita correlata: [NVIDIA_A100](NVIDIA_A100.md).
- Entita correlata: [Llama_3_1_70B](Llama_3_1_70B.md).
- Concetto correlato: [Dimensionamento_Hardware_AI](../concepts/Dimensionamento_Hardware_AI.md).

## Contraddizioni e note
- L'elevato assorbimento termico puo richiedere raffreddamento a liquido in rack ad alta densita.
