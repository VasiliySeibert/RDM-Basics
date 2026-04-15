# NFDI4ING RDM Basics for Engineers -- Teil 3: Metadata & Semantics

| | |
|---|---|
| **Kurs** | NFDI4ING RDM Basics for Engineers |
| **Teil** | 3 von 4: Metadata & Semantics |
| **Datum** | 13.04.2026, online |
| **Autoren** | Dorothea Iglezakis (Universitaet Stuttgart), Felix Engels (Technische Informationsbibliothek TIB) |
| **Lizenz** | CC BY 4.0 |

---

## Agenda

1. Datendokumentation -- Warum?
2. Veroeffentlichen und Suchen von Daten
3. Metadatenstandards
4. Lokales Datenmanagement

---

## 1. Datendokumentation -- Warum?

> "Wouldn't it be great if we would be able to combine any dataset with any other dataset we would want to?"
> -- EOSC Strategic Implementation Plan, p. 4

Die zentrale Idee: Daten **finden**, **verstehen**, **nutzen** und **kombinieren**.

- Die meisten Daten sind ohne Beschreibung nicht nutzbar.
- Informationen werden mit der Zeit vergessen -- Dokumentation ermoeglicht langfristiges Verstaendnis (vgl. Michener et al. 1997: Informationsgehalt nimmt ueber die Zeit ab).
- Dokumentation ist das wesentliche Element guten Datenmanagements und erleichtert den Datenaustausch.

### FAIR Data -- Wiederholung

| Prinzip | Beschreibung |
|---|---|
| **F**indable | Persistenter Identifier (z. B. DOI) |
| **A**ccessible | Offene Protokolle, Authentifizierung und Autorisierung |
| **I**nteroperable | Standardisierte Formate und Vokabulare |
| **R**eusable | Lizenz und Provenienz dokumentiert |

---

## 2. Veroeffentlichen und Suchen von Daten

### Uebung: Informationen fuer die Datendokumentation sammeln

- Welche Informationen wuerde man bei der Suche nach Daten erwarten?
- Welche Informationen braucht man, um Daten zu verstehen?
- Welche Informationen braucht man, um Daten zu nutzen?

### FDM anhand eines beispielhaften Datensatzes

- **Anwendungsfall:** Zwei industrielle Bohrmaschinen im 24/7-Betrieb, Mehrschichtsystem
- **Sensordaten:** Umgebungstemperatur, Prozesstemperatur, Drehzahl, Drehmoment
- **Ziel:** Datengetriebenes Condition Monitoring und Prozessanalyse

### Datenrepositorien fuer FAIR Data

- **PIDs:** DOI fuer veroeffentlichte Daten, Handles fuer unveroeffentlichte Daten
- Daten und Metadaten zugaenglich mit Authentifizierung/Autorisierung
- Standardisierte Metadaten ueber Such-Indizes
- Unterstuetzung fuer domainspezifische Metadatenstandards oder individuelle Profile
- Standardisierte Lizenzvergabe

### Beispiel: TU datalib

Institutionelles Repositorium mit folgenden Feldern:

- Files
- Description
- Keywords
- Identifier
- DFG-Fach
- Fachbereich
- License (z. B. CC BY 4.0)

### Finden von Daten -- data.nfdi4ing.de

Zentrale Datenindizes aggregieren Metadaten aus verschiedenen Repositorien.

| Suchplattform | URL |
|---|---|
| NFDI4ING Data | data.nfdi4ing.de |
| B2FIND | b2find.eudat.eu |
| OpenAIRE Explore | explore.openaire.eu |
| Google Dataset Search | datasetsearch.research.google.com |

### Wo veroeffentlichen?

**Vision:** NFDI und EOSC

| Typ | Beispiele |
|---|---|
| Generalistisch | Zenodo, PANGAEA |
| Disziplinaer | TORE |
| Institutionell | RWTH Publications, DaRUS, TU Datalib |
| Weitere | RADAR4ING, B2Share (coming soon) |

- Eine gemeinsame Sprache ist noetig fuer das Auffinden (FAIR) und Beschreiben (FAIR) von Daten.
- **re3data.org** hilft, passende Repositorien zu finden.

---

## 3. Metadatenstandards

### Was definieren Metadatenstandards?

- Welche Felder zur Beschreibung verfuegbar sind
- Welche Art von Daten in die Felder eingetragen werden kann
- Wie oft ein Feld vorkommen darf
- Ob ein Feld ausgefuellt werden **muss**, **sollte** oder **kann**

**Sie ermoeglichen:** Datensuche und Datenaustausch

**Beispiele:** DataCite, CodeMeta, AVM

**Kataloge:**

- FAIRsharing.org
- RDA Metadata Standards Catalog (rdamsc.bath.ac.uk)

### DataCite als allgemeines Metadatenschema

| Kategorie | Feld | Pflicht |
|---|---|---|
| **Identifikation** | Identifier | Mandatory |
| | AlternateIdentifier | Recommended |
| | Version | Recommended |
| | PublicationYear | Mandatory |
| | Date | Recommended |
| **Beschreibung** | Title | Mandatory |
| | Description | Recommended |
| | Subject | Recommended |
| | Language | Optional |
| | GeoLocation | Optional |
| **Verbindungen** | RelatedIdentifier | Recommended |
| | RelatedItem | Optional |
| | FundingReference | Optional |
| | Creator | Mandatory |
| | Publisher | Mandatory |
| | Contributor | Recommended |
| **Technische Informationen** | ResourceType | Mandatory |
| | Size | Optional |
| | Format | Optional |
| **Nutzung und Rechte** | Rights | Recommended |

### PIDs und ihre Metadaten -- Content Negotiation

Eine DOI (z. B. `doi:10.5281/zenodo.17455425`) kann je nach `Accept`-Header in verschiedenen Formaten zurueckgegeben werden:

| Accept-Header | Ergebnis |
|---|---|
| `text/html` | Webseite |
| `text/x-bibliography; style=apa` | Zitation (APA-Format) |
| `application/vnd.datacite.datacite+json` | Vollstaendige JSON-Metadaten |

### Uebung: Verarbeitung von Metadaten

- Jupyter Service nutzen: **jupyter.nfdi4ing.de**
- Notebook: `DataCite.ipynb`
- Experimentieren mit verschiedenen Datensaetzen, Personen und Institutionen
- Weitergehende Ressourcen: Library Carpentry (OpenRefine), Software Carpentry (Python)

### Metadaten fuer Menschen -- Titel und Beschreibung

**Titel** und **Beschreibung** sind die beiden wichtigsten Metadatenfelder fuer Menschen (und LLMs).

**Titelformat:**

- `"<Datentyp> for <Grund der Erhebung>"`
- `"<Datentyp> of <Forschungsgegenstand>"`

**Die Beschreibung sollte enthalten:**

- Datentyp
- Zugrunde liegende Fragestellung
- Datenstruktur
- Abkuerzungen
- Notwendige Schritte zur Nutzung

### Was Datenrepositorien nicht von alleine tun

Uebungen mit echten Datensaetzen:

- Wissen Sie, um welche Art von Daten es sich handelt?
- Wie wurden sie erhoben/verarbeitet?
- Vertrauen Sie den Daten?
- Koennen Sie sie nutzen?

---

## 4. Lokales Datenmanagement

### Verknuepfung von Daten und Metadaten

Es gibt sechs grundlegende Muster:

| Nr. | Muster | Beispiele |
|---|---|---|
| 1 | Metadaten **bei** den Daten | Readme-Datei, Metadaten neben den Daten |
| 2 | Metadaten **in** den Daten | Datei-Header (z. B. HDF5) |
| 3 | Metadaten **an** den Daten | Object-Storage, Datei-/Ordnernamen |
| 4 | Metadaten **mit** Daten verpackt | RO-Crate, BagIt |
| 5 | Metadaten-DB **mit Link** zu den Daten | Such-Index, Repositorium, ELN |
| 6 | Persistente Identifier | DOI, EPIC, PID |

### Metadaten in den Dateien

Beispiele fuer eingebettete Metadaten:

- **NetCDF-Dateien:** Dimensions, Coordinates, Data Variables, Attributes
- **PDF-Dokumente:** Properties (Autor, Titel etc.)
- **Bilddateien:** EXIF-Daten

### Datei- und Ordnerbenennungen

Konsistente Benennung hilft:

- Informative Metadaten an Dateien zu binden
- Die Suche zu erleichtern
- Die automatisierte Verarbeitung zu verbessern
- Den Datenaustausch zu vereinfachen

**Maschinenlesbarkeit:**

- Keine Leerzeichen
- Keine Sonderzeichen
- `_` zwischen Metadaten-Einheiten
- `-` zwischen Woertern

**Menschenlesbarkeit:**

- Beschreibende Namen statt kryptischer Kuerzel

**Standardisierte Sortierung:**

- Datumsformat: `YYYY-MM-DD`
- Zahlen am Anfang
- Nullen auffuellen (z. B. `01`, `02`, ...)

### Prinzipien bei der Organisation von Ordnern

| Bereich | Beschreibung | Eigenschaften |
|---|---|---|
| **Input** | Rohdaten | Schreibgeschuetzt |
| **Verarbeitung** | Zwischenergebnisse | Automatisiert, versionskontrolliert, inhaltlich organisiert |
| **Output** | Finale Ergebnisse | Nach Projektstruktur organisiert, versioniert |

### Beispiel: Einfacher Berechnungs-Workflow

```
project/
├── CITATION
├── README
├── LICENSE
├── requirements.txt
├── data/
├── doc/
├── results/
└── src/
```

### Beispiel: Komplexes Projekt

```
project/
├── 01_project_management/
├── 02_material_and_methods/
├── 03_data/
├── 04_data_analysis/
├── 05_figures/
├── 06_disseminations/
├── 07_misc/
├── datacite.yml
├── LICENSE-CC-BY
└── README.md
```

### Metadaten bei den Daten

Metadaten koennen als separate Dateien (YAML, JSON(-LD), XML) neben den Daten gespeichert werden.

### Metadaten auf verschiedenen Ebenen

**Projektebene** (`metadata.yml`):

```yaml
project-name: "..."
task-area: "..."
grant-info: "..."
contact: "..."
```

**Studienebene** (`metadata.yml`):

```yaml
methods: "..."
instruments: "..."
computing-environment: "..."
```

**Datenebene** (`metadata.yml`):

```yaml
variables-measured: "..."
variables-controlled: "..."
parameters:
  - name: "..."
    value: "..."
    unit: "..."
```

**Provenienz-Tracking:** Beziehungen zwischen Rohdaten, verarbeiteten Daten und analysierten Daten (input-of-Beziehungen).

### Beispiel: Citation File Format (CFF)

YAML-basierte Datei (`CITATION.cff`) mit Informationen ueber Forschungssoftware:

```yaml
cff-version: 1.2.0
message: "If you use this software, please cite it as below."
authors:
  - family-names: "Nachname"
    given-names: "Vorname"
    orcid: "https://orcid.org/0000-0000-0000-0000"
title: "Software Title"
version: 1.0.0
doi: "10.5281/zenodo.XXXXXXX"
date-released: "2026-01-01"
```

GitHub-Integration: "Cite this repository"-Popup mit APA- und BibTeX-Formaten.

### Beispiel: CodeMeta

JSON-LD-Schema zur Beschreibung von Forschungssoftware (`codemeta.json`):

```json
{
  "@context": "https://doi.org/10.5063/schema/codemeta-2.0",
  "@type": "Code",
  "author": [{ ... }],
  "version": "1.0.0",
  "codeRepository": "https://github.com/...",
  "dateCreated": "2026-01-01",
  "description": "...",
  "name": "Software Name"
}
```

Generierung ueber den **CodeMeta Generator**.

### Beispiel: Metadata4Ing (m4i)

Schema zur Beschreibung von Forschungsprozessen mittels JSON-LD:

- **Context:** `https://w3id.org/nfdi4ing/metadata4ing/m4i_context.jsonld`
- Beschreibt Verarbeitungsschritte mit:
  - Label
  - Employed Tool
  - Input / Output
  - Investigates Property (mit Kind of Quantity und Unit)

**Ontologie-Beziehungen:**

```
Research Project
  └── Processing Step
        ├── Method
        ├── Tool
        └── Variable (Kind of Quantity + Unit)
```

### Metadaten mit Daten zusammenpacken -- RO-Crate

RO-Crate verpackt Daten zusammen mit einer Metadatendatei:

```
ro-crate/
├── ro-crate-metadata.json
├── ro-crate-preview.html          (optional)
├── ro-crate-preview_files/        (optional)
└── <payload files>
```

- Enthaelt umfassende Informationen ueber Dateistruktur und Datenprovenienz
- Beliebt als Exportformat aus anderen Tools

### Tools zur Verwaltung von Metadaten

**Datenmanagementplattformen:**

| Tool | Beschreibung |
|---|---|
| Coscine | Fuer grosse Dateien |
| eLabFTW | ELN-Software zur Dokumentation von Experimenten und Workflows |
| kadi4mat | ELN-Software zur Dokumentation von Experimenten und Workflows |

**Metadatenstandards und Terminologien:**

| Service | Funktion |
|---|---|
| Metadata Profile Service | Erstellung individueller Metadatenprofile |
| Terminology Service | Auffinden standardisierter Begriffe |

### Coscine Workflow

```
Login (DFN-AAI / ORCiD)
  → Start Now
    → Project
      → Invite Participants
        → Resources (GitLab, Linked Data, Storage Space)
          → Create Metadata Profiles
            → Add Metadata
              → Data (Manage Files)
                → Archiving
                  → Reuse (Meta)Data
```

---

## Kursplan

| Teil | Thema | Datum | Status |
|---|---|---|---|
| 1 | Motivation und Grundlagen | 16.03.2026 | Abgeschlossen |
| 2 | DMPs und Best Practices | 30.03.2026 | Abgeschlossen |
| 3 | Metadaten und Semantik | 13.04.2026 | Abgeschlossen |
| 4 | Software Validation & Verification | 27.04.2026, 17:00 | Ausstehend |
