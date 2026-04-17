---
type: concept
status: active
updated: 2026-04-17
source_ids: [SRC-20260417-openclaw-ollama]
tags: [bootstrap, ollama, automation, gateway]
---

# Bootstrap OpenClaw via Ollama

## Definizione
Procedura di avvio rapido in cui Ollama orchestra setup e lancio di OpenClaw tramite un singolo comando.

## Perche conta
Riduce attrito operativo iniziale: meno step manuali, onboarding guidato e configurazione agente piu rapida.

## Regole operative
- Usa `ollama launch openclaw` per setup guidato standard.
- Per automazione usa `ollama launch openclaw --model <modello> --yes`.
- Per cambio modello senza avvio usa `ollama launch openclaw --config`.
- Per modelli locali prevedi contesto di almeno 64k token.

## Evidenze
- La guida descrive l'automazione completa (installazione, onboarding, avvio gateway) con un solo launch ([SRC-20260417-openclaw-ollama](../sources/SRC-20260417-openclaw-ollama.md)).
- Il plugin web search/fetch viene abilitato automaticamente nel flusso launch ([fonte raw](../../raw/sources/2026-04-17--openclaw-via-ollama.md)).

## Collegamenti
- Entita correlata: [OpenClaw](../entities/OpenClaw.md).
- Entita correlata: [Ollama](../entities/Ollama.md).
- Concetto correlato: [Gateway_Multi_Canale](Gateway_Multi_Canale.md).

## Contraddizioni e limiti
- Limite: non sono indicate soglie prestazionali minime (CPU/RAM) per scenari headless continuativi.
