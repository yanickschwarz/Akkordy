# Akkordy

Grifftabellen-Editor für das chromatische Knopfakkordeon. Gedacht für Spielerinnen und Spieler, die ohne Noten arbeiten und ihre Lieder stattdessen als Grifftabelle festhalten — auf Papier, zum Abheften im Liederordner.

## Was das Tool macht

- **Knöpfe ausfüllen** — Klick auf einen Kreis füllt ihn schwarz, ein zweiter Klick macht es rückgängig.
- **Akkorde markieren** — Farbe wählen, 2–3 Knöpfe antippen, «Fertig»: ein breiter Leuchtstift-Strich verbindet sie.
- **Kopfzeile** — Liedname links, Bass-Lage rechts (z. B. `+ 1`, `-3`, ausgehend vom C).
- **Drucken / PDF** — A4 quer, nur Titel und Tabelle, ohne Bedienelemente.
- **Speichern / Öffnen** — jedes Lied als `.json`-Datei, jederzeit wieder bearbeitbar.
- **C-Griff und B-Griff** umschaltbar.

## Aufbau

Eine einzige Datei, `index.html`. Kein Build, kein Backend, keine Abhängigkeiten. Lokal öffnen genügt:

```
open index.html
```

## Deployment auf Vercel

1. vercel.com/new öffnen
2. dieses Repo auswählen
3. Framework Preset: **Other** — Build Command und Output Directory leer lassen
4. Deploy

## Tastatur-Layout anpassen

Die Tonreihen stehen im `<script>`-Block als Listen unter `FAM`. Wer mehr Knöpfe pro Reihe braucht (60 / 70 / 82 / 87 Knöpfe), verlängert dort die Reihen; die Oktavstriche werden über `withPrimes()` automatisch gesetzt.

Geometrie über die Konstanten `R` (Radius), `DX` / `DY` (Abstände) und `PAD` (Rand).
