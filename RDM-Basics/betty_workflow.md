# Task Area Betty -- Revised Workflow

**Source:** 2026-03-11-betty_workflow_revised.pdf
**Context:** NFDI4ING Task Area Betty -- Benchmarking Workflows for Engineering Simulation Software
**Status:** Draft -- March 2026

---

## Feedback Requirements

The Geschaeftsstelle NFDI4ING requested two versions of the workflow:

### Version 1: External Communication

A condensed overview for external communication with the following requirements:
- A clearly named **starting point** (e.g., experiment, data collection, problem statement)
- A clearly defined **end station** (e.g., publication, transfer product, consulting result)
- **2--4 central stations** in between that represent the truly decisive steps
- **Conscious prioritization** -- which stations are indispensable to make the path from A to Z understandable?
- **Clear reference to core offerings** -- the chosen stations should make these visible, not just describe generic process steps

### Version 2: Internal Consolidation

A more detailed representation of the overall process:
- A logically structured sequence of stations
- Clear and precise naming of the central steps
- A clearly recognizable reference of each station to the core offerings
- A clearly defined start and end point
- Additional stations and intermediate steps to make the full process visible

Specifically requested improvements:
- Stronger reference to core offerings
- Clearer naming of central stations
- Unambiguous structuring from start to goal

---

## Version 1: External Communication Workflow

**START:** Engineering research question (e.g., "Does my simulation software produce correct results?")
**END:** Published, reproducible benchmark results

### Step 1: Plan
Define benchmark scope and create a Software Management Plan.
- **RDMO** (Core Service) -- create and manage the Software Management Plan

### Step 2: Develop & Prepare
Search for benchmarks and simulation software. Develop or adapt simulation software. Define benchmark cases using standardized terminology.
- **Terminology Service** (Core Service) -- standardized vocabularies for benchmark descriptions
- **BRE** -- search for benchmark descriptions and simulation software
- **GitLab** -- version control for simulation code
- **CIM** -- standardized schema for benchmark cases

### Step 3: Execute & Evaluate
Run benchmarks in a reproducible environment. Compare results against metrics. Create publication-ready figures.
- **Jupyter Service** (Core Service) -- reproducible environment for simulations and analysis
- **fieldcompare** -- quantitative comparison of field data
- **gridformat** -- mesh/grid data format conversion
- **plotID** -- traceable, publication-ready plots

### Step 4: Publish
Archive research data. Publish article. Link software, data, and benchmarks as FAIR Digital Objects.
- **ing.grid** (Core Service) -- Diamond Open Access journal for FAIR publication
- **Coscine** (Core Service) -- FAIR data archiving with metadata and PIDs
- **RO Hub** -- package outputs as Research Objects

---

## Version 2: Internal Full Workflow

**START:** Idea / Research Question
**END:** Published & linked FAIR Digital Objects (software, data, benchmark, publication)

### Personas

| Persona | Description |
|---------|-------------|
| **SW Developer** | Develops or maintains simulation software (e.g., CFD solver or structural analysis tool). Responsible for code quality, licensing, version control, and publishing the software as a FAIR Digital Object. |
| **BM Developer** | Designs and defines benchmark cases for simulation software, including input data, boundary conditions, reference solutions, and evaluation metrics. Ensures benchmarks are well-documented and reproducible. |
| **V&V Engineer** | Performs verification and validation by executing benchmarks against simulation software, comparing results to reference data, and assessing accuracy criteria. |
| **SW User** | Uses existing simulation software and published benchmarks to answer a specific research question. Searches for suitable tools and benchmark cases, runs simulations, and interprets results. |

### Step 1: Plan
Define research question, create SMP.
- **RDMO** (Core) -- create Software Management Plan
- **Output:** Software Management Plan (SMP)
- **Personas:** SW Dev, BM Dev

### Step 2: Search
Find simulation software, benchmark descriptions, reference data, standardized terminology.
- **Terminology Service** (Core) -- standardized vocabularies/ontologies
- **BRE** -- search benchmarks & software
- **Output:** Identified software, benchmark descriptions, reference data
- **Personas:** All

### Step 3: Develop
Develop/adapt simulation software. Define benchmark cases (input, boundary conditions, metrics) using standardized models.
- **Terminology Service** (Core) -- standardized vocabulary for descriptions
- **GitLab** -- version control for simulation code
- **CIM** -- standardized benchmark description schema
- **License Checker** -- verify licensing compliance
- **Software FDO** -- register software as FAIR Digital Object
- **Output:** Simulation software (versioned), benchmark description
- **Personas:** SW Dev, BM Dev

### Step 4: Prepare & Execute
Combine simulation software with benchmark input files. Run simulations in reproducible environment.
- **Jupyter Service** (Core) -- reproducible computational environment
- **gridformat** -- mesh/grid format conversion
- **Output:** Simulation result files (field data, logs, convergence data)
- **Personas:** V&V, User

### Step 5: Visualize & Compare
Compare results against benchmark metrics. Create publication-ready figures.
- **Jupyter Service** (Core) -- interactive analysis & visualization
- **fieldcompare** -- quantitative field data comparison
- **plotID** -- traceable publication-ready plots
- **Output:** Figures, benchmark metric evaluations, comparison reports
- **Personas:** V&V, User

### Step 6: Store & Document
Archive all outputs with FAIR metadata and PIDs. Package as Research Objects.
- **Coscine** (Core) -- FAIR storage, metadata, PIDs
- **RO Hub** -- bundle outputs as RO-Crate
- **Output:** Archived data with PIDs, Research Object RO Crates
- **Personas:** SW Dev, V&V

### Step 7: Publish & Link
Publish article. Link all outputs into connected FAIR Digital Objects.
- **ing.grid** (Core) -- Diamond OA journal, open peer review
- **Coscine** (Core) -- persistent linking via PIDs
- **RO Hub** -- navigable Research Object
- **CIM** -- machine-readable benchmark description
- **Output:** Published article, linked FAIR Digital Objects
- **Personas:** SW Dev, V&V

---

## Core Services Referenced

| Service | Role |
|---------|------|
| RDMO | Software Management Plan creation |
| Terminology Service | Standardized vocabularies and ontologies |
| Jupyter Service | Reproducible computational environment |
| Coscine | FAIR data archiving with metadata and PIDs |
| ing.grid | Diamond Open Access journal |

## Additional Tools Referenced

| Tool | Purpose |
|------|---------|
| BRE | Benchmark & software search |
| GitLab | Version control |
| CIM | Standardized benchmark description schema |
| License Checker | Licensing compliance verification |
| Software FDO | FAIR Digital Object registration for software |
| fieldcompare | Quantitative field data comparison |
| gridformat | Mesh/grid data format conversion |
| plotID | Traceable publication-ready plots |
| RO Hub | Research Object packaging |
