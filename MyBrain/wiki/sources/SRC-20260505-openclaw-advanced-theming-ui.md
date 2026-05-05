---
type: source
status: active
updated: 2026-05-05
source_ids: [SRC-20260505-openclaw-advanced-theming-ui]
source_id: SRC-20260505-openclaw-advanced-theming-ui
raw_path: raw/sources/2026-05-05--openclaw-advanced-theming-ui.md
tags: [openclaw, ui, theming, customization, self-hosted]
---

# SRC-20260505-openclaw-advanced-theming-ui

## TL;DR
Guida pratica alla personalizzazione avanzata della UI di OpenClaw Selfhost con CSS, template e JavaScript, centrata su controllo totale del branding e della user experience.

## Punti chiave
- L'interfaccia di OpenClaw e modulare e separa presentazione da funzionalita, permettendo personalizzazioni senza cambiare la logica core ([fonte raw](../../raw/sources/2026-05-05--openclaw-advanced-theming-ui.md)).
- Il motore di temi comprende override CSS, file di template e sovrascritture JavaScript per layout e comportamenti dinamici ([fonte raw](../../raw/sources/2026-05-05--openclaw-advanced-theming-ui.md)).
- Le modifiche pratiche includono CSS personalizzato, override dei template (es. login) e temi dinamici con variabili CSS e scripting ([fonte raw](../../raw/sources/2026-05-05--openclaw-advanced-theming-ui.md)).
- Il self-hosting elimina vincoli di branding e consente adattamenti per accessibilita e policy locali ([fonte raw](../../raw/sources/2026-05-05--openclaw-advanced-theming-ui.md)).
- Best practice: procedere per step, usare Git, preferire temi figlio/override e test cross-browser/device ([fonte raw](../../raw/sources/2026-05-05--openclaw-advanced-theming-ui.md)).

## Evidenze estratte
- "L'interfaccia utente di OpenClaw e essenzialmente modulare" e separa presentazione e funzionalita ([fonte raw](../../raw/sources/2026-05-05--openclaw-advanced-theming-ui.md)).
- "OpenClaw ti permette di sovrascrivere gli stili esistenti e di introdurne di completamente nuovi" tramite CSS ([fonte raw](../../raw/sources/2026-05-05--openclaw-advanced-theming-ui.md)).
- La personalizzazione dinamica con preferenze utente e variabili CSS e descritta come pratica realizzabile ([fonte raw](../../raw/sources/2026-05-05--openclaw-advanced-theming-ui.md)).

## Impatti sulla wiki
- Creata pagina concetto [Personalizzazione_UI_OpenClaw](../concepts/Personalizzazione_UI_OpenClaw.md).
- Aggiornata pagina entita [OpenClaw](../entities/OpenClaw.md).

## Contraddizioni e incertezze
- Nessuna contraddizione interna esplicita.
- Incertezza: il testo cita motori template "Handlebars, Jinja2 o simili" senza indicare il motore effettivo o i path ufficiali dei file tema.

## Azioni successive
- Verificare nella documentazione ufficiale i punti di override (CSS, template, JS) supportati dalla versione in uso.
- Definire struttura tema (CSS + template + JS) con versioning e backup dei template originali.
- Eseguire test di usabilita, accessibilita e responsivita su browser/dispositivi.
