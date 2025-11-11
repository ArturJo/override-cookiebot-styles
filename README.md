override-cookiebot-styles
=========================

Kleine Sammlung von CSS/SCSS-Overrides für den Cookiebot-Banner und das Widget. Der Fokus liegt darauf, eine primäre Akzentfarbe zentral zu steuern, ohne das Cookiebot-Markup anzupassen.

Inhalt
- Was ist das?
- Voraussetzungen
- Installation
- Nutzung
  - Im Browser (fertige CSS-Dateien)
  - In Build-Projekten (SCSS/CSS importieren)
  - Primärfarbe anpassen
- Build-Skripte
- Projektstruktur
- Support & Beiträge
- Lizenz

Was ist das?
Dieses Paket überschreibt ausgewählte Cookiebot-Styles (Dialog, Widget, Links, Buttons), wobei die Akzentfarbe über die CSS-Variable `--cb-primary-color` gesteuert wird.

Voraussetzungen
- Node.js und npm

Installation
Du kannst die fertigen CSS-Dateien direkt nutzen oder das Repo/Package in dein Projekt aufnehmen.

Option A: Direkt verwenden (CDN/Copy)
- Kopiere eine der Dateien aus `dist/` in dein Projekt:
  - `dist/cookiebot-overrides.css`
  - `dist/cookiebot-overrides-compressed.css`
- Binde sie nach den Cookiebot-Styles ein:

  <link rel="stylesheet" href="/pfad/zu/cookiebot-overrides.css" />

Option B: Als Abhängigkeit im Projekt (lokal)
1. Repository klonen oder als Abhängigkeit hinzufügen.
2. In das Projektverzeichnis wechseln und Abhängigkeiten installieren:

   npm install

Nutzung

Im Browser (fertige CSS-Dateien)
1. Cookiebot wie gewohnt einbinden.
2. Danach die gewünschte CSS-Datei aus `dist/` laden.
3. Optional die Akzentfarbe per CSS-Variable setzen (siehe unten).

In Build-Projekten (SCSS/CSS importieren)
- SCSS importieren:

  @use "src/cookiebot-overrides.scss";

- oder die generierte CSS importieren:

  @import "dist/cookiebot-overrides.css";

Primärfarbe anpassen
Setze die CSS-Variable auf Root-Ebene, um die Akzentfarbe zu ändern (Standard ist `#86674b`):

html {
  --cb-primary-color: #0d6efd; /* Beispiel: Blau */
}

Build-Skripte
- CSS bauen (nicht minimiert):

  npm run build

- CSS bauen (minimiert):

  npm run build:compressed

Projektstruktur
- `src/cookiebot-overrides.scss` – Quelle der Anpassungen
- `dist/cookiebot-overrides.css` – generierte CSS (lesbar)
- `dist/cookiebot-overrides-compressed.css` – generierte CSS (minimiert)

Hinweise
- Dieses Paket setzt auf die Standard-Klassen/IDs von Cookiebot. Sollten sich Selektoren ändern, müssen ggf. die Overrides aktualisiert werden.
- Stelle sicher, dass die Overrides nach den Cookiebot-Styles geladen werden, damit sie greifen.

Support & Beiträge
- Issues: https://github.com/ArturJo/override-cookiebot-styles/issues
- Pull Requests sind willkommen. Bitte kurz beschreiben, was geändert und warum es nötig ist.

Lizenz
Dieses Projekt ist unter der Unlicense veröffentlicht – faktisch Public Domain. Du kannst den Code ohne Einschränkungen nutzen, verändern und weiterverbreiten.

