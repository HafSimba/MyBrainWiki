# LLM Wiki Schema

Versione: 1.0
Ultimo aggiornamento: 2026-04-17
Stato: attivo

## 1) Missione
Questo vault implementa un modello "LLM Wiki":
- Le fonti raw sono la verita di partenza.
- La wiki e un artefatto persistente e cumulativo gestito dall'agente LLM.
- Ogni nuova fonte viene integrata nella wiki, non solo recuperata al momento della query.

## 2) Regole non negoziabili
1. `raw/` e immutabile dopo ingestione.
2. Ogni ingest aggiorna sempre `index.md` e `log.md`.
3. Ogni output utile di query puo diventare pagina wiki persistente.
4. Ogni claim sostanziale deve avere almeno una citazione a pagina wiki o fonte raw.
5. Contraddizioni, ambiguita e gap devono essere esplicitati, mai nascosti.
6. `log.md` e append-only: non riscrivere la storia operativa.
7. Se mancano dati critici, l'agente fa domande mirate prima di finalizzare.

## 3) Convenzioni cartelle (canoniche)
| Path | Ruolo | Mutabilita | Owner |
|---|---|---|---|
| `raw/inbox/` | Nuove fonti in attesa di ingest | mutabile | umano + agente |
| `raw/sources/` | Fonti canoniche ingestite | immutabile | umano |
| `raw/assets/` | Allegati locali (immagini, pdf, media) | immutabile dopo ingest | umano |
| `wiki/sources/` | Pagine per singola fonte | mutabile | agente |
| `wiki/concepts/` | Pagine concettuali trasversali | mutabile | agente |
| `wiki/entities/` | Persone, aziende, tool, progetti | mutabile | agente |
| `wiki/syntheses/` | Tesi, comparative, mappe | mutabile | agente |
| `wiki/queries/` | Risposte utili promosse a pagina | mutabile | agente |
| `wiki/lint/` | Report di salute del vault | mutabile | agente |
| `templates/` | Template standard delle pagine | mutabile | agente |

## 4) Naming convention
### 4.1 Source ID
Formato obbligatorio: `SRC-YYYYMMDD-slug`
Esempio: `SRC-20260417-rituali-revisione`

### 4.2 File raw
Formato consigliato: `raw/sources/YYYY-MM-DD--slug.md`
Esempio: `raw/sources/2026-04-17--rituali-di-revisione-personale.md`

### 4.3 File wiki
- Fonte: `wiki/sources/SRC-YYYYMMDD-slug.md`
- Concetto: `wiki/concepts/Nome_Concetto.md`
- Entita: `wiki/entities/Nome_Entita.md`
- Sintesi: `wiki/syntheses/Nome_Sintesi.md`
- Query persistita: `wiki/queries/YYYY-MM-DD--slug-domanda.md`
- Lint report: `wiki/lint/YYYY-MM-DD--lint.md`

## 5) Frontmatter minimo (obbligatorio per pagine wiki)
Usare questo blocco YAML all'inizio di ogni pagina wiki:

```yaml
---
type: source|concept|entity|synthesis|query|lint
status: active|draft|deprecated
updated: YYYY-MM-DD
source_ids: []
tags: []
---
```

Campi aggiuntivi consigliati:
- Per `type: source`: `source_id`, `raw_path`.
- Per `type: query`: `question`, `query_date`.
- Per `type: lint`: `coverage`, `orphan_count`, `contradiction_count`.

## 6) Workflow operativi

### 6.1 Ingest (obbligatorio)
Checklist:
1. Normalizza la fonte in `raw/sources/` (se necessario da `raw/inbox/`).
2. Assegna uno `source_id`.
3. Crea/aggiorna pagina in `wiki/sources/`.
4. Aggiorna pagine `wiki/concepts/` e `wiki/entities/` toccate dalla fonte.
5. Registra contraddizioni o incertezze.
6. Aggiorna `index.md`.
7. Appendi una entry in `log.md`.

Output minimo ingest:
- 1 pagina `wiki/sources/...`
- 1 update `index.md`
- 1 entry `log.md`

### 6.2 Query
Checklist:
1. Leggi prima `index.md`.
2. Identifica e leggi pagine wiki rilevanti.
3. Rispondi con citazioni esplicite.
4. Se emerge un insight riusabile, crea pagina in `wiki/queries/` o `wiki/syntheses/`.
5. Se viene creata una pagina nuova, aggiorna `index.md` e `log.md`.

### 6.3 Lint
Checklist:
1. Trova contraddizioni tra pagine.
2. Trova claim obsoleti rispetto a fonti recenti.
3. Trova pagine orfane (senza link in ingresso).
4. Trova concetti citati ma senza pagina dedicata.
5. Crea report in `wiki/lint/` con azioni consigliate.
6. Appendi entry in `log.md`.

## 7) Protocollo interazione obbligatorio
Da questo momento ogni interazione deve seguire questa struttura operativa.

### 7.1 Input utente (consigliato)
```text
operazione: ingest | query | lint | evolve-schema
obiettivo: <risultato desiderato>
input:
- <fonti, domande, vincoli>
output_atteso:
- <formato richiesto>
```

### 7.2 Comportamento agente (obbligatorio)
Per ogni interazione l'agente deve:
1. Classificare l'operazione.
2. Proporre un piano breve (3-7 passi).
3. Eseguire modifiche ai file.
4. Elencare file creati/aggiornati.
5. Aggiornare `index.md` e/o `log.md` quando richiesto dal workflow.
6. Concludere con il prossimo passo suggerito.

## 8) Regole di citazione
Usare sempre link relativi.

Pattern consigliati:
- Citazione fonte raw: `[SRC-...](raw/sources/...)`
- Citazione pagina wiki: `Titolo pagina -> wiki/<sezione>/<file>.md`

Ogni sezione "Punti chiave" o "Claim" deve avere almeno una citazione.

## 9) Politica contraddizioni e incertezza
Quando una nuova fonte confligge con pagine esistenti:
1. Non cancellare subito il claim precedente.
2. Aggiungi sezione "Contraddizioni" in pagina coinvolta.
3. Marca i claim con stato: `supported`, `contested`, `superseded`.
4. Registra il conflitto nel `log.md`.

## 10) Definizione di Done
Una operazione e considerata completa solo se:
- i file richiesti sono stati creati/aggiornati,
- il contenuto e coerente con questo schema,
- `index.md` e `log.md` sono allineati quando previsto,
- i prossimi passi sono chiari.

## 11) Regola di evoluzione schema
Questo file puo essere aggiornato nel tempo con `operazione: evolve-schema`.
Ogni modifica allo schema va annotata in `log.md` come `schema-update`.
