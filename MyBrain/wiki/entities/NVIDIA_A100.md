---
type: entity
status: active
updated: 2026-04-29
source_ids: [SRC-20260429-dimensionamento-hardware-ai]
tags: [nvidia, gpu, datacenter, inference]
---

# NVIDIA A100

## Definizione
Acceleratore GPU datacenter NVIDIA di generazione precedente a H100, ancora usato in molte installazioni enterprise per inferenza e calcolo AI.

## Fatti rilevanti
- Memoria tipica trattata nel report: 80 GB HBM2e.
- Larghezza di banda riportata: ~2.04 TB/s.
- TDP indicativo: ~400 W.

## Caratteristiche
- Profilo costo/prestazioni spesso competitivo su workload meno estremi.
- Inferiore a H100 su throughput nei carichi agentici pesanti a 70B.
- Opzione praticabile per profili 8B con concorrenza alta ma latenza meno critica.

## Evidenze
- Il documento cita configurazioni 2x A100 80GB come opzione per scenario 8B (20 utenti, 32K), con OPEX e complessita termica piu contenuti rispetto a cluster 70B ([SRC-20260429-dimensionamento-hardware-ai](../sources/SRC-20260429-dimensionamento-hardware-ai.md)).

## Relazioni
- Entita correlata: [NVIDIA_H100](NVIDIA_H100.md).
- Entita correlata: [Llama_3_1_8B](Llama_3_1_8B.md).
- Concetto correlato: [Dimensionamento_Hardware_AI](../concepts/Dimensionamento_Hardware_AI.md).

## Contraddizioni e note
- Su task ad altissimo reasoning/throughput, la minore banda memoria puo diventare il collo di bottiglia principale.
