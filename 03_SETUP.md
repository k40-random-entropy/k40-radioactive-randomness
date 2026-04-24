# SETUP

## Measurement Setup

This document describes the physical measurement setup used to generate integer random numbers from the radioactive decay of potassium‑40.  
The procedure ensures reproducibility, transparency, and consistent data quality.

## Required Components

- A Geiger counter capable of measuring CPM (counts per minute)  
- A stable potassium‑40 source (e.g., potassium chloride or potassium carbonate)  
- A fixed measurement distance between detector and source  
- A stable, low‑noise environment without movement or shielding changes  
- A computer for recording and exporting the CPM time series

## Physical Arrangement

1. The potassium‑40 source is placed at a fixed, reproducible distance from the Geiger counter.  
2. The detector is positioned so that neither angle nor distance change during the measurement.  
3. The environment remains undisturbed throughout the entire measurement period.  
4. No additional shielding, objects, or materials are introduced or removed during the measurement.

## Device Configuration

- The Geiger counter is set to record CPM values in fixed time intervals.  
- The measurement duration is chosen to ensure statistically meaningful data.  
- All automatic filtering, smoothing, or correction functions are disabled if present.

## Measurement Procedure

1. The detector is powered on and allowed to stabilize.  
2. The potassium‑40 source is placed in the defined position.  
3. The CPM time series is recorded over the full measurement duration.  
4. The measurement may include planned interruptions for saving and restarting the recording software.  
   These interruptions do not affect the statistical validity of the CPM time series  
   as long as the physical setup (detector position, source position, distance, shielding) remains unchanged.  
   Any change in the physical setup would become immediately visible in the Poisson distribution.  
5. After completion, the CPM data is exported in raw numerical form.

## Data Export

The measurement device must export:

- a time‑ordered CPM series  
- without modification, smoothing, or post‑processing  
- in a machine‑readable format (CSV or equivalent)

The exported data serves as the basis for statistical analysis and random number extraction.

## Output Provided to Users

After processing, users receive:

- physically generated integer random numbers  
- statistical evaluation of the measurement  
- a signed certificate of analysis  
- machine‑readable result files (CSV or JSON)

All results correspond to the measurement performed with the setup described above.



# SETUP (Deutsch)

## Messaufbau

Dieses Dokument beschreibt den physikalischen Messaufbau zur Erzeugung ganzzahliger Zufallszahlen aus dem radioaktiven Zerfall von Kalium‑40.  
Das Verfahren stellt Reproduzierbarkeit, Transparenz und gleichbleibende Datenqualität sicher.

## Benötigte Komponenten

- Ein Geigerzähler, der CPM‑Werte (Counts per Minute) erfassen kann  
- Eine stabile Kalium‑40‑Quelle (z. B. Kaliumchlorid oder Kaliumcarbonat)  
- Ein fester Messabstand zwischen Detektor und Quelle  
- Eine ruhige Umgebung ohne Bewegung oder Veränderung der Abschirmung  
- Ein Computer zur Aufzeichnung und zum Export der CPM‑Zeitreihe

## Physische Anordnung

1. Die Kalium‑40‑Quelle wird in einem festen, reproduzierbaren Abstand zum Geigerzähler platziert.  
2. Der Detektor wird so positioniert, dass sich weder Winkel noch Abstand während der Messung verändern.  
3. Die Umgebung bleibt während der gesamten Messdauer unverändert.  
4. Es werden keine zusätzlichen Gegenstände oder Materialien hinzugefügt oder entfernt.

## Gerätekonfiguration

- Der Geigerzähler wird so eingestellt, dass er CPM‑Werte in festen Zeitintervallen aufzeichnet.  
- Die Messdauer wird so gewählt, dass statistisch aussagekräftige Daten entstehen.  
- Automatische Filter‑, Glättungs‑ oder Korrekturfunktionen werden deaktiviert, sofern vorhanden.

## Messablauf

1. Der Detektor wird eingeschaltet und stabilisiert sich.  
2. Die Kalium‑40‑Quelle wird in die definierte Position gebracht.  
3. Die CPM‑Zeitreihe wird über die gesamte Messdauer aufgezeichnet.  
4. Die Messung kann geplante Unterbrechungen zum Speichern und Neustarten der Aufzeichnungssoftware enthalten.  
   Diese Unterbrechungen beeinträchtigen die statistische Gültigkeit der CPM‑Zeitreihe nicht,  
   solange der physische Aufbau (Detektorposition, Quellenposition, Abstand, Abschirmung) unverändert bleibt.  
   Änderungen am Aufbau würden sich unmittelbar in der Poisson‑Verteilung bemerkbar machen.  
5. Nach Abschluss wird die CPM‑Zeitreihe unverändert exportiert.

## Datenexport

Das Messgerät muss exportieren:

- eine zeitlich geordnete CPM‑Serie  
- ohne Modifikation, Glättung oder Nachbearbeitung  
- in einem maschinenlesbaren Format (CSV oder gleichwertig)

Die exportierten Daten bilden die Grundlage für die statistische Analyse und die Ableitung der Zufallszahlen.

## Bereitgestellte Ergebnisse

Nach der Verarbeitung erhalten Nutzer:

- physikalisch erzeugte ganzzahlige Zufallszahlen  
- eine statistische Auswertung der Messreihe  
- ein signiertes Analysezertifikat  
- maschinenlesbare Ergebnisdateien (CSV oder JSON)

Alle Ergebnisse entsprechen der Messung, die mit dem oben beschriebenen Aufbau durchgeführt wurde.
