# STATISTICS — Statistical Analysis of K‑40 Decay Measurements

This document describes the statistical methods used to analyze the radioactive decay data generated from Potassium‑40 (K‑40).  
The goal is to validate the randomness, stability, and entropy of the measured decay events.

---

## 1. Statistical Model

Radioactive decay is a stochastic process governed by the Poisson distribution.  
For a given time interval, the number of detected decay events follows:

P(k; λ) = (λ^k · e^(−λ)) / k!

Where:

- k = number of detected events  
- λ = expected number of events (mean count rate)

The defining property of a Poisson process is:

**Variance = Mean**

This relationship is used as a primary verification criterion.

---

## 2. CPM and Event Statistics

The measurement device provides **CPM (Counts per Minute)** as the number of detected decay events within a **fixed 60‑second counting window**.  
Each CPM value is therefore **one statistical sample** from the underlying Poisson process.

From CPM we derive:

- Mean count rate: λ = CPM  
- Event rate per second: CPS = CPM / 60  
- Expected variance: Var = λ  
- Standard deviation: σ = √λ  

These values are used to compare theoretical and observed fluctuations.

---

## 3. Histogram Analysis

A histogram of CPM values over time reveals:

- the spread of the distribution  
- deviations from Poisson expectations  
- stability of the measurement setup  
- presence of systematic drift or noise  

The histogram is evaluated in **normalized form** (sum of all bin probabilities = 1).  
This allows comparison across datasets of different lengths and enables entropy calculation.

A stable K‑40 source produces a **unimodal distribution** centered around the mean CPM.

---

## 4. Fano Factor

The Fano factor quantifies deviations from ideal Poisson behavior:

F = Variance / Mean

Interpretation:

- F ≈ 1 → ideal Poisson process  
- F < 1 → sub‑Poisson (over‑regular, often due to smoothing or electronics)  
- F > 1 → super‑Poisson (excess noise, environmental influence)  

Expected statistical fluctuation:

Std(F) ≈ √(2 / N)

where N is the number of samples.

Significant deviations indicate non‑Poisson behavior.

---

## 5. Entropy Estimation

Entropy quantifies the randomness contained in the CPM distribution.

Entropy is computed from the normalized histogram:

H = − Σ p(i) · log₂(p(i))

Where p(i) is the probability of observing count value i.

This entropy represents the **randomness per sample**,  
and each sample corresponds to **one 60‑second counting window**.

Entropy increases with the mean count rate λ.

---

## 6. Autocorrelation (Not Used)

Autocorrelation can theoretically detect temporal dependencies.  
However, because CPM values represent independent 60‑second counting windows,  
short‑lag autocorrelation does not reflect physical correlations and provides no useful information.

For this reason, autocorrelation is not computed and not used for verification.


## 7. Verification Summary

A dataset is statistically valid if:

- mean and variance match Poisson expectations  
- the Fano factor is close to 1  
- the histogram is stable and unimodal  
- entropy per sample is consistent  
- no systematic drift is observed  

These criteria ensure that the dataset reflects true radioactive decay behavior.

---

# STATISTIK — Analyse der K‑40‑Zerfallsdaten

Dieses Dokument beschreibt die statistischen Methoden zur Analyse der durch Kalium‑40 (K‑40) erzeugten Zerfallsdaten.  
Ziel ist die Validierung der Zufälligkeit, Stabilität und Entropie der gemessenen Ereignisse.

---

## 1. Statistisches Modell

Radioaktiver Zerfall folgt einem Poisson‑Prozess.  
Für ein Zeitintervall gilt:

P(k; λ) = (λ^k · e^(−λ)) / k!

Dabei:

- k = Anzahl der registrierten Ereignisse  
- λ = erwartete Ereigniszahl (mittlere Zählrate)

Kennzeichen eines Poisson‑Prozesses:

**Varianz = Mittelwert**

Dies dient als zentrales Prüfkriterium.

---

## 2. CPM und Ereignisstatistik

Das Messgerät liefert **CPM (Counts per Minute)** als Anzahl der registrierten Ereignisse innerhalb eines **festen 60‑Sekunden‑Zählfensters**.  
Jeder CPM‑Wert ist somit **eine Stichprobe** aus dem zugrunde liegenden Poisson‑Prozess.

Daraus ergeben sich:

- Mittlere Zählrate: λ = CPM  
- Ereignisse pro Sekunde: CPS = CPM / 60  
- Erwartete Varianz: Var = λ  
- Standardabweichung: σ = √λ  

Diese Werte dienen zum Vergleich von Theorie und Messung.

---

## 3. Histogramm‑Analyse

Ein Histogramm der CPM‑Werte zeigt:

- die Verteilung der Messwerte  
- Abweichungen vom Poisson‑Modell  
- Stabilität des Messaufbaus  
- systematische Drift oder Störungen  

Das Histogramm wird **normalisiert** (Summe aller Bin‑Wahrscheinlichkeiten = 1).  
Dies ermöglicht den Vergleich zwischen Datensätzen unterschiedlicher Länge und ist Voraussetzung für die Entropieberechnung.

Eine stabile K‑40‑Quelle erzeugt eine **unimodale Verteilung** um den Mittelwert.

---

## 4. Fano‑Faktor

Der Fano‑Faktor misst Abweichungen vom idealen Poisson‑Verhalten:

F = Varianz / Mittelwert

Interpretation:

- F ≈ 1 → idealer Poisson‑Prozess  
- F < 1 → sub‑Poisson (zu regelmäßige Werte, oft durch Glättung)  
- F > 1 → super‑Poisson (zusätzliches Rauschen, Umwelteinflüsse)  

Erwartete statistische Schwankung:

Std(F) ≈ √(2 / N)

wobei N die Anzahl der Messwerte ist.

---

## 5. Entropie‑Schätzung

Die Entropie wird aus der normalisierten CPM‑Verteilung berechnet:

H = − Σ p(i) · log₂(p(i))

Sie beschreibt die **Zufälligkeit pro Stichprobe**,  
wobei eine Stichprobe einem **60‑Sekunden‑Zählfenster** entspricht.

Die Entropie steigt mit der mittleren Zählrate λ.

---

## 6. Autokorrelation (nicht verwendet)

Autokorrelation kann grundsätzlich zeitliche Abhängigkeiten sichtbar machen.  
Da CPM‑Werte jedoch unabhängige 60‑Sekunden‑Zählintervalle darstellen,  
besitzt die Autokorrelation für kurze Lags keine physikalische Aussagekraft und liefert keinen Mehrwert.

Aus diesem Grund wird die Autokorrelation nicht berechnet und nicht zur Verifikation verwendet.

---

## 7. Zusammenfassung der Verifikation

Ein Datensatz gilt als statistisch valide, wenn:

- Mittelwert und Varianz dem Poisson‑Modell entsprechen  
- der Fano‑Faktor nahe 1 liegt  
- das Histogramm stabil und unimodal ist  
- die Entropie pro Stichprobe konsistent ist  
- keine systematische Drift erkennbar ist  

Diese Kriterien gewährleisten, dass die Daten echten radioaktiven Zerfall widerspiegeln.
