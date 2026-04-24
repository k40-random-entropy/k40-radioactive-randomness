# SETUP

## Purpose

This document describes how to perform a measurement with the GQ GMC‑500+ / GMC‑600+ Geiger counter, how to export CPM data, and how to prepare the dataset for analysis with the Excel tools in this repository.

## Hardware Requirements

- GQ GMC‑500+ or GMC‑600+
- USB‑C cable
- PC or laptop (Windows recommended)
- Stable radioactive potassium source (e.g., potassium carbonate, potassium chloride)
- Stable mechanical setup with fixed distance between source and detector

## Measurement Setup

1. Fill a small dish with potassium salt and level the surface.
2. Place a thin plastic or acrylic plate on top to ensure reproducible geometry.
3. Attach two Dual‑Lock pads on the plate.
4. Click the Geiger counter onto the pads so the detector window is centered above the salt.
5. Connect USB‑C to the PC for power and data.
6. Place the setup on a stable desk, away from vibrations or drafts.

## Device Configuration

- Measurement mode: CPM
- Logging interval: 1 minute
- USB mode: Auto / Data
- Audio: optional
- Display: optional
- Keep the device running continuously during the measurement period.

## Data Export

1. Open GQ GMC Data Viewer on the PC.
2. Connect the device via USB‑C.
3. Select “Download Data” → “History Data”.
4. Export as CSV.
5. Save the file under:

   /data/raw/YYYY-MM-DD_cpm_min.csv

## Preparing the Excel Workbook

1. Open the Excel workbook included in this repository.
2. Import the CSV into the sheet CPM_MIN.
3. Ensure the timestamp is in column A and CPM in column B.
4. Do not modify column order or header names.

## Running the Analysis

1. Press ALT+F8.
2. Run the macro:

   Poisson_From_CPM_MIN

3. Results are written to the sheet POISSON.
4. The output includes:

- Mean CPM
- Variance
- Variance/Mean ratio
- Overdispersion Z‑score
- Poisson compatibility test
- Per‑minute Z‑scores and p‑values

## Notes

- The device reports CPM as a 60‑second moving average.
- Short‑lag autocorrelation is therefore not meaningful and is not computed.
- Histogram analysis uses normalized bin frequencies.
- Raw data is never modified; all analysis is derived from the CSV.

## Completion

The dataset is now ready for statistical analysis and verification.



# SETUP (Deutsch)

## Zweck

Dieses Dokument beschreibt, wie eine Messung mit dem GQ GMC‑500+ / GMC‑600+ durchgeführt wird, wie man CPM‑Daten exportiert und wie der Datensatz für die Analyse mit den Excel‑Werkzeugen dieses Repositories vorbereitet wird.

## Hardware‑Voraussetzungen

- GQ GMC‑500+ oder GMC‑600+
- USB‑C‑Kabel
- PC oder Laptop (Windows empfohlen)
- Stabile radioaktive Kaliumquelle (z. B. Kaliumcarbonat, Kaliumchlorid)
- Stabiler mechanischer Aufbau mit festem Abstand zwischen Quelle und Detektor

## Messaufbau

1. Eine kleine Schale mit Kaliumsalz füllen und Oberfläche glätten.
2. Eine dünne Kunststoff‑ oder Acrylplatte oben auflegen, um eine reproduzierbare Geometrie zu gewährleisten.
3. Zwei Dual‑Lock‑Pads auf die Platte kleben.
4. Den Geigerzähler auf die Pads klicken, sodass das Detektorfenster zentriert über dem Salz liegt.
5. USB‑C‑Kabel für Strom und Daten an den PC anschließen.
6. Aufbau auf einem stabilen Tisch platzieren, fern von Vibrationen oder Luftzug.

## Gerätekonfiguration

- Messmodus: CPM
- Log‑Intervall: 1 Minute
- USB‑Modus: Auto / Data
- Audio: optional
- Display: optional
- Gerät während der gesamten Messdauer eingeschaltet lassen.

## Datenexport

1. GQ GMC Data Viewer auf dem PC öffnen.
2. Gerät per USB‑C verbinden.
3. „Download Data“ → „History Data“ auswählen.
4. Als CSV exportieren.
5. Datei speichern unter:

   /data/raw/YYYY-MM-DD_cpm_min.csv

## Excel‑Vorbereitung

1. Die Excel‑Arbeitsmappe aus diesem Repository öffnen.
2. CSV in das Tabellenblatt CPM_MIN importieren.
3. Sicherstellen, dass der Zeitstempel in Spalte A und CPM in Spalte B steht.
4. Spaltenreihenfolge und Überschriften nicht ändern.

## Analyse ausführen

1. ALT+F8 drücken.
2. Makro ausführen:

   Poisson_From_CPM_MIN

3. Ergebnisse erscheinen im Blatt POISSON.
4. Die Ausgabe enthält:

- Durchschnittliche CPM
- Varianz
- Varianz/Mittelwert
- Overdispersion‑Z‑Score
- Poisson‑Kompatibilitätstest
- Z‑Scores und p‑Werte pro Minute

## Hinweise

- Das Gerät liefert CPM als gleitenden 60‑Sekunden‑Durchschnitt.
- Autokorrelation für kurze Lags ist daher nicht aussagekräftig und wird nicht berechnet.
- Histogramme werden auf Basis normalisierter Bin‑Wahrscheinlichkeiten ausgewertet.
- Rohdaten werden nie verändert; alle Analysen basieren auf der CSV.

## Abschluss

Der Datensatz ist nun bereit für statistische Analyse und Verifikation.

