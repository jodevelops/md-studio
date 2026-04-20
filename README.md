# MD Studio

> **Ein schlanker, vollständig lokaler Markdown-Editor — eine einzige HTML-Datei, kein Server, keine Installation.**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Single File](https://img.shields.io/badge/size-single%20HTML-blue.svg)]()
[![Works Offline](https://img.shields.io/badge/works-100%25%20offline-green.svg)]()

**[▶ Live Demo öffnen](https://jodevelops.github.io/md-studio/md-studio.html)** &nbsp;·&nbsp; **[Dokumentation](handbuch.md)** &nbsp;·&nbsp; **[Download](https://raw.githubusercontent.com/jodevelops/md-studio/main/md-studio.html)**

---

## Was ist MD Studio?

MD Studio ist ein vollständiger Markdown-Editor, der als **eine einzige `.html`-Datei** funktioniert. Einfach herunterladen, im Browser öffnen — fertig. Keine Installation, kein Server, keine Cloud. Alle Dateien bleiben lokal auf deinem Rechner.

Entwickelt für die tägliche Arbeit mit Markdown-Dokumenten, strukturierten Formularen.

---

## Features

### Dateimanagement
- 📁 **Ordner öffnen** — lädt alle `.md`-Dateien eines Verzeichnisses auf einmal *(Chrome/Edge)*
- 📄 **Dateien laden** — einzelne oder mehrere `.md`-Dateien per Dialog *(alle Browser)*
- 🖱 **Drag & Drop** — Dateien direkt ins Browserfenster ziehen
- ✦ **Neue Datei** — mit vorausgefülltem YAML-Frontmatter
- 💾 **Direkt speichern** — schreibt in die Originaldatei zurück *(Chrome/Edge)* oder Download-Fallback
- 📋 **Versionierung** — exportiert als neue Datei (`bericht_v2.md`) mit auto-inkrementierter Versionsnummer
- ✏️ **Umbenennen** — umbenennen mit optionalem Löschen der alten Datei

### Editor & Vorschau
- ⊞ **Split-Ansicht** — Editor und Vorschau nebeneinander, Trennlinie frei verschiebbar
- ↕ **Scroll-Synchronisation** — Editor und Vorschau scrollen proportional mit
- 👁 **GFM-Rendering** — vollständiges GitHub Flavored Markdown inkl. Tabellen, Checkboxen, Code
- 🎨 **Syntax-Highlighting** — 50+ Sprachen über highlight.js
- ☑ **Interaktive Checkboxen** — direkt in der Vorschau klickbar, sync mit Quelltext
- 🔗 **Interne Navigation** — Anker-Links im IVZ springen zu Überschriften (GFM-Slug-Algorithmus)

### Intelligentes Editieren
- **Formatierungsleiste** — Klick-Toolbar für Überschriften, Fett/Kursiv/Code, Listen, Links, Bilder und Tabellen; erscheint automatisch im Editor- und Split-Modus
- **`Ctrl+B` / `Ctrl+I` / `Ctrl+K`** — Fett, Kursiv, Link per Tastatur; markierter Text wird automatisch eingeschlossen
- **Tabellen-Editor** — grafischer Dialog: Zeilen/Spalten hinzufügen/entfernen, Spaltenausrichtung (links/zentriert/rechts) per Klick wählen, vorhandene Tabellen erkennen und direkt bearbeiten, TSV/CSV aus Zwischenablage importieren
- **Smart Enter** — Enter in einer Listenzeile setzt die Liste automatisch fort; Enter auf leerer Listenzeile beendet die Liste
- **Auto-Pairing** — öffnende Klammern `( [ {` und Backticks werden automatisch geschlossen; markierter Text wird direkt eingeschlossen
- **TSV/CSV-Einfügen** — Tab-getrennte Daten aus der Zwischenablage werden automatisch zu einer Markdown-Tabelle umgewandelt

### Formular-Modus
- ⊟ **`{{typ:name:optionen}}`-Syntax** — Markdown wird zu interaktivem Formular
- 12 Feldtypen: `text`, `textarea`, `date`, `number`, `select`, `multiselect`, `radio`, `checkbox`, `range`, `button`, `reset`, `note`
- Werte werden ins **YAML-Frontmatter** gespeichert — persistent in der Datei selbst
- **Formular-Split-Ansicht** — Editor und gerendertes Formular live nebeneinander; Tipp im Quelltext, Formular aktualisiert sich sofort
- **Formularfelder-Leiste** — Klick-Toolbar für alle Feldtypen; erscheint automatisch in Formular-Modi
- **Felder-Konfigurationsdialog** — geführter Dialog mit allen Parametern und Makro-Vorschau für jeden Feldtyp

### Weitere Funktionen
- 📅 **Datum & Version** — aktuelles Datum und Versionsnummer ins Frontmatter eintragen, konfigurierbares Format
- 🔍 **Volltextsuche** — mit Treffer-Navigation und Highlighting in der Vorschau
- ⏱ **Auto-Save** — speichert automatisch alle 180 Sekunden (Countdown sichtbar in Statusleiste)
- 📖 **MD Syntax Referenz** — integriertes Cheatsheet mit 11 Kategorien und Live-Filter
- 🖨 **PDF-Export** — druckt vollständiges Dokument über Browser-Druckdialog

---

## Schnellstart

### Option A — Direkt im Browser nutzen (GitHub Pages)
```
https://jodevelops.github.io/md-studio/md-studio.html
```

### Option B — Lokal verwenden
```bash
# 1. Datei herunterladen
curl -O https://raw.githubusercontent.com/jodevelops/md-studio/main/md-studio.html

# 2. Im Browser öffnen (doppelklicken oder):
open md-studio.html        # macOS
start md-studio.html       # Windows
xdg-open md-studio.html    # Linux
```

> **Empfehlung:** Chrome oder Edge für vollen Funktionsumfang (Ordner öffnen, direkt speichern).  
> Firefox und Safari funktionieren mit leichten Einschränkungen (Speichern per Download).

---

## Tastaturkürzel

| Kürzel | Funktion |
|--------|----------|
| `Ctrl+S` | Speichern |
| `Ctrl+F` | Suchen öffnen/schliessen |
| `Ctrl+Shift+P` | PDF-Druckdialog |
| `Ctrl+B` | Fett (markierter Text wird eingeschlossen) |
| `Ctrl+I` | Kursiv (markierter Text wird eingeschlossen) |
| `Ctrl+K` | Link-Dialog öffnen |
| `Tab` (im Editor) | 2 Leerzeichen einrücken; in Tabelle: nächste Zelle |
| `Shift+Tab` (in Tabelle) | Vorherige Tabellenzelle |
| `Enter` (in Liste) | Listenstruktur fortsetzen / bei leerer Zeile beenden |
| `Esc` | Suche / Dialoge / Link-Dialog schliessen |

---

## Formular-Syntax (Kurzübersicht)

Felder direkt im Markdown-Text einbetten — im **Formular-Modus** werden sie zu interaktiven Eingaben:

```markdown
**Projektname:** {{text:name:Name des Projekts}}

**Status:** {{select:status:offen,in Bearbeitung,abgeschlossen}}

**Priorität:** {{radio:prio:niedrig|mittel|hoch}}

**Datum:** {{date:datum}}

**Anzahl Objekte:** {{number:anzahl:0:100000:100}}

**Beschreibung:**
{{textarea:beschreibung:4}}

{{button:Speichern}} {{reset:Zurücksetzen}}
```

Werte werden beim Speichern ins YAML-Frontmatter geschrieben und beim nächsten Öffnen vorausgefüllt.  
→ [Vollständige Dokumentation aller Feldtypen](handbuch.md#52-formularfeld-syntax)

---

## Browser-Kompatibilität

| Feature | Chrome/Edge | Firefox | Safari |
|---------|:-----------:|:-------:|:------:|
| Editor & Vorschau | ✅ | ✅ | ✅ |
| Formular-Modus | ✅ | ✅ | ✅ |
| Drag & Drop | ✅ | ✅ | ✅ |
| Ordner öffnen | ✅ | ❌ | ❌ |
| Direkt speichern | ✅ | ↓ Download | ↓ Download |
| PDF-Export | ✅ | ✅ | ✅ |

---

## Projektstruktur

```
md-studio/
├── md-studio.html     ← Die komplette Anwendung (eine Datei)
├── handbuch.md        ← Vollständige Benutzer-Dokumentation
├── README.md          ← Diese Datei
└── LICENSE            ← MIT License
```

Das ist kein Scherz — die gesamte Anwendung steckt in `md-studio.html`. Keine Build-Tools, kein `node_modules`, kein Framework-Overhead.

**Abhängigkeiten** (werden über CDN geladen, kein lokales Bundle nötig):
- [marked.js 9.1.6](https://github.com/markedjs/marked) — Markdown → HTML
- [highlight.js 11.9.0](https://github.com/highlightjs/highlight.js) — Syntax-Highlighting

---

## Dokumentation

Die vollständige Benutzeranleitung ist in [`handbuch.md`](handbuch.md) enthalten:

- UI-Beschreibung & Grundstruktur
- Illustrierte Click-Through-Workflows
- Alle Funktionen im Detail
- Formatierungsleiste & Tabellen-Editor
- Formular-Modus Referenz (alle 12 Feldtypen)
- Tastaturkürzel
- Browser-Kompatibilität
- FAQ

---

## License

MIT — frei verwendbar, änderbar, verteilbar. Volltext in [`LICENSE`](LICENSE).

---

*MD Studio — Standalone HTML Markdown Editor · Entwickelt mit Claude (Anthropic)*
