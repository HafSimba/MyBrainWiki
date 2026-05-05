---
type: concept
status: active
updated: 2026-05-05
source_ids: [SRC-20260505-openclaw-advanced-theming-ui]
tags: [openclaw, ui, theming, customization]
---

# Personalizzazione UI OpenClaw

## Definizione
Approccio operativo per personalizzare l'interfaccia di OpenClaw Selfhost con override CSS, template e JavaScript, in modo da controllare brand, layout e comportamento.

## Perche conta
Abilita sovranita visiva e UX coerente con il brand, riduce dipendenza dalle impostazioni predefinite e facilita l'adeguamento a requisiti di accessibilita o policy locali.

## Regole operative
- Inizia con piccoli override CSS prima di intervenire sui template ([SRC-20260505-openclaw-advanced-theming-ui](../sources/SRC-20260505-openclaw-advanced-theming-ui.md)).
- Usa controllo versione (Git) e conserva backup dei template originali ([SRC-20260505-openclaw-advanced-theming-ui](../sources/SRC-20260505-openclaw-advanced-theming-ui.md)).
- Preferisci temi figlio/override per ridurre frizioni con gli update di OpenClaw ([SRC-20260505-openclaw-advanced-theming-ui](../sources/SRC-20260505-openclaw-advanced-theming-ui.md)).
- Testa su browser e dispositivi diversi prima del rilascio ([SRC-20260505-openclaw-advanced-theming-ui](../sources/SRC-20260505-openclaw-advanced-theming-ui.md)).

## Evidenze
- La UI e modulare e separa presentazione e funzionalita, quindi e personalizzabile senza toccare il core ([SRC-20260505-openclaw-advanced-theming-ui](../sources/SRC-20260505-openclaw-advanced-theming-ui.md)).
- CSS, template e JavaScript sono indicati come leve principali per personalizzazione avanzata e temi dinamici ([SRC-20260505-openclaw-advanced-theming-ui](../sources/SRC-20260505-openclaw-advanced-theming-ui.md)).

## Collegamenti
- Entita: [OpenClaw](../entities/OpenClaw.md).
- Concetto: [Bootstrap_OpenClaw_via_Ollama](Bootstrap_OpenClaw_via_Ollama.md).

## Contraddizioni e limiti
- La fonte non specifica il motore template o i path ufficiali per la versione OpenClaw in uso.
