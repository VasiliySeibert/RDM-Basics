
Context

     This is the fourth 90-minute lecture (~50 slides) in the NFDI4ING RDM
     Basics
     series. Lectures 1–3 (in RDM-Basics-1-3/) covered the motivation & FAIR
     fundamentals for data, best practices with RDMO (incl. SMP), and metadata &
     semantics. Lecture 4 pivots from data to research software, which behaves
     differently (it executes, has dependencies, versions, and sustainability
     needs).

     The user wants a practical, engineering-oriented introduction that takes
     the
     abstract FAIR4RS Principles (in fair4rs/fair4rs.md) and makes them
     concrete: every principle must be anchored in a tangible artifact a
     participant
     can see or produce (a DOI on Zenodo, an SPDX id in a LICENSE file, a
     CITATION.cff, a pinned requirements.txt, etc.).

     The session is structured as three rounds of 15 min theory + 15 min 
     hands-on
     practical, where the practicals use NFDI4ING services from the Betty
     workflow (RDM-Basics-1-3/betty_workflow.md). A small generic Python
     repository threads through the whole lecture as the running example, and
     DuMux appears as the realistic reference case used in Practical 1.

     The goal of this first step is to produce RDM-Basics-4/Agenda.md — a
     section-level agenda plus narrative describing what each section will
     cover.
     Slide content itself is out of scope for now.

     User decisions confirmed:
     - FAIR4RS mapping: F+A | I | R across the three theory blocks
     - Running example: small generic Python repo (e.g., a minimal awesome-sim
     package on GitHub), with DuMux as realistic reference in Practical 1
     - Language: English only
     - Detail level: section-level with narrative (agenda table + 1–2 paragraphs
     per section)

     Approach

     Create one new file: RDM-Basics-4/Agenda.md. No other files change in this
     step. The file will contain:

     1. Header & framing (short)

     - Title, series context (Lecture 4/4), duration, slide target
     - One-paragraph abstract: why research software needs its own FAIR
     treatment
     - Learning objectives (3–4 bullets tied to FAIR4RS: find, publish,
     describe,
     reuse research software in practice)
     - Running example declaration (the sample Python repo + DuMux as reference)

     2. Time-block agenda table

     Compact table with columns: Time · Block · Format · NFDI4ING service · 
     FAIR4RS
     anchor. Totals to 90 min:

     ┌─────┬───────────┬────────────────────────────────────────┬──────────────┐
     │  #  │   Time    │                 Block                  │    Format    │
     │     │   (min)   │                                        │              │
     ├─────┼───────────┼────────────────────────────────────────┼──────────────┤
     │ 0   │ 0:00–0:03 │ Opening & recap                        │ Theory       │
     ├─────┼───────────┼────────────────────────────────────────┼──────────────┤
     │ 1   │ 0:03–0:16 │ Findable & Accessible research         │ Theory (13   │
     │     │           │ software                               │ min)         │
     ├─────┼───────────┼────────────────────────────────────────┼──────────────┤
     │ 2   │ 0:16–0:30 │ Discover — Betty Research Engine:      │ Practical    │
     │     │           │ search DuMux                           │ (14 min)     │
     ├─────┼───────────┼────────────────────────────────────────┼──────────────┤
     │ 3   │ 0:30–0:43 │ Interoperable research software        │ Theory (13   │
     │     │           │                                        │ min)         │
     ├─────┼───────────┼────────────────────────────────────────┼──────────────┤
     │ 4   │ 0:43–0:57 │ Describe — Terminology Service +       │ Practical    │
     │     │           │ CITATION.cff/codemeta.json             │ (14 min)     │
     ├─────┼───────────┼────────────────────────────────────────┼──────────────┤
     │ 5   │ 0:57–1:10 │ Reusable research software             │ Theory (13   │
     │     │           │                                        │ min)         │
     ├─────┼───────────┼────────────────────────────────────────┼──────────────┤
     │ 6   │ 1:10–1:24 │ Run & sustain — Jupyter Service + repo │ Practical    │
     │     │           │  fork                                  │ (14 min)     │
     ├─────┼───────────┼────────────────────────────────────────┼──────────────┤
     │ 7   │ 1:24–1:30 │ Wrap-up, checklist, Q&A                │ Theory       │
     └─────┴───────────┴────────────────────────────────────────┴──────────────┘

     3. Per-section narrative

     For each numbered block, 1–2 paragraphs covering:
     - Content to deliver (the FAIR4RS sub-principles addressed, made concrete
     with specific artifacts)
     - Running-example touchpoints (what participants will see in the sample
     repo
     / DuMux at this point)
     - Transition to / from adjacent block

     Key concretizations per block (to be expanded in the narrative):

     - Block 1 (F+A): DOIs via the GitHub↔Zenodo integration; component/version
     PIDs via git tags & versioned DOIs; README.md + CITATION.cff as
     machine-readable metadata; retrieval via git clone / pip install; auth via
     GitHub tokens; metadata persistence via Software Heritage & Zenodo.
     - Block 2 (I): domain formats (CSV/HDF5), APIs & OpenAPI specs,
     codemeta.json with ORCID-qualified authors, requirements.txt/pyproject.toml
     with pinned versions as qualified software references, the NFDI4ING
     Terminology Service for controlled vocabulary.
     - Block 3 (R): SPDX license identifiers (MIT/Apache-2.0 trade-offs),
     LICENSE
     file in the repo, provenance via git log + AUTHORS + CHANGELOG, pinned
     dependencies & lockfiles & containers, PyPI / conda-forge packaging, CI
     smoke-tests, and sustainability — linking back to the RDMO Software
     Management Plan from Lecture 2.

     4. Practical-session scripts (brief)

     Step-by-step task lists for the three hands-on blocks, designed to build on
     each other:

     - Practical 1 — Discover (Betty Research Engine): navigate to the site,
     log in with GitHub, search "Dumux", sort by citations, export the search
     results as .json, inspect the exported metadata fields. Reflection prompt:
     what metadata was necessary for this result to surface?
     - Practical 2 — Describe (Terminology Service + sample repo): open the
     sample Python repo's CITATION.cff and codemeta.json; use the NFDI4ING
     Terminology Service to look up URIs for domain terms; annotate the repo's
     metadata with those URIs and with ORCID-qualified authorship.
     - Practical 3 — Run & sustain (Jupyter Service): launch a notebook on
     jupyter.nfdi4ing.de, pip install the sample repo from its git tag, run a
     minimal example, then fork the repo and add a proper SPDX LICENSE
     identifier + a CITATION.cff. Reflection prompt: what would have broken
     reusability if missing?

     5. Running-example spec

     Half-page section describing the sample Python repo to be prepared before
     the
     lecture: minimal, single-purpose (e.g., "awesome-sim" — a tiny solver or
     analysis utility); hosted on GitHub; tagged releases with Zenodo DOIs;
     includes README.md, LICENSE (SPDX: MIT), CITATION.cff, codemeta.json,
     pyproject.toml with pinned deps, minimal GitHub Actions workflow. This list
     serves as a prep checklist for the lecturer.

     6. Slide budget (indicative)

     Opening 3 · T1 7 · P1 3 · T2 7 · P2 3 · T3 7 · P3 3 · Wrap 3 · transitions
     &
     visuals ~14 = ~50 slides.

     7. Open items / next steps

     Short list: decide on the concrete sample-repo name & location, confirm
     Terminology Service availability for a specific engineering term to be used
      in
     P2, confirm the Jupyter Service account provisioning workflow for
     participants.

     Critical files to reference while drafting

     - RDM-Basics-1-3/01_motivation_grundlagen.md — style & recap hooks (FAIR
     introduction, DOI/ORCID coverage) to link back to
     - RDM-Basics-1-3/02_best_practices_rdmo.md — RDMO Software Management
     Plan to cite in Block 3 (R / sustainability)
     - RDM-Basics-1-3/03_metadaten.md — existing coverage of CITATION.cff,
     CodeMeta, RO-Crate to build on, not duplicate
     - RDM-Basics-1-3/betty_workflow.md — authoritative list of Betty services
     (RDMO, BRE/Research Engine, Terminology Service, Jupyter, Coscine,
     ing.grid)
     - fair4rs/fair4rs.md — FAIR4RS principles & sub-principles (F1–F4, A1–A2,
     I1–I2, R1–R3) to map each theory block against
     - RunningNotes.md — project context & pilot feedback (open questions from
     Hochschule RheinMain pilot regarding software for data analysis)

     Verification

     After creating RDM-Basics-4/Agenda.md:

     1. Time math: rows in the agenda table sum to exactly 90 min.
     2. Slide math: per-section slide estimates sum to ~50 (±3).
     3. FAIR4RS coverage: every sub-principle (F1–F4, A1–A2, I1–I2, R1–R3)
     appears at least once in the narrative, mapped to a concrete artifact.
     4. Betty services coverage: the three chosen services (Research Engine,
     Terminology Service, Jupyter Service) each appear in exactly one practical,
     and RDMO (SMP) is referenced in the R-block for sustainability.
     5. Continuity: at least one explicit back-reference per block to Lecture
     1, 2, or 3 so the series feels cohesive.
     6. Read-through test: a colleague who hasn't attended lectures 1–3 should
     be able to read Agenda.md and understand, for each 15-min block, what
     happens, what the participant produces or sees, and which FAIR4RS principle
     it concretizes.



※ recap: We're designing a 90-minute Lecture 4 on research software for the NFDI4ING RDM Basics series, and I just created RDM-Basics-4/Agenda.md with the full agenda, FAIR4RS-mapped theory blocks, and three Betty-service practicals. Next: review the agenda and pick what to build next (sample repo or Block 1 slides). (disable recaps in /config)