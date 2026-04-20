# Best Practices in Research Data Management: DMPs, RDMO und Best Practice im Umgang mit Forschungsdaten

**NFDI4ING's RDM Basics for Engineers -- Teil 2 von 4**

|              |                                                                                         |
|--------------|-----------------------------------------------------------------------------------------|
| **Datum**    | 30.03.2026, online                                                                      |
| **Autorinnen** | Isabel Hohle (ULB Darmstadt), Michaela Lestakova (TU Darmstadt, Institut fuer Fluidsystemtechnik) |
| **Lizenz**   | CC BY 4.0                                                                               |

---

## Teil I: Forschungsdatenmanagement und DMPs / RDMO

### Herausforderungen des FDM

| Herausforderung | Beschreibung |
|-----------------|-------------|
| **Diverse Data** | Engineering research generates heterogeneous data (simulations, experiments, software) |
| **Compliance** | Foerderorganisationen (DFG, EU) verlangen zunehmend Datenmanagementplaene |
| **FAIR Prinzipien** | Data should be Findable, Accessible, Interoperable, Reusable |
| **Zusammenarbeit** | Teams need shared, version-controlled, accessible data management solutions; interdisciplinarity; industry integration |
| **Zeitdruck** | Researchers lack time and expertise for comprehensive RDM planning |

### Was ist ein DMP?

A Data Management Plan (DMP) answers central questions about research data:

- Projektbezogene administrative Informationen
- Rollen, Verantwortlichkeiten und Verpflichtungen
- Budget, Kosten, Ressourcen
- Datentypen und -formate
- Metadaten (-Standards), Nachweisbarkeit
- Zugang zu Daten und deren Publikation
- Datenaufbewahrung
- Datenloeschung

### DMPs -- Anforderungen von Foerderinstitutionen

| Foerderinstitution | Anforderung |
|--------------------|-------------|
| **DFG** | Requires DMP (checklist available) |
| **BMBF** | Depends on funding program |
| **VolkswagenStiftung** | Requires DMP |
| **Horizon Europe** | Requires DMP (template available) |

### DMPs -- Roadmap und Planungstool

- Checkliste, Roadmap und Unterstuetzung bei der Planung des eigenen Projekts
- Useful overview at [forschungsdaten.info](https://forschungsdaten.info)

### Datenmanagementplaene -- Vorteile vs Nachteile

#### Vorteile

| Vorteil | Beschreibung |
|---------|-------------|
| Strukturierte Planung | Clear roadmap for the project |
| Foerderkonformitaet | Meets funder requirements |
| Effiziente Dokumentation | Simplifies reports |
| Nachnutzbarkeit | Clear structures enable reuse |
| Mehr Sichtbarkeit | Higher citation chances |
| Datenpublikation | Counts as scientific achievement |
| Datensicherheit | Reduces data loss risk |
| Langfristige Lesbarkeit | Readable formats ensure long-term access |
| Wissenssicherung | Knowledge transfer at personnel changes |

#### Nachteile

| Nachteil | Beschreibung |
|----------|-------------|
| Ressourcenaufwand | Oversight and communication require personnel |
| Zeit- und Kostenfaktor | Creation takes time and possibly infrastructure |
| Technische Anpassungen | May need format conversions |

### Unterstuetzung durch ein DMP Tool

- RDMO supports planning and documentation of FDM processes
- Adapted to specific domains and requirements
- Integration in workflows (repositories, lab databases)
- User-friendly for beginners and experts

### DMP4NFDI -- NFDI Basic Service

Support development and provision of standardized DMP/SMP services within NFDI.

**Three pillars:**

1. Hosting & Integration
2. Template standardisation & Support for development
3. Training & Support for outreach

Link: <https://dmp.services.base4nfdi.de/>

### RDMO -- Research Data Management Organiser

- **Open-source** web-based tool for creating and managing DMPs
- **RDMO NFDI4ING:** engineering-specific client with special catalogs and guides
- **Community und Verein:** <https://rdmorganiser.github.io/>

### RDMO Service

- Many institutions offer their own RDMO instances
- Multi-site hosting with RDMO clients for different tenants
- Examples: ZIB, Max Weber Stiftung, TU Braunschweig, various universities

### NFDI4ING RDMO Service

| Eigenschaft | Detail |
|-------------|--------|
| **URL** | [rdmo.nfdi4ing.de](https://rdmo.nfdi4ing.de) |
| **Login** | via NFDI-AAI |
| **Kataloge** | NFDI4ING DMP Template, Software Management Plan |

### RDMO Workflow

1. Login via NFDI-AAI
2. Create a new project (title, description, choose catalog, link parent project)
3. Invite members
4. Start interview ("Answer questions")
5. Add datasets
6. Answer questions
7. Share or export DMP

### NFDI4ING DMP Template

- Designed for researchers of engineering sciences
- Based on RDA survey and community workshops
- Follows DFG checklist

### The Interview

**Topics covered:**

- Data description
- Documentation
- Quality measures
- Storage and backup
- Data exchange
- Legal obligations / responsibilities / resources

**Export formats:**

| Format | Typ |
|--------|-----|
| PDF | Document |
| Rich Text | Document |
| Open Office | Document |
| Microsoft Office | Document |
| HTML | Web |
| Markdown | Text |
| mediawiki | Text |
| LaTeX | Typesetting |

Export can include the full DMP or specific "views" for templates.

### Software Management Plan (SMP)

Separate catalog in RDMO for scientific software projects. Supports scientists through approximately 50 questions in different topic blocks (v3.0).

**Topic blocks:**

1. General
2. Code
3. Third-Party Components
4. Infrastructure
5. Preservation
6. Security
7. Quality Assurance
8. Release and Publish
9. Legal and Ethics

---

## Teil II: Best Practice im Umgang mit Forschungsdaten

**Practical example:** Resilience Assessment of Water Distribution Networks
*(Michaela Lestakova, TU Darmstadt)*

### Trinkwasserversorgungssysteme

- Modellierung von Wasserversorgungsnetzen (water distribution network modeling)
- **Sektorisierung:** Node Clustering Stage -> Dividing Stage
  - Better fault detection
  - Monitoring
  - Pressure management
  - Resilience

### Methods Pipeline

```
Fallgenerierung -> Sektorisierung -> Resilienzbewertung -> Ergebnisanalyse
                          (all under Forschungsdatenmanagement)
```

### Data Flow

**Step 1 -- Sektorisierung:**

| Richtung | Dateien |
|----------|---------|
| Input | `networks/scenarios/*.pickle`, `networks/Anytown.inp` |
| Script | `sctr_Anytown.py` |
| Output | `*.mps`, `*.sol`, `sctr_results*.hdf5` |

**Step 2 -- Resilienzbewertung:**

| Richtung | Dateien |
|----------|---------|
| Input | `sctr_results*.hdf5` |
| Script | `resilience_eval*.py` |
| Output | `evaluation_res*.hdf5`, `plot.json` |

### Konzept fuer FDM

| Bereich | Inhalt | Plattform | Zweck |
|---------|--------|-----------|-------|
| **CODE BASE** | Source, scripts, demos | GitLab | Maintenance & version control |
| **DATA** | WDN files, opt. files, results, plotted data (with METADATA4ING) | TU datalib | Archiving |

### FDM -- wichtigste Bausteine

1. **Versionskontrolle fuer Code**
2. **Daten- und Codedokumentation mittels Metadaten** (metadata4ing)
3. **Daten- und Codedokumentation mittels Text/Publikationen** (inggrid.org)
4. **Offene Lizenzierung der Daten & Code**
5. **Speichern & Archivierung in geeigneten Repositorien** (Coscine, RADAR4ING)

### RDMO Project Example

- Project: "Resilience Assessment of Water Distribution Networks"
- Catalog: NFDI4ING DMP Template (Version 2)

---

## Abschluss / Organisatorisches

- Feedback surveys available (DE/EN)
- **Homework:** Register at [Coscine](https://about.coscine.de/) before next session
- **Next session:** Metadaten und Semantik, 13.04.2026, 17:00

### Kontakt & Support

| Kontakt | Adresse |
|---------|---------|
| RDMO Support | rdmo@nfdi4ing.de |
| Geschaeftsstelle | geschaeftsstelle@nfdi4ing.de |

### Acknowledgement

DFG project number 442146713
