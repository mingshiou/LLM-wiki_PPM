---
type: method
category: "diagnostic"
aliases: ["In planta bacterial RNA-seq", "Phyllosphere and apoplast transcriptomics", "植物體內細菌轉錄組學"]
target_organisms: ["[[xanthomonas-perforans]]", "[[xanthomonas-euvesicatoria]]"]
tags: ["method", "protocol", "transcriptomics", "rna-seq", "in-planta", "epiphytic", "apoplastic"]
last_updated: 2026-11-20
---

# In Planta Bacterial Dual-Compartment Transcriptomics

## Principle & Purpose
Deciphering phytopathogen behavior in natural hosts requires capturing gene expression during distinct phases of the infection cycle: the surface **epiphytic/phyllosphere** phase and the internal **endophytic/apoplastic** phase. Because host plant tissue typically overwhelms bacterial biomass by several orders of magnitude (often >99:1 plant to bacterial RNA), standard bulk leaf RNA extraction yields poor bacterial sequencing depth and coverage.

This specialized dual-compartment protocol enables high-resolution bacterial transcriptomic profiling across time and leaf microenvironments:
1. **Phyllosphere (Epiphytic) Sampling**: Dip inoculation of host plants followed by vacuum-free leaf-surface bacterial washing and differential filtration to isolate free-living epiphytic bacteria before stomatal entry.
2. **Apoplastic (Endophytic) Sampling**: Low-pressure vacuum infiltration followed by post-incubation recovery of apoplastic fluids or leaf homogenate fractionation.
3. **Differential Filtration & Ribodepletion**: Selective sieving (70-µm mesh to eliminate intact plant cells, followed by 5-µm pore filtration to eliminate plant debris while allowing bacteria to pass through for pelleting at 0.22–0.45 µm) combined with mixed-species rRNA depletion (targeting both plant cytoplasmic/chloroplastic/mitochondrial and bacterial 16S/23S rRNAs).

## Materials & Reagents
- **Host & Pathogen Inoculum**: *Solanum lycopersicum* cv. FL-47 (4–5 weeks old) and *Xanthomonas perforans* strain AL65 (grown in nutrient broth to $\text{OD}_{600} \approx 0.3\text{--}0.5$, resuspended in sterile $10\text{ mM }\text{MgCl}_2$ at $10^8\text{ CFU/mL}$ for dip or $10^6\text{ CFU/mL}$ for infiltration).
- **Extraction Buffers**: Ice-cold RNAlater (or equivalent RNA stabilization solution), sterile ice-cold PBS with 0.02% Silwet L-77 (for surface wash).
- **Physical Filtration Hardware**:
  - 70-µm nylon cell strainers.
  - 5-µm polyethersulfone (PES) or polycarbonate syringe/membrane filters.
  - High-speed refrigerated centrifuge ($4^\circ\text{C}$, $10,000 \times g$).
- **Reagents for Lysis & Extraction**:
  - Lysozyme ($10\text{ mg/mL}$) and Proteinase K.
  - TRIzol Reagent / Acid-phenol:chloroform ($5:1$, pH 4.5).
  - High-capacity RNA clean-and-concentrator spin columns (with on-column DNase I digestion).
- **Ribosomal RNA Depletion**:
  - Illumina Ribo-Zero Plus rRNA Depletion Kit or Qiagen QIAseq FastSelect -5S/16S/23S combined with plant-specific rRNA depletion probes (targeting tomato cytoplasmic 18S/28S and organellar 16S/23S rRNAs).
- **Quality Control & Sequencing**:
  - Agilent 2100 Bioanalyzer (RNA 6000 Pico Chip; target $\text{RIN} \ge 7.0$).
  - NovaSeq X Plus or NovaSeq 6000 (paired-end 150 bp, aiming for $\ge 30\text{--}50\text{ million}$ reads per in planta sample).

## Step-by-Step Procedure

### 1. Inoculation Regimens for Distinct Microenvironments
- **Surface Epiphytic Niche**:
  1. Prepare bacterial suspension in $10\text{ mM }\text{MgCl}_2$ adjusted to $1 \times 10^8\text{ CFU/mL}$ with $0.01\%$ Silwet L-77.
  2. Dip entire 5-week-old tomato plant canopies into the suspension for 30 seconds.
  3. Maintain plants in a high-humidity chamber ($28^\circ\text{C}$, 85–90% RH, 12-h photoperiod).
  4. Harvest at early epiphytic exploration timepoints (e.g., 8 hours post-inoculation, hpi) and surface-attachment/microcolony timepoints (e.g., 24 hpi).
- **Internal Apoplastic Niche**:
  1. Infiltrate tomato leaflets with bacterial suspension ($1 \times 10^6\text{ CFU/mL}$ in $10\text{ mM }\text{MgCl}_2$) using a needleless syringe or whole-plant vacuum infiltration (-70 kPa for 2 min).
  2. Harvest leaflets at early apoplastic colonization (24 hpi) and late apoplastic colonization / egression stage (72 hpi).

### 2. Physical Enrichment of Bacterial Cells & RNA Stabilization
- **For Epiphytic Wash**:
  1. Excise harvested leaves and submerge them in ice-cold PBS + 0.02% Silwet L-77 in sterile 50-mL conical tubes.
  2. Sonicate gently for 5 minutes in an ultrasonic water bath at $4^\circ\text{C}$ followed by 10 minutes of vigorous mechanical shaking (220 rpm) at $4^\circ\text{C}$ to release surface-attached cells without lysing plant cells.
  3. Pass wash suspension through a 70-µm cell strainer, then through a 5-µm syringe filter to retain plant debris while letting bacterial cells pass.
  4. Centrifuge filtrate at $10,000 \times g$ for 12 minutes at $4^\circ\text{C}$ to pellet bacterial cells.
  5. Immediately resuspend pellet in $500\text{ µL}$ ice-cold RNAlater or RNAprotect Bacteria Reagent, incubate 5 min, pellet again, and flash-freeze in liquid nitrogen.
- **For Whole-Tissue In Planta Extraction (Apoplastic Stages)**:
  1. Snap-freeze infected leaf tissue immediately in liquid nitrogen.
  2. Grind tissue into ultra-fine powder using pre-chilled mortars or bead-beaters under liquid nitrogen.
  3. Resuspend powder directly in TRIzol reagent or hot phenol extraction buffer to instantly arrest RNases.

### 3. RNA Isolation & Stringent Quality Verification
1. Lyse bacterial pellets with lysozyme ($3\text{ mg/mL}$) in TE buffer (pH 8.0) for 10 min at room temperature before adding TRIzol.
2. Perform phase separation using chloroform ($0.2\text{ vol}$), centrifuge at $12,000 \times g$ for 15 min at $4^\circ\text{C}$.
3. Precipitate aqueous phase with isopropanol or bind directly to silica columns.
4. Perform on-column DNase I digestion (30 min at $25^\circ\text{C}$) to eliminate contaminating genomic DNA.
5. Elute in nuclease-free water; quantify by Qubit fluorometer and determine RNA integrity on an Agilent Bioanalyzer (Pico Chip).

### 4. Library Construction & Dual Ribodepletion
1. Input $100\text{--}500\text{ ng}$ total RNA into dual-species ribodepletion workflow.
2. Hybridize simultaneously with:
   - Probes targeting plant cytoplasmic and chloroplastic/mitochondrial rRNAs.
   - Probes targeting bacterial 16S and 23S rRNAs.
3. Treat with RNase H (or bead-capture) to selectively remove rRNA-probe hybrids.
4. Synthesize stranded cDNA libraries (dUTP second-strand method) with unique dual indexes (UDI).
5. Sequence on NovaSeq X Plus platform (PE150).

### 5. Bioinformatic Processing & Differential Expression
1. **Dual Alignment**: Map raw reads against the host reference genome (*Solanum lycopersicum* Heinz 1706 or ITAG4.0) to filter host reads; align remaining reads to pathogen reference genome (*Xanthomonas perforans* AL65 / 91-118).
2. **Quantification & Normalization**: Quantify gene-level counts using FeatureCounts / HTSeq; apply DESeq2 or edgeR for pairwise differential expression analysis ($\text{FDR} < 0.05, |\log_2\text{FC}| \ge 1.0$).
3. **Spatiotemporal Clustering**: Perform Weighted Gene Co-expression Network Analysis (WGCNA) or k-means clustering across the 4 conditions:
   - Surface Epiphytic: 8 hpi vs. 24 hpi.
   - Apoplastic: 24 hpi vs. 72 hpi.
   - Cross-compartment: Phyllosphere 24 hpi vs. Apoplast 24 hpi.

## Critical Notes & Troubleshooting
- **Plant RNA Dominance in Apoplastic Samples**: In late-stage leaf tissue, plant RNA can account for >95% of reads. Dual-probe depletion is essential. If bacterial read counts are insufficient, increase sequencing depth to 60–80 million paired reads per sample.
- **In Situ RNA Degradation**: Bacterial mRNAs have short half-lives ($< 3\text{ minutes}$). Flash-freezing in liquid nitrogen must be executed within seconds of tissue harvest; leaf-wash buffers must be kept at $0\text{--}4^\circ\text{C}$ throughout.
- **Surface Contamination Control**: Ensure non-inoculated negative controls are run through the wash and PCR verification steps to confirm that phyllosphere isolates are strictly the inoculated target strain and not endophytes or environmental epiphytes.

## Citations & Standard References
- Kaur, A., Ramamoorthy, S., Ghosh, P., Weis, K., & Potnis, N. (2026). Spatiotemporal coordination of virulence, metabolism, and stress responses shapes infection dynamics of *Xanthomonas perforans*. *Applied and Environmental Microbiology*, 92(8), e00681-26. [[raw/papers/kaur2026spatiotemporal.pdf]]
- Nobori, T., et al. (2018). Transcriptome landscape of plant pathogen in planta reveals adaptations to host microenvironments. *Molecular Plant-Microbe Interactions*, 31(6), 612–621.
