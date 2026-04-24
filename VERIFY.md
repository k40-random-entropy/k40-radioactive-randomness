# VERIFY — Reproduzierbare Verifikation der Messdaten

Dieses Dokument beschreibt, wie jede Messung, jeder Datensatz und jede Entropieanalyse dieses Projekts reproduzierbar verifiziert werden kann.<br>Ziel ist es, eine transparente, nachvollziehbare und auditierbare Grundlage für alle Ergebnisse zu schaffen.

---

## 1. Physikalische Grundlage

Die Messungen basieren auf dem radioaktiven Zerfall von Kalium‑40 (K‑40), insbesondere den Betazerfällen, die durch einen Geigerzähler registriert werden. Jeder registrierte Impuls wird als diskretes physikalisches Ereignis behandelt.

---

## 2. Messaufbau

- Geigerzähler: SBM‑20 oder vergleichbarer Zählrohrtyp  
- Abstand Quelle–Zählrohr: 0–5 cm  
- Quellen: KCl, Pottasche, Haushaltsprodukte mit Kaliumanteil  
- Messdauer pro Intervall: 60 s  
- Erfassung: CPM (Counts per Minute)

---

## 3. Datenstruktur

Jeder Datensatz enthält:

- Zeitstempel  
- CPM‑Wert  
- Rohzählungen  
- Quelle / Material  
- Messdauer  
- Setup‑Parameter

---

## 4. Statistische Verifikation

Zur Überprüfung der Messdaten werden folgende Methoden verwendet:

- Poisson‑Verteilung der Zählraten  
- Varianz‑Analyse  
- Histogramm der Ereignisverteilung  
- Entropieberechnung aus diskreten Ereignissen  
- Vergleich mit theoretischen Erwartungswerten

---

## 5. Reproduzierbarkeit

Eine Messung gilt als reproduzierbar, wenn:

- die CPM‑Werte innerhalb ±10 % der Referenz liegen  
- die Varianz mit der Poisson‑Erwartung übereinstimmt  
- die Entropie pro Ereignis stabil bleibt  
- keine systematischen Abweichungen auftreten

---

## 6. Audit‑Checkliste

- [ ] Messaufbau dokumentiert  
- [ ] Quelle eindeutig benannt  
- [ ] Rohdaten vollständig vorhanden  
- [ ] Statistische Analyse durchgeführt  
- [ ] Entropiewerte nachvollziehbar  
- [ ] Ergebnisse replizierbar

---

# English Version

## VERIFY — Reproducible Verification of Measurement Data

This document describes how each measurement, dataset, and entropy analysis in this project can be reproduced and verified. The goal is to provide a transparent, auditable foundation for all results.

(Die englischen Abschnitte entsprechen inhaltlich den deutschen und werden bei Bedarf erweitert.)
