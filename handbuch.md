---
title: MD Studio — Benutzerhandbuch
version: 1.0
date: 2026-04-14
author: MD Studio Dokumentation
---

# MD Studio — Benutzerhandbuch

> **MD Studio** ist ein schlanker, vollständig lokaler Markdown-Editor, der als einzelne HTML-Datei direkt im Browser läuft — ohne Installation, ohne Server, ohne Cloud.  
> Diese Anleitung richtet sich gleichermassen an Erstnutzer (→ Abschnitte 1–4) und versierte Nutzer (→ Abschnitte 5–11).

---

## Inhaltsverzeichnis

1. [Schnellstart — 5 Minuten bis zur ersten Datei](#1-schnellstart)
2. [Benutzeroberfläche im Überblick](#2-benutzeroberfläche)
3. [Grundlegende Workflows](#3-grundlegende-workflows)
4. [Ansichtsmodi](#4-ansichtsmodi)
5. [Formular-Modus](#5-formular-modus)
6. [Datum & Versionierung](#6-datum--versionierung)
7. [Suche](#7-suche)
8. [PDF-Export](#8-pdf-export)
9. [Markdown Syntax — Schnellreferenz](#9-markdown-syntax)
10. [Auto-Save](#10-auto-save)
11. [Tastaturkürzel](#11-tastaturkürzel)
12. [Browser-Kompatibilität](#12-browser-kompatibilität)
13. [FAQ — Häufige Fragen](#13-faq)

---

## 1. Schnellstart

**MD Studio öffnen:** Doppelklick auf `md-studio.html` — der Editor öffnet sich sofort im Browser.

### Weg A — Ordner öffnen *(empfohlen, Chrome/Edge)*

```
① Klick auf  📁 Ordner  in der Seitenleiste
② Ordner im Dateidialog auswählen → Zugriff erlauben
③ Alle .md-Dateien im Ordner erscheinen links in der Dateiliste
④ Klick auf eine Datei → öffnet im Editor
```

### Weg B — Einzelne Dateien laden *(alle Browser)*

```
① Klick auf  + Laden  in der Seitenleiste
② Eine oder mehrere .md-Dateien auswählen
③ Dateien erscheinen in der Liste links
```

### Weg C — Drag & Drop *(alle Browser)*

```
① .md-Datei(en) aus dem Dateimanager direkt ins Browser-Fenster ziehen
② Goldener Rahmen erscheint → loslassen
③ Dateien sind sofort geöffnet
```

### Erste eigene Datei erstellen

```
① Klick auf  ✦ Neu  in der Seitenleiste
② Neue Datei öffnet sich mit vorausgefülltem YAML-Frontmatter
③ Inhalte eingeben
④ Ctrl+S  zum Speichern
```

---

## 2. Benutzeroberfläche

### 2.1 Grundstruktur

Die Oberfläche besteht aus vier Zonen:

```
┌────────────────┬─────────────────────────────────────────────────────────────┐
│                │  WERKZEUGLEISTE (Toolbar)                                   │
│   SEITENLEISTE │  dateiname.md │ Speichern │ Version │ ... │ 🔍 │ MD Syntax │ PDF │
│   (Sidebar)    ├────────────────────────────────────────────────────────────  │
│                │                                                              │
│  📁 Ordner     │   ARBEITSBEREICH (Work Area)                                 │
│  + Laden       │                                                              │
│  ✦ Neu         │   [Editor]  │▐│  [Vorschau]       — Split-Modus             │
│  ─────────     │                                                              │
│  📄 datei1.md  │   oder: [Editor allein]  — Editor-Modus                     │
│  📄 datei2.md● │   oder: [Vorschau allein] — Vorschau-Modus                  │
│  📄 datei3.md  │   oder: [Formular]        — Formular-Modus                  │
│                │                                                              │
│                ├─────────────────────────────────────────────────────────────┤
│                │  STATUSLEISTE   ● Gespeichert · 342 Wörter · ⏱ 2:47        │
└────────────────┴─────────────────────────────────────────────────────────────┘
```

---

### 2.2 Seitenleiste (links)

```
┌─────────────────────┐
│  M↓  MD STUDIO      │  ← Logo & Programmname
├─────────────────────┤
│ 📁Ordner +Laden ✦Neu │  ← Drei Schaltflächen zum Laden/Erstellen
├─────────────────────┤
│ 📁 /mein/ordner     │  ← Aktuell geöffneter Ordner
├─────────────────────┤
│  📄 bericht.md      │  ← Dateiliste: Klick öffnet Datei
│  📄 notizen.md  ●   │  ← ● = ungespeicherte Änderungen
│  📄 vorlage.md      │
└─────────────────────┘
```

| Element | Bedeutung |
|---------|-----------|
| `📁 Ordner` | Öffnet einen lokalen Ordner — alle `.md`-Dateien darin werden geladen (Chrome/Edge) |
| `+ Laden` | Einzelne `.md`-Datei(en) per Dateidialog laden (alle Browser) |
| `✦ Neu` | Erstellt eine neue leere Datei mit vorausgefülltem YAML-Frontmatter |
| Dateiname in der Liste | Klick öffnet die Datei im Editor |
| Orangener Punkt `●` | Die Datei hat ungespeicherte Änderungen |

---

### 2.3 Werkzeugleiste (Toolbar)

```
 dateiname.md │ Speichern │ Version │ Umbenennen │ Datum/Version │ ⊞ │ ✎ │ 👁 │ ⊟ Formular │ 🔍 Suchen │ MD Syntax │               PDF
              │           │         │            │               │   │   │   │            │           │           │               ───
              │  Datei-   │         │            │   Datum &     │   Ansichtsmodi          │  Suche &  │  PDF-     
              │  aktionen │         │            │   Version     │                         │  Referenz │  Export   
```

Die Werkzeugleiste ist in funktionale Gruppen unterteilt:

| Gruppe | Schaltflächen | Funktion |
|--------|--------------|----------|
| **Dateiname** | `dateiname.md` | Zeigt den Namen der aktuell geöffneten Datei |
| **Dateiaktionen** | `Speichern` `Version` `Umbenennen` | Speichern, neue Version erstellen, Datei umbenennen |
| **Datum** | `Datum/Version` | Aktuelles Datum und/oder Versionsnummer ins Frontmatter eintragen |
| **Ansicht** | `⊞` `✎` `👁` `Formular` | Zwischen Split-Ansicht, reinem Editor, Vorschau und Formular-Modus wechseln |
| **Suche** | `Suchen` | Suchleiste ein-/ausblenden |
| **Referenz** | `MD Syntax` | Markdown-Schnellreferenz öffnen |
| **Export** | `PDF` (gold) | Dokument als PDF drucken/speichern |

---

### 2.4 Arbeitsbereich

Der Arbeitsbereich zeigt je nach aktivem Modus unterschiedliche Inhalte:

**Split-Modus (Standard):**
```
┌──────────────────────────┬─┬──────────────────────────────┐
│  # Mein Titel            │▐│  Mein Titel                  │
│                          │ │  ════════════════            │
│  Hier tippe ich meinen   │ │  Hier tippe ich meinen       │
│  Text in **Markdown**.   │ │  Text in Markdown.            │
│                          │ │                              │
│  - Punkt 1               │ │  • Punkt 1                   │
│  - [x] Erledigt          │ │  ☑ Erledigt                  │
│                          │▐│                              │
│    EDITOR                │ │    VORSCHAU                  │
└──────────────────────────┴─┴──────────────────────────────┘
                            ↑
               Trennlinie: Ziehen zum Verschieben
```

Die Trennlinie zwischen Editor und Vorschau lässt sich mit der Maus frei verschieben.  
**Standard:** Editor 38% — Vorschau 62% (optimiert für breite Tabellen).

**Beim Scrollen:** Editor und Vorschau scrollen proportional synchron — der angezeigte Inhalt bleibt immer auf der gleichen Dokumentposition.

---

### 2.5 Statusleiste (unten)

```
● Gespeichert  ·  342 Wörter  ·  1.847 Zeichen  ·  28 Zeilen  ·  Z 14, Sp 6   [Leerraum]   ⏱ 2:47  ·  UTF-8
      ↑                ↑               ↑               ↑             ↑                         ↑
  Speicherstatus    Wörter        Zeichenzahl      Zeilenzahl    Cursor-             Auto-Save-
  (orange=unges.)                                              position            Countdown
```

| Anzeige | Bedeutung |
|---------|-----------|
| `● Gespeichert` (grün) | Alle Änderungen gespeichert |
| `● Ungespeichert` (orange) | Es gibt nicht gespeicherte Änderungen |
| `● Formular geändert` (orange) | Im Formular-Modus wurden Werte geändert, aber noch nicht gespeichert |
| `⏱ 2:47` | Auto-Save zählt rückwärts (wird orange bei < 15 Sekunden) |
| `Z 14, Sp 6` | Aktuelle Cursor-Position (Zeile, Spalte) |

---

## 3. Grundlegende Workflows

### 3.1 Ordner öffnen und Dateien verwalten

```
  START
    │
    ▼
┌───────────────────┐      ┌────────────────────────────┐
│ Klick: 📁 Ordner  │─────►│ Dateidialog: Ordner wählen │
└───────────────────┘      └──────────────┬─────────────┘
                                          │ Zugriff erlauben
                                          ▼
                           ┌────────────────────────────┐
                           │ Seitenleiste füllt sich mit │
                           │ allen .md-Dateien im Ordner │
                           └──────────────┬─────────────┘
                                          │
                    ┌─────────────────────┼─────────────────────┐
                    ▼                     ▼                     ▼
             Datei anklicken       ✦ Neu klicken         + Laden klicken
             → öffnet im Editor    → neue Datei           → weitere Dateien
                                     erstellen              hinzuladen
```

> **Hinweis Chrome/Edge:** MD Studio kann direkt in die Dateien im Ordner schreiben (Ctrl+S speichert direkt). In Firefox/Safari wird beim Speichern ein Download ausgelöst.

---

### 3.2 Neue Datei erstellen

```
① Klick auf ✦ Neu
          │
          ▼
   Neue Datei wird erstellt mit:

   ---
   title: Neues Dokument          ← automatisch ausgefüllt
   date: 2026-04-14               ← heutiges Datum
   version: 1.0
   author:                        ← leer lassen oder eintragen
   ---

   # Titel

   Inhalt hier...
          │
          ▼
③ Datei bearbeiten → Ctrl+S speichern
          │
          ▼
④ Dialog: Dateiname vergeben (z.B. mein-bericht.md)
```

---

### 3.3 Speichern und Versionieren

```
SPEICHERN (bestehende Version überschreiben):
  Ctrl+S  oder  Klick auf "Speichern"
    │
    ├─► Chrome/Edge + Ordner geöffnet: speichert direkt in die Datei ✓
    └─► Firefox / kein Ordner:         Download der .md-Datei ↓

NEUE VERSION ERSTELLEN (Original bleibt erhalten):
  Klick auf "Version"
    │
    ▼
  Dialog erscheint:
  ┌─────────────────────────────────────────┐
  │  Als neue Version exportieren           │
  │                                         │
  │  Dateiname: bericht_v2.md    ← auto     │
  │             [______________]            │
  │                                         │
  │  [Abbrechen]        [Exportieren]       │
  └─────────────────────────────────────────┘
    │
    ▼
  Neue Datei erscheint in der Seitenleiste
  (Original bleibt unverändert)
```

**Automatische Versionsnummerierung:**  
`bericht.md` → `bericht_v2.md` → `bericht_v3.md`  
`bericht_v1.0.md` → `bericht_v1.1.md` → `bericht_v1.2.md`

---

### 3.4 Datei umbenennen

```
Klick auf "Umbenennen"  oder  Doppelklick auf Dateinamen in Seitenleiste
    │
    ▼
  ┌─────────────────────────────────────────┐
  │  Datei umbenennen                       │
  │                                         │
  │  Neuer Dateiname:                       │
  │  [bericht-final.md____________]         │
  │                                         │
  │  [Abbrechen]        [Umbenennen]        │
  └─────────────────────────────────────────┘
    │
    ▼
  In Chrome/Edge mit Ordner:  alte Datei wird gelöscht, neue angelegt
  Sonst:                      nur in der aktuellen Sitzung umbenannt
```

---

### 3.5 Drag & Drop

```
  Dateimanager             Browser-Fenster
  ┌──────────┐             ┌─────────────────────────────┐
  │          │             │                             │
  │ notiz.md ├─────────────►  .md Dateien hier ablegen   │
  │          │   ziehen    │  (goldener Rahmen erscheint) │
  └──────────┘             └─────────────────────────────┘
                                        │
                                        ▼
                           Datei(en) werden sofort geladen
                           und in der Seitenleiste angezeigt
```

Mehrere Dateien gleichzeitig ziehen ist möglich.

---

## 4. Ansichtsmodi

MD Studio bietet vier Ansichtsmodi, umschaltbar über die Toolbar:

```
TOOLBAR-BUTTONS:
  ┌──┐ ┌─┐ ┌─┐ ┌──────────┐
  │⊞ │ │✎│ │👁│ │⊟ Formular│
  └──┘ └─┘ └─┘ └──────────┘
   ↑    ↑   ↑       ↑
 Split  Ed. Vor.  Formular
```

### Modus 1: Split-Ansicht `⊞` *(Standard)*

```
┌─────────────────┬─┬──────────────────┐
│   EDITOR        │▐│   VORSCHAU       │
│   (38%)         │ │   (62%)          │
│                 │ │                  │
│ # Titel         │ │ Titel            │
│                 │ │ ═════            │
│ **Fett**        │ │ Fett             │
└─────────────────┴─┴──────────────────┘
        ↕ Synchrones Scrollen ↕
```

- Trennlinie ist per Maus verschiebbar (min. 18%, max. 82%)
- Editor und Vorschau scrollen automatisch synchron

### Modus 2: Nur Editor `✎`

```
┌──────────────────────────────────────┐
│                                      │
│   EDITOR  (volle Breite)             │
│                                      │
│ # Mein Dokument                      │
│                                      │
│ Text hier...                         │
└──────────────────────────────────────┘
```

Ideal für: konzentriertes Schreiben, Bearbeitung langer Dokumente.

### Modus 3: Nur Vorschau `👁`

```
┌──────────────────────────────────────┐
│                                      │
│   VORSCHAU  (volle Breite)           │
│                                      │
│   Mein Dokument                      │
│   ════════════                       │
│                                      │
│   Text hier...                       │
└──────────────────────────────────────┘
```

Ideal für: Lesemodus, Präsentation, Qualitätskontrolle vor dem Druck.

### Modus 4: Formular-Modus `⊟ Formular`

```
┌──────────────────────────────────────────────────┐
│ ⊟ Formular-Modus — Felder ausfüllen und Speichern│
├──────────────────────────────────────────────────┤
│ Frontmatter: title: Bericht · date: 2026-04-14   │
├──────────────────────────────────────────────────┤
│                                                  │
│  Sammlungsname: [________________________]       │
│                                                  │
│  Status: ○ Entwurf  ● Review  ○ Freigegeben      │
│                                                  │
│  Datum: [2026-04-14 ▼]                           │
│                                                  │
│  Beschreibung:                                   │
│  ┌──────────────────────────────────────┐        │
│  │                                      │        │
│  └──────────────────────────────────────┘        │
│                                                  │
│  [ ↓ Speichern ]  [ ↺ Reset ]                    │
└──────────────────────────────────────────────────┘
```

→ Ausführliche Beschreibung in Abschnitt 5.

---

## 5. Formular-Modus

### 5.1 Konzept

Der Formular-Modus verwandelt jede Markdown-Datei in ein interaktives Formular. Die Idee:

```
  Markdown-Datei (Quelltext)         Formular-Modus (Ansicht)
  ─────────────────────────          ────────────────────────
  **Name:** {{text:name}}        →   Name: [______________]
  **Status:** {{select:s:a,b,c}} →   Status: [ a ▼ ]
  **Datum:** {{date:datum}}      →   Datum: [2026-04-14 ▼]
                                 
  {{button:Speichern}}           →   [ Speichern ]
```

**Wie Werte gespeichert werden:**

```
  ① Formular ausfüllen
  ② "Speichern" klicken (oder Ctrl+S)
  ③ Alle Werte werden ins YAML-Frontmatter geschrieben:
  
     ---
     name: Max Mustermann
     s: a
     datum: 2026-04-14
     ---
```

Das Dokument selbst bleibt unverändert — nur der Frontmatter wird aktualisiert.  
Beim nächsten Öffnen des Formular-Modus sind die Werte vorausgefüllt.

---

### 5.2 Formularfeld-Syntax

Alle Felder werden mit der `{{typ:name:optionen}}` Notation direkt in den Markdown-Text eingebettet:

```
{{typ:feldname:option1:option2:...}}
  ↑       ↑         ↑
 Typ    Name des  Typ-spezifische
       Feldes     Optionen
```

#### Übersicht aller Feldtypen

| Typ | Syntax | Ergebnis |
|-----|--------|---------|
| `text` | `{{text:name}}` | Einzeiliges Textfeld |
| `text` | `{{text:name:Platzhalter:280}}` | Mit Platzhaltertext und Breite in px |
| `textarea` | `{{textarea:name:5}}` | Mehrzeiliges Textfeld, 5 Zeilen |
| `date` | `{{date:datum}}` | Datumsauswahl (Browser-eigener Datepicker) |
| `number` | `{{number:menge:0:100:1}}` | Zahlfeld mit Min:Max:Schritt |
| `select` | `{{select:status:offen,aktiv,fertig}}` | Dropdown-Menü |
| `multiselect` | `{{multiselect:tags:A,B,C,D}}` | Mehrfachauswahl-Liste |
| `radio` | `{{radio:typ:A\|B\|C}}` | Radio-Schaltflächen (Optionen mit `\|` getrennt) |
| `checkbox` | `{{checkbox:ok:Bestätigt}}` | Checkbox mit Label |
| `range` | `{{range:prio:1:5:1}}` | Schieberegler Min:Max:Schritt |
| `button` | `{{button:Speichern}}` | Speichert alle Felder ins Frontmatter |
| `reset` | `{{reset:Zurücksetzen}}` | Setzt alle Felder auf gespeicherte Werte zurück |
| `divider` | `{{divider}}` | Gestrichelte Trennlinie |
| `note` | `{{note:Pflichtfelder mit * markiert}}` | Kursiver Hinweistext |

#### Vollständiges Beispiel

Das folgende Markdown erzeugt im Formular-Modus ein vollständiges Formular:

```markdown
---
title: Projekterfassung
---

# Neues Projekt erfassen

{{note:Alle Felder mit * sind Pflicht}}

**Projektname *:** {{text:projektname:Name des Projekts:300}}

**Status:** {{select:status:offen,in Bearbeitung,abgeschlossen,abgebrochen}}

**Priorität:** {{radio:prioritaet:niedrig|mittel|hoch|kritisch}}

**Startdatum:** {{date:startdatum}} · **Enddatum:** {{date:enddatum}}

**Budget (CHF):** {{number:budget:0:1000000:1000}}

**Beschreibung:**

{{textarea:beschreibung:4}}

{{divider}}

**Internes Projekt?** {{checkbox:intern:Nur intern sichtbar}}

{{button:Speichern}} {{reset:Zurücksetzen}}
```

**Ergebnis im Formular-Modus:**

```
┌─────────────────────────────────────────────────────┐
│ Alle Felder mit * sind Pflicht                      │
├─────────────────────────────────────────────────────┤
│                                                     │
│ Projektname *: [Name des Projekts_____________]     │
│                                                     │
│ Status: [ offen ▼ ]                                 │
│                                                     │
│ Priorität: ○ niedrig  ○ mittel  ● hoch  ○ kritisch │
│                                                     │
│ Startdatum: [2026-04-14 ▼] · Enddatum: [────── ▼]  │
│                                                     │
│ Budget (CHF): [______0_______]                      │
│ (0 ──────────────────── 1'000'000)                  │
│                                                     │
│ Beschreibung:                                       │
│ ┌─────────────────────────────────────────────┐    │
│ │                                             │    │
│ │                                             │    │
│ └─────────────────────────────────────────────┘    │
│                                                     │
│ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─      │
│                                                     │
│ ☐ Nur intern sichtbar                               │
│                                                     │
│ [ ↓ Speichern ]  [ ↺ Zurücksetzen ]                 │
└─────────────────────────────────────────────────────┘
```

---

### 5.3 Felder inline im Fliesstext

Felder können direkt im normalen Text stehen:

```markdown
Der Antrag wurde am {{date:antrag_datum}} von {{text:antragsteller}} eingereicht.
Die Bewilligung erfolgte durch {{select:behoerde:BAFU,ASTRA,SECO}} am {{date:bewilligung_datum}}.
```

Ergebnis im Formular-Modus:
```
Der Antrag wurde am [2026-04-14 ▼] von [______________] eingereicht.
Die Bewilligung erfolgte durch [ BAFU ▼ ] am [────── ▼].
```

---

### 5.4 Werte und Frontmatter

Nach dem Klick auf `{{ button:Speichern }}` werden alle ausgefüllten Felder automatisch ins YAML-Frontmatter der Datei geschrieben:

```yaml
---
title: Projekterfassung
projektname: Digitalisierungsprojekt 2026
status: in Bearbeitung
prioritaet: hoch
startdatum: 2026-04-14
enddatum: 2026-12-31
budget: 45000
beschreibung: Digitalisierung von ca. 8300 Glasdias aus dem Bestand 1890-1950.
intern: false
---
```

Beim nächsten Öffnen der Datei im Formular-Modus sind alle Felder mit diesen Werten vorausgefüllt.

---

## 6. Datum & Versionierung

### 6.1 Datum / Version-Dialog

Der Dialog erlaubt das automatische Eintragen von Datum und Versionsnummer ins YAML-Frontmatter.

```
Klick auf "Datum/Version" in der Toolbar
    │
    ▼
┌─────────────────────────────────────────┐
│  Datum & Version                        │
│                                         │
│  Datumsfeld:     [date_____________]    │  ← YAML-Schlüssel, z.B. "date"
│  Format:         [YYYY-MM-DD_______]    │  ← Datumsformat
│                                         │
│  Versionsfeld:   [version__________]    │  ← YAML-Schlüssel, z.B. "version"
│  Versionswert:   [__________________]   │  ← leer = auto-increment
│                                         │
│  Aktuell: 2026-04-14                    │  ← Vorschau
│                                         │
│  [Abbrechen]         [Aktualisieren]    │
└─────────────────────────────────────────┘
```

### 6.2 Datumsformate

| Format | Ausgabe | Verwendung |
|--------|---------|------------|
| `YYYY-MM-DD` | `2026-04-14` | ISO 8601, Standard |
| `DD.MM.YYYY` | `14.04.2026` | Schweizer/Deutsches Format |
| `YYYY.MM.DD` | `2026.04.14` | Alternativer Punkt-Stil |
| `YYYY-MM-DD HH:mm` | `2026-04-14 14:30` | Mit Uhrzeit |
| `DD. MM. YYYY` | `14. 04. 2026` | Deutsch mit Leerzeichen |

### 6.3 Auto-Increment der Versionsnummer

Wenn das Versionsfeld **leer** gelassen wird, erhöht MD Studio die Versionsnummer automatisch:

```
  Vorher:   version: 1.3    →   Nachher:  version: 1.4
  Vorher:   version: 2.0    →   Nachher:  version: 2.1
  Vorher:   version: 1.9    →   Nachher:  version: 1.10
```

### 6.4 Verhalten bei vorhandenem vs. fehlendem Frontmatter

```
  Frontmatter vorhanden?
        │
   ┌────┴────┐
  JA         NEIN
   │           │
   ▼           ▼
  Vorhandene  Neuer Frontmatter-
  Felder      Block wird am
  werden      Anfang der Datei
  aktualisiert eingefügt
```

---

## 7. Suche

### 7.1 Suche öffnen und schliessen

```
Öffnen:   Ctrl+F  oder  Klick auf "🔍 Suchen"
Schliessen: Esc  oder  Klick auf ✕

┌─────────────────────────────────────────────────────────────┐
│  🔍  [Suchbegriff_______________________]  3 / 7  ▲ ▼  ✕   │
└─────────────────────────────────────────────────────────────┘
```

### 7.2 Navigation in den Treffern

| Aktion | Tastatur | Schaltfläche |
|--------|----------|-------------|
| Nächster Treffer | `Enter` | `▼` |
| Vorheriger Treffer | `Shift+Enter` | `▲` |
| Suche schliessen | `Esc` | `✕` |

### 7.3 Was wird durchsucht?

- Der **komplette Quelltext** der aktuell geöffneten Datei (Editor)
- Treffer werden im Editor **markiert und angesprungen**
- In der Vorschau werden Treffer **gelb hinterlegt**
- Die Suche ist **nicht case-sensitive** (Gross-/Kleinschreibung wird ignoriert)
- **Reguläre Ausdrücke** werden nicht unterstützt — es wird nach Klartext gesucht

---

## 8. PDF-Export

### 8.1 PDF erstellen

```
Klick auf "PDF" (goldene Schaltfläche) oder  Ctrl+Shift+P
    │
    ▼
Browser-Druckdialog öffnet sich:

┌─────────────────────────────────────────────────────┐
│  Drucken                                            │
│                                                     │
│  Drucker:  [ Als PDF speichern ▼ ]  ←── wichtig!   │
│                                                     │
│  Layout:   ○ Hochformat  ● Querformat               │
│  Seiten:   Alle                                     │
│                                                     │
│  [  Abbrechen  ]       [  Speichern  ]              │
└─────────────────────────────────────────────────────┘
    │
    ▼
Dateiname und Speicherort wählen → PDF wird erstellt
```

### 8.2 Was erscheint im PDF?

```
  WIRD ANGEZEIGT:              WIRD AUSGEBLENDET:
  ─────────────────            ──────────────────────
  ✓ Frontmatter-Box            ✗ Seitenleiste
  ✓ Alle Überschriften         ✗ Werkzeugleiste
  ✓ Tabellen                   ✗ Editor-Bereich
  ✓ Listen & Checkboxen        ✗ Statusleiste
  ✓ Code-Blöcke                ✗ Suchleiste
  ✓ Bilder                     ✗ Modale Dialoge
  ✓ Links (als Text + URL)
  ✓ Alle Markdown-Formatierungen
```

### 8.3 Hinweise zum PDF-Druck

- Der Druck erfolgt immer aus der **Vorschau** (nicht dem Editor)
- Das PDF enthält **alle Seiten** des Dokuments
- Für saubere Seitenumbrüche: Überschriften und Tabellen werden nicht geteilt
- Code-Blöcke erhalten im PDF einen grauen Hintergrund
- Empfohlen: **Chrome oder Edge** für besten PDF-Output

---

## 9. Markdown Syntax

### 9.1 Schnellreferenz öffnen

```
Klick auf "MD Syntax" in der Toolbar
    │
    ▼
┌──────────────────────────────────────────────────────────────┐
│  Markdown Syntax · Schnellreferenz                      [✕] │
├──────────────────────────────────────────────────────────────┤
│  [Filtern... z.B. Tabelle, fett, Link, Formular____________] │
├────────────────────────────┬─────────────────────────────────┤
│  ① Textformatierung        │  ⑦ Blockzitate                  │
│  ② Überschriften           │  ⑧ Trennlinien & Umbrüche       │
│  ③ Listen                  │  ⑨ Frontmatter (YAML)           │
│  ④ Links & Bilder          │  ⑩ Sonstiges                    │
│  ⑤ Code                    │  ⑪ Formular-Felder ← NEU        │
│  ⑥ Tabellen                │                                  │
└────────────────────────────┴─────────────────────────────────┘
```

### 9.2 Filter verwenden

Durch Eingabe im Filterfeld wird die Referenz sofort gefiltert:

```
Eingabe:  "tabelle"   → zeigt nur Tabellen-Syntax
Eingabe:  "fett"      → zeigt nur Fettdruck-Syntax
Eingabe:  "formular"  → zeigt alle Formular-Feldtypen
Eingabe:  "link"      → zeigt Link- und Bild-Syntax
Eingabe:  "date"      → zeigt Datumsfeld-Syntax
```

### 9.3 Wichtigste Markdown-Elemente

```markdown
# Überschrift 1      ## Überschrift 2      ### Überschrift 3

**fett**   *kursiv*   ~~durchgestrichen~~   `code`   ==markiert==

- Aufzählung          1. Nummeriert         - [ ] Aufgabe offen
- Punkt               2. Zweiter            - [x] Aufgabe erledigt

[Linktext](https://url.de)     ![Bildtext](bild.png)

| Spalte A | Spalte B |     > Blockzitat
|----------|----------|
| Wert 1   | Wert 2   |     ---  (Trennlinie)

```python
code-block mit Syntax-Highlighting
```
```

### 9.4 YAML-Frontmatter

Jede Markdown-Datei kann am Anfang einen YAML-Block haben:

```yaml
---
title: Mein Dokument
date: 2026-04-14
version: 1.3
author: Max Mustermann
tags:
  - forschung
  - bericht
status: Entwurf
---

# Hier beginnt der Inhalt
```

MD Studio zeigt den Frontmatter-Block als **informativen Badge** über dem Dokumentinhalt an — er wird nie im PDF gedruckt (der Badge schon, aber das ist gewollt als Metadaten-Referenz).

---

## 10. Auto-Save

### 10.1 Funktionsprinzip

MD Studio speichert automatisch alle **180 Sekunden**, wenn:
- Eine Datei geöffnet ist **UND**
- Ungespeicherte Änderungen vorhanden sind

```
Countdown in der Statusleiste:
  ⏱ 3:00  → Countdown startet bei 3 Minuten
  ⏱ 2:47  → läuft normal rückwärts
  ⏱ 0:14  → wird orange (< 15 Sekunden)
  ⏱ 0:00  → Auto-Save wird ausgelöst
  ⏱ 3:00  → Countdown startet neu
```

### 10.2 Verhalten nach Auto-Save

```
Auto-Save ausgelöst:
    │
    ├─► Chrome/Edge + Ordner geöffnet:
    │   Direkt in Datei gespeichert → Toast: "⏱ Auto-gespeichert"
    │
    └─► Firefox / kein Ordner:
        Download der Datei wird ausgelöst
        (kann lästig werden — Ordner-Modus empfohlen)
```

### 10.3 Auto-Save und manuelle Speicherung

- **Ctrl+S** setzt den Auto-Save-Countdown zurück auf 3 Minuten
- Auto-Save und manuelles Speichern überschreiben sich nicht gegenseitig
- Beim Auto-Save wird kein neuer Versionseintrag erzeugt

---

## 11. Tastaturkürzel

| Kürzel | Funktion |
|--------|----------|
| `Ctrl+S` / `Cmd+S` | Speichern |
| `Ctrl+F` / `Cmd+F` | Suchen öffnen/schliessen |
| `Ctrl+Shift+P` | PDF-Druckdialog öffnen |
| `Enter` (in Suche) | Nächster Treffer |
| `Shift+Enter` (in Suche) | Vorheriger Treffer |
| `Esc` | Suche / Dialoge schliessen |
| `Tab` (im Editor) | 2 Leerzeichen einrücken |
| `Tab` (mit Selektion) | Alle ausgewählten Zeilen einrücken |

---

## 12. Browser-Kompatibilität

MD Studio funktioniert in allen modernen Browsern, aber mit unterschiedlichem Funktionsumfang:

```
┌───────────────┬──────────────┬──────────────┬──────────────┬──────────────┐
│ Funktion      │ Chrome/Edge  │   Firefox    │    Safari    │   Mobile     │
├───────────────┼──────────────┼──────────────┼──────────────┼──────────────┤
│ Editor & Vor- │      ✓       │      ✓       │      ✓       │      ✓       │
│ schau         │              │              │              │              │
│ Formular-Modus│      ✓       │      ✓       │      ✓       │      ✓       │
│ Drag & Drop   │      ✓       │      ✓       │      ✓       │      ✗       │
│ + Laden       │      ✓       │      ✓       │      ✓       │      ✓       │
│ 📁 Ordner     │      ✓       │      ✗       │      ✗       │      ✗       │
│ öffnen        │ (empfohlen)  │  Warnung     │  Warnung     │              │
│ Direkt-Speich.│      ✓       │      ✗       │      ✗       │      ✗       │
│ in Datei      │              │  Download    │  Download    │  Download    │
│ Auto-Save     │      ✓       │   Download   │   Download   │              │
│ PDF-Export    │      ✓       │      ✓       │      ✓       │  eingeschr.  │
└───────────────┴──────────────┴──────────────┴──────────────┴──────────────┘
```

> **Empfehlung:** Für den vollen Funktionsumfang (Ordner öffnen, direkt speichern) Chrome oder Edge verwenden.

### Was passiert in Firefox/Safari?

- Der `📁 Ordner`-Button zeigt einen Hinweis, dass Ordner-Zugriff nicht verfügbar ist
- `+ Laden` funktioniert normal für einzelne Dateien
- Beim Speichern (Ctrl+S) wird ein **Download** ausgelöst statt direkt in die Datei zu schreiben
- Die heruntergeladene Datei hat denselben Namen und kann die Originaldatei ersetzen

---

## 13. FAQ — Häufige Fragen

**F: Werden meine Dateien irgendwo hochgeladen?**  
A: Nein. MD Studio läuft vollständig lokal im Browser. Es gibt keinen Server, keine Cloud, keine Datenübertragung.

**F: Ich habe Änderungen gemacht — wo sind sie gespeichert?**  
A: Solange du nicht gespeichert hast, befinden sich Änderungen nur im Browser-Speicher. Beim Schliessen des Tabs gehen sie verloren. Immer mit **Ctrl+S** speichern oder auf Auto-Save vertrauen.

**F: Kann ich Bilder in meine Markdown-Dateien einbinden?**  
A: Ja, mit der normalen Markdown-Syntax `![Alt-Text](pfad/zum/bild.png)`. Das Bild muss lokal erreichbar sein — relative Pfade funktionieren wenn MD Studio aus demselben Verzeichnis geöffnet wird.

**F: Warum sehe ich den Ordner-Button ausgegraut (Firefox/Safari)?**  
A: Die File System Access API ist nur in Chrome/Edge verfügbar. Mit Firefox oder Safari kann man Dateien per `+ Laden` oder Drag & Drop öffnen und beim Speichern als Download erhalten.

**F: Wie kann ich mehrere Dokumente gleichzeitig bearbeiten?**  
A: Lade alle Dateien über `📁 Ordner` oder mehrfachen `+ Laden`. Sie erscheinen alle in der Seitenleiste. Per Klick zwischen ihnen wechseln. Beim Wechsel wird der aktuelle Stand automatisch gesichert.

**F: Der Formular-Modus zeigt "Keine Formularfelder gefunden".**  
A: Die Datei enthält noch keine `{{...}}`-Feldmarkierungen. Wechsle in den Editor-Modus (✎), füge z.B. `{{text:name}}` ein und wechsle zurück in den Formular-Modus.

**F: Das PDF hat nur eine Seite — wie bekomme ich alle Seiten?**  
A: Im Druckdialog des Browsers darauf achten, dass "Alle Seiten" und nicht nur "Aktuelle Seite" ausgewählt ist. MD Studio ist für mehrseitigen Druck optimiert.

**F: Kann ich eigene Dropdown-Optionen für `{{select:...}}`-Felder definieren?**  
A: Ja — die Optionen stehen direkt in der Syntax: `{{select:status:offen,aktiv,abgeschlossen}}`. Im Editor einfach die Optionsliste anpassen.

**F: Werden meine Formulardaten beim Schliessen des Browsers gelöscht?**  
A: Nein — wenn du auf "Speichern" geklickt hast, werden die Werte ins YAML-Frontmatter der Datei geschrieben. Beim nächsten Öffnen sind sie wieder vorhanden, solange die Datei gespeichert wurde.

**F: Wie funktioniert die Synchronisierung des Scrollens im Split-Modus?**  
A: Das Verhältnis der Scrollposition (von oben nach unten) wird übertragen. Bei sehr unterschiedlich langen Dokumenten in Editor und Vorschau (z.B. durch Tabellenrendering) kann die Synchronisation leicht abweichen.

---

## Anhang: Vollständige Funktionsliste

### Dateimanagement
- Lokalen Ordner öffnen und alle `.md`-Dateien laden (Chrome/Edge)
- Einzelne Dateien laden (alle Browser)
- Mehrere Dateien gleichzeitig laden
- Dateien per Drag & Drop öffnen
- Neue Datei erstellen (mit vorbefülltem Frontmatter)
- Datei direkt speichern (Chrome/Edge) oder als Download speichern
- Als neue Version exportieren (automatische Versionsnummerierung)
- Datei umbenennen
- Mehrere Dateien gleichzeitig in der Seitenleiste verwalten
- Ungespeicherte-Änderungen-Indikator (orangener Punkt)

### Editor
- Vollständiger Markdown-Editor mit Monospace-Schrift
- Tab-Taste: 2 Leerzeichen einrücken (auch für Selektion)
- Cursor-Position in Statusleiste (Zeile, Spalte)
- Wort-, Zeichen-, Zeilenzählung in Echtzeit

### Vorschau
- Vollständiges GitHub Flavored Markdown (GFM) Rendering
- Syntax-Highlighting für Codeblöcke (50+ Sprachen via highlight.js)
- Interaktive Checkboxen (☐/☑ klickbar, sync mit Editor)
- YAML-Frontmatter als Badge angezeigt
- Tabellen mit alternierendem Zeilenhintergrund
- Blockquotes, Bilder, Links

### Ansichten & Layout
- Split-Ansicht (Standard, 38/62)
- Reiner Editor-Modus
- Reine Vorschau
- Formular-Modus
- Trennlinie im Split-Modus frei verschiebbar (18–82%)
- Synchrones Scrollen in der Split-Ansicht

### Formular-Modus
- 12 Feldtypen: text, textarea, date, number, select, multiselect, radio, checkbox, range, button, reset, divider, note
- Felder inline im Fliesstext einbettbar
- Werte werden ins YAML-Frontmatter gespeichert
- Vorausfüllen aus bestehendem Frontmatter
- Syntax-Dokumentation integriert (Anhang E / MD Syntax)

### Datum & Versionierung
- Datum in konfiguriertem Format ins Frontmatter eintragen
- Versionsnummer eintragen oder auto-incrementieren
- Frontmatter anlegen falls nicht vorhanden
- Vorschau des formatierten Datums im Dialog

### Suche
- Volltextsuche im Editor-Quelltext
- Navigation mit Enter/Shift+Enter
- Treffer-Highlighting in Vorschau
- Trefferzähler (n / Gesamt)

### Auto-Save
- Automatisches Speichern alle 180 Sekunden
- Countdown-Anzeige in der Statusleiste
- Orangefarbene Warnung bei < 15 Sekunden

### PDF-Export
- Druckt vollständige Dokumentvorschau (alle Seiten)
- Keine Seitengrössenbegrenzung
- Seitenumbruch-Optimierung für Überschriften und Tabellen

### Referenz
- Eingebaute Markdown-Schnellreferenz (11 Kategorien, ~80 Einträge)
- Live-Filterung der Referenz
- Formular-Syntax vollständig dokumentiert

---

*MD Studio — Standalone HTML Markdown Editor · Vollständig lokal · Keine Installation erforderlich*
