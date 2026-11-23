---
name: educational-slides
description: >-
  Generates standalone, responsive 16:9 Reveal.js educational HTML presentations and companion Markdown
  lecture scripts for plant pathology topics following strict viewport budgets, biological accuracy,
  natural editorial layouts, and automated self-linting with a circuit breaker.
---

# Educational Slide Deck Builder Skill

This skill defines the technical specifications, boilerplate templates, visual standards, and automated verification procedures for creating collegiate-level, interactive, 16:9 Reveal.js HTML presentations and companion lecture notes from the Plant Pathology & MPMI Wiki.

---

## 1. Core Visual & Layout Specifications

### 1.1 16:9 Canvas & Geometry Budget
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

### 1.2 Viewport Budget Rules
- **Header**: Height $\le 80\text{px}$. Topic pill (11px uppercase) + Title (32px) + Subtitle (17px).
- **Body (`slide-body`)**: Height budget $\le 520\text{px}$, `flex-grow: 1`.
- **Footer (`slide-footer`)**: Height $\approx 45\text{px}$, `border-top: 1px solid #e2e8f0`.
  - **Left**: Clean citation string `Author (Year)` without any "Refs:" prefix. No repository or wiki watermarks.
  - **Right**: Independent single-number page number (`.page-num`, e.g., `1`, `2`, `3`). Must NOT be enclosed in content cards.

### 1.3 Natural Editorial Layout (Anti-Box Syndrome)
- **Do NOT wrap every paragraph, list, or image inside card borders.**
- Body narrative text, bullet lists, and summary takeaways must flow naturally on the subtle background canvas (`#f8faf7`).
- **Cards/Boxes are strictly reserved for**:
  1. *Parallel Comparative Concepts*: E.g., `Layer 1 (PTI)` vs. `Layer 2 (ETI)`, or 3 distinct PAMP molecules (`compare-grid-2`, `compare-grid-3`).
  2. *Single Prominent Metric Callouts*: E.g., `2,733× Amplified ROS Surge` (`metric-banner`).

---

## 2. Scientific Visualization & Diagram Standards

### 2.1 Diagram Aspect Ratios & Typography
- **Never compress diagrams into flat horizontal ribbons** (e.g., $560 \times 76\text{ px}$ is strictly prohibited).
- Diagrams must use balanced, comfortable proportions:
  - Full-column diagrams: $480 \times 260\text{ px}$ to $520 \times 300\text{ px}$.
  - Side-by-side comparative diagrams: $440 \times 160\text{ px}$ to $460 \times 200\text{ px}$.
- SVG attributes must include `preserveAspectRatio="xMidYMid meet"`.
- Text labels must have font sizes $\ge 11\text{--}14\text{px}$, high-contrast fills, and clear separation from paths/axes. Zero text-over-line collisions.

### 2.2 Kinetic Curves (Real Biological Dynamics)
- In vitro / in planta kinetic curves (e.g., apoplastic ROS burst RLU over time) must **never have sharp, triangular peaks**.
- Curves must be drawn using **smooth cubic Bézier splines (`C` commands)** showing:
  1. Basal lag phase (0–3 min).
  2. Sigmoidal takeoff (3–8 min).
  3. **Smooth rounded dome peak (15–20 min)**.
  4. Asymptotic exponential decay back to baseline (20–60 min).
- Coordinate ticks and numbers must be offset by $\ge 12\text{px}$ outside the axis lines.

### 2.3 Biological Membrane Topology & Complex Verification
- Verify anatomical and molecular topologies before drawing:
  - **FLS2**: Transmembrane LRR-RLK (28 extracellular LRRs + 1 TM helix + intracellular kinase).
  - **BAK1 / SERK3**: Transmembrane co-receptor LRR-RLK (5 extracellular LRRs + 1 TM helix + intracellular kinase). Extracellular LRRs sandwich flg22 against FLS2.
  - **BIK1**: **Strictly intracellular / cytoplasmic** Receptor-Like Cytoplasmic Kinase (RLCK). No TM helix; anchored to inner membrane. Phosphorylated by BAK1 and dissociates to activate RBOHD.
- Multi-step signaling cascades must use **pure CSS Flexbox pipelines** (`pipeline-container`) instead of embedding paragraphs of text inside SVG `<text>` elements.

---

## 3. Dual-Track Speaker Notes & Companion Script

1. **Reveal.js Native Notes**: Embed a lecturing script in `<aside class="notes">` inside every `<section>`.
2. **On-Screen Notes Modal**: Include an on-screen button (`📝 Speaker Notes (N)`) and bottom slide-up drawer (`#notes-modal`) toggled via button click or pressing keyboard `N`. This guarantees notes are 100% accessible when running locally via `file://` protocol where browser popups are blocked.
3. **Companion Markdown Script**: Every HTML presentation must be accompanied by an identical companion Markdown lecture document: `wiki/presentations/<slug>-notes.md` containing the full slide-by-slide script.

---

## 4. Final Reference Slide Architecture

The last slide of the presentation (Slide 13) must be a dedicated **References & Knowledge Base Sources** slide containing full bibliographic citations:
```html
<p>
  <strong>Author, A. B., & Author, C. D. (Year).</strong> Paper title. 
  <em>Journal Name</em>, Vol(Issue), pp–pp.<br>
  <code>[wiki/path/to/source.md]</code>
</p>
```

---

## 5. Automated Self-Linting Checklist & Circuit Breaker

Before delivering the presentation files to the user, the agent must run the following 6-point verification:

- [ ] **L1: Language Conformance**: Matches the agreed language specification (Default: 100% Academic English, 0 Chinese tag badges or text unless explicitly requested).
- [ ] **L2: 16:9 Viewport & Geometry**: 1280×720 canvas, `.slide-container` with flexbox layout, no horizontal/vertical clipping, no text overlapping.
- [ ] **L3: Natural De-boxed Styling**: No card borders wrapping standard text or images; boxes used only for comparative grids or stat banners.
- [ ] **L4: Scientific Precision**: Slide titles accurately match scope (e.g. ROS Quantification vs. PTI); biological curves are smooth dome splines; membrane topologies verified.
- [ ] **L5: Footers & Page Numbers**: Left footer has clean citation without "Refs:"; right footer has independent bare number; last slide has full references.
- [ ] **L6: Dual Notes Accessibility**: Notes toggleable on-screen via `N`, and companion `<slug>-notes.md` exists and matches slides.

### Circuit Breaker Rule (Max 2 Auto-Repairs)
- If any check fails, the agent automatically executes a code fix.
- **Maximum auto-repair attempts: 2 cycles** (Round 0: initial draft; Round 1: first auto-fix; Round 2: second auto-fix).
- **Graceful Escalation**: If after 2 auto-repair attempts a check still fails due to structural conflicts (e.g., text density inherently exceeds the 520px budget), the agent must **halt auto-repair and transparently escalate to the user**:
  1. Report the file location and explain the exact structural trade-off.
  2. Offer 2 clear user choices (e.g., Option A: Split into two slides; Option B: Prune bullet points).

---

## 6. Reveal.js Initialization Boilerplate

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
  plugins: [ RevealNotes, RevealMath.KaTeX ]
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
