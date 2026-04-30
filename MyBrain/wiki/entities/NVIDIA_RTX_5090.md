---
type: entity
status: active
updated: 2026-04-29
source_ids: [SRC-20260429-hmas-on-prem]
tags: [nvidia, gpu, workstation, hedt, on-prem]
---

# NVIDIA RTX 5090

## Definizione
GPU di fascia alta consumer/prosumer considerata nel report come base per cluster HEDT multi-GPU dedicati a inferenza AI on-premise.

## Fatti rilevanti
- Configurazione proposta: 6 GPU per un totale di 192 GB VRAM aggregata.
- TDP unitario usato nei calcoli: circa 550 W.
- Ruolo: supportare il profilo supervisore 70B quantizzato nel worst-case operativo analizzato.

## Caratteristiche
- Accessibile in contesti HEDT rispetto a stack datacenter top-tier.
- Richiede ingegnerizzazione fisica (riser PCIe/chassis rack) per densita multi-GPU elevate.
- Richiede pianificazione facility dedicata per potenza e raffreddamento continuo.

## Evidenze
- Il documento usa la configurazione 6x RTX 5090 come opzione fattibile per raggiungere margine VRAM rispetto al requisito stimato di 176 GB ([SRC-20260429-hmas-on-prem](../sources/SRC-20260429-hmas-on-prem.md)).

## Relazioni
- Concetto correlato: [Architettura_HMAS_On_Premise](../concepts/Architettura_HMAS_On_Premise.md).
- Concetto correlato: [Dimensionamento_Hardware_AI](../concepts/Dimensionamento_Hardware_AI.md).

## Contraddizioni e note
- Non sostituisce i vantaggi di interconnessione e affidabilita delle piattaforme datacenter enterprise.
