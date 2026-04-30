---
type: entity
status: active
updated: 2026-04-24
source_ids: [SRC-20260424-gpt-5-5]
tags: [openai, gpt-series, llm, frontier-model]
---

# GPT-5.5

## Definizione
Modello linguistico frontier di OpenAI rilasciato il 2026-04-22, positioning come smartest e most intuitive model fino ad oggi.

## Caratteristiche chiave
- Intelligence level superiore a GPT-5.4 mantenendo latenza equivalente per token
- Token efficiency migliorata: completamento task con meno token rispetto a GPT-5.4
-Disponibile in ChatGPT e Codex; API in arrivo
- Cyber safeguards avanzati sotto Preparedness Framework "High"
- Training e serving su NVIDIA GB200 e GB300 NVL72 systems

## Benchmark confermati
| Benchmark | GPT-5.5 | GPT-5.4 | Claude Opus 4.7 |
|---|---|---|---|
| Terminal-Bench 2.0 | 82.7% | 75.1% | 69.4% |
| Expert-SWE (internal) | 73.1% | 68.5% | - |
| GDPval | 84.9% | 83.0% | 80.3% |
| OSWorld-Verified | 78.7% | 75.0% | 78.0% |
| CyberGym | 81.8% | 79.0% | 73.1% |
| FrontierMath Tier 4 | 35.4% | 27.1% | 22.9% |

## Varianti
- **GPT-5.5**: versione standard
- **GPT-5.5 Pro**: versione per compiti più difficili, disponibile per Pro/Business/Enterprise
- **GPT-5.5 in Fast mode**: 1.5x token generation speed a 2.5x cost

## Pricing (API imminente)
- gpt-5.5: $5/1M input, $30/1M output
- gpt-5.5-pro: $30/1M input, $180/1M output
- Batch/Flex: 50% standard rate
- Priority: 2.5x standard rate

## Capacità distintive
- **Agentic coding**: planning, iteration, tool coordination; state-of-the-art su Terminal-Bench 2.0
- **Knowledge work**: documenti, spreadsheet, operational research
- **Scientific research**: GeneBench 25.0% (vs 19.0% GPT-5.4), nuove dimostrazioni matematiche
- **Computer use**: navigazione autonoma interfacce, OSWorld-Verified 78.7%

## Evidenze
- Dan Shipper (CEO Every): "First coding model I've used that has serious conceptual clarity"
- Engineer at NVIDIA: "Losing access to GPT-5.5 feels like I've had a limb amputated"
- NVIDIA VP: "It's a new way of working that helps people operate at a fundamentally different speed"
- 85%+ of OpenAI employees use Codex weekly

## Sicurezza
-cyber safeguards avanzati rispetto a GPT-5.2
- Trusted Access for Cyber program per defender verificati
- Preparedness Framework: High per cybersecurity e biology/chemistry
- Red team e valutazioni esterne prima del rilascio

## Limiti e incertezze
- SWE-Bench Pro ha evidence of memorization segnalato da Anthropic
- API pricing non ancora confermato ufficialmente
- Alcuni benchmark (es. SWE-Bench Pro) vedono Claude Opus 4.7 superiore (64.3% vs 58.6%)

## Collegamento al concetto
- Entità correlata: [Selezione_LLM_Per_Caso_d_Uso](../concepts/Selezione_LLM_Per_Caso_d_Uso.md)
- Entità correlata: [OpenAI](../entities/OpenAI.md)