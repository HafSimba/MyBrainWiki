# Log

Formato entry: `## [YYYY-MM-DD] operazione | titolo`

## [2026-04-17] setup | Bootstrap LLM Wiki
- Azione: creata struttura iniziale del vault per il pattern LLM Wiki.
- File creati: `schema.md`, `index.md`, `templates/source-page.template.md`, `templates/concept-page.template.md`, `templates/entity-page.template.md`.
- Cartelle create: `raw/`, `wiki/`, `templates/` con sottocartelle operative.
- Note: pronto per primo ingest guidato.

## [2026-04-17] ingest | SRC-20260417-rituali-revisione
- Fonte raw: `raw/sources/2026-04-17--rituali-di-revisione-personale.md`.
- Pagine create: `wiki/sources/SRC-20260417-rituali-revisione.md`, `wiki/concepts/Cattura_Frictionless.md`, `wiki/concepts/Review_Settimanale.md`, `wiki/entities/Inbox_Unica.md`.
- File aggiornati: `index.md`.
- Contraddizioni rilevate: nessuna; presente solo gap su metriche quantitative.
- Note operative: ingest completato con cross-link tra source, concept ed entity.

## [2026-04-17] ingest | SRC-20260417-openclaw-docs
- Fonte input: `Clippings/OpenClaw.md`.
- Fonte raw canonica: `raw/sources/2026-04-17--openclaw.md`.
- Pagine create: `wiki/sources/SRC-20260417-openclaw-docs.md`, `wiki/concepts/Gateway_Multi_Canale.md`, `wiki/entities/OpenClaw.md`.
- File aggiornati: `index.md`.
- Contraddizioni rilevate: nessuna nel documento processato; assenti metriche quantitative comparative.
- Note operative: ingest completato con normalizzazione da clippings e cross-link tra source, concept ed entity.

## [2026-04-17] ingest | SRC-20260417-openclaw-ollama
- Fonte input: `Clippings/OpenClaw ollama.md`.
- Fonte raw canonica: `raw/sources/2026-04-17--openclaw-via-ollama.md`.
- Pagine create: `wiki/sources/SRC-20260417-openclaw-ollama.md`, `wiki/concepts/Bootstrap_OpenClaw_via_Ollama.md`, `wiki/entities/Ollama.md`.
- Pagine aggiornate: `wiki/entities/OpenClaw.md`, `index.md`.
- Contraddizioni rilevate: nessuna nella fonte; presenti gap su benchmark quantitativi e requisiti infrastrutturali dettagliati.
- Note operative: ingest completato con focus su bootstrap `ollama launch`, plugin web search/fetch e modalita headless.

## [2026-04-17] ingest | SRC-20260417-intelligenza-artificiale-wikipedia
- Fonte input: `Clippings/Intelligenza artificiale.md`.
- Fonte raw canonica: `raw/sources/2026-04-17--intelligenza-artificiale-wikipedia.md`.
- Pagine create: `wiki/sources/SRC-20260417-intelligenza-artificiale-wikipedia.md`, `wiki/concepts/IA_Definizioni_Classificazioni.md`, `wiki/concepts/Governance_Regolazione_IA.md`, `wiki/entities/Wikipedia.md`.
- File aggiornati: `index.md`.
- Contraddizioni rilevate: nessuna contraddizione interna esplicita; presenti sezioni eterogenee con affidabilita non uniforme e claim da verificare su fonti primarie.
- Note operative: ingest completato con sintesi tematica su definizioni, storia, governance e regolazione IA.

## [2026-04-17] ingest | SRC-20260417-cervello-anatomia-wikipedia
- Fonte input: `Clippings/Cervello (anatomia umana).md`.
- Fonte raw canonica: `raw/sources/2026-04-17--cervello-anatomia-umana-wikipedia.md`.
- Pagine create: `wiki/sources/SRC-20260417-cervello-anatomia-wikipedia.md`, `wiki/concepts/Neuroanatomia_Funzionale.md`, `wiki/entities/Cervello_Umano.md`.
- File aggiornati: `index.md`.
- Contraddizioni rilevate: nessuna contraddizione interna esplicita; fonte enciclopedica ampia con parti da validare su letteratura primaria per uso specialistico.
- Note operative: ingest completato con allineamento al dominio IA tramite collegamento a `IA_Definizioni_Classificazioni`.

## [2026-04-17] ingest | SRC-20260417-confronto-llm-benchmark
- Fonte input: `Clippings/Quale AI usare per fare cosa il confronto tra i migliori LLM del momento.md`.
- Fonte raw canonica: `raw/sources/2026-04-17--confronto-migliori-llm-benchmark.md`.
- Pagine create: `wiki/sources/SRC-20260417-confronto-llm-benchmark.md`, `wiki/concepts/Selezione_LLM_Per_Caso_d_Uso.md`, `wiki/entities/Chatbot_Arena.md`.
- File aggiornati: `index.md`.
- Contraddizioni rilevate: nessuna contraddizione interna esplicita; benchmark utili ma non assoluti e soggetti a variabilita temporale.
- Note operative: ingest completato con focus su scelta LLM per task (ricerca, coding, ragionamento) tramite benchmark dedicati.

## [2026-04-17] ingest | SRC-20260417-multi-agent-system-wikipedia
- Fonte input: `Clippings/Multi-agent system.md`.
- Fonte raw canonica: `raw/sources/2026-04-17--multi-agent-system-wikipedia.md`.
- Pagine create: `wiki/sources/SRC-20260417-multi-agent-system-wikipedia.md`, `wiki/concepts/Sistemi_Multi_Agente.md`, `wiki/entities/JADE_Framework.md`.
- File aggiornati: `index.md`.
- Contraddizioni rilevate: nessuna contraddizione interna esplicita; contenuto eterogeneo con riferimenti teorici e industriali da verificare per dominio specifico.
- Note operative: ingest completato con collegamento tra MAS classici e orchestrazione LLM-based.

## [2026-04-17] maintenance | README operativo del brain
- Azione: trasformata guida iniziale in README operativo.
- File creati: `README.md`.
- File aggiornati: `Benvenuto.md`, `index.md`.
- Crediti aggiunti: gist di Karpathy e video guida richiesti.

## [2026-04-17] ingest | SRC-20260417-python-algoritmi-ia-humai
- Fonte input: `Clippings/Python un’ottima scelta per gli algoritmi di intelligenza artificiale – Intelligenza artificiale e umana. Il giusto mix tra uomo e macchina.md`.
- Fonte raw canonica: `raw/sources/2026-04-17--python-algoritmi-ia-humai.md`.
- Pagine create: `wiki/sources/SRC-20260417-python-algoritmi-ia-humai.md`, `wiki/concepts/Ecosistema_Python_per_IA.md`, `wiki/entities/Python.md`.
- Pagine aggiornate: `wiki/concepts/IA_Definizioni_Classificazioni.md`, `index.md`.
- Contraddizioni rilevate: nessuna contraddizione interna esplicita; fonte divulgativa con base quantitativa comparativa limitata.
- Note operative: ingest completato con focus su ecosistema Python per IA, librerie principali e implicazioni operative di prototipazione.

## [2026-04-17] lint | Audit coerenza wiki
- Scope: controllo su pagine `wiki/sources`, `wiki/concepts`, `wiki/entities` e file core (`schema.md`, `index.md`, `README.md`).
- Report creato: `wiki/lint/2026-04-17--lint.md`.
- Esito: 0 contraddizioni critiche, 0 pagine orfane, 1 area a rischio obsolescenza (benchmark LLM), 1 gap concettuale (LLM Wiki senza pagina dedicata).
- Note tecniche: rilevato 1 placeholder link in `schema.md` (non bloccante, da normalizzare per evitare falsi positivi di lint).
- File aggiornati: `index.md`.

## [2026-04-17] ingest | SRC-20260417-claude-code-ollama
- Fonte input: `Clippings/Claude Code.md`.
- Fonte raw canonica: `raw/sources/2026-04-17--claude-code.md`.
- Pagine create: `wiki/sources/SRC-20260417-claude-code-ollama.md`, `wiki/concepts/Bootstrap_Claude_Code_via_Ollama.md`, `wiki/entities/Claude_Code.md`.
- Pagine aggiornate: `wiki/entities/Ollama.md`, `index.md`.
- Contraddizioni rilevate: nessuna contraddizione interna esplicita; gap su benchmark quantitativi e profili costo/latenza dei modelli consigliati.
- Note operative: ingest completato con focus su bootstrap `ollama launch claude`, modalita headless, `/loop` per task ricorrenti e integrazione API Anthropic-compatible.

## [2026-04-17] ingest | SRC-20260417-claude-code-memory
- Fonte input: `Clippings/How Claude remembers your project.md`.
- Fonte raw canonica: `raw/sources/2026-04-17--how-claude-remembers-project.md`.
- Pagine create: `wiki/sources/SRC-20260417-claude-code-memory.md`, `wiki/concepts/Memoria_Persistente_Claude_Code.md`.
- Pagine aggiornate: `wiki/entities/Claude_Code.md`, `index.md`.
- Contraddizioni rilevate: nessuna contraddizione interna esplicita; presenti limiti su metriche quantitative dell'impatto memoria.
- Note operative: ingest completato con focus su `CLAUDE.md`, auto memory, comando `/memory`, rules path-scoped e gestione conflitti istruzioni.

## [2026-04-17] lint | Audit coerenza wiki (refresh)
- Scope: controllo su pagine `wiki/sources`, `wiki/concepts`, `wiki/entities` e file core (`schema.md`, `index.md`, `README.md`).
- Report aggiornato: `wiki/lint/2026-04-17--lint.md`.
- Esito: 0 contraddizioni critiche, 0 pagine orfane, 2 aree a rischio obsolescenza (benchmark LLM + guida operativa Claude Code/Ollama), 1 gap concettuale (LLM Wiki senza pagina dedicata).
- Note tecniche: rilevati 2 link non bloccanti da correggere (placeholder in `schema.md`, path README in `index.md`).
- File aggiornati: `wiki/lint/2026-04-17--lint.md`.

## [2026-04-17] schema-update | Correzione pattern citazioni
- Azione: sostituito il pattern placeholder di citazione wiki in `schema.md` con forma testuale non linkabile per evitare falsi positivi lint.
- File aggiornati: `schema.md`.
- Note: aggiornamento conforme alla regola di evoluzione schema.

## [2026-04-17] lint | Audit coerenza wiki (post-correzioni link)
- Scope: verifica link e coerenza su file core e pagine wiki dopo le correzioni suggerite dal lint precedente.
- Report aggiornato: `wiki/lint/2026-04-17--lint.md`.
- Esito: 0 contraddizioni critiche, 0 pagine orfane, 2 aree a rischio obsolescenza, 1 gap concettuale (LLM Wiki senza pagina dedicata).
- Note tecniche: link placeholder in `schema.md` risolto; link README in `index.md` corretto (`../README.md`); broken link residui: 0 wiki, 0 core.
- File aggiornati: `index.md`, `wiki/lint/2026-04-17--lint.md`.

## [2026-04-17] ingest | SRC-20260417-a-z-index-windows-cmd-commands
- Fonte input: `Clippings/An A-Z Index of Windows CMD commands.md`.
- Fonte raw canonica: `raw/sources/2026-04-17--a-z-index-windows-cmd-commands.md`.
- Pagine create: `wiki/sources/SRC-20260417-a-z-index-windows-cmd-commands.md`, `wiki/concepts/Indice_Comandi_CMD_Windows.md`, `wiki/entities/CMD_Windows.md`.
- Pagine aggiornate: `index.md`.
- Contraddizioni rilevate: nessuna contraddizione interna esplicita; fonte di tipo reference con limiti su contesto operativo e hardening.
- Note operative: ingest completato con distinzione comandi interni/esterni CMD e collegamenti a uso CLI su ambiente Windows.

## [2026-04-17] ingest | SRC-20260417-a-z-index-linux-command-line
- Fonte input: `Clippings/An A-Z Index of the Linux command line.md`.
- Fonte raw canonica: `raw/sources/2026-04-17--a-z-index-linux-command-line.md`.
- Pagine create: `wiki/sources/SRC-20260417-a-z-index-linux-command-line.md`, `wiki/concepts/Indice_Comandi_Bash_Linux.md`, `wiki/entities/Bash.md`.
- Pagine aggiornate: `index.md`.
- Contraddizioni rilevate: nessuna contraddizione interna esplicita; fonte di tipo reference con limiti su policy di sicurezza e contesto operativo locale.
- Note operative: ingest completato con distinzione tra built-in bash e utility esterne, e collegamento cross-OS con la mappa comandi CMD Windows.

## [2026-04-17] ingest | SRC-20260417-claude-mythos-preview-cybersecurity
- Fonte input: `Clippings/Claude Mythos Preview  red.anthropic.com.md`.
- Fonte raw canonica: `raw/sources/2026-04-17--claude-mythos-preview-red-anthropic.md`.
- Pagine create: `wiki/sources/SRC-20260417-claude-mythos-preview-cybersecurity.md`, `wiki/concepts/Transizione_Cybersecurity_con_LLM.md`, `wiki/entities/Claude_Mythos_Preview.md`.
- Pagine aggiornate: `index.md`.
- Contraddizioni rilevate: nessuna contraddizione interna esplicita; presenti limiti di verificabilita immediata per dettagli non divulgati durante il periodo di responsible disclosure.
- Note operative: analisi completata con focus su impatto operativo per team difensivi (patch latency, triage scalabile, automazione incident response).

## [2026-04-24] ingest | SRC-20260424-gpt-5-5
- Fonte input: `Clippings/Introducing GPT-5.5.md`.
- Fonte raw canonica: `raw/sources/2026-04-24--gpt-5-5.md`.
- Pagine create: `wiki/sources/SRC-20260424-gpt-5-5.md`, `wiki/entities/GPT_5_5.md`, `wiki/entities/OpenAI.md`.
- Pagine aggiornate: `wiki/concepts/Selezione_LLM_Per_Caso_d_Uso.md`, `index.md`.
- Contraddizioni rilevate: nessuna contraddizione interna esplicita; presenti caveat su SWE-Bench Pro (memorization) e benchmark internal non indipendenti.
- Note operative: ingest completato con focus su benchmark GPT-5.5 vs competition (Claude Opus 4.7, Gemini 3.1 Pro), pricing API imminente, e cyber safeguards "High" sotto Preparedness Framework.

## [2026-04-29] ingest | SRC-20260429-dimensionamento-hardware-ai
- Fonte input: `raw/sources/Dimensionamento Hardware AI_ Calcoli e Specifiche.pdf`.
- Fonte raw canonica: `raw/sources/Dimensionamento Hardware AI_ Calcoli e Specifiche.pdf`.
- Pagine create: `wiki/sources/SRC-20260429-dimensionamento-hardware-ai.md`, `wiki/concepts/Dimensionamento_Hardware_AI.md`.
- Pagine aggiornate: `index.md`.
- Contraddizioni rilevate: nessuna contraddizione interna esplicita verificabile; presente gap tecnico su estrazione testo/tabelle dal PDF.
- Note operative: ingest iniziale completato in modalita metadata-first (stato `draft`), con tracciamento fonte e concetto; necessaria estrazione/OCR successiva per consolidare claim numerici e raccomandazioni hardware.

## [2026-04-29] ingest | SRC-20260429-dimensionamento-hardware-ai (refresh da .md)
- Fonte input: `raw/sources/analisi Matematica e archietturale.md`.
- Fonte raw canonica: `raw/sources/analisi Matematica e archietturale.md`.
- Pagine create: nessuna.
- Pagine aggiornate: `wiki/sources/SRC-20260429-dimensionamento-hardware-ai.md`, `wiki/concepts/Dimensionamento_Hardware_AI.md`, `index.md`.
- Contraddizioni rilevate: nessuna contraddizione interna esplicita; presenti assunzioni da validare su workload reali (concorrenza, contesto, utilizzo medio) e fonti non primarie in bibliografia.
- Note operative: pagina source promossa a `status: active`; consolidati numeri di sizing (70B vs 8B), requisiti termici (CFM/BTU) e stime OPEX energetiche per scenario Lombardia 2026.

## [2026-04-29] ingest-update | Entita hardware e modelli Llama
- Fonte di riferimento: `raw/sources/analisi Matematica e archietturale.md`.
- Pagine create: `wiki/entities/NVIDIA_H100.md`, `wiki/entities/NVIDIA_A100.md`, `wiki/entities/Llama_3_1_70B.md`, `wiki/entities/Llama_3_1_8B.md`.
- Pagine aggiornate: `wiki/sources/SRC-20260429-dimensionamento-hardware-ai.md`, `wiki/concepts/Dimensionamento_Hardware_AI.md`, `index.md`.
- Contraddizioni rilevate: nessuna nuova contraddizione esplicita; resta il limite di generalizzazione delle stime su workload reali.
- Note operative: formalizzati i nodi principali del dominio (hardware + modelli) per migliorare navigabilita e query semantiche cross-page.

## [2026-04-29] ingest | SRC-20260429-hmas-on-prem
- Fonte input: `raw/sources/analisi sistema ai azienda.md`.
- Fonte raw canonica: `raw/sources/analisi sistema ai azienda.md`.
- Pagine create: `wiki/sources/SRC-20260429-hmas-on-prem.md`, `wiki/concepts/Architettura_HMAS_On_Premise.md`, `wiki/entities/NVIDIA_RTX_5090.md`.
- Pagine aggiornate: `wiki/concepts/Sistemi_Multi_Agente.md`, `wiki/concepts/Dimensionamento_Hardware_AI.md`, `index.md`.
- Contraddizioni rilevate: nessuna contraddizione interna esplicita; presenti stime dipendenti da ipotesi operative (concorrenza costante, quality gate, profilo traffico).
- Note operative: ingest completato con focus su architettura gerarchica supervisor-worker, fallback deterministico, adozione RAG e vincoli facility/termici per deployment on-prem.

## [2026-04-29] maintenance | Normalizzazione unita + lint calcoli
- File aggiornato: `raw/sources/analisi sistema ai azienda.md`.
- Azione: allineate unita e variabili matematiche (`Ctoken`, `Tuser`, `Kuser`, `VRAMkv`, `VRAMtot`) per distinguere coerentemente componente KV dinamica e memoria totale.
- Lint report creato: `wiki/lint/2026-04-29--lint.md`.
- File aggiornati: `index.md`.
- Esito lint: 0 contraddizioni critiche, 1 divergenza non bloccante di assunzioni (scenario datacenter FP16/BF16 vs scenario HEDT quantizzato), 0 pagine orfane.
