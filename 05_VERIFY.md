# VERIFY — Reproducible Verification of Measurement Data

This document describes how each measurement, dataset, and statistical analysis in this project can be independently verified.  
The goal is to provide a transparent, audit‑ready foundation for all results derived from K‑40 decay events.

---

## 1. Physical Basis

All measurements are based on the natural beta decay of potassium‑40 (K‑40).  
Each detected decay event is a discrete physical event.  
Radioactive decay follows a Poisson process, and therefore the statistical properties of the data must match the Poisson model.

---

## 2. Measurement System

The measurement system provides:

- one CPM value per fixed 60‑second counting window  
- one timestamp per second  

The device does **not** export:

- raw CPS events  
- metadata such as material, distance, geometry, shielding, or environment  

Only the exported CPM values are used for verification.

---

## 3. Raw Data Structure

The raw dataset contains:

### Timestamp  
One row per second.

### CPM value  
Number of detected decay events within the last 60‑second counting window.  
Each CPM value is one statistical sample.

### Measurement duration  
Implicitly defined by the number of rows (1 row = 1 second).

### Derived count values (optional)  
raw_counts = CPM

No additional metadata is required for statistical verification.

---

## 4. Statistical Verification

### 4.1 Poisson Distribution  
Mean and variance must match Poisson expectations:  
Variance ≈ Mean

### 4.2 Fano Factor  
F = Variance / Mean  
Expected:  
F ≈ 1  
Std(F) ≈ √(2 / N)

### 4.3 Histogram  
The normalized histogram must be unimodal and centered around the mean CPM.

### 4.4 Entropy  
Entropy is computed from the CPM distribution:  
H = − Σ p(i) · log₂(p(i))  
Entropy describes the randomness per sample, where one sample corresponds to one 60‑second counting window.

### 4.5 Drift Detection  
Long‑term deviations from the mean indicate:

- detector instability  
- shielding changes  
- geometric changes  
- environmental influence  

Autocorrelation is not used, because CPM values represent independent 60‑second samples.

---

## 5. Reproducibility Criteria

A measurement is considered reproducible if:

- CPM values remain within a stable range for the same source  
- mean and variance match Poisson expectations  
- the Fano factor is close to 1  
- the histogram is stable and unimodal  
- entropy per sample is consistent  
- no systematic drift is observed  

The histogram of CPM values must be unimodal when generated from the raw data.  
A histogram is not included in the delivered results; it can be created by the user from the provided CPM values.

---

## 6. Audit Checklist

- Raw data available  
- Timestamp and CPM values intact  
- Statistical analysis performed  
- Poisson compatibility verified  
- Fano factor within expected range  
- Histogram unimodal  
- Entropy traceable  
- No drift detected  
- Results reproducible  

---

# VERIFY — Reproduzierbare Verifikation der Messdaten

Dieses Dokument beschreibt, wie jede Messung, jeder Datensatz und jede statistische Analyse dieses Projekts unabhängig verifiziert werden kann.  
Ziel ist eine transparente, auditierbare Grundlage für alle aus K‑40‑Zerfallsereignissen abgeleiteten Ergebnisse.

---

## 1. Physikalische Grundlage

Alle Messungen basieren auf dem natürlichen Betazerfall von Kalium‑40 (K‑40).  
Jedes registrierte Zerfallsereignis ist ein diskretes physikalisches Ereignis.  
Radioaktiver Zerfall folgt einem Poisson‑Prozess, daher müssen die statistischen Eigenschaften der Daten dem Poisson‑Modell entsprechen.

---

## 2. Messsystem

Das Messsystem liefert:

- einen CPM‑Wert pro festem 60‑Sekunden‑Zählfenster  
- einen Zeitstempel pro Sekunde  

Das Gerät exportiert **keine**:

- Rohimpulse (CPS)  
- Metadaten wie Material, Abstand, Geometrie oder Umgebung  

Für die Verifikation werden ausschließlich die CPM‑Werte verwendet.

---

## 3. Datenstruktur

Der Rohdatensatz enthält:

### Zeitstempel  
Eine Zeile pro Sekunde.

### CPM‑Wert  
Anzahl der registrierten Ereignisse im letzten 60‑Sekunden‑Zählfenster.  
Jeder CPM‑Wert ist eine Stichprobe.

### Messdauer  
Implizit durch die Anzahl der Zeilen definiert.

### Abgeleitete Zählwerte (optional)  
raw_counts = CPM

Weitere Metadaten sind für die statistische Verifikation nicht erforderlich.

---

## 4. Statistische Verifikation

### 4.1 Poisson‑Verteilung  
Varianz und Mittelwert müssen übereinstimmen:  
Varianz ≈ Mittelwert

### 4.2 Fano‑Faktor  
F = Varianz / Mittelwert  
Erwartet:  
F ≈ 1  
Std(F) ≈ √(2 / N)

### 4.3 Histogramm  
Das normalisierte Histogramm muss unimodal und um den mittleren CPM zentriert sein.

### 4.4 Entropie  
Die Entropie wird aus der CPM‑Verteilung berechnet:  
H = − Σ p(i) · log₂(p(i))  
Sie beschreibt die Zufälligkeit pro Stichprobe, wobei eine Stichprobe einem 60‑Sekunden‑Zählfenster entspricht.

### 4.5 Drift‑Erkennung  
Langfristige Abweichungen vom Mittelwert weisen auf:

- Instabilität  
- Abschirmungsänderungen  
- geometrische Veränderungen  
- Umwelteinflüsse  

Autokorrelation wird nicht verwendet, da CPM‑Werte unabhängige Stichproben darstellen.

---

## 5. Reproduzierbarkeitskriterien

Eine Messung gilt als reproduzierbar, wenn:

- die CPM‑Werte für dieselbe Quelle stabil bleiben  
- Mittelwert und Varianz dem Poisson‑Modell entsprechen  
- der Fano‑Faktor nahe 1 liegt  
- das Histogramm stabil und unimodal ist  
- die Entropie pro Stichprobe konsistent ist  
- keine Drift erkennbar ist  

Das Histogramm der CPM‑Werte muss bei Erzeugung aus den Rohdaten unimodal sein.  
Ein Histogramm wird nicht mitgeliefert; es kann vom Nutzer jederzeit aus den bereitgestellten CPM‑Werten erzeugt werden.

---

## 6. Audit‑Checkliste

- Rohdaten vorhanden  
- Zeitstempel und CPM‑Werte vollständig  
- Statistische Analyse durchgeführt  
- Poisson‑Kompatibilität bestätigt  
- Fano‑Faktor im erwarteten Bereich  
- Histogramm unimodal  
- Entropie nachvollziehbar  
- Keine Drift  
- Ergebnisse reproduzierbar  

