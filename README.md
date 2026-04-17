# MyBrain - README

Questo vault implementa un secondo cervello in stile LLM Wiki: le fonti raw sono immutabili, mentre la wiki viene mantenuta in modo incrementale dall'agente.

## Obiettivo
- Accumulare conoscenza nel tempo, non solo fare retrieval puntuale.
- Tenere allineati contenuti, collegamenti, contraddizioni e cronologia operativa.
- Rendere ogni nuova fonte immediatamente utile per query future.

## Struttura del vault
- `raw/inbox/`: nuove fonti da processare.
- `raw/sources/`: fonti canoniche ingestite (immutabili).
- `raw/assets/`: allegati locali (immagini, pdf, media).
- `wiki/sources/`: pagine per singola fonte.
- `wiki/concepts/`: concetti trasversali.
- `wiki/entities/`: entita (persone, tool, aziende, framework, ecc.).
- `wiki/syntheses/`: sintesi trasversali (tesi, confronti, mappe).
- `wiki/queries/`: risposte utili promosse a pagina persistente.
- `wiki/lint/`: report di salute del vault.
- `templates/`: template markdown operativi.

## File chiave
- `schema.md`: regole e workflow ufficiali.
- `index.md`: catalogo contenuti.
- `log.md`: timeline append-only delle operazioni.

## Come usare il brain
Usa sempre questo formato nelle richieste all'agente:

```text
operazione: ingest | query | lint | evolve-schema
obiettivo: <risultato desiderato>
input:
- <fonti, domande, vincoli>
output_atteso:
- <formato finale>
```

## Workflow operativo

### 1) Ingest
Quando aggiungi un file in `Clippings/` o `raw/inbox/`, richiedi `operazione: ingest`.

L'agente deve:
1. Normalizzare la fonte in `raw/sources/`.
2. Creare una pagina in `wiki/sources/` con `source_id`.
3. Creare/aggiornare pagine in `wiki/concepts/` e `wiki/entities/`.
4. Registrare incertezze/contraddizioni.
5. Aggiornare `index.md`.
6. Appendere entry in `log.md`.

### 2) Query
Quando fai domande sul contenuto del vault, richiedi `operazione: query`.

L'agente deve:
1. Leggere `index.md`.
2. Cercare pagine rilevanti.
3. Rispondere con citazioni.
4. Se emerge un output riusabile, promuoverlo in `wiki/queries/` o `wiki/syntheses/`.
5. Aggiornare `index.md` e `log.md` se crea nuove pagine.

### 3) Lint
Periodicamente richiedi `operazione: lint`.

L'agente deve:
1. Cercare contraddizioni tra pagine.
2. Trovare claim obsoleti.
3. Trovare pagine orfane.
4. Trovare concetti citati ma senza pagina.
5. Scrivere report in `wiki/lint/`.
6. Appendere entry in `log.md`.

## Convenzioni essenziali
- Source ID: `SRC-YYYYMMDD-slug`
- File raw: `raw/sources/YYYY-MM-DD--slug.md`
- File source wiki: `wiki/sources/SRC-YYYYMMDD-slug.md`
- Ogni claim sostanziale deve avere almeno una citazione.
- `log.md` e append-only.

## Ruolo delle cartelle vuote
- `wiki/syntheses/` si popola quando produci sintesi trasversali (non a ogni ingest).
- `wiki/queries/` si popola quando una risposta e abbastanza utile da diventare conoscenza persistente.
- `wiki/lint/` si popola quando esegui audit di salute del vault.

Se queste cartelle sono vuote, non e necessariamente un errore: puo significare che finora sono state fatte soprattutto operazioni di ingest.

## Quickstart
1. Metti una nuova fonte in `Clippings/` o `raw/inbox/`.
2. Invia richiesta `operazione: ingest`.
3. Controlla nuove pagine in `wiki/`.
4. Verifica aggiornamenti in `index.md` e `log.md`.
5. Ogni 3-5 ingest, esegui un `operazione: lint`.

## Crediti
- Pattern LLM Wiki: https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f
- Video guida di riferimento: https://youtu.be/RZlHSLxpyc4?si=E51fXb1BGtcn7bwR
