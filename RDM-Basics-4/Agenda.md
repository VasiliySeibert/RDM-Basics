# RDM Basics 4 Engineers — Lecture 4: Research Software

**Series:** NFDI4ING RDM Basics · **Lecture:** 4 of 4
**Duration:** 90 minutes · **Slide target:** ~50
**Language:** English

---

## Abstract

Lectures 1–3 established how to manage research **data** in a FAIR way:
motivation and lifecycle, how to plan with RDMO, and how to describe data with
standardized metadata. This fourth lecture pivots to research **software** —
which is not just "another kind of data." Software runs, evolves, depends on
other software, and needs maintenance. The community answer to this is the
**FAIR4RS Principles** (FAIR Principles for Research Software).

FAIR4RS is written as a set of abstract guidelines. Our job today is to make
them concrete. Every principle will be anchored in an artifact a researcher
can actually see, write, or click on: a DOI on Zenodo, an `SPDX` identifier in
a `LICENSE` file, a `CITATION.cff`, a pinned `requirements.txt`, a Jupyter
session, a search export from the Betty Research Engine.

The session alternates **3 × 15 min theory** blocks (aligned to FAIR4RS) with
**3 × 15 min hands-on practicals** built on NFDI4ING services from the Betty
workflow. The practicals build on each other: first *find* software, then
*describe* it, then *run and sustain* it.

## Learning objectives

By the end of this session, participants will be able to:

1. **Publish** research software with a persistent identifier and
   machine-readable metadata (FAIR4RS: F + A).
2. **Describe** research software using community standards and qualified
   references, so other tools and researchers can consume it
   (FAIR4RS: I).
3. **Reuse** someone else's research software — and prepare their own so that
   others can do the same (FAIR4RS: R).
4. Map these activities onto the NFDI4ING service landscape introduced in
   the Betty workflow (Research Engine, Terminology Service, Jupyter Service,
   RDMO, Coscine, ing.grid).

## Running example

Two artifacts thread through the lecture:

- **`awesome-sim`** — a deliberately small, generic Python repository prepared
  by the lecturer. Hosted on GitHub, with tagged releases, a Zenodo DOI, a
  `README.md`, a `LICENSE` (SPDX: `MIT`), a `CITATION.cff`, a `codemeta.json`,
  a `pyproject.toml` with pinned dependencies, and a minimal GitHub Actions
  workflow. It is the "what YOU could do" repo.
- **DuMux** — a real engineering simulator (porous-media flow) from the
  community. It is the "what a mature research-software project looks like"
  reference, and the search target in Practical 1.

Every theory slide that introduces a FAIR4RS concept immediately shows it in
one of these two repos.

---

## Agenda at a glance

| # | Time          | Block                                                                   | Format             | NFDI4ING service          | FAIR4RS anchor |
|---|---------------|-------------------------------------------------------------------------|--------------------|---------------------------|----------------|
| 0 | 0:00 – 0:03   | Opening & recap of Lectures 1–3                                         | Theory (3 min)     | —                         | —              |
| 1 | 0:03 – 0:16   | **Findable & Accessible research software**                             | Theory (13 min)    | —                         | F1–F4, A1–A2   |
| 2 | 0:16 – 0:30   | **Practical 1: Discover** — search "Dumux", export `.json`              | Practical (14 min) | Betty Research Engine     | F, A           |
| 3 | 0:30 – 0:43   | **Interoperable research software**                                     | Theory (13 min)    | —                         | I1, I2         |
| 4 | 0:43 – 0:57   | **Practical 2: Describe** — `CITATION.cff` + `codemeta.json` + vocab    | Practical (14 min) | Terminology Service       | I              |
| 5 | 0:57 – 1:10   | **Reusable research software**                                          | Theory (13 min)    | (back-ref RDMO / SMP)     | R1–R3          |
| 6 | 1:10 – 1:24   | **Practical 3: Run & sustain** — launch notebook, fork, add license     | Practical (14 min) | Jupyter Service           | R              |
| 7 | 1:24 – 1:30   | Wrap-up, FAIR4RS checklist, Q&A                                         | Theory (6 min)     | —                         | —              |

Total = **90 min**.

---

## 0 · Opening & recap (3 min, ~3 slides)

Welcome, framing and a short recap of where the series has taken us so far:
the FAIR principles for data (Lecture 1), planning and SMP authoring in RDMO
(Lecture 2), and metadata & semantics for datasets (Lecture 3). The pivot:
*software behaves differently from data — it executes, depends on things,
versions, breaks.* Hence **FAIR4RS**, a software-specific refinement of FAIR.
Close the opening by introducing the two running examples (`awesome-sim` and
DuMux) and the alternating theory/practical rhythm of the session.

## 1 · Theory — Findable & Accessible (13 min, ~7 slides)

**Scope:** FAIR4RS F1–F4 and A1–A2, paired because they share the same mental
model: *making software publishable and retrievable by both humans and
machines.*

Concrete anchors to cover:

- **F1 — persistent identifier.** What a DOI actually *is* (prefix/suffix,
  resolver). Show the GitHub ↔ Zenodo integration live: a tagged release on
  GitHub auto-deposits to Zenodo and receives a DOI. Show it on `awesome-sim`.
- **F1.1 / F1.2 — granularity & versions.** One DOI for "the project", version
  DOIs for `v1.0.0`, `v1.1.0`. Git tags vs release IDs.
- **F2 / F3 / F4 — rich, machine-readable metadata.** Walk through the
  `README.md`, `CITATION.cff`, and `codemeta.json` of `awesome-sim` and of
  DuMux. Emphasize that `CITATION.cff` is read by GitHub's "Cite this
  repository" button — a tangible F4 example.
- **A1 — retrieval via open protocol.** `git clone https://…`, `pip install
  awesome-sim` from PyPI. The protocols are HTTPS/git — open, free,
  universally implementable (A1.1).
- **A1.2 — auth where necessary.** Personal access tokens for private repos;
  why public research software still benefits from optional auth (rate limits,
  provenance of contributions).
- **A2 — metadata persists even if the software disappears.** **Software
  Heritage** as the canonical "never-forget" archive; Zenodo immutability.

**Back-reference:** Lecture 1 introduced DOIs and ORCIDs for data and people —
same concept, now for software artifacts.

## 2 · Practical 1 — Discover research software (14 min, ~3 slides + hands-on)

**Service:** Betty **Research Engine** (BRE).
**Goal:** Experience findability from the *consumer* side — what metadata
needs to exist for software to be discoverable at all?

Participant task list:

1. Navigate to the Betty Research Engine site.
2. Log in interactively via GitHub (OAuth handshake — notice A1.2 in action).
3. Search the query `Dumux`.
4. Sort the result list by **citations (descending)**.
5. Export the full search result set as a `.json` file.
6. Open the exported JSON in a text editor and inspect the metadata fields
   present per entry (title, authors, PID, license, version, citation count).

**Reflection prompt (last 2 min):** *which fields were required for DuMux to
surface at rank 1? Which of these fields does your own code currently expose?*

## 3 · Theory — Interoperable (13 min, ~7 slides)

**Scope:** FAIR4RS I1 and I2 — *software talking to other software*.

Concrete anchors to cover:

- **I1 — domain-relevant formats & APIs.** Compare: exchanging simulation
  results as `CSV` vs `HDF5` vs a domain-standard format; when a REST API with
  an OpenAPI spec beats a bespoke file format. Show an OpenAPI snippet.
- **I2 — qualified references to other objects.** Not "authors: Alice, Bob"
  but `authors: [{given-names: Alice, orcid: https://orcid.org/0000-0001-…}]`.
  Not "depends on numpy" but `numpy>=1.26,<2.0` with a PyPI URL. Walk through
  `awesome-sim`'s `codemeta.json` and `pyproject.toml` showing both.
- **Terminology & ontologies.** Controlled vocabulary is what makes "I2
  qualified" *actually* qualified across disciplines. Introduce the **NFDI4ING
  Terminology Service** (`terminology.nfdi4ing.de/ts/`) — a one-stop shop for
  engineering-relevant term URIs (physical quantities, methods, materials).

**Back-reference:** Lecture 3 introduced `CITATION.cff`, CodeMeta, and
Metadata4Ing for data description — today we see them applied to **software**
as a first-class citizen.

## 4 · Practical 2 — Describe research software (14 min, ~3 slides + hands-on)

**Service:** NFDI4ING **Terminology Service** (with the sample repo as
working surface).
**Goal:** Experience interoperability from the *producer* side — make
machine-readable claims about your software.

Participant task list:

1. Open `awesome-sim`'s `CITATION.cff` and `codemeta.json` on GitHub and read
   them aloud in pairs. Identify every qualified reference (ORCID, SPDX,
   DOIs of dependencies).
2. Open the NFDI4ING Terminology Service. Look up URIs for 2–3 domain terms
   the sample repo concerns (e.g., *finite volume method*, *porous media*,
   *Darcy flow*).
3. In a forked copy (or via a GitHub web-edit), extend `codemeta.json` with a
   `keywords` / `applicationCategory` block referencing those URIs.
4. Use GitHub's "Cite this repository" button to generate a BibTeX / APA
   citation from the updated `CITATION.cff` — confirm the metadata you added
   flows through.

**Reflection prompt:** *which parts of this description did you have to write
freely, and which parts were constrained by a standard? Which felt more
reliable?*

## 5 · Theory — Reusable (13 min, ~7 slides)

**Scope:** FAIR4RS R1–R3 — *making software understandable, modifiable, and
sustainable.* This is the biggest block in spirit; the time budget is the
same, so we triage to the highest-leverage anchors.

Concrete anchors to cover:

- **R1 — a plurality of accurate attributes.** Documentation layers: `README`
  (start here), `docs/` (how it works), `examples/` (how to use it), changelog
  (how it has changed).
- **R1.1 — clear, accessible, machine-readable license.** The **SPDX License
  List**: `MIT`, `Apache-2.0`, `GPL-3.0-or-later`. Why the string identifier
  matters (tooling). Brief and practical on license choice: permissive vs
  copyleft, compatibility, "no license" is *not* the same as "public domain".
- **R1.2 — detailed provenance.** `git log`, `AUTHORS`, `CHANGELOG.md`. The
  "who / what / when / why" trail.
- **R2 — qualified references to other software.** Lockfiles and pinned
  versions (`requirements.txt`, `poetry.lock`, `conda env export`), and
  containers (`Dockerfile`) as the strongest reusability guarantee.
- **R3 — community standards.** Packaging for your language's registry (PyPI,
  conda-forge, CRAN, CPAN); CI smoke-tests so "does it still install and run?"
  is answered automatically.
- **Sustainability.** This is where today's lecture loops back to Lecture 2:
  the **RDMO Software Management Plan** is *the* instrument for writing down
  maintenance, versioning, and archival policy *before* the code rots.

**Back-reference:** Lecture 2 introduced the RDMO **SMP**; Lecture 3 covered
RO-Crate for packaging artifacts. Both resurface here as operational tools.

## 6 · Practical 3 — Run & sustain (14 min, ~3 slides + hands-on)

**Service:** NFDI4ING **Jupyter Service** (`jupyter.nfdi4ing.de`).
**Goal:** Experience reusability — can you actually run a stranger's software
*and* make your own runnable by a stranger?

Participant task list:

1. Log in to the NFDI4ING Jupyter Service and launch a fresh Python notebook.
2. Install the version pinned for this lecture:
   `pip install "git+https://github.com/VasiliySeibert/awesome-sim@v1.1.0"`.
   Notice this pins a specific git tag — a concrete example of FAIR4RS **R2**
   (qualified reference to another software at a specific version).
3. In a fresh cell, run:
   ```python
   from awesome_sim import HeatDiffusion2D
   from awesome_sim.viz import plot_snapshot
   sim = HeatDiffusion2D(nx=200, ny=200, alpha=1e-2, dt=5e-5)
   sim.run(500)
   plot_snapshot(sim.u, "out.png", title="t = %.4f" % sim.t)
   ```
   and inspect the resulting heatmap. (The full 1–2 minute
   `examples/minimal_example.py` can also be run if time permits.)
4. Deliberately break reusability: in a clone of the repo, remove the upper
   version bound on `numpy` in `pyproject.toml`, or delete the `LICENSE`.
   Reflect on which tools would complain and when.
5. In the remaining time: fork `awesome-sim` on GitHub and add one thing you
   think would improve its FAIR4RS coverage (a `CONTRIBUTING.md`, a
   `Dockerfile`, an extended `CHANGELOG` entry, …). Commit.

**Reflection prompt:** *what was the smallest thing that would have broken
this reuse — a missing license, an unpinned dep, no example, a broken install
command? That is your first priority in your own repos.*

## 7 · Wrap-up (6 min, ~3 slides)

- **FAIR4RS checklist** — one-slide, printable: for each of F, A, I, R, the
  minimum artifact in the repo that evidences it.
- **NFDI4ING service map** — one-slide recap of the six services touched
  today, positioned on the Betty workflow stages.
- **Connection across the series** — *data + software, together, is
  reproducible research.* Point back to the industrial drilling-machine
  example from Lectures 1–3 and ask: where would its analysis software live
  under FAIR4RS?
- **Q&A + pointers** — Software Heritage, Zenodo, SPDX License List,
  `CITATION.cff` schema, CodeMeta crosswalk.

---

## Slide budget (indicative)

| Block            | Slides |
|------------------|-------:|
| 0 · Opening      | 3      |
| 1 · F+A theory   | 7      |
| 2 · Practical 1  | 3      |
| 3 · I theory     | 7      |
| 4 · Practical 2  | 3      |
| 5 · R theory     | 7      |
| 6 · Practical 3  | 3      |
| 7 · Wrap-up      | 3      |
| Dividers & visuals (buffer) | ~14 |
| **Total**        | **~50** |

## Pre-lecture preparation checklist

Before the session, the lecturer must have ready:

- [x] **`awesome-sim` GitHub repository**, public, live at
      <https://github.com/VasiliySeibert/awesome-sim>, with:
  - [x] Three tagged releases `v0.1.0`, `v1.0.0`, `v1.1.0` (all visible on
        the [Releases page](https://github.com/VasiliySeibert/awesome-sim/releases))
  - [x] Zenodo DOIs minted via the GitHub ↔ Zenodo integration:
        concept DOI [`10.5281/zenodo.19677548`](https://doi.org/10.5281/zenodo.19677548),
        version DOIs [v1.1.0](https://doi.org/10.5281/zenodo.19677552) and
        [v1.0.0](https://doi.org/10.5281/zenodo.19677549)
  - [x] `README.md` with install + minimal usage
  - [x] `LICENSE` file using the SPDX identifier `MIT`
  - [x] `CITATION.cff` (CFF 1.2.0) — GitHub's "Cite this repository" button
        renders it
  - [x] `codemeta.json` (CodeMeta 2.0) referencing ORCID author and PyPI
        dependencies
  - [x] `pyproject.toml` with pinned dependencies
        (`numpy`, `matplotlib`, `pillow`)
  - [x] GitHub Actions CI (Python 3.11 + 3.12) running tests and a headless
        smoke example
  - Install path for Practical 3:
        `pip install "git+https://github.com/VasiliySeibert/awesome-sim@v1.1.0"`
        (no PyPI release — the git-tag install demonstrates R2 directly)
- [ ] Verified Betty Research Engine access; confirmed the "Dumux" query
      returns results sortable by citation count and exportable as `.json`
- [ ] Verified at least one engineering term URI exists on the NFDI4ING
      Terminology Service suitable for Practical 2 (e.g., *finite volume
      method* or *porous media*)
- [ ] Confirmed Jupyter Service account provisioning flow for participants
      (pre-created accounts vs self-signup, installation policy)

## Zenodo archival (done)

The GitHub ↔ Zenodo integration is enabled and both `v1.0.0` and `v1.1.0`
are archived. Zenodo issued the following DOIs, already recorded in the
repo's `CITATION.cff`, `codemeta.json`, and README badge:

| Level                | DOI                                                                                            |
|----------------------|------------------------------------------------------------------------------------------------|
| Concept (all versions) | [10.5281/zenodo.19677548](https://doi.org/10.5281/zenodo.19677548)                           |
| v1.1.0 (pinned by lecture) | [10.5281/zenodo.19677552](https://doi.org/10.5281/zenodo.19677552)                       |
| v1.0.0 (historical)  | [10.5281/zenodo.19677549](https://doi.org/10.5281/zenodo.19677549)                             |

**Pedagogical handle for lecture:** Block 1 (Findable) can demo these three
DOIs side-by-side — one concept, two versions, all resolvable — as a direct
instantiation of FAIR4RS **F1.1** (component granularity) and **F1.2**
(version granularity). The concept DOI always redirects to the latest, so
students can compare `doi.org/10.5281/zenodo.19677548` (latest) vs
`doi.org/10.5281/zenodo.19677549` (v1.0.0) in two browser tabs.

## Open items

- Confirm which specific domain terms in the Terminology Service are
  appropriate for Practical 2 (dependent on participant audience).
- Confirm participant login flow for the Jupyter Service on lecture day.
- Confirm whether a backup plan is needed if any NFDI4ING service is
  unavailable during the session (fall-back: show recorded walkthroughs).
