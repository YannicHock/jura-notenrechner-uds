# Jura Notenrechner UdS

Ein schlanker, clientseitiger Notenrechner für das Erste Juristische Staatsexamen an der **Universität des Saarlandes (UdS)**. Die Anwendung läuft vollständig im Browser – ohne Backend, ohne Abhängigkeiten.

🔗 **Live:** [https://yannickhock.github.io/jura-notenrechner-uds/](https://yannickhock.github.io/jura-notenrechner-uds/)

---

## Features

- **Gesamtnote berechnen** aus staatlicher Pflichtfachprüfung (70 %) und universitärer Schwerpunktprüfung (30 %)
- **Pflichtfachprüfung:** 6 Klausuren + 3 mündliche Teilnoten (Klausuren 12/17 ≈ 71 %, Mündlich 5/17 ≈ 29 %)
- **Schwerpunktprüfung:** 2 Klausuren + 1 mündliche Note (gleiche Gewichtung 12/17 / 5/17)
- **Ziel-Rechner:** Berechnet, welche Schwerpunkt-Endnote (und ggf. welchen Klausurenschnitt) man bei einer angestrebten Gesamtnote benötigt
- Echtzeit-Berechnung ohne Seitenneuladen
- Validierung: Warnung bei Werten außerhalb der Skala (0–18)
- Reset-Button zum Leeren aller Felder

## Notenberechnung

```
Pflichtfachnote  = (Ø Klausuren × 12/17) + (Ø Mündlich × 5/17)
Schwerpunktnote  = (Ø Klausuren × 12/17) + (Mündliche Note × 5/17)
Gesamtnote       = Pflichtfachnote × 0,70 + Schwerpunktnote × 0,30
```

## Technologie

| Merkmal | Detail |
|---|---|
| Sprache | HTML, CSS, Vanilla JavaScript |
| Abhängigkeiten | keine |
| Hosting | GitHub Pages |
| Einstiegspunkt | `index.html` |

## Lokale Nutzung

Da es sich um eine reine HTML-Datei handelt, reicht es, `index.html` direkt im Browser zu öffnen:

```bash
# Repository klonen
git clone https://github.com/YannicHock/jura-notenrechner-uds.git

# Datei im Browser öffnen
open jura-notenrechner-uds/index.html   # macOS
xdg-open jura-notenrechner-uds/index.html  # Linux
```

## Deployment

Änderungen auf dem `main`-Branch werden automatisch via GitHub Actions auf GitHub Pages veröffentlicht (`.github/workflows/static.yml`).

## Lizenz

[MIT](LICENSE)