---
type: concept
status: active
updated: 2026-04-29
source_ids: [SRC-20260429-dimensionamento-hardware-ai, SRC-20260429-hmas-on-prem]
tags: [ai-infrastructure, hardware, sizing, capacity-planning, kv-cache, thermal]
---

# Dimensionamento Hardware AI

## Definizione
Pratica di stima e configurazione delle risorse hardware necessarie a sostenere workload AI (training, inferenza e serving) in base a carico, latenza attesa e vincoli di costo.

## Perche conta
Un dimensionamento corretto riduce colli di bottiglia e costo totale di esercizio, evitando sia overprovisioning sia saturazione operativa.

## Regole operative
- Calcolare sempre il budget memoria come somma di pesi statici, KV cache dinamica, attivazioni e overhead runtime.
- Modellare il worst-case agentico con utenti concorrenti e contesto massimo esplicito (es. 20 utenti, 32K token), non solo con medie di traffico.
- Trattare termica e alimentazione come parte del dimensionamento primario, non come check finale.
- Distinguere profilo high-end reasoning (70B) da profilo mini-agent (8B) per ottimizzare il rapporto prestazioni/costo.

## Evidenze
- Per 70B in FP16, il documento stima requisito VRAM >360 GB nel worst-case 20x32K, con configurazione consigliata 8x H100 80GB (640 GB aggregati) ([SRC-20260429-dimensionamento-hardware-ai](../sources/SRC-20260429-dimensionamento-hardware-ai.md)).
- Per 8B, la stima totale e poco oltre 100 GB VRAM con opzioni operative come 2x H100 80GB o 2x A100 80GB ([SRC-20260429-dimensionamento-hardware-ai](../sources/SRC-20260429-dimensionamento-hardware-ai.md)).
- La componente termica differenzia fortemente le architetture: ~7000W e ~1106 CFM per 70B vs ~1400W e ~221 CFM per 8B ([SRC-20260429-dimensionamento-hardware-ai](../sources/SRC-20260429-dimensionamento-hardware-ai.md)).
- Nel caso analizzato, l'OPEX energetico mensile stimato in Lombardia e ~840 EUR (70B) contro ~168 EUR (8B), con PUE 1.30 ([SRC-20260429-dimensionamento-hardware-ai](../sources/SRC-20260429-dimensionamento-hardware-ai.md)).
- In un'alternativa HEDT, il documento HMAS stima 176 GB VRAM per profilo 70B quantizzato (20 utenti) e propone 6x RTX 5090 (192 GB) con margine operativo ([SRC-20260429-hmas-on-prem](../sources/SRC-20260429-hmas-on-prem.md)).

## Collegamenti
- Fonte correlata: [SRC-20260429-dimensionamento-hardware-ai](../sources/SRC-20260429-dimensionamento-hardware-ai.md).
- Concetto correlato: [Selezione_LLM_Per_Caso_d_Uso](Selezione_LLM_Per_Caso_d_Uso.md).
- Entita correlata: [NVIDIA_H100](../entities/NVIDIA_H100.md).
- Entita correlata: [NVIDIA_A100](../entities/NVIDIA_A100.md).
- Entita correlata: [Llama_3_1_70B](../entities/Llama_3_1_70B.md).
- Entita correlata: [Llama_3_1_8B](../entities/Llama_3_1_8B.md).
- Entita correlata: [NVIDIA_RTX_5090](../entities/NVIDIA_RTX_5090.md).

## Contraddizioni e limiti
- Alcune assunzioni (utilizzo medio 80%, contesto 32K costante, profilo carico uniforme) possono divergere in ambienti reali.
- Parte della bibliografia e non primaria; serve validazione finale con benchmark interni e specifiche ufficiali vendor.
