---
type: concept
status: active
updated: 2026-04-17
source_ids: [SRC-20260417-multi-agent-system-wikipedia, SRC-20260417-openclaw-docs, SRC-20260429-hmas-on-prem]
tags: [mas, coordination, decentralization, llm]
---

# Sistemi Multi Agente

## Definizione
Architettura computazionale in cui piu agenti autonomi interagiscono e coordinano decisioni per risolvere problemi complessi.

## Perche conta
Abilita scalabilita, resilienza e parallelismo su compiti che superano la capacita di un singolo agente.

## Regole operative
- Definisci ruoli agenti e confini di responsabilita.
- Scegli protocollo decisionale esplicito (voto, consenso, negoziazione).
- Progetta comunicazione e memoria con vincoli chiari di costo e latenza.
- Prevedi meccanismi di fault tolerance e recupero.

## Evidenze
- La fonte MAS identifica autonomia, vista locale e decentralizzazione come proprieta essenziali ([SRC-20260417-multi-agent-system-wikipedia](../sources/SRC-20260417-multi-agent-system-wikipedia.md)).
- Nel vault, OpenClaw documenta routing multi-agent con sessioni isolate come caso applicativo concreto ([SRC-20260417-openclaw-docs](../sources/SRC-20260417-openclaw-docs.md)).
- Lo studio HMAS on-prem estende il pattern in forma gerarchica (supervisore + worker) con escalation deterministica orientata all'affidabilita enterprise ([SRC-20260429-hmas-on-prem](../sources/SRC-20260429-hmas-on-prem.md)).

## Collegamenti
- Concetto correlato: [Gateway_Multi_Canale](Gateway_Multi_Canale.md).
- Concetto correlato: [Selezione_LLM_Per_Caso_d_Uso](Selezione_LLM_Per_Caso_d_Uso.md).
- Entita correlata: [OpenClaw](../entities/OpenClaw.md).
- Entita correlata: [JADE_Framework](../entities/JADE_Framework.md).
- Concetto correlato: [Architettura_HMAS_On_Premise](Architettura_HMAS_On_Premise.md).

## Contraddizioni e limiti
- Aumentare il numero di agenti non garantisce automaticamente qualita migliore; la governance del coordinamento e spesso il collo di bottiglia.
