# Rahmen Froesch — Website

Statische Website für **Rahmen Froesch · Gregor Froesch**, Burgfreiheit 25, 41199 Mönchengladbach.

- `index.html` — die komplette Seite (HTML + CSS inline, kein Build, keine Abhängigkeiten)
- `img/` — Bilder (lokale Kopien, damit die Seite unabhängig läuft)
- `favicon.svg` — Icon
- `Rahmen Froesch.dc.html`, `support.js`, `Archiv/` — ursprüngliche Entwurfsdateien (nicht Teil der Live-Seite)

## Mobil-Optimierung

Der erste Bildschirm auf dem Handy zeigt nur noch Logo, Telefonnummer, Überschrift,
einen Satz und einen Button — alles andere ist nach unten gewandert.

- **Burgermenü** auf dem Handy: Vollbild-Overlay mit allen Sektionen, Anruf-Button und Adresse;
  schließt per X, per Escape, beim Klick auf einen Link und beim Wechsel auf Desktop-Breite
- Telefonnummer steht auf dem Handy im Menü, ab 721 px als Pille in der Kopfzeile
- keine fixe Aktionsleiste am unteren Rand; Kontaktkarten stehen im Bereich „Besuch"
- Hero füllt den Bildschirm (`100svh` — `svh` statt `vh`, damit die Browserleiste keinen Sprung erzeugt)
- **Öffnungszeiten** sind eine eigene Sektion (`#zeiten`) statt Leiste im Hero plus Kasten im Kontaktbereich
- flachere Bildausschnitte auf dem Handy (4:3 statt 4:5, 3:2 statt 16:11)
- Touch-Flächen 52–64 px hoch, Buttons volle Breite
- Ränder `clamp(20px, 5vw, 40px)`, Überschriften per `clamp()`
- Galerie als Wisch-Karussell (72 vw pro Karte)
- `svh` statt `vh` (kein Springen durch die Browserleiste), kein horizontales Scrollen
- Bilder lokal, `loading="lazy"`, feste Seitenverhältnisse gegen Layout-Sprünge
- zusätzlich: Meta-Description, Open Graph, Favicon, LocalBusiness-JSON-LD

## Lokal ansehen

```bash
python -m http.server 8000
```

Danach http://localhost:8000 öffnen.
