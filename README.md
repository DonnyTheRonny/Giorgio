# Giorgio's Paralia – Ferienwohnung & Ferienhaus

Website und A4-Aushang für die Ferienwohnung und das Ferienhaus in Paralia Katerinis.

**Aktuell ist das ein Entwurf mit Platzhaltern** (Bilder, Videos, Preise, Kontakt).

## Aufbau

| Datei | Inhalt |
|---|---|
| `index.html` | Website (Deutsch-Texte direkt hier) |
| `js/main.js` | Englische und griechische Übersetzungen, Video-Steuerung, Galerie |
| `css/style.css` | Design |
| `assets/img/` | Fotos (`hero.jpg`, `wohnung-1..3.jpg`, `haus-1..3.jpg`, `umgebung-1..2.jpg`, `restaurant.jpg`) und QR-Code |
| `assets/video/` | Videos `wohnung.mp4`, `haus.mp4` (laufen automatisch, stumm, in Schleife) |
| `aushang/aushang.html` | A4-Aushang (im Browser öffnen → Drucken) |
| `aushang/aushang.pdf` | A4-Aushang als druckfertiges PDF |

## Echte Inhalte einsetzen

- **Fotos:** gleiche Dateinamen in `assets/img/` überschreiben (Querformat, ca. 1600 px breit).
- **Videos:** `assets/video/wohnung.mp4` / `haus.mp4` ersetzen. Kurz halten (10–30 s) und
  verkleinern, z. B.:
  `ffmpeg -i original.mov -vf scale=1280:-2 -an -c:v libx264 -crf 28 -movflags +faststart wohnung.mp4`
- **Kontakt:** Telefonnummer in `index.html` (`wa.me/…`, `tel:…`) und im Aushang ändern.

## Online stellen (GitHub Pages, kostenlos)

Repository → *Settings* → *Pages* → *Deploy from a branch* → Branch wählen, Ordner `/ (root)`.
Danach ist die Seite unter `https://donnytheronny.github.io/Giorgio/` erreichbar. Auf genau
diese Adresse zeigt der QR-Code. Bei einer eigenen Domain muss der QR-Code neu erzeugt werden.
