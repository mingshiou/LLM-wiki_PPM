# Plant Immunity 101: PAMP-Triggered Immunity (PTI)
## Undergraduate Lecture Companion Notes & Slide-by-Slide Script

*Curated from Plant Pathology & MPMI Wiki*  
*Corresponding Presentation: `wiki/presentations/plant-pti-response.html`*

---

### Slide 1: Title & Overview
- **Slide Title**: PAMP-Triggered Immunity: The First Molecular Line of Active Defense in Plants
- **Key Concepts**: Plant innate immunity, autonomous cellular defense, lack of circulating antibodies/adaptive immune cells in plants.
- **Lecturer Script**:
  > "Welcome students. Today we explore the molecular foundation of plant defense: PAMP-Triggered Immunity (PTI). 
  > A guiding question: Plants have no bloodstream, no wandering macrophages, and no adaptive antibodies. How does a single tomato leaf cell detect an invading bacterium within minutes of contact? 
  > The answer lies in plasma membrane pattern recognition receptors that stand continuous surveillance."

---

### Slide 2: The Multi-Layered Plant Immune Architecture
- **Slide Title**: The Multi-Layered Plant Immune Architecture (The Zig-Zag Framework)
- **Key Concepts**: Zig-Zag model, Layer 1 (PTI) at apoplastic cell-surface boundary vs. Layer 2 (ETI) inside the host cell.
- **In-Slide Citations**: *Jones & Dangl (2006); Cook et al. (2015)*
- **Lecturer Script**:
  > "Notice the evolutionary architecture of plant immunity:
  > Layer 1 is PTI, located on the outer plasma membrane, sensing conserved microbial components in the apoplast. It halts 99% of environmental microbes and establishes basal resistance.
  > Layer 2 is ETI, mediated by intracellular NLR receptors that detect specific virulence effectors injected by adapted pathogens. Today's focus is squarely on Layer 1."

---

### Slide 3: Conserved Microbial Signatures (PAMPs / MAMPs)
- **Slide Title**: Conserved Microbial Signatures (PAMPs / MAMPs)
- **Key Concepts**: Molecular nature of `flg22` (flagellin), `elf18` (EF-Tu), and fungal chitin. Difference between PAMPs and MAMPs.
- **In-Slide Citations**: *Boller & Felix (2009); Chang et al. (2019)*
- **Lecturer Script**:
  > "Why are PAMPs so difficult for pathogens to mutate away? 
  > Because flagellin is required for bacterial swimming motility, EF-Tu is essential for protein translation, and chitin is required for fungal cell-wall integrity. If a bacterium mutates flagellin to evade detection, it often loses its ability to swim and cannot infect plant stomata. 
  > Furthermore, because beneficial bacteria also carry flagellin, the term MAMPs (Microbe-Associated Molecular Patterns) is often used interchangeably."

---

### Slide 4: Cell-Surface Perception: FLS2, BAK1 & BIK1
- **Slide Title**: Cell-Surface PRRs: Molecular Surveillance Antennas
- **Key Concepts**: 
  - **FLS2**: Transmembrane LRR-RLK (28 extracellular LRRs + TM helix + intracellular kinase). Direct flg22 receptor.
  - **BAK1 / SERK3**: Transmembrane co-receptor LRR-RLK (5 extracellular LRRs + TM helix + intracellular kinase). Recruited by flg22 binding to sandwich the ligand and initiate transphosphorylation (Sun et al., 2013).
  - **BIK1**: Receptor-Like Cytoplasmic Kinase (RLCK). **Strictly intracellular/cytoplasmic**, anchored to the inner plasma membrane. Phosphorylated by BAK1, then dissociates to activate RBOHD and MAPK cascades.
- **In-Slide Citations**: *Boller & Felix (2009); Sun et al. (2013) Science*
- **Lecturer Script**:
  > "Let's examine the membrane topology of this receptor complex:
  > Notice that FLS2 and BAK1 are BOTH transmembrane proteins spanning the plasma membrane with extracellular LRR domains. The flg22 peptide acts as a molecular glue: FLS2 binds its main body, and BAK1 clamps its C-terminus.
  > Inside the cell, their kinase domains transphosphorylate.
  > What is purely intracellular? BIK1! BIK1 is an RLCK sitting in the cytosol anchored to the inner membrane. Once phosphorylated, BIK1 detaches and carries the signal directly to the NADPH oxidase RBOHD!"

---

### Slide 5: Intracellular Signaling Cascades (0–15 Minutes)
- **Slide Title**: Intracellular Signaling Cascades (0–15 Minutes)
- **Key Concepts**: Rapid calcium influx (seconds), BIK1 kinase release, MAPK cascades (`MEKK1 -> MKK4/5 -> MPK3/MPK6`), CDPK activation, phosphorylation of RBOHD and WRKY transcription factors.
- **In-Slide Citations**: *Boller & Felix (2009); Jones & Dangl (2006)*
- **Lecturer Script**:
  > "Observe how extracellular spatial information is rapidly converted into intracellular biochemical actions:
  > Within seconds, plasma membrane calcium channels open, causing a surge in cytosolic [Ca²⁺].
  > BIK1 phosphorylates the membrane-bound NADPH oxidase RBOHD, while MAPKs carry phosphorylation signals into the nucleus to activate WRKY transcription factors."

---

### Slide 6: Hallmark Defense 1: The Apoplastic ROS Burst
- **Slide Title**: Hallmark Defense 1: The Apoplastic ROS Burst
- **Key Concepts**: Plasma membrane NADPH oxidase `RBOHD`, enzymatic conversion ($\text{NADPH} + 2\text{O}_2 \to \text{NADP}^+ + \text{H}^+ + 2\text{O}_2^{\cdot-} \to \text{H}_2\text{O}_2$), cytotoxicity, cell wall cross-linking, systemic alarm signaling.
- **In-Slide Citations**: *Torres (2010); Gupta et al. (2024)*
- **Lecturer Script**:
  > "A crucial biological question: Why generate reactive oxygen species outside the cell in the apoplast? 
  > Because that is where the invading bacteria reside! Generating ROS inside the cytosol would harm plant chloroplasts and mitochondria. RBOHD acts as a targeted cannon pointing directly into the apoplast."

---

### Slide 7: Laboratory Quantification of the Apoplastic ROS Burst
- **Slide Title**: Laboratory Quantification of the Apoplastic ROS Burst
- **Key Concepts**: HRP-Luminol chemiluminescence (RLU kinetics, smooth bell-shaped curve peaking at 15–20 min), $\text{H}_2\text{DCFDA}$ confocal microscopy, pharmacological control via DPI (diphenyleneiodonium) inhibition.
- **In-Slide Citations**: *Gupta et al. (2024); Chang et al. (2019)*
- **Lecturer Script**:
  > "In the laboratory, how do we measure this burst? 
  > We float leaf discs in 96-well microplates with luminol and horseradish peroxidase. 
  > As you see on the plot, the kinetic curve follows a smooth, rounded bell profile: it starts around 3 to 5 minutes, reaches a smooth rounded dome peak at 15 to 20 minutes, and gradually declines back to basal levels by 45 to 60 minutes.
  > When we pre-treat discs with DPI—a specific inhibitor of plant NADPH oxidases—the burst is completely eliminated, proving the ROS is generated by host enzymes."

---

### Slide 8: Hallmark Defenses 2 & 3: Physical Barrier Reinforcement
- **Slide Title**: Hallmark Defenses 2 & 3: Physical Barrier Reinforcement
- **Key Concepts**: Callose synthase `PMR4/GSL5`, $\beta$-(1,3)-glucan papillae mounds, 0.01% aniline blue fluorometry, ABA/NO-dependent stomatal immune closure within 1 hour.
- **In-Slide Citations**: *Luna et al. (2011); Boller & Felix (2009)*
- **Lecturer Script**:
  > "Notice the dual physical defense mechanisms on this slide:
  > On the left, callose papillae are dense beta-glucan cushions deposited between the cell wall and plasma membrane by PMR4, forming a thick physical reinforcement beneath penetration sites.
  > On the right, stomatal immune closure occurs within 1 hour: guard cells perceive PAMPs, trigger NO and ABA signaling, and dump turgor to seal the foliar entry portals tight, locking the bacteria outside!"

---

### Slide 9: Pathogen Counter-Attack: Effector-Triggered Susceptibility
- **Slide Title**: Pathogen Counter-Attack: Effector-Triggered Susceptibility (ETS)
- **Key Concepts**: Type III Secretion Systems (T3SS), delivery of effectors (e.g. *Xanthomonas* AvrBs2, Xop family), inhibition of BAK1, dephosphorylation of MAPKs, suppression of RBOHD.
- **In-Slide Citations**: *Jones & Dangl (2006); Potnis et al. (2015); Osdaghi et al. (2021)*
- **Lecturer Script**:
  > "If PTI were completely impenetrable, plants would never get sick. 
  > Adapted pathogens like Xanthomonas and Pseudomonas use molecular syringes (T3SS) to inject effector proteins directly into plant cells. 
  > Effectors like AvrBs2 dismantle the PTI machinery, leading to Effector-Triggered Susceptibility (ETS). This, in turn, drove the evolution of intracellular NLR receptors (ETI)."

---

### Slide 10: Agricultural Application: Defense Priming by Beneficial Microbes
- **Slide Title**: Agricultural Application: Defense Priming by Beneficial Microbes
- **Key Concepts**: PGPR (e.g. *Bacillus velezensis*), physiological priming (sensitization), 2,733-fold ROS surge and 150-fold callose increase in watermelon against *Acidovorax citrulli*.
- **In-Slide Citations**: *Chang et al. (2019); Gupta et al. (2024)*
- **Lecturer Script**:
  > "Here is the direct agricultural translation:
  > Plants colonized by beneficial bacilli enter a sensitized 'primed' state. They do not waste energy continuously expressing defense genes. 
  > But when a real pathogen attacks, primed watermelon seedlings launch a hyper-amplified ROS burst up to 2,733-fold higher than unprimed plants, conferring >95% protection in field conditions."

---

### Slide 11: The Root Immune Paradox: Microenvironmental pH Quenching
- **Slide Title**: The Root Immune Paradox: Microenvironmental pH Quenching
- **Key Concepts**: Root immune paradox, Growth-defense trade-off, *Pseudomonas* secretion of D-gluconic acid, acidification to pH 3.5–3.7, biochemical inhibition of RBOHD.
- **In-Slide Citations**: *Yu et al. (2019)*
- **Lecturer Script**:
  > "Consider this paradox: Roots are surrounded by billions of soil bacteria displaying flagellin. Why aren't roots constantly inflamed with destructive ROS bursts? 
  > Yu et al. (2019) discovered that beneficial Pseudomonas secrete gluconic acid, dropping the local boundary pH to 3.5–3.7. 
  > Plant RBOHD requires a neutral pH of ~6.5 to function; at pH 3.7, the local ROS burst is completely quenched, avoiding growth arrest while distal leaves remain primed."

---

### Slide 12: Summary & Learning Checkpoint
- **Slide Title**: Summary & Learning Checkpoint
- **Key Concepts**: Master summary table, review questions on DPI vs heat-killed bacteria and root microenvironment.
- **In-Slide Citations**: *Jones & Dangl (2006); Boller & Felix (2009)*
- **Lecturer Script**:
  > "To conclude our lecture, let's review the two self-study questions:
  > 1. Why does DPI block the ROS burst, while heat-killing bacteria does not? Because DPI inhibits the host plant's RBOHD enzyme, whereas PAMPs like flagellin are heat-stable peptides that remain intact after boiling!
  > 2. How does root acidification protect growth without sacrificing leaf immunity? Local pH 3.7 quenches root-surface RBOHD locally, but systemic priming signals still travel to the foliage."

---

### Slide 13: References & Knowledge Base Sources
- **Slide Title**: References & Knowledge Base Sources
- **Full Literature Citations**:
  - Boller, T., & Felix, G. (2009). *Annu. Rev. Plant Biol.*, 60, 379–406.
  - Chang, C. J., et al. (2019). *J. Plant Med.*, 61(1), 39–48.
  - Gupta, R., et al. (2024). *Food Sec.*, 16(3), 675–690.
  - Jones, J. D. G., & Dangl, J. L. (2006). *Nature*, 444(7117), 323–329.
  - Luna, E., et al. (2011). *Mol. Plant-Microbe Interact.*, 24(2), 183–193.
  - Potnis, N., et al. (2015). *Mol. Plant Pathol.*, 16(9), 907–920.
  - Sun, Y., et al. (2013). *Science*, 342(6158), 624–628.
  - Yu, K., et al. (2019). *Curr. Biol.*, 29(23), 3913–3920.
