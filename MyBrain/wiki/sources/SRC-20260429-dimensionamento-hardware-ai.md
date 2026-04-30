---
type: source
status: active
updated: 2026-04-29
source_ids: [SRC-20260429-dimensionamento-hardware-ai]
source_id: SRC-20260429-dimensionamento-hardware-ai
raw_path: raw/sources/analisi Matematica e archietturale.md
tags: [ai-infrastructure, hardware, sizing, gpu, capacity-planning, thermal, opex]
---

# SRC-20260429-dimensionamento-hardware-ai

## TL;DR
Analisi tecnica completa sul dimensionamento hardware per agenti LLM: nel worst-case di 20 utenti concorrenti con contesto 32K, il profilo 70B richiede infrastruttura multi-GPU di fascia alta (tipicamente 8x H100), mentre il profilo 8B e molto piu sostenibile in memoria, termica e OPEX.

## Punti chiave
- La memoria VRAM non dipende solo dai pesi del modello: nei workflow agentici la KV cache cresce linearmente con utenti concorrenti e lunghezza contesto, diventando il collo di bottiglia principale ([fonte raw](../../raw/sources/analisi%20Matematica%20e%20archietturale.md)).
- Scenario 70B (20 utenti, 32K): il documento stima oltre 360 GB VRAM necessari e propone 8x H100 80GB (640 GB aggregati) come configurazione stabile per produzione ([fonte raw](../../raw/sources/analisi%20Matematica%20e%20archietturale.md)).
- Scenario 8B (20 utenti, 32K): stima poco oltre 100 GB VRAM totali, con configurazioni pratiche tipo 2x H100 80GB o 2x A100 80GB ([fonte raw](../../raw/sources/analisi%20Matematica%20e%20archietturale.md)).
- Il report include anche dimensionamento termico e costo energetico mensile (PUE 1.30, Lombardia 2026) come vincoli architetturali di primo livello ([fonte raw](../../raw/sources/analisi%20Matematica%20e%20archietturale.md)).

## Evidenze estratte
- 70B: pesi FP16 ~140 GB; con KV cache worst-case (20 utenti, 32K) + overhead si arriva a un requisito totale >360 GB VRAM ([fonte raw](../../raw/sources/analisi%20Matematica%20e%20archietturale.md)).
- 70B: il testo raccomanda un nodo con 8x H100 80GB e RAM host almeno 512 GB, preferibilmente 1 TB ([fonte raw](../../raw/sources/analisi%20Matematica%20e%20archietturale.md)).
- 8B: pesi ~16 GB; requisito totale riportato poco oltre 100 GB VRAM; RAM host consigliata 128 GB per carico agentico concorrente ([fonte raw](../../raw/sources/analisi%20Matematica%20e%20archietturale.md)).
- Termica: 70B ~7000W, ~23.898 BTU/h, ~1106 CFM (raccomandato DLC); 8B ~1400W, ~4.780 BTU/h, ~221 CFM (aria forzata standard) ([fonte raw](../../raw/sources/analisi%20Matematica%20e%20archietturale.md)).
- OPEX energia (Lombardia, PUE 1.30, 0.158 EUR/kWh): ~840 EUR/mese per profilo 70B vs ~168 EUR/mese per profilo 8B ([fonte raw](../../raw/sources/analisi%20Matematica%20e%20archietturale.md)).

## Impatti sulla wiki
- Aggiornare linee guida di capacity planning con separazione esplicita tra profilo high-end (70B) e profilo mini-agent (8B).
- Rafforzare il concetto [Dimensionamento_Hardware_AI](../concepts/Dimensionamento_Hardware_AI.md) con metrica integrata VRAM + termica + OPEX.
- Formalizzare entita infrastrutturali e modello: [NVIDIA_H100](../entities/NVIDIA_H100.md), [NVIDIA_A100](../entities/NVIDIA_A100.md), [Llama_3_1_70B](../entities/Llama_3_1_70B.md), [Llama_3_1_8B](../entities/Llama_3_1_8B.md).

## Contraddizioni e incertezze
- Alcune fonti bibliografiche citate sono divulgative/comunitarie (blog, forum), quindi alcuni valori vanno verificati su documentazione primaria vendor in fase di procurement.
- Il testo usa ipotesi operative (20 utenti sempre concorrenti, contesto fisso 32K, carico medio 80%) che devono essere ricalibrate sul traffico reale.

## Azioni successive
- Definire un profilo SLO interno (latenza p95, token/s, max context, tasso di tool-call) e ricalcolare il dimensionamento sui dati reali.
- Aggiungere una tabella comparativa tra SKU GPU candidate (H100, A100, L40S, eventuali Blackwell) con costo totale annuo.
