---
type: source
status: active
updated: 2026-04-29
source_ids: [SRC-20260429-hmas-on-prem]
source_id: SRC-20260429-hmas-on-prem
raw_path: raw/sources/analisi sistema ai azienda.md
tags: [hmas, on-prem, ai-infrastructure, rag, security, capex]
---

# SRC-20260429-hmas-on-prem

## TL;DR
Studio di fattibilita per un sistema HMAS on-premise per 20 utenti: propone un supervisore 70B con worker 8B-14B, regole di escalation deterministiche, architettura RAG con Vector DB e piattaforma HEDT multi-GPU RTX 5090.

## Punti chiave
- L'architettura target e HMAS (Supervisor-Worker): 70B per reasoning complesso e worker 8B-14B per task operativi a latenza contenuta ([fonte raw](../../raw/sources/analisi%20sistema%20ai%20azienda.md)).
- Per il profilo 70B quantizzato, la stima memoria riportata e 176 GB VRAM (42 GB pesi + 134 GB KV cache utenti), con proposta 6x RTX 5090 (192 GB) ([fonte raw](../../raw/sources/analisi%20sistema%20ai%20azienda.md)).
- Il documento scarta la ricerca lineare su wiki (Wiki-LLM) e raccomanda RAG: da ~201 GB VRAM teorici a ~0.26 GB nello scenario numerico indicato ([fonte raw](../../raw/sources/analisi%20sistema%20ai%20azienda.md)).
- Sicurezza: obbligo di sandbox containerizzata e reverse proxy per ridurre rischio da tool-calling e codice generato ([fonte raw](../../raw/sources/analisi%20sistema%20ai%20azienda.md)).

## Evidenze estratte
- Escalation deterministica: fallback al supervisore per dati sensibili/transazioni e dopo due fallimenti JSON consecutivi del worker ([fonte raw](../../raw/sources/analisi%20sistema%20ai%20azienda.md)).
- Distinta hardware HEDT proposta: Threadripper PRO + piattaforma WRX90, 512 GB RAM ECC, storage NVMe ad alta banda, doppio PSU 2000W ([fonte raw](../../raw/sources/analisi%20sistema%20ai%20azienda.md)).
- Carico energetico stimato per configurazione 6x RTX 5090: circa 3.9 kW continui, con requisiti facility industriali (linea dedicata/UPS/H24 cooling) ([fonte raw](../../raw/sources/analisi%20sistema%20ai%20azienda.md)).
- CAPEX hardware server stimato nel range 19.5k-25k EUR (esclusi software, operation e facility estese) ([fonte raw](../../raw/sources/analisi%20sistema%20ai%20azienda.md)).

## Impatti sulla wiki
- Nuovo concetto operativo: [Architettura_HMAS_On_Premise](../concepts/Architettura_HMAS_On_Premise.md).
- Nuova entita hardware: [NVIDIA_RTX_5090](../entities/NVIDIA_RTX_5090.md).
- Aggiornati concetti trasversali su multi-agent e dimensionamento hardware.

## Contraddizioni e incertezze
- Parte delle stime assume carico worst-case costante e parametri operativi fissi; il risultato reale dipende dal traffico effettivo.
- Le stime economiche sono CAPEX hardware-only e non includono in modo completo OPEX operativo annuale.

## Azioni successive
- Validare con PoC misure reali di latenza, consumo VRAM e tasso errori JSON in workload aziendale.
- Definire policy RBAC e test di sicurezza su pipeline RAG + sandbox prima del rollout esteso.
