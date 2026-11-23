# Plant Pathology & Molecular Plant-Microbe Interactions (MPMI) Wiki Schema

This document (`AGENTS.md`) defines the schema, operational workflows, and maintenance rules for this Plant Pathology LLM Wiki. The LLM agent strictly follows these rules when ingesting sources, maintaining entity pages, updating indexes, generating educational materials, and answering user queries.

---

## 1. Domain & Philosophy

- **Domain Scope**: Comprehensive Plant Pathology and Molecular Plant-Microbe Interactions (MPMI), including classical phytopathology, molecular mechanisms (effectors, immune receptors, signaling pathways), research methodologies/protocols, diagnostics, and integrated management.
- **Persistent Compounding Knowledge**: The wiki is not just a collection of summaries; it is a cross-linked web of evergreen knowledge. New sources incrementally enrich existing pages, clarify contradictions, and update taxonomic classifications.
- **Language Policy**:
  - **Wiki Content**: Written in clear, academic **English**.
  - **Aliases & Searchability**: YAML frontmatter MUST include Chinese common names (`aliases: ["...", "..."]`), Latin binomials, historical synonyms, and common acronyms.

---

## 2. Directory Structure

```text
.
├── AGENTS.md                 # Configuration and operational rules for the LLM
├── README.md                 # Public documentation and repository overview
├── .gitignore                # Git exclusions (OS files, Obsidian cache, raw binary handling)
├── raw/                      # Immutable raw sources (Source of Truth)
│   ├── papers/               # Research articles, reviews, preprints (PDF, Markdown)
│   └── assets/               # Micrographs, symptom photos, gel images, diagrams
└── wiki/                     # LLM-maintained Markdown wiki
    ├── index.md              # Global content catalog & link directory
    ├── log.md                # Chronological append-only operational log
    ├── pathogens/            # Fungi, bacteria, viruses, oomycetes, nematodes, etc.
    ├── diseases/             # Specific disease entries (e.g. late-blight.md)
    ├── hosts/                # Plant hosts and crops (e.g. solanum-lycopersicum.md)
    ├── molecular-biology/    # Effectors, NLR/PRR receptors, signaling, virulence factors
    ├── methods/              # Protocols, assays, inoculation, transformation, diagnostics
    ├── management/           # Fungicides (FRAC), biocontrol, IPM, cultural practices
    ├── concepts/             # Core principles (e.g. zig-zag model, disease triangle)
    ├── presentations/        # Marp-formatted educational slide decks for lectures
    └── syntheses/            # High-value query syntheses and comparative analyses
```

---

## 3. GitHub Hygiene & Publishing Guidelines

1. **Clean Markdown & Git Tracking**:
   - Keep markdown strictly standard GitHub Flavored Markdown (GFM) compatible.
   - Use standard YAML frontmatter for Obsidian and Dataview integration.
2. **Copyright & Raw Data**:
   - If this repository is hosted publicly on GitHub, avoid committing proprietary publisher PDFs directly if copyright is restrictive. The LLM processes raw sources locally, while the generated `wiki/` content constitutes transformative notes and syntheses.
3. **Commit Messages**:
   - Follow conventional commit style:
     - `feat(ingest): ingest <Author Year> on <Topic>`
     - `fix(taxonomy): update reclassification for <Pathogen>`
     - `docs(slides): generate lecture slides for <Topic>`

---

## 4. Taxonomic History & Reclassification Policy

Taxonomy in plant pathology evolves rapidly (e.g., *1 Fungus = 1 Name* rule, genus splitting like *Ralstonia*, *Xanthomonas*, *Phytophthora*). 

Every pathogen page MUST feature:
1. **Frontmatter Synonyms**: All historical names, basionyms, teleomorph/anamorph variants.
2. **Dedicated Section**: `## Taxonomic History & Reclassifications` documenting:
   - Former scientific names and date/rationale of reclassification.
   - Citation of the reclassification paper.
   - Note on how older literature refers to this organism.
3. **Cross-Referencing**: If an ingested paper uses a legacy name, the LLM maps it to the current consensus name while adding a note on the legacy name.

---

## 5. Entity Categories & Templates

All wiki files must use YAML frontmatter compatible with Obsidian and Dataview.

### 5.1 Pathogen (`wiki/pathogens/<scientific-name-slug>.md`)
```markdown
---
type: pathogen
scientific_name: "Phytophthora infestans"
kingdom: "Stramenopila"
phylum: "Oomycota"
aliases: ["致病疫黴", "Phytophthora infestans", "Montagne"]
historical_names: ["Botrytis infestans"]
primary_hosts: ["[[solanum-tuberosum]]", "[[solanum-lycopersicum]]"]
primary_diseases: ["[[late-blight]]"]
tags: ["pathogen", "oomycete", "hemibiotroph"]
last_updated: YYYY-MM-DD
---

# [[scientific_name]]

## Overview
Brief introduction to the organism, lifestyle (biotroph / hemibiotroph / necrotroph), host range, and economic impact.

## Taxonomic History & Reclassifications
- **Current Classification**: Kingdom, Phylum, Class, Order, Family, Genus, Species.
- **Historical Synonyms & Nomenclature Changes**: Detail previous classifications and why/when they changed.

## Biology & Morphology
Reproductive structures (sporangia, zoospores, oospores), survival structures, infection cycle.

## Molecular Pathogenicity & Virulence Factors
- **Effectors**: Key RXLR, CRN, or other effectors (links to `[[wiki/molecular-biology/...]]`).
- **Pathogenicity Determinants**: Cell wall degrading enzymes, toxins, etc.

## Associated Diseases
- [[disease-link]]: Brief note on symptoms and host relationship.

## Key Research Protocols & Model Strains
Reference to model strains (e.g., T30-4) and handling techniques (`[[wiki/methods/...]]`).

## References & Sources
- [[raw-source-citation]]
```

### 5.2 Molecular Biology (`wiki/molecular-biology/<entity-slug>.md`)
```markdown
---
type: molecular-biology
category: "effector" # effector | receptor | pathway | virulence-factor | sRNA
aliases: ["Avr3a", "PiAvr3a"]
organism: "[[phytophthora-infestans]]"
target_host_proteins: ["[[host-target-protein]]"]
corresponding_r_gene: ["[[r3a]]"]
tags: ["molecular-biology", "effector", "rxlr"]
last_updated: YYYY-MM-DD
---

# Entity Name

## Function & Biochemical Activity
Mechanism of action, domain structure (e.g., RXLR-dEER motif, kinase domain), subcellular localization.

## Host Interaction & Target
How it manipulates the host cell (suppressing PTI, altering vesicle trafficking, transcription modulation).

## Host Immune Recognition (ETI / Resistance)
Which host immune receptors recognize this factor (direct vs. indirect guard/decoy models).

## References & Sources
```

### 5.3 Research Methods & Protocols (`wiki/methods/<protocol-slug>.md`)
```markdown
---
type: method
category: "inoculation" # inoculation | transformation | diagnostic | phenotyping | microscopy
aliases: ["Detached leaf assay", "離體葉片接種法"]
target_organisms: ["[[pathogen-name]]"]
tags: ["method", "protocol", "phenotyping"]
last_updated: YYYY-MM-DD
---

# Protocol Title

## Principle & Purpose
Why this method is used and its advantages over alternatives.

## Materials & Reagents
Media composition, spore concentrations, host stage, environmental requirements.

## Step-by-Step Procedure
Detailed workflow steps.

## Critical Notes & Troubleshooting
Common failure points, humidity control, spore viability verification.

## Citations & Standard References
```

---

## 6. Standard Operating Procedures (SOP)

### Operation 1: Interactive Ingest (One Paper at a Time)
1. **Source Reception**: User specifies a paper in `raw/papers/` or provides text/links.
2. **Extraction & Synthesis**:
   - The LLM reads the document in full.
   - Extracts: Pathogen, host, disease, molecular mechanisms, experimental methods, taxonomic updates, conflicting findings.
3. **Pre-commit Discussion (Crucial)**:
   - LLM presents key takeaways to the user.
   - LLM outlines proposed changes:
     - New pages to create.
     - Existing pages to update (and what specific sections will change).
     - Contradictions or novelty compared to existing wiki knowledge.
4. **User Feedback**: User approves or redirects emphasis.
5. **Execution**:
   - LLM updates/creates the target markdown files.
   - LLM updates `wiki/index.md` with links and one-line summaries.
   - LLM appends a structured record to `wiki/log.md`:
     `## [YYYY-MM-DD] ingest | <Paper Title> | touched: [[page1]], [[page2]]`

### Operation 2: Thematic Educational Presentation Generation (SOP)
When the user requests an educational slide deck or lecture presentation on a specific topic, the LLM must execute the following structured 5-phase SOP:

1. **Phase 1: Knowledge Retrieval & Corpus Audit (Three-Tier Boundary Check)**:
   - Query `wiki/index.md` and related entity files to evaluate topic coverage against the wiki corpus:
     - **Sufficient Coverage ($\ge 70\%$)**: Proceed directly to outline planning using existing wiki knowledge.
     - **Partial Coverage ($30\%\text{--}70\%$)**: Propose a "Scope Convergence" plan (default recommendation) substituting missing details with documented wiki pathosystems. If the user explicitly requires the missing subtopic, allow expanding at most 1 target paper via Operation 1 upon explicit user approval.
     - **Insufficient / Out-of-Scope ($< 30\%$)**: Halt boundary defense. Transparently inform the user that the topic falls outside the current wiki corpus; suggest splitting the request into an initial literature ingestion project before generating presentations. **Never silently search the web or hallucinate ungrounded facts.**
2. **Phase 2: Outline Planning & Mandatory User Alignment (Gatekeeper Checkpoint)**:
   - Formulate a 10–13 slide outline detailing pedagogical goals, target audience level (e.g., undergraduate vs. graduate), and in-slide citations `(Author, Year)` linking to wiki files.
   - **MANDATORY CHECKPOINT**: The agent must stop and present the proposed outline to the user. **Do NOT generate any presentation code until the user explicitly approves ("可以 / 同意")**.
3. **Phase 3: Execution via Presentation Builder Skill**:
   - Activate and strictly adhere to `.agents/skills/educational-slides/SKILL.md`.
   - Ensure standard 16:9 canvas (`width: 1280, height: 720`), clean flexbox layout, natural de-boxed typography, proportional scientific diagrams, smooth cubic Bézier kinetic curves, verified biological topologies, dual-track speaker notes, and a dedicated final references slide.
4. **Phase 4: Automated Self-Linting & Circuit Breaker (Max 2 Auto-Repairs)**:
   - Execute the 6-point linting checklist (Language conformance, 16:9 geometry, natural un-boxed flow, scientific accuracy, citations without "Refs:", and notes accessibility).
   - **Circuit Breaker**: Limit automatic repair cycles to **maximum 2 iterations**. If any check fails after 2 auto-fixes, trigger graceful escalation: halt auto-repair and present the specific structural trade-off to the user for decision.
5. **Phase 5: Delivery & Operational Logging**:
   - Deliver the standalone HTML file (`wiki/presentations/<slug>.html`) and companion Markdown lecture script (`wiki/presentations/<slug>-notes.md`).
   - Catalog the presentation in `wiki/index.md` (Section 8) and append an audit record to `wiki/log.md`.

### Operation 3: Query & Synthesis
1. Check `wiki/index.md` and relevant entity folders.
2. Formulate cross-document synthesis citing specific wiki pages and sources.
3. If the query yields a significant novel synthesis, comparison table, or review, LLM offers to file it into `wiki/syntheses/<topic>.md`.

### Operation 4: Wiki Lint & Health Check
Periodically run a health check:
- **Orphan Pages**: Identify pages without incoming links.
- **Taxonomic drift**: Ensure legacy names link to updated pages.
- **Incomplete Placeholders**: Flag stubs needing more experimental data.
- **Contradiction Audits**: Flag where older papers' mechanistic claims are overturned by recent findings.
