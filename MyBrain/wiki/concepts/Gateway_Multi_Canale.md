---
type: concept
status: active
updated: 2026-04-17
source_ids: [SRC-20260417-openclaw-docs]
tags: [gateway, routing, multi-channel]
---

# Gateway Multi Canale

## Definizione
Pattern architetturale in cui un unico gateway riceve messaggi da piu canali e li instrada verso uno o piu agenti, mantenendo stato sessioni e policy operative.

## Perche conta
Riduce duplicazione configurativa per canale, centralizza sicurezza/routing e abilita uso ubiquo dell'assistente AI da superfici diverse.

## Regole operative
- Un punto di ingresso per canali eterogenei.
- Sessioni isolate per sender, workspace o agente.
- Configurazione centralizzata con allowlist e regole menzioni nei gruppi.

## Evidenze
- La documentazione OpenClaw descrive il gateway come source of truth per sessioni e connessioni canale ([SRC-20260417-openclaw-docs](../sources/SRC-20260417-openclaw-docs.md)).
- Sono previsti canali built-in e plugin esterni in uno stesso runtime ([fonte raw](../../raw/sources/2026-04-17--openclaw.md)).

## Collegamenti
- Entita correlata: [OpenClaw](../entities/OpenClaw.md).

## Contraddizioni e limiti
- Limite: la fonte non include dati numerici su scalabilita e affidabilita in produzione.
