# NFDI4ING RDM Basics for Engineers -- Overview

This folder contains structured markdown extractions from the NFDI4ING "RDM Basics for Engineers" training materials. These documents make the presentation content searchable and accessible for LLM-assisted work.

---

## Course Summary

**NFDI4ING** (National Research Data Infrastructure for Engineering Sciences) offers a 4-part online training series on Research Data Management (RDM) fundamentals for engineers. The course covers the full data life cycle -- from planning and collecting data through analysis, sharing, archiving, and reuse -- with engineering-specific tools, examples, and best practices.

**Key themes across all modules:**
- **FAIR Principles** -- making data Findable, Accessible, Interoperable, and Reusable
- **Data Management Plans (DMPs)** -- structured planning using RDMO
- **Metadata & Semantics** -- DataCite, CodeMeta, Metadata4Ing, CITATION.cff
- **NFDI4ING Services** -- RDMO, Coscine, GitLab, Jupyter Service, Terminology Service, ing.grid, AIMS Metadata Profile Service
- **Licenses** -- Creative Commons, MIT, GPL
- **Persistent Identifiers** -- DOI, ORCID, Handles

**Running example:** Industrial drilling machines generating sensor time-series data (temperature, rotational speed, torque), used to demonstrate RDM concepts across all sessions.

---

## Documents

### Module 1: Motivation & Grundlagen
**File:** [01_motivation_grundlagen.md](01_motivation_grundlagen.md)
**Date:** 16.03.2026 | **Authors:** Mario Moser, Marcos Galdino, Tobias Hamann (WZL, RWTH Aachen)

Covers the *why* and *what* of RDM: good scientific practice, funder requirements (DFG, BMBF), FAIR principles, persistent identifiers, the data life cycle, DMPs, licenses, repositories, and NFDI4ING's structure (6 archetypes: Alex, Betty, Caden, Doris, Ellen, Fiona). Includes a practical walkthrough with the drilling machine dataset and an overview of all NFDI4ING services.

### Module 2: Best Practices, DMPs & RDMO
**File:** [02_best_practices_rdmo.md](02_best_practices_rdmo.md)
**Date:** 30.03.2026 | **Authors:** Isabel Hohle (ULB Darmstadt), Michaela Lestakova (TU Darmstadt)

Covers the *how* of RDM: DMP creation using RDMO (workflow, templates, interview process, export formats), the Software Management Plan (SMP), and a real-world best practice example -- resilience assessment of water distribution networks -- showing version control (GitLab), metadata (Metadata4Ing), archiving (TU Datalib, Coscine), and publication (ing.grid).

### Module 3: Metadata & Semantics
**File:** [03_metadaten.md](03_metadaten.md)
**Date:** 13.04.2026 | **Authors:** Dorothea Iglezakis (Uni Stuttgart), Felix Engels (TIB)

Deep dive into metadata: why documentation matters, data repositories for FAIR data, metadata standards (DataCite schema with all fields), content negotiation via PIDs, local data management (file/folder naming conventions, directory organization), metadata at different levels (project/study/data), and metadata formats (YAML, JSON-LD, CFF, CodeMeta, Metadata4Ing, RO-Crate). Includes Coscine workflow.

### Module 3: Metadaten Board (Concept Map)
**File:** [03_metadaten_board.md](03_metadaten_board.md)
**Date:** 13.04.2026 | **Authors:** Dorothea Iglezakis

Visual concept board mapping metadata needed to *find*, *understand*, and *use* different data types (simulation, experimental, survey, software). Also shows the full DataCite metadata schema with mandatory/recommended/optional field classification.

### Betty Workflow (Task Area Betty)
**File:** [betty_workflow.md](betty_workflow.md)
**Date:** March 2026 (Draft)

Two versions of the benchmarking workflow for engineering simulation software:
- **Version 1 (External):** 4-step condensed workflow (Plan -> Develop & Prepare -> Execute & Evaluate -> Publish) with core service references
- **Version 2 (Internal):** 7-step detailed workflow with 4 personas (SW Developer, BM Developer, V&V Engineer, SW User), explicit inputs/outputs per step, and full tool mapping

### Feedback Evaluation
**File:** [feedback_auswertung.md](feedback_auswertung.md)
**Date:** 2026-03-23

Evaluation of participant feedback from the first pilot run with Hochschule RheinMain. 7 responses from 11 participants. Key takeaways: FAIR principles and licenses well received; open questions around software handling, file sizes for publication, directory structures, and data quality requirements.

---

## NFDI4ING Core Services Quick Reference

| Service | Purpose | URL |
|---------|---------|-----|
| **RDMO** | Data/Software Management Plan creation | rdmo.nfdi4ing.de |
| **Coscine** | FAIR data storage, metadata, PIDs | coscine.rwth-aachen.de |
| **GitLab** | Version control for code | git.rwth-aachen.de |
| **Jupyter Service** | Reproducible computational environment | jupyter.nfdi4ing.de |
| **Terminology Service** | Standardized vocabularies/ontologies | terminology.nfdi4ing.de/ts/ |
| **AIMS Metadata Profile Service** | Modular metadata profiles | profiles.nfdi4ing.de |
| **ing.grid** | Diamond OA journal for FAIR publication | inggrid.org |
| **Data Collections Explorer** | Find and filter data repositories | data-collections.nfdi4ing.de |
| **Betty's (Re)Search Engine** | Search software repositories | nfdi4ing.rz-housing.tu-clausthal.de |
| **Education Portal** | RDM training materials | education.nfdi4ing.de |

---

## Course Schedule

| # | Topic | Date | Status |
|---|-------|------|--------|
| 1 | Motivation und Grundlagen | 16.03.2026 | Done |
| 2 | DMPs und Best Practices | 30.03.2026 | Done |
| 3 | Metadaten und Semantik | 13.04.2026 | Done |
| 4 | Software Validation & Verification | 27.04.2026 | Upcoming |

---

## Contact

- **NFDI4ING:** contact@nfdi4ing.de
- **Helpdesk:** nfdi4ing.de/helpdesk
- **RDMO Support:** rdmo@nfdi4ing.de
- **Funded by:** DFG, project number 442146713
