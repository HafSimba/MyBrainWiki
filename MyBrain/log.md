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
