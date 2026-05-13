# Koerper / 100kg Tracking

Dieses Repository sammelt Rohdaten zu Gewicht, Koerperumfang, Ernaehrung und Garmin-Werten.

Ziel ist nicht nur Kalorien zu zaehlen, sondern Trends zu erkennen:

- Gewichtsentwicklung
- Bauchumfang / Taille
- Kalorien- und Makroaufnahme
- Vergleich Garmin-Verbrauch vs. reale Gewichtsveraenderung
- spaetere Trendberechnung mit Python/Pandas

## Struktur

```text
data/
  daily/              Tagesdaten im JSONL-Format
  imports/garmin/     exportierte Garmin-Rohdaten
summaries/            spaetere Auswertungen als CSV
schema/               Dokumentation der Datenfelder
scripts/              spaetere Python-Auswertungen
```

## Tagesdaten

Die Tagesdaten liegen als JSONL-Dateien vor, also eine JSON-Zeile pro Tag.

Beispiel:

```json
{"date":"2026-05-13","weight_kg":102.6,"waist_navel_cm":null,"garmin":{"body_fat_percent":30.0,"muscle_mass_kg":37.8},"nutrition":{"meals":[],"daily_total":{"kcal":null,"protein_g":null,"carbs_g":null,"fat_g":null}},"notes":""}
```

## Messregeln

Gewicht und Umfang am besten morgens messen:

- nach Toilette
- vor Fruehstueck
- entspannt stehen
- Bauch nicht einziehen
- Massband immer an gleicher Stelle

Wichtigste Umfangsmessung: Bauchumfang auf Nabelhoehe.
