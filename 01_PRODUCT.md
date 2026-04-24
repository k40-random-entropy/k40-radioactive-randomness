# PRODUCT

## Offering

Users receive physically generated integer random numbers derived from the radioactive decay of potassium‑40.  
These random numbers are not simulated or algorithmically produced; they are entirely based on real physical measurement data.

Two product types are available:

1. User‑specific physical random numbers  
   A unique sequence of integer random values is generated exclusively for the user based on a dedicated measurement.

2. Random numbers matching a specified entropy level  
   A dataset of physical random numbers is delivered whose statistical entropy reaches or exceeds the requested value.

## What users can receive

- A defined set of physically generated integer random values  
- Random numbers with a guaranteed minimum entropy  
- A complete statistical analysis of the measurement series  
- A signed certificate of analysis documenting methods, results, and Poisson compatibility

## What users receive

Each delivery includes:

- A file containing physically generated integer random numbers  
- A statistical evaluation consisting of:
  - Poisson compatibility assessment  
  - Variance and Fano‑factor analysis  
  - Overdispersion Z‑score  
  - Entropy estimation  
  - Per‑value deviation metrics  
- Machine‑readable result files (CSV or JSON) included as part of the delivery  
- A signed certificate of analysis suitable for documentation, audits, and trust verification
  
The data may not be shared with third parties without the explicit consent of the provider.

## User use cases

The delivered data can be used for:

- Cryptographic applications  
- Randomness injection into software systems  
- Scientific simulations  
- Quality assessment of radioactive sources  
- Auditable documentation  
- Research and education

## Technical approach (high‑level)

The generation of random numbers is performed through:

1. Measurement of a CPM time series from a potassium source  
2. Validation of the measurement  
3. Statistical analysis of the time series  
4. Extraction or selection of integer random values according to user requirements  
5. Delivery of the results in the corresponding format together with documentation

## Repository structure

- 00_DESCRIPTION.md — Description of the offering  
- 01_PRODUCT.md — Product definition  
- 02_SETUP.md — Measurement procedure  
- 03_STATISTICS.md — Statistical methods  
- 04_VERIFY.md — Source validation logic  
- /data/raw/ — Input datasets  
- /data/results/ — Output datasets



# PRODUCT (Deutsch)

## Angebot

Nutzer erhalten physikalisch erzeugte ganzzahlige Zufallszahlen, die aus dem radioaktiven Zerfall von Kalium‑40 gewonnen werden.  
Die Zufallszahlen werden nicht simuliert oder algorithmisch erzeugt, sondern basieren vollständig auf realen physikalischen Messdaten.

Es stehen zwei Produktvarianten zur Verfügung:

1. Nutzerindividuell erzeugte physikalische Zufallszahlen  
   Eine exklusive Folge ganzzahliger Zufallswerte wird für den Nutzer aus einer eigenen Messreihe erzeugt.

2. Zufallszahlen mit definierter Entropie  
   Es wird eine Menge physikalischer Zufallszahlen geliefert, deren statistische Entropie einen vorgegebenen Wert mindestens erreicht oder übertrifft.

## Was Nutzer erhalten können

- Eine definierte Menge physikalisch erzeugter ganzzahliger Zufallswerte  
- Zufallszahlen mit garantierter Mindestentropie  
- Eine vollständige statistische Analyse der Messreihe  
- Ein signiertes Analysezertifikat, das Methoden, Ergebnisse und Poisson‑Kompatibilität dokumentiert

## Was Nutzer erhalten

Jede Lieferung enthält:

- Eine Datei mit physikalisch erzeugten ganzzahligen Zufallszahlen  
- Eine statistische Auswertung bestehend aus:
  - Poisson‑Kompatibilitätsprüfung  
  - Varianz‑ und Fano‑Faktor‑Analyse  
  - Overdispersion‑Z‑Score  
  - Entropie‑Abschätzung  
  - Abweichungsanalyse pro Messpunkt  
- Maschinenlesbare Ergebnisdateien (CSV oder JSON) als Bestandteil der Lieferung  
- Ein signiertes Analysezertifikat, das für Dokumentation, Audits und Vertrauensnachweise verwendet werden kann

Die Weitergabe der Daten an Dritte ist ohne ausdrückliche Zustimmung des Lieferanten nicht gestattet.

## Einsatzmöglichkeiten

Die gelieferten Daten können verwendet werden für:

- Kryptographische Anwendungen  
- Zufallsquellen in Softwaresystemen  
- Wissenschaftliche Simulationen  
- Qualitätsprüfung radioaktiver Quellen  
- Auditierbare Dokumentation  
- Forschung und Lehre

## Technischer Ansatz (High‑Level)

Die Erzeugung der Zufallszahlen erfolgt durch:

1. Messung einer CPM‑Zeitreihe einer Kaliumquelle  
2. Validierung der Messdaten  
3. Statistische Analyse der Zeitreihe  
4. Ableitung oder Auswahl ganzzahliger Zufallswerte entsprechend der Nutzeranforderung  
5. Bereitstellung der Ergebnisse im entsprechenden Format zusammen mit Dokumentation

## Repository‑Struktur

- 00_DESCRIPTION.md — Beschreibung des Angebots  
- 01_PRODUCT.md — Produktdefinition  
- 02_SETUP.md — Messaufbau  
- 03_STATISTICS.md — Statistische Methoden  
- 04_VERIFY.md — Quellenvalidierung  
- /data/raw/ — Eingabedaten  
- /data/results/ — Ausgabedaten
