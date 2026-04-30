---
type: concept
status: active
updated: 2026-04-29
source_ids: [SRC-20260429-hmas-on-prem]
tags: [hmas, multi-agent, on-prem, escalation, rag]
---

# Architettura HMAS On Premise

## Definizione
Pattern architetturale gerarchico in cui un supervisore LLM di fascia alta orchestra worker compatti, con escalation deterministica e integrazione RAG, per erogare servizi AI on-premise a piu utenti concorrenti.

## Perche conta
Permette di mantenere qualita logica sui task complessi senza sostenere il costo di far eseguire ogni richiesta da un modello massimo.

## Regole operative
- Separare chiaramente i ruoli: supervisore per casi ad alto rischio/complessita, worker per richieste standard.
- Applicare escalation deterministica (regole hardcoded), non auto-valutazione del worker.
- Rendere obbligatori sandboxing e reverse proxy per tutto il tool-calling.
- Usare RAG + Vector DB per evitare saturazione del contesto con ricerca lineare documentale.

## Evidenze
- Il documento propone formalmente paradigma supervisor-worker con regole di fallback JSON e routing sensibile verso modello superiore ([SRC-20260429-hmas-on-prem](../sources/SRC-20260429-hmas-on-prem.md)).
- Nello scenario numerico indicato, il passaggio da Wiki-LLM a RAG riduce drasticamente il consumo VRAM teorico per query concorrenti ([SRC-20260429-hmas-on-prem](../sources/SRC-20260429-hmas-on-prem.md)).
- La fattibilita on-prem viene legata a una piattaforma HEDT multi-GPU con vincoli forti su elettrico e termica ([SRC-20260429-hmas-on-prem](../sources/SRC-20260429-hmas-on-prem.md)).

## Collegamenti
- Concetto correlato: [Sistemi_Multi_Agente](Sistemi_Multi_Agente.md).
- Concetto correlato: [Dimensionamento_Hardware_AI](Dimensionamento_Hardware_AI.md).
- Entita correlata: [NVIDIA_RTX_5090](../entities/NVIDIA_RTX_5090.md).
- Entita correlata: [Llama_3_1_70B](../entities/Llama_3_1_70B.md).
- Entita correlata: [Llama_3_1_8B](../entities/Llama_3_1_8B.md).

## Contraddizioni e limiti
- Le metriche dichiarate dipendono da ipotesi di carico e quality gate che devono essere convalidate in ambiente reale.
