# MD Studio

> **Lokaler Markdown-Editor als Single-HTML-Datei** – ohne Installation, ohne Build-Prozess, ohne Cloud.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Single File](https://img.shields.io/badge/app-single%20html-blue.svg)]()
[![Offline](https://img.shields.io/badge/offline-ready-green.svg)]()

**Links:** [Live-Demo](https://jodevelops.github.io/md-studio/md-studio.html) · [Handbook](handbuch.md) · [Direktdownload](https://raw.githubusercontent.com/jodevelops/md-studio/main/md-studio.html)

---

## Überblick

MD Studio ist ein vollständiger Markdown-Arbeitsplatz in **einer Datei** (`md-studio.html`).

- Läuft direkt im Browser
- Speichert lokal
- Unterstützt klassischen Markdown-Flow plus Formular-Modus
- Kein Setup notwendig

---

## Kernfunktionen

### 1) Dateien & Speichern
- **Ordner öffnen** (Chrome/Edge): lädt alle `.md`-Dateien im Verzeichnis
- **Dateien laden** (alle Browser): eine oder mehrere `.md`-Dateien
- **Drag & Drop** in die App
- **Neue Datei** mit YAML-Frontmatter-Vorlage
- **Direktes Speichern** in die Originaldatei (mit File System Access API)
- **Export als neue Version** (z. B. `bericht_v2.md`)
- **Umbenennen** inkl. Dialog

### 2) Schreiben & Vorschau
- **Split-Ansicht** (Editor + Preview)
- **Editor-only / Preview-only**
- **Scroll-Synchronisation** zwischen Editor und Vorschau
- **GFM-Rendering** mit `marked`
- **Code-Highlighting** mit `highlight.js`
- **Interaktive Checklisten** in der Vorschau

### 3) Produktives Editieren
- **Formatierungsleiste** (Überschriften, Listen, Links, Bilder, Tabellen …)
- **Shortcuts**: `Ctrl+B`, `Ctrl+I`, `Ctrl+K`, `Ctrl+S`, `Ctrl+F`
- **Smart Enter** in Listen
- **Auto-Pairing** für Klammern/Backticks
- **Tabellen-Editor** mit Ausrichtung, Zeilen/Spalten-Steuerung und TSV/CSV-Import

### 4) Formular-Modus
- Formular-Makros per `{{typ:name:optionen}}`
- Unterstützte Felder: `text`, `textarea`, `date`, `number`, `select`, `multiselect`, `radio`, `checkbox`, `range`, `button`, `reset`, `note`
- Werte werden in YAML-Frontmatter persistiert
- Eigene Formular-Toolbar + Feld-Dialog

### 5) Weitere Tools
- **Datum/Version** ins Frontmatter schreiben
- **Suche** mit Treffer-Navigation
- **Markdown-Cheatsheet** in der App
- **PDF-Export** via Browser-Druck
- **Auto-Save** mit Countdown in der Statusleiste

---

## Schnellstart

### Lokal starten
1. `md-studio.html` herunterladen.
2. Datei im Browser öffnen.
3. Markdown-Datei laden oder neu erstellen.

```bash
curl -O https://raw.githubusercontent.com/jodevelops/md-studio/main/md-studio.html
```

> Empfehlung: **Chrome oder Edge** für vollen Datei-System-Funktionsumfang.

---

## Tastaturkürzel (Auszug)

| Kürzel | Funktion |
|---|---|
| `Ctrl+S` | Speichern |
| `Ctrl+F` | Suche ein-/ausblenden |
| `Ctrl+Shift+P` | PDF-Druckdialog |
| `Ctrl+B` | Fett |
| `Ctrl+I` | Kursiv |
| `Ctrl+K` | Link einfügen |
| `Esc` | Dialoge/Suche schließen |

---

## Browser-Kompatibilität

| Funktion | Chrome/Edge | Firefox | Safari |
|---|:---:|:---:|:---:|
| Editor & Vorschau | ✅ | ✅ | ✅ |
| Formular-Modus | ✅ | ✅ | ✅ |
| Drag & Drop | ✅ | ✅ | ✅ |
| Ordner öffnen | ✅ | ❌ | ❌ |
| Direktes Speichern | ✅ | Download | Download |

---

## Projektdateien

```text
md-studio/
├── md-studio.html   # komplette App
├── README.md        # Kurzüberblick
├── handbuch.md      # Vollständiges Handbook
└── LICENSE
```

---

## Lizenz

MIT – siehe [LICENSE](LICENSE).
