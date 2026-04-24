# VERIFY — Reproducible Verification of Measurement Data

This document describes how each measurement, dataset, and entropy analysis in this project can be reproduced and independently verified.<br>The goal is to provide a transparent, auditable foundation for all results derived from K‑40 decay events.

## 1. Physical Basis

All measurements rely on the natural beta decay of Potassium‑40 (K‑40). Each detected decay event is treated as a discrete physical occurrence recorded by the Geiger–Müller tube.

## 2. Measurement Setup

- Geiger counter: QMC-500+ or comparable tube  
- Source distance: 0–5 cm  
- Materials: KCl, potassium carbonate (Pottasche), potassium‑rich household products  
- Measurement interval: 60 seconds  
- Recorded quantity: CPM (Counts per Minute)

# VERIFY — Reproducible Verification of Measurement Data

This document describes how each measurement, dataset, and entropy analysis in this project can be reproduced and independently verified.  
The goal is to provide a transparent, auditable foundation for all results derived from K‑40 decay events.

## 1. Physical Basis

All measurements rely on the natural beta decay of Potassium‑40 (K‑40).  
Each detected decay event is treated as a discrete physical occurrence recorded by the Geiger–Müller tube.

## 2. Measurement Setup

The measurement system provides one data row per second and a rolling CPM (Counts per Minute) value based on a 60‑second window.  
The device does not export raw CPS events or metadata such as material, distance, geometry, or environmental parameters.

## 3. Data Structure (cleaned)

The raw datasets contain only the information exported by the device:

**Timestamp**  
One row per second, representing the exact time of each measurement.

**CPM value**  
The count rate as a rolling 60‑second average.

**Measurement duration**  
Implicitly defined by the number of rows (1 row = 1 second).

**Derived raw counts (optional)**  
These can be reconstructed from CPM/60 but are not directly included in the raw data.

Additional contextual information (material, distance, geometry, setup parameters) is not part of the raw export and is not required for statistical verification.  
Such metadata may be documented separately if needed, but it is optional.

## 4. Statistical Verification

The following methods are used to verify the statistical validity of the measurements:

- Poisson distribution of count rates  
- Variance analysis  
- Histogram of event distribution  
- Entropy estimation from discrete decay events  
- Comparison with theoretical expectations

## 5. Reproducibility Criteria

A measurement is considered reproducible if:

- CPM values remain within ±10% of a reference measurement  
- Variance matches Poisson expectations  
- Entropy per event remains stable  
- No systematic deviations appear

## 6. Audit Checklist

- [ ] Raw data available  
- [ ] Timestamp and CPM values intact  
- [ ] Statistical analysis performed  
- [ ] Entropy values traceable  
- [ ] Results reproducible

# VERIFY — Reproduzierbare Verifikation der Messdaten

Dieses Dokument beschreibt, wie jede Messung, jeder Datensatz und jede Entropieanalyse dieses Projekts reproduzierbar und unabhängig verifiziert werden kann.  
Ziel ist es, eine transparente, auditierbare Grundlage für alle aus K‑40‑Zerfallsereignissen abgeleiteten Ergebnisse zu schaffen.

## 1. Physikalische Grundlage

Alle Messungen basieren auf dem natürlichen Betazerfall von Kalium‑40 (K‑40).  
Jedes registrierte Zerfallsereignis wird als diskretes physikalisches Ereignis behandelt, das vom Geiger‑Müller‑Zählrohr erfasst wird.

## 2. Messaufbau

Das Messsystem liefert eine Datenzeile pro Sekunde sowie einen CPM‑Wert (Counts per Minute) als gleitenden 60‑Sekunden‑Durchschnitt.  
Das Gerät exportiert keine Rohimpulse (CPS) und keine Metadaten wie Material, Abstand, Geometrie oder Umgebungsparameter.

## 3. Datenstruktur (bereinigt)

Die Rohdatensätze enthalten ausschließlich die vom Gerät exportierten Informationen:

**Zeitstempel**  
Eine Zeile pro Sekunde, entsprechend dem genauen Zeitpunkt jeder Messung.

**CPM‑Wert**  
Die vom Gerät ausgegebene Zählrate als gleitender 60‑Sekunden‑Durchschnitt.

**Messdauer**  
Implizit durch die Anzahl der Zeilen definiert (1 Zeile = 1 Sekunde).

**Abgeleitete Rohzählungen (optional)**  
Diese können aus CPM/60 rekonstruiert werden, sind aber nicht direkt im Rohdatensatz enthalten.

Zusätzliche Kontextinformationen (Material, Abstand, Geometrie, Setup‑Parameter) sind nicht Teil des Rohexports und werden für die statistische Verifikation nicht benötigt.  
Sie können bei Bedarf separat dokumentiert werden, sind aber optional.

## 4. Statistische Verifikation

Zur Überprüfung der Messdaten werden folgende Methoden eingesetzt:

- Poisson‑Verteilung der Zählraten  
- Varianz‑Analyse  
- Histogramm der Ereignisverteilung  
- Entropieschätzung aus diskreten Zerfallsereignissen  
- Vergleich mit theoretischen Erwartungswerten

---

## 5. Reproduzierbarkeitskriterien

Eine Messung gilt als reproduzierbar, wenn:

- die CPM‑Werte innerhalb ±10 % einer Referenzmessung liegen  
- die Varianz der Poisson‑Erwartung entspricht  
- die Entropie pro Ereignis stabil bleibt  
- keine systematischen Abweichungen auftreten

---

## 6. Audit‑Checkliste

- [ ] Rohdaten vorhanden  
- [ ] Zeitstempel und CPM‑Werte vollständig  
- [ ] Statistische Analyse durchgeführt  
- [ ] Entropiewerte nachvollziehbar  
- [ ] Ergebnisse reproduzierbar


