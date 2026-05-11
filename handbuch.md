---
title: MD Studio — Handbuch
version: 1.1
date: 2026-05-11
author: MD Studio
---

# MD Studio — Handbuch

Dieses Handbuch beschreibt die aktuelle Funktionsweise von `md-studio.html`.

---

## Inhaltsverzeichnis

1. [Ziel & Konzept](#1-ziel--konzept)
2. [Oberfläche](#2-oberfläche)
3. [Datei-Workflows](#3-datei-workflows)
4. [Ansichten & Editor](#4-ansichten--editor)
5. [Formular-Modus](#5-formular-modus)
6. [Tabellen-Editor](#6-tabellen-editor)
7. [Suche, Syntaxhilfe, PDF](#7-suche-syntaxhilfe-pdf)
8. [Auto-Save & Statusleiste](#8-auto-save--statusleiste)
9. [Tastaturkürzel](#9-tastaturkürzel)
10. [Browser-Kompatibilität](#10-browser-kompatibilität)
11. [Tipps & Grenzen](#11-tipps--grenzen)

---

## 1. Ziel & Konzept

MD Studio ist ein **lokaler Markdown-Editor** als Single-File-Web-App.

- Eine Datei: `md-studio.html`
- Keine Installation
- Keine Server-Abhängigkeit
- Dokumente bleiben lokal

---

## 2. Oberfläche

Die App besteht aus vier Hauptbereichen:

1. **Seitenleiste** (Dateien/Ordner laden, neue Datei, Dateiliste)
2. **Toolbar** (Speichern, Version, Umbenennen, Ansichtsmodi, Suche, PDF, Syntax)
3. **Arbeitsbereich** (Editor, Preview, Formularansicht je nach Modus)
4. **Statusleiste** (Speicherstatus, Wort-/Zeichenanzahl, Cursor, Auto-Save)

### Seitenleiste
- **📁 Ordner**: lädt alle Markdown-Dateien aus einem Verzeichnis (FSA-unterstützte Browser)
- **+ Laden**: Datei(en) laden
- **✦ Neu**: neue Datei mit Frontmatter-Grundgerüst
- **● Punkt an Datei**: ungespeicherte Änderungen

### Toolbar
- **Speichern**
- **Version** (Export als neue Datei)
- **Umbenennen**
- **Datum/Version** (ins Frontmatter einfügen)
- **Ansichten**: Split, Editor, Preview, Formular
- **Suchen**
- **MD Syntax**
- **PDF**

---

## 3. Datei-Workflows

### 3.1 Ordner öffnen
1. `📁 Ordner` klicken
2. Ordner wählen
3. Zugriff bestätigen
4. Dateien links auswählen

### 3.2 Dateien laden
1. `+ Laden`
2. Eine oder mehrere `.md`-Dateien wählen
3. Dateien erscheinen in der Liste

### 3.3 Neue Datei
- `✦ Neu` erstellt eine neue Markdown-Datei mit YAML-Frontmatter

### 3.4 Speichern
- `Ctrl+S` oder Toolbar-Button
- Mit File-System-Zugriff: direkt in die Ursprungsdatei
- Ohne File-System-Zugriff: Download-Fallback

### 3.5 Version exportieren
- `Version` öffnet Exportdialog
- Ziel-Dateiname wird vorgeschlagen (z. B. `_v2`)

### 3.6 Umbenennen
- Über `Umbenennen` in der Toolbar
- Je nach Browser/Dateizugriff wird real umbenannt oder sitzungsbasiert geführt

---

## 4. Ansichten & Editor

### 4.1 Ansichtsmodi
- **Split**: Editor + Vorschau
- **Editor**: nur Textbearbeitung
- **Preview**: nur gerendertes Dokument
- **Formular**: Formularvorschau aus Makros

### 4.2 Editor-Verhalten
- Monospace-Editor mit Markdown-freundlicher Eingabe
- **Smart Enter** in Listen
- **Auto-Pairing** (Klammern/Backticks)
- **Formatierungsleiste** mit Schnellaktionen

### 4.3 Vorschau
- Rendering via `marked`
- Syntax-Highlighting via `highlight.js`
- Interaktive Checklisten
- Anker-Navigation für Überschriften

---

## 5. Formular-Modus

Im Markdown können Formulare per Makros eingebettet werden:

```md
{{text:name:Max Mustermann}}
{{select:status:offen,in Bearbeitung,erledigt}}
{{radio:prio:niedrig|mittel|hoch}}
{{textarea:notiz:4}}
```

### Unterstützte Typen
- `text`
- `textarea`
- `date`
- `number`
- `select`
- `multiselect`
- `radio`
- `checkbox`
- `range`
- `button`
- `reset`
- `note`

### Datenpersistenz
Formularwerte werden ins YAML-Frontmatter geschrieben und beim erneuten Öffnen wieder geladen.

---

## 6. Tabellen-Editor

Der Tabellen-Editor unterstützt:

- Zeilen/Spalten hinzufügen und entfernen
- Ausrichtung pro Spalte (links/zentriert/rechts)
- Bearbeiten vorhandener Tabellen
- Einfügen von TSV/CSV aus der Zwischenablage

---

## 7. Suche, Syntaxhilfe, PDF

### Suche
- `Ctrl+F` oder Toolbar
- Trefferzählung + Navigation
- Hervorhebung im Dokument

### MD Syntax
- Integriertes Cheatsheet
- Kategorien + Filter

### PDF
- Toolbar-Button `PDF`
- Ausgabe über Browser-Druckdialog

---

## 8. Auto-Save & Statusleiste

### Auto-Save
- Periodisches Speichern mit Countdown
- Anzeige in der Statusleiste

### Statusleiste zeigt
- Speicherstatus
- Wort-/Zeichen-/Zeilenanzahl
- Cursorposition
- Auto-Save-Timer

---

## 9. Tastaturkürzel

| Kürzel | Funktion |
|---|---|
| `Ctrl+S` | Speichern |
| `Ctrl+F` | Suche |
| `Ctrl+Shift+P` | Drucken / PDF |
| `Ctrl+B` | Fett |
| `Ctrl+I` | Kursiv |
| `Ctrl+K` | Link |
| `Tab` | Einrücken / Tabellen-Navigation |
| `Shift+Tab` | Tabellen-Navigation rückwärts |
| `Esc` | Dialoge/Suche schließen |

---

## 10. Browser-Kompatibilität

| Funktion | Chrome/Edge | Firefox | Safari |
|---|:---:|:---:|:---:|
| Editor & Preview | ✅ | ✅ | ✅ |
| Formular-Modus | ✅ | ✅ | ✅ |
| Drag & Drop | ✅ | ✅ | ✅ |
| Ordner öffnen | ✅ | ❌ | ❌ |
| Direktes Speichern | ✅ | Download-Fallback | Download-Fallback |

---

## 11. Tipps & Grenzen

- Für maximale Dateifunktionen Chrome/Edge verwenden.
- Bei Firefox/Safari Speichern über Download einplanen.
- `md-studio.html` kann lokal genutzt werden; externe Bibliotheken (`marked`, `highlight.js`) werden per CDN eingebunden.

