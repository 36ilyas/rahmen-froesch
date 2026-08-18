# Rahmen Froesch — Website

Statische Website für **Rahmen Froesch · Gregor Froesch**, Burgfreiheit 25, 41199 Mönchengladbach.

- `index.html` — die komplette Seite (HTML + CSS inline, kein Build, keine Abhängigkeiten)
- `img/` — Bilder (lokale Kopien, damit die Seite unabhängig läuft)
- `favicon.svg` — Icon
- `Rahmen Froesch.dc.html`, `support.js`, `Archiv/` — ursprüngliche Entwurfsdateien (nicht Teil der Live-Seite)

## Mobil-Optimierung

- echte Breakpoints bei 900 px / 720 px / 380 px statt reiner Inline-Styles
- Navigation bricht auf dem Handy in eine eigene Zeile um, Telefonnummer bleibt oben rechts
- feste Aktionsleiste unten auf dem Handy: **Anrufen** und **Anfahrt** (mit `safe-area-inset` für iPhones)
- Touch-Flächen mind. 52–64 px hoch, Buttons auf dem Handy volle Breite
- Ränder skalieren mit `clamp(20px, 5vw, 40px)`, Überschriften mit `clamp()`
- Galerie als Wisch-Karussell (76 vw pro Karte auf dem Handy)
- `100svh` statt `100vh` (keine Sprünge durch die Browserleiste), kein horizontales Scrollen
- Bilder lokal, `loading="lazy"`, feste Seitenverhältnisse gegen Layout-Sprünge
- zusätzlich: Meta-Description, Open Graph, Favicon, LocalBusiness-JSON-LD

## Lokal ansehen

```bash
python -m http.server 8000
```

Danach http://localhost:8000 öffnen.
