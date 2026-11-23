---
name: educational-slides
description: >-
  Generates standalone, responsive 16:9 Reveal.js educational HTML presentations and companion Markdown
  lecture scripts for plant pathology topics following strict viewport budgets, biological accuracy,
  natural editorial layouts, SVG sanitation standards, and automated self-linting with a circuit breaker.
---

# Educational Slide Deck Builder Skill

This skill defines the technical specifications, boilerplate templates, visual standards, and automated verification procedures for creating collegiate-level, interactive, 16:9 Reveal.js HTML presentations and companion lecture notes from the Plant Pathology & MPMI Wiki.

---

## 1. Core Visual & Layout Specifications

### 1.1 16:9 Canvas & Elastic Geometry Budget
Every presentation must strictly conform to a **16:9 aspect ratio** configured in Reveal.js (`width: 1280, height: 720, margin: 0.04`).

Each slide must be structured using a flexbox layout container to eliminate vertical clipping and prevent overlapping:
```html
<section>
  <div class="slide-container">
    <header class="slide-header">
      <div class="topic-pill">Topic Category</div>
      <h2>Slide Title</h2>
      <p class="subtitle">Descriptive Subtitle</p>
    </header>

    <main class="slide-body">
      <!-- Natural content flow, diagrams, or comparative columns -->
    </main>

    <footer class="slide-footer">
      <div class="citation">Author (Year); Author2 (Year)</div>
      <div class="page-num">1</div>
    </footer>
  </div>

  <aside class="notes">
    Speaker lecture script for this slide.
  </aside>
</section>
```

#### Viewport Budget Rules
- **Header (`.slide-header`)**: Height $\le 80\text{px}$ (Fixed $\sim 76\text{px}$). Topic pill ($11.5\text{px}$ uppercase) + Title ($30\text{px}$) + Subtitle ($15\text{px}$).
- **Body (`.slide-body`)**: Elastic height budget (`flex: 1; min-height: 500px; max-height: 535px; overflow: hidden;`). Must never be hard-coded to a rigid height that clips on minor font-size adjustments.
- **Footer (`.slide-footer`)**: Height $\approx 44\text{px}$, `border-top: 1px solid #cbd5e1`.
  - **Left (`.citation`)**: Clean citation string `Author (Year)` without any "Refs:" prefix. No repository or wiki watermarks.
  - **Right (`.page-num`)**: Independent single-number page number (`.page-num`, e.g., `1`, `2`, `3`). Must NOT be enclosed in content cards.

### 1.2 Minimalist Authoritative Cover (Slide 1) & Learning Objectives (Slide 2)
- **Slide 1 (Minimalist Cover)**:
  - Consists strictly of: Main Title ($48\text{px}$ bold) + Subtitle ($20\text{--}21\text{px}$) + clean navigation prompt (`[SPACE] to advance • [N] for speaker notes`).
  - **STRICTLY PROHIBITED ON SLIDE 1**:
    1. Do NOT include top category badges or topic pills.
    2. Do NOT add internal metadata boxes (e.g. `Course: ...`, `Module: ...`, `Target Hosts: ...`).
    3. Do NOT put any watermark or citation text in the bottom-left footer (keep `.citation` empty: `<div class="citation"></div>`).
- **Slide 2 (Pedagogical Alignment & Competencies)**:
  - Must feature a dedicated section or card defining **3 to 4 Core Learning Objectives** (e.g., Phylogenomic Differentiation, Spatiotemporal Infection Stages, Effector-Target Perception, Integrated Management).
  - Explicitly states what analytical and biological competencies students will master by the end of the lecture.

### 1.3 Typography Hierarchy & Legibility
- Overall presentation font size must be large enough to read easily in lecture halls:
  - Slide Titles (`h2`): $28\text{--}30\text{px}$, weight 800.
  - Subtitles: $14\text{--}15\text{px}$, weight 500.
  - Body Lead Text: $16.5\text{--}17.5\text{px}$, line-height 1.6.
  - Body Regular Text: $15\text{--}15.5\text{px}$.
  - Card Titles: $17\text{--}19\text{px}$, weight 700.
  - Card Body Text: $14\text{--}15\text{px}$.
  - Table Cells: $14\text{--}14.5\text{px}$.
  - Reference Slide (Slide 13): $12\text{--}12.5\text{px}$, line-height 1.5.

### 1.4 Natural Editorial Layout (Anti-Box Syndrome)
- **Do NOT wrap every paragraph, list, or image inside card borders.**
- Body narrative text, bullet lists, and summary takeaways must flow naturally on the subtle background canvas (`#f8faf7`).
- **Cards/Boxes are strictly reserved for**:
  1. *Parallel Comparative Concepts*: E.g., `Layer 1 (PTI)` vs. `Layer 2 (ETI)`, or distinct receptor models (`grid-2col`, `grid-3col`).
  2. *Single Prominent Metric Callouts*: E.g., `23%–44% Direct Marketable Yield Collapse` (`metric-banner`).

---

## 2. Standard Layout Archetypes & Dual-Track Blueprint

### 2.1 The 5 Standard Layout Archetypes
Every educational slide proposal in Phase 2 must explicitly assign one of the following 5 standard archetypes:

1. **Archetype 1: Comparison Matrix Table (`.matrix-table`)**
   - *Application*: Multi-species/lineage taxonomic comparisons, differential host ranges, enzyme profiles (amylolytic/pectolytic), resistance spectra.
   - *Design*: 4–6 column table with clear headers, bold species names, high-contrast badges (`+`, `-`, `High`, `Low`), and horizontal row hover styling. Never use 4 parallel cards.
   ```html
   <table class="matrix-table">
     <thead>
       <tr>
         <th>Species &amp; Lineage</th>
         <th>Primary Hosts</th>
         <th>Amylolytic / Pectolytic</th>
         <th>Climate &amp; Ecological Niche</th>
         <th>Distinctive Virulence Traits</th>
       </tr>
     </thead>
     <tbody>
       <tr>
         <td><strong>X. euvesicatoria</strong> (Group A)</td>
         <td>Tomato &amp; Pepper</td>
         <td>Non-amylolytic (-)</td>
         <td>Temperate / Subtropical</td>
         <td>Model for T3SS and TALE (AvrBs2, AvrBs3)</td>
       </tr>
     </tbody>
   </table>
   ```

2. **Archetype 2: Split Diagram + Panel (`.diagram-split`)**
   - *Application*: Diagnostic symptoms, leaf surface topology, or experimental assay comparisons.
   - *Design*: Horizontal 50/50 or 60/40 layout. Left side contains an embedded vector schematic (or photo asset from `raw/assets/`); right side contains 2–3 structured takeaway blocks with bullet points.

3. **Archetype 3: Spatiotemporal Flow & Progression (`.flow-progression`)**
   - *Application*: Infection cycles, symptom evolution (water-soaking $\to$ halo $\to$ shot-hole), or multi-stage timecourses (8h $\to$ 24h $\to$ 72h).
   - *Design*: Horizontal step progression or upper/lower stage vector pipeline with directional arrows and state badges (`.pipeline-container` and `.pipeline-step`).

4. **Archetype 4: Full-Width Focus Mechanism (`.focus-mechanism`)**
   - *Application*: Deep molecular machinery (T3SS syringe, gene operons, receptor-ligand complexes, membrane redox systems).
   - *Design*: Full-width canvas centered around a contiguous multi-compartment vector diagram (bacterial membrane, apoplast, host cytoplasm/nucleus) with explicit callout annotations and zero text overflows.

5. **Archetype 5: Dual Contrast Grid (`.contrast-grid`)**
   - *Application*: Binary biological paradigms (Compatible vs. Incompatible interactions; Copper-sensitive vs. Copper-resistant; Traditional bactericide vs. Bacteriophage biocontrol).
   - *Design*: Two balanced columns with contrasting border accents (e.g. green for defense/resistance, amber/red for susceptibility/disease).

### 2.2 Phase 2 Dual-Track Blueprint Format
When proposing slides during Phase 2 (Gatekeeper Checkpoint A), the LLM must present the outline in this structured format:

```markdown
* **Slide [N]: [Slide Title]**
  * **Core Pedagogical Point**: [1 clear sentence explaining the specific biological or analytical takeaway]
  * **Layout Archetype**: [Archetype 1: Matrix Table | Archetype 2: Split Diagram + Panel | Archetype 3: Flow Progression | Archetype 4: Focus Mechanism | Archetype 5: Dual Contrast Grid]
  * **Visual Strategy & Elements**:
    * [Diagram / Table details: list specific compartments, arrows, molecular entities, or table columns]
    * [Asset source: Local photo asset / Embedded SVG / HTML Table]
  * **In-slide Citation**: `(Author, Year)` linking to wiki files
```

---

## 3. Scientific Visualization & Strict SVG Standards (Anti-Wall-of-Text)

### 3.1 Visual Pedagogy Mandate
Plant pathology is fundamentally morphological and spatial. **A presentation must NEVER consist solely of text cards.** Slides 4 through 10 must incorporate visual schematics:
1. **Symptomology (Slide 4)**: Must embed visual morphological progression diagrams (e.g., foliar water-soaking $\to$ chlorotic halo $\to$ shot-hole perforation; fruit blister scabs $\to$ cracked craters $\to$ sunscald).
2. **Spatiotemporal Dynamics (Slides 6 & 7)**: Must embed leaf cross-section / stomatal pore schematics mapping the timeline (ingress: swimming $\to$ stressome pre-arming $\to$ *ycgR* brake; egression: maceration $\to$ hypoxia $\to$ flagellar reactivation).
3. **Molecular Mechanisms & Receptors (Slides 8–10)**: Must embed accurate vector schematics of secretion systems (T3SS syringe), plant cell immune perception (intracellular NB-LRR vs. nuclear executor R-genes), and membrane detoxification machinery (*copLAB*).

### 3.2 Strict SVG Technical Sanitation Rules
To eliminate rendering glitches, text collisions, and broken browser graphics:
1. **ZERO HTML TAGS INSIDE SVG `<text>`**:
   - **STRICTLY FORBIDDEN**: Never write `<text>...<em>...</em>...</text>` or `<text>...<strong>...</strong>...</text>` inside SVG.
   - SVG parsers do not support HTML tags inside text nodes. In Safari/Chrome, this breaks SVG text positioning engines, shifts coordinates, and causes words to pile up. Use plain text or `<tspan font-style="italic">` / `<tspan font-weight="bold">`.
2. **MANDATORY `<defs>` FOR ARROWHEAD MARKERS**:
   - Never reference `marker-end="url(#id)"` without declaring `<defs><marker id="id" ...></marker></defs>` inside that SVG.
3. **MANDATORY BOUNDARY PADDING & TEXT CENTERING**:
   - SVG does NOT auto-wrap text. Never write single text strings longer than 35 characters inside an SVG box without manual line breaks.
   - For text centered over boxes or shapes, always use `text-anchor="middle"` with calculated center coordinates ($x = x_{\text{box}} + w/2$).
   - Ensure at least $15\text{--}20\text{px}$ padding between text edges and enclosing rect borders.
4. **CONTIGUOUS ANATOMICAL LAYERS**:
   - Cellular layers (e.g. Apoplast $\to$ Outer Membrane $\to$ Periplasm $\to$ Inner Membrane $\to$ Cytoplasm) must be contiguous without artificial white gap stripes between membrane rects.

### 3.3 Smooth Kinetic Curves
- In vitro / in planta curves (e.g. ROS burst) must use **smooth cubic Bézier splines (`C` commands)** with rounded dome peaks. Never draw sharp triangular peaks.

---

## 4. Scientific Notation, Chemical Ions & Nomenclature

1. **Sans-Serif HTML Superscripts for Simple Ions**:
   - In prose and diagrams, write simple ion charges using HTML superscripts: `Cu<sup>+</sup>` and `Cu<sup>2+</sup>`.
   - **Do NOT use KaTeX Times-serif math (`$\text{Cu}^+$`)** in the middle of sans-serif body text; it creates a jarring font style clash with `Plus Jakarta Sans`.
2. **Standard Greek Characters**:
   - Use standard Greek unicode characters (e.g., **`KΦ1`**) rather than lookalike Cyrillic glyphs (`KФ1`).
3. **Mandatory Abbreviation Expansion**:
   - On the first occurrence of specialized quantitative indices, always write out the full name in parentheses: e.g. **Niche Overlap Index (NOI: 0.8–1.0)**.

---

## 5. Dual-Track Speaker Notes & Companion Script

1. **Reveal.js Native Notes**: Embed a lecturing script in `<aside class="notes">` inside every `<section>`.
2. **On-Screen Notes Modal**: Include an on-screen button (`N`) and bottom slide-up drawer (`#notes-modal`) toggled via button click or pressing keyboard `N`. This guarantees notes are 100% accessible when running locally via `file://` protocol where browser popups are blocked.
3. **Companion Markdown Script**: Every HTML presentation must be accompanied by an identical companion Markdown lecture document: `wiki/presentations/<slug>-notes.md` containing the full slide-by-slide script.

---

## 6. Final Reference Slide Architecture

The last slide of the presentation (Slide 13) must be a dedicated **References & Knowledge Base Sources** slide containing full bibliographic citations:
```html
<p>
  <strong>Author, A. B., & Author, C. D. (Year).</strong> Paper title. 
  <em>Journal Name</em>, Vol(Issue), pp–pp.<br>
</p>
```
Font size should be $12\text{--}12.5\text{px}$ with generous line-height ($1.5\text{--}1.6$) and bottom buffer to prevent boundary clipping.

---

## 7. Automated Self-Linting Checklist & Circuit Breaker

Before delivering the presentation files to the user, the agent must run the following 6-point verification:

- [ ] **L1: Language, Chemical & Notation Conformance**: 100% Academic English (0 Chinese characters); sans-serif HTML superscripts (`Cu<sup>+</sup>`/`Cu<sup>2+</sup>`); Greek standards (`KΦ1`); expanded abbreviations (`NOI`).
- [ ] **L2: 16:9 Viewport & Elastic Budget**: 1280×720 canvas; `.slide-body` has elastic budget (`flex: 1; min-height: 500px; max-height: 535px;`); references slide does not clip.
- [ ] **L3: Cover & Pedagogical Alignment**: Slide 1 is minimalist (0 metadata boxes, 0 category pills, empty bottom-left footer); Slide 2 features explicit Core Learning Objectives.
- [ ] **L4: Visual Pedagogy & Structural Matrices**: Pathogen comparison uses `matrix-table` (no 4-card grids); symptoms, spatiotemporal dynamics, and molecular mechanisms include vector schematics.
- [ ] **L5: SVG Technical Sanitation**: 0 HTML tags (`<em>`, `<strong>`) inside SVG `<text>`; all markers declared in `<defs>`; text centered with `text-anchor="middle"` and $\ge 15\text{px}$ padding; no text overflows.
- [ ] **L6: Dual Notes Accessibility**: Notes toggleable on-screen via `N`, and companion `<slug>-notes.md` exists and matches slides.

### Circuit Breaker Rule (Max 2 Auto-Repairs)
- If any check fails, the agent automatically executes a code fix.
- **Maximum auto-repair attempts: 2 cycles** (Round 0: initial draft; Round 1: first auto-fix; Round 2: second auto-fix).
- **Graceful Escalation**: If after 2 auto-repair attempts a check still fails due to structural conflicts, halt auto-repair and transparently escalate to the user with 2 clear options.

---

## 8. Reveal.js Initialization Boilerplate

```javascript
Reveal.initialize({
  hash: true,
  slideNumber: false, // Clean independent page numbers rendered in footer
  controls: true,
  progress: true,
  center: true,
  transition: 'slide',
  backgroundTransition: 'fade',
  margin: 0.04,
  width: 1280,
  height: 720,
  minScale: 0.2,
  maxScale: 2.0,
  plugins: [ RevealNotes ]
});

// On-screen Notes Modal handler
function updateNotesModal() {
  var currentSlide = Reveal.getCurrentSlide();
  var notesEl = currentSlide.querySelector('aside.notes');
  var modalBody = document.getElementById('notes-body');
  if (notesEl && notesEl.innerHTML.trim() !== "") {
    modalBody.innerHTML = notesEl.innerHTML;
  } else {
    modalBody.innerHTML = "<em>No speaker notes for this slide.</em>";
  }
}

function toggleNotesModal() {
  var modal = document.getElementById('notes-modal');
  modal.classList.toggle('visible');
  if (modal.classList.contains('visible')) {
    updateNotesModal();
  }
}

Reveal.on('slidechanged', updateNotesModal);
window.addEventListener('keydown', function(e) {
  if (e.key === 'n' || e.key === 'N') toggleNotesModal();
});
Reveal.on('ready', updateNotesModal);
```
