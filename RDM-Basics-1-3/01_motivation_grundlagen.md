# NFDI4ING RDM Basics for Engineers

**Teil 1 von 4: Grundlagen des Forschungsdatenmanagements fuer Ingenieurwissenschaften -- Motivation und Einfuehrung in die Grundlagen**

| | |
|---|---|
| **Datum** | 16.03.2026, online |
| **Autoren** | Mario Moser, Marcos Galdino, Tobias Hamann |
| **Affiliation** | Werkzeugmaschinenlabor WZL der RWTH Aachen University |
| **Task Area** | Training, Education & Standardisation (TA TES) |
| **Lizenz** | CC BY 4.0 |

---

## Kursplan / Course Schedule

| Teil | Thema | Datum | Uhrzeit |
|------|-------|-------|---------|
| 1 | Motivation und Grundlagen | 16.03.2026 | 17:00 |
| 2 | DMPs und Best Practices | 30.03.2026 | 17:00 |
| 3 | Metadaten und Semantik | 13.04.2026 | 17:00 |
| 4 | Software | 27.04.2026 | 17:00 |

---

## 1. Motivation

### 1.1 Gute wissenschaftliche Praxis & Nachvollziehbarkeit

Kernprinzipien:

- **Lege artis arbeiten** -- nach den Regeln der Kunst forschen
- **Gegenseitige Unterstuetzung** innerhalb der Forschungsgemeinschaft
- **Qualitaetssicherung bei Veroeffentlichungen**
- **Klare Rollen und Verantwortlichkeiten**
- **Nachvollziehbare Dokumentation** aller Forschungsprozesse

Die DFG stellt Leitlinien in einer dreistufigen Pyramide bereit:

1. **Leitlinien** (oberste Ebene)
2. **Erlaeuterungen**
3. **Detaillierte fachspezifische Ausfuehrungen** (unterste Ebene)

> Quelle: DFG Leitlinien zur Sicherung guter wissenschaftlicher Praxis

### 1.2 Daten nachnutzen

Die Wiederverwendung vorhandener Forschungsdaten eroeffnet neue Moeglichkeiten fuer die Forschung.

**Rechtliche und ethische Fragen:**
- Datenschutz
- Dateneigentum
- Zitierregeln

**Herausforderungen:**
- Datenaufbereitung
- Datenqualitaet
- Datenzugang
- Datenschutz
- Interoperabilitaet

### 1.3 Anforderungen von Forschungsfoerderern

- **DMP als Steuerungselement** -- Datenmanagementplaene werden zunehmend gefordert
- **Oeffentlichkeit der Ergebnisse** -- Forschungsergebnisse sollen zugaenglich sein
- **Zeitliche Fristen** fuer die Veroeffentlichung
- **Formale und inhaltliche Vorgaben**

**BMBF-Anforderungen im Detail:**
- Open Access fuer Publikationen
- Erstellung von Datenmanagementplaenen (DMPs)
- Einhaltung der FAIR-Datenstandards
- Verwendung persistenter Identifikatoren (DOI, EPIC-Handle, ARK, URN)

### 1.4 Vorbehalte und Loesungsansaetze

| Vorbehalt | Loesungsansatz |
|-----------|---------------|
| Mehraufwand | Effektive Datenverwaltung fuehrt zu Zeitersparnis |
| Datenschutzbedenken / Diebstahl | Datenschutzgesetz und Lizenzen; Veroeffentlichung unter Embargo |
| Personenbezogene Daten | Anonymisierung |
| Fehlendes Bewusstsein | Initiativen und Ansprechpartner |
| Fehlende Standardisierung | Orientierung an Vorgaben und Organisationen |
| Fehlendes Wissen | Trainingsangebote, Beispiele, Erfahrungen |
| "Arbeit fuer Andere" | Mehr Anreize fuer Data Sharing |

---

## 2. Grundlagen

### 2.1 FAIR Prinzipien

Die FAIR-Prinzipien definieren, wie Forschungsdaten beschaffen sein sollen:

- **F** -- Findable (Auffindbar)
- **A** -- Accessible (Zugaenglich)
- **I** -- Interoperable (Interoperabel)
- **R** -- Reusable (Wiederverwendbar)

Insgesamt umfassen die FAIR-Prinzipien **15 Einzelprinzipien**.

**Wichtig:** FAIR != Open Data. Daten koennen FAIR sein, ohne offen zugaenglich zu sein.

> Quelle: Wilkinson et al. 2016, *Scientific Data* 3, 160018

### 2.2 Persistente Identifikatoren (PIDs)

Eigenschaften guter Identifikatoren:
- **Eindeutig** -- genau einem Objekt zugeordnet
- **Dauerhaft** -- langfristig gueltig
- **Kuenstlich / Nicht-sprechend** -- keine inhaltliche Bedeutung
- **Kurz** -- kompakt und handhabbar

**Beispiele:** ISBN, DOI, ORCID

#### Vergleich von Identifikator-Eigenschaften

| Eigenschaft | Name | Detaillierte Beschreibung | Author-ID (z.B. ORCID) |
|-------------|------|--------------------------|------------------------|
| Eindeutig | Nein (Namensvettern) | Ja | Ja |
| Persistent | Nein (Namensaenderung) | Nein (Adressaenderung) | Ja |
| Nicht-sprechend | Nein | Nein | Ja |
| Kurz | Ja | Nein | Ja |

### 2.3 Datenlebenszyklus (DLC)

Der Datenlebenszyklus besteht aus **6 Phasen**, die zyklisch durchlaufen werden:

```
Planen -> Erheben -> Analysieren -> Teilen -> Archivieren -> Nachnutzen
   ^                                                            |
   |____________________________________________________________|
```

### 2.4 Datenmanagementplan (DMP)

Ein DMP ist ein Dokument zur **Vorausplanung**, das den Umgang mit Forschungsdaten festlegt. Er ist gueltig **waehrend und nach der Projektlaufzeit** und sollte domainspezifische Fragebogen enthalten.

#### 8 uebliche Bestandteile eines DMP

1. Projektbeschreibung
2. Datenbestand
3. Umfang und Art
4. Datenorganisation / Workflow
5. Administrative und rechtliche Aspekte
6. Archivierung / Datenaustausch / Publikation
7. Verantwortliche und Pflichten
8. Kosten und Ressourcen

#### Ressourcen fuer DMPs

- **Beispiel-DMPs** vom Digital Curation Centre (DCC)
- **Data Management Plan Catalogue** von LIBER
- **Anleitung und Muster-DMP** der HU Berlin
- **RDMO** -- vereinfachtes, toolgestuetztes Erstellen von DMPs

### 2.5 FDM Policy RWTH Aachen

Die RWTH Aachen hat eine eigene Leitlinie zum Forschungsdatenmanagement, verabschiedet am **8. Maerz 2016**.

**Verfuegbare Tools an der RWTH:**
- GitLab
- RDMO
- Coscine
- RWTH Publications

### 2.6 Lizenzen

**Grundbegriffe:**
- **Urheberrecht** -- automatischer Schutz des geistigen Eigentums
- **Nutzungsrecht** -- durch Lizenzen geregelte Verwendungserlaubnis

**Creative Commons Bausteine:**

| Kuerzel | Bedeutung |
|---------|-----------|
| BY | Namensnennung (Attribution) |
| SA | Weitergabe unter gleichen Bedingungen (Share Alike) |
| NC | Nicht-kommerziell (Non-Commercial) |
| ND | Keine Bearbeitung (No Derivatives) |
| 0 | Public Domain / Kein Copyright |

**Weitere Lizenzen:**
- **MIT License** -- permissive Softwarelizenz
- **GNU GPL 3** -- Copyleft-Softwarelizenz

### 2.7 Repositorien

Ein Repositorium ist eine **verwaltete Datenbank mit digitalen Inhalten**, die Such- und Zugriffsmethoden bietet und persistente Identifikatoren (PIDs) vergibt.

**Typen von Repositorien:**
- **Institutionell** -- von einer Einrichtung betrieben
- **Generisch** -- fachuebergreifend
- **Fachspezifisch** -- auf ein bestimmtes Fachgebiet zugeschnitten

**Beispiele:** Zenodo, Dryad, FIGSHARE, CORDIS

### 2.8 Repositorien-Suchmaschinen

- **re3data.org** -- Registry of Research Data Repositories
- **fairsharing.org** -- Standards, Datenbanken und Richtlinien
- **NFDI4ING Storage Offers**
- **NFDI4ING Data Collections Explorer**

### 2.9 Software Repositorien

- GitLab
- GitHub
- Debian
- PyPI
- winget.run

### 2.10 Electronic Laboratory Notebooks (ELN)

- **eLabFTW** -- Open-Source-Loesung fuer elektronische Laborbuecher

### 2.11 Laboratory Management Information Systems (LMIS)

Systeme zur Verwaltung von Laborprozessen und -daten.

---

## 3. Ingenieurspezifische Herausforderungen im FDM

### 3.1 Vielfaeltigkeit der Daten

Die Ingenieurwissenschaften umfassen **41-45 Teildisziplinen**, was zu enormer Heterogenitaet fuehrt in:

- Schemata
- Speicherung
- Uebertragung
- Formate
- Datenentstehung

### 3.2 NFDI4ING Funktionalstruktur (Stand: Oktober 2025)

**Uebergreifende Loesungen:**
- TES (Training, Education & Standardisation)
- SKG (Scientific Knowledge Graphs)
- FIS (Forschungsinformationssysteme)
- Copilot
- ing.grid

**Archetypes (Musterforschende):**

| Archetype | Schwerpunkt |
|-----------|------------|
| **Alex** | Bespoke experiments (massgeschneiderte Experimente) |
| **Betty** | Engineering research software |
| **Caden** | Provenance tracking of samples (Rueckverfolgung von Proben) |
| **Doris** | High Performance Computing (HPC) |
| **Ellen** | Simulations & heterogeneous data |
| **Fiona** | Data re-use, combination & enrichment |

**Forschungsdisziplinen:** 41-45 ingenieurwissenschaftliche Teildisziplinen

### 3.3 Zentrale Herausforderungen

**Grosse Heterogenitaet in:**
- Themenfeldern
- Datenarten
- Datengroessen
- Datenherkunft
- Alterung von Daten
- Verteilung von Daten

**Weitere Herausforderungen:**
- **Anforderungen von Unternehmen** -- Geheimhaltungspflicht
- **Personenbezogene Daten** -- Datenschutzanforderungen
- **Interdisziplinaritaet** -- Zusammenarbeit ueber Fachgrenzen hinweg

**Datenherkunft (Data Origins):**
- Experiment
- Simulation
- Befragung / Beobachtung
- Programmierung

---

## 4. How to FDM?

### 4.1 Das FDM-Spektrum

```
Kein FDM ---------> Schlechtes FDM ---------> Gutes FDM
```

**Schlechtes FDM (Einstieg):**
- Code versionieren
- Phasen des Datenlebenszyklus befolgen
- Daten zugaenglich machen

**Gutes FDM (Ziel):**
- Richtlinien und Leitlinien nutzen
- Geeignete Tools einsetzen
- DMP erstellen
- Metadaten verwenden
- Daten archivieren und publizieren
- FDM an eigene Beduerfnisse anpassen
- Trainingsangebote wahrnehmen

### 4.2 FDM an der RWTH Aachen

- FDM-Richtlinie der RWTH befolgen
- UB-Trainings nutzen
- FDM-Teams konsultieren
- Tools einsetzen: RDMO, Coscine, GitLab, RWTH Publications

### 4.3 Entlang des Datenlebenszyklus

| Phase | Aktivitaeten |
|-------|-------------|
| **Planen** | Planung & Dokumentation |
| **Erheben** | Nachvollziehbare Erhebung und Analyse; bestehende Tools nutzen |
| **Analysieren** | Speicherplatzbedarf und -optionen klaeren |
| **Teilen** | Daten teilen und zugaenglich machen |
| **Archivieren** | Langfristige Sicherung der Daten |
| **Nachnutzen** | Evtl. auch selbst nachnutzen |

---

## 5. Tools und Services entlang des DLC

### 5.1 User Story: Prepare for Research

Ablauf / Flow:

```
NFDI4ING Website -> RDM Training -> Data Collections Explorer -> RDMO -> Knowledge Base
```

### 5.2 User Story: Metadata

Ablauf / Flow:

```
Terminology Service -> Metadata Profile Service -> Metadata Hub -> Coscine -> FAIR DO
```

### 5.3 RDMO (Research Data Management Organiser)

- Werkzeug zur Erstellung von Datenmanagementplaenen
- Urspruenglich ein DFG-Projekt
- Seit 2020 Community-Projekt
- Web-Applikation
- Verschiedene Instanzen, darunter NFDI4ING: **rdmo.nfdi4ing.de**

### 5.4 Basic RDM Trainings

- **URL:** education.nfdi4ing.de
- Modularer Aufbau
- Selbstlernmaterialien

### 5.5 Data Collections Explorer

- **URL:** https://data-collections.nfdi4ing.de/
- Suche und Exploration von Datensammlungen

### 5.6 Betty's (Re)Search Engine

- Suche nach Software-Repositorien
- Verknuepfte Software- und Textpublikationen

### 5.7 GitLab

- Webbasierte Versionsverwaltung
- DevSecOps-Plattform
- **RWTH-Instanz:** git.rwth-aachen.de

### 5.8 Jupyter Service

- Programmierumgebung mit Rechenressourcen
- Unterstuetzte Sprachen: Python, Julia, R
- **URL:** jupyter.nfdi4ing.de

### 5.9 Terminology Service

- Suche nach existierenden Begriffen und Terminologien
- **URL:** terminology.nfdi4ing.de/ts/

### 5.10 AIMS Metadata Profile Service

- Modulare Metadatenprofile
- **URL:** profiles.nfdi4ing.de

### 5.11 Kadi4Mat

- Forschungsdatenmanagement-Plattform

### 5.12 Coscine (Collaborative Scientific Integration Environment)

- Archivierung, Speicherung, Metadaten
- Schwerpunkt NRW
- **URL:** coscine.rwth-aachen.de

### 5.13 ing.grid

- Diamond Open Access Journal
- Open Access, Open Peer Review, Open Data & Code
- **URL:** inggrid.org

---

## 6. FDM anhand eines beispielhaften Datensatzes

### 6.1 Anwendungsfall (Use Case)

**Szenario:** Zwei industrielle Bohrmaschinen im 24/7-Betrieb mit Mehrschichtsystem.

**Sensordaten:**
- Umgebungstemperatur
- Prozesstemperatur
- Drehzahl
- Drehmoment

**Ziel:** Datengetriebenes Condition Monitoring und Prozessanalyse

**Datensatz:** https://git.rwth-aachen.de/nfdi4ing/education/exampledatasets/drillprocess-timeseries-machinelearning/-/tree/main/data

### 6.2 Forschungsvorhaben planen (7 Schritte)

1. **Zieldefinition** -- Was soll erreicht werden?
2. **Fragestellungen** -- Welche Forschungsfragen leiten sich ab?
3. **Datenanforderungen** -- Welche Daten werden benoetigt?
4. **Datenerfassung** -- Wie werden die Daten erhoben?
5. **Infrastruktur** -- Welche technische Infrastruktur ist noetig?
6. **Qualitaetsplan** -- Wie wird die Datenqualitaet gesichert?
7. **Ressourcenplanung** -- Welche Ressourcen stehen zur Verfuegung?

### 6.3 Datenerhebung

Systematische, reproduzierbare und qualitaetsgesicherte Erfassung von Rohdaten aus definierten Quellen.

### 6.4 Data Pipeline

```
Kollektion / Akquisition
        |
        v
Bereinigung / Transformation / Integration
        |
        v
Repraesentation (Merkmalsextraktion)
        |
        v
Modellierung / "Interpretation"
        |
        v
Visualisierung
```

### 6.5 Quo vadis -- Offene Fragen zum Datensatz

Fehlende Informationen, die fuer gutes FDM noetig waeren:
- Wer hat gemessen?
- Welche Einheiten?
- Welche Messtechnik?
- Keine Lizenz angegeben
- Kein Identifikator vorhanden
- Datenqualitaet unklar

---

## 7. Initiativen und Ansprechpartner

### 7.1 Initiativen

| Initiative | Seit | Beschreibung |
|-----------|------|-------------|
| **NFDI4ING** | 2017 | Konsortium mit Fokus auf ingenieurwissenschaftliche Forschungsdaten |
| **NFDI** | -- | Nationale ForschungsDaten Infrastruktur; Netzwerk von Konsortien |
| **OpenAIRE** | 2008 | Support-Strukturen, Interoperabilitaet, Open Science |
| **Research Data Alliance (RDA)** | 2013 | Standards und Richtlinien fuer Daten-Interoperabilitaet |
| **European Open Science Cloud (EOSC)** | 2015 | "Web of FAIR Data and Services"; eosc-portal.eu |

### 7.2 Kontakt

- **E-Mail:** contact@nfdi4ing.de
- **Helpdesk:** nfdi4ing.de/helpdesk
- **Services:** nfdi4ing.de/services
- **Direkt:** Mario.Moser@wzl-iqs.rwth-aachen.de
