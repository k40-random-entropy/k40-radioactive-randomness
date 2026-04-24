# STATISTICS — Statistical Analysis of K‑40 Decay Measurements

This document describes the statistical methods used to analyze the radioactive decay data generated from Potassium‑40 (K‑40).  
The goal is to validate the randomness, stability, and entropy of the measured decay events.

## 1. Statistical Model

Radioactive decay is a stochastic process governed by the Poisson distribution.  
For a given time interval, the number of detected decay events follows:

**P(k; λ) = (λ^k * e^(-λ)) / k!**

Where:  
- k = number of detected events  
- λ = expected number of events (mean count rate)

The defining property of a Poisson process is:

**Variance = Mean**

This relationship is used as a primary verification criterion.

## 2. CPM and Event Statistics

The measurement device provides CPM (Counts per Minute) as a rolling 60‑second average.  
From CPM we derive:

- **Mean count rate:** λ = CPM  
- **Event rate per second:** CPS = CPM / 60  
- **Expected variance:** Var = λ  
- **Standard deviation:** σ = √λ

These values are used to compare theoretical and observed fluctuations.

## 3. Histogram Analysis

A histogram of CPM values over time reveals:

- The spread of the distribution
- Deviations from Poisson expectations
- Stability of the measurement setup
- Presence of systematic drift or noise

The histogram is evaluated in normalized form (sum of all bin probabilities = 1).  
This allows comparison across datasets of different lengths and enables entropy calculation.

A well‑behaved K‑40 source produces a unimodal distribution centered around the mean CPM.


## 4. Fano Factor

The Fano factor quantifies deviations from ideal Poisson behavior:

**F = Variance / Mean**

Interpretation:

- **F ≈ 1** → ideal Poisson process  
- **F < 1** → sub‑Poisson (over‑regular, often due to smoothing or electronics)  
- **F > 1** → super‑Poisson (excess noise, environmental influence)
  
Note: For large datasets, the Fano factor should remain very close to 1.  
The expected statistical fluctuation is approximately:

Std(F) ≈ √(2 / N)

where N is the number of samples.  
Significant deviations from this range indicate non-Poisson behavior.




## 5. Entropy Estimation

Each decay event contributes physical randomness.  
The entropy per event is estimated using:

**H = − Σ p(i) · log₂(p(i))**

Where p(i) is the probability of observing count value i.

For a Poisson process, entropy increases with λ.

Entropy is computed from:

- CPM distribution  
- Normalized histogram  
- Probability mass function

---

## 6. Autocorrelation

Autocorrelation is used to detect temporal dependencies:

- **ACF ≈ 0** → events are independent  
- **ACF > 0** → correlation (e.g., environmental drift)  
- **ACF < 0** → anti‑correlation (rare in decay processes)

A valid radioactive randomness source must show **no significant autocorrelation**.

Note: Autocorrelation analysis is optional.  
Because CPM values are based on a 60‑second moving average, short‑lag autocorrelation (e.g., lag 1–59) is dominated by the smoothing window and does not reflect physical dependencies.  
Therefore, autocorrelation is not computed by default but may be applied to raw CPS data if available.


## 7. Verification Summary

A dataset is statistically valid if:

- Mean and variance match Poisson expectations  
- Fano factor is close to 1  
- Histogram shows a stable unimodal distribution  
- Entropy per event is consistent  
- No autocorrelation is present  
- No systematic drift is observed

---

# STATISTIK — Analyse der K‑40‑Zerfallsdaten

Dieses Dokument beschreibt die statistischen Methoden zur Analyse der durch Kalium‑40 (K‑40) erzeugten Zerfallsdaten.  
Ziel ist die Validierung der Zufälligkeit, Stabilität und Entropie der gemessenen Ereignisse.

---

## 1. Statistisches Modell

Radioaktiver Zerfall folgt einem Poisson‑Prozess.  
Für ein Zeitintervall gilt:

**P(k; λ) = (λ^k * e^(-λ)) / k!**

Dabei:  
- k = Anzahl der registrierten Ereignisse  
- λ = erwartete Ereigniszahl (mittlere Zählrate)

Kennzeichen eines Poisson‑Prozesses:

**Varianz = Mittelwert**

Dies dient als zentrales Prüfkriterium.

---

## 2. CPM und Ereignisstatistik

Das Messgerät liefert CPM (Counts per Minute) als gleitenden 60‑Sekunden‑Durchschnitt.  
Daraus ergeben sich:

- **Mittlere Zählrate:** λ = CPM  
- **Ereignisse pro Sekunde:** CPS = CPM / 60  
- **Erwartete Varianz:** Var = λ  
- **Standardabweichung:** σ = √λ

Diese Werte dienen zum Vergleich von Theorie und Messung.

---

## 3. Histogramm‑Analyse

Ein Histogramm der CPM‑Werte zeigt:

- die Verteilung der Messwerte
- Abweichungen vom Poisson‑Modell
- Stabilität des Messaufbaus
- systematische Drift oder Störungen

Das Histogramm wird in normalisierter Form ausgewertet (Summe aller Bin‑Wahrscheinlichkeiten = 1).  
Dies ermöglicht den Vergleich zwischen Datensätzen unterschiedlicher Länge und ist Voraussetzung für die Entropieberechnung.

Eine stabile K‑40‑Quelle erzeugt eine unimodale Verteilung um den Mittelwert.


## 4. Fano‑Faktor

Der Fano‑Faktor misst Abweichungen vom idealen Poisson‑Verhalten:

**F = Varianz / Mittelwert**

Interpretation:

- **F ≈ 1** → idealer Poisson‑Prozess  
- **F < 1** → sub‑Poisson (zu regelmäßige Werte, oft durch Glättung)  
- **F > 1** → super‑Poisson (zusätzliches Rauschen, Umwelteinflüsse)

Hinweis: Bei großen Datensätzen sollte der Fano-Faktor sehr nahe bei 1 liegen.  
Die erwartete statistische Schwankung beträgt näherungsweise:

Std(F) ≈ √(2 / N)

wobei N die Anzahl der Messwerte ist.  
Deutliche Abweichungen von diesem Bereich weisen auf ein nicht-poissonartiges Verhalten hin.


## 5. Entropie‑Schätzung

Jedes Zerfallsereignis trägt physikalische Zufälligkeit.  
Die Entropie pro Ereignis wird berechnet als:

**H = − Σ p(i) · log₂(p(i))**

wobei p(i) die Wahrscheinlichkeit für den Zählwert i ist.

Die Entropie steigt mit der mittleren Zählrate λ.

Berechnungsgrundlage:

- CPM‑Verteilung  
- Normalisiertes Histogramm  
- Wahrscheinlichkeitsverteilung

---

## 6. Autokorrelation

Autokorrelation dient zur Erkennung zeitlicher Abhängigkeiten:

- **ACF ≈ 0** → unabhängige Ereignisse  
- **ACF > 0** → Korrelation (z. B. Drift)  
- **ACF < 0** → Anti‑Korrelation (selten)

Eine gültige radioaktive Zufallsquelle zeigt **keine signifikante Autokorrelation**.

---

## 7. Zusammenfassung der Verifikation

Ein Datensatz gilt als statistisch valide, wenn:

- Mittelwert und Varianz dem Poisson‑Modell entsprechen  
- der Fano‑Faktor nahe 1 liegt  
- das Histogramm stabil und unimodal ist  
- die Entropie pro Ereignis konsistent ist  
- keine Autokorrelation vorliegt  
- keine systematische Drift erkennbar ist
