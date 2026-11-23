---
type: management
category: "chemical-control"
aliases: ["銅劑與抗藥性", "Copper bactericides", "Copper resistance", "Bordeaux mixture", "cop operon", "FRAC M01"]
target_pathogens: ["[[xanthomonas-euvesicatoria]]", "[[xanthomonas-perforans]]", "[[xanthomonas-vesicatoria]]", "[[xanthomonas-gardneri]]"]
target_diseases: ["[[bacterial-spot-tomato-pepper]]"]
frac_code: "FRAC M01"
tags: ["management", "bactericide", "copper", "resistance", "ipm", "frac-m01"]
last_updated: 2026-11-20
---

# Copper Bactericides and Bacterial Resistance

## Overview
Copper-based agrochemicals (FRAC Code M01, inorganic multi-site activity) have formed the backbone of bacterial and fungal disease management in agriculture for over 13 decades, beginning with Millardet’s 1885 discovery of Bordeaux mixture (*bouillie bordelaise*). In solanaceous crops, preventive foliar sprays of fixed coppers (copper hydroxide, copper oxychloride, basic copper sulfate, cuprous oxide) co-applied with dithiocarbamates (mancozeb) have historically been standard practice to suppress [[bacterial-spot-tomato-pepper]]. However, intensive, uninterrupted reliance on copper has driven the global emergence of plasmid-borne copper resistance in phytopathogenic bacteria, causing widespread chemical control failures and severe environmental soil accumulation.

## Biochemical Mode of Action (FRAC M01)
- **Multi-Site Disruption**:
  - Solubilized cupric ions ($\text{Cu}^{2+}$) penetrate bacterial cells and act non-specifically as cellular toxins.
  - $\text{Cu}^{2+}$ denatures essential proteins and enzymes by binding sulfhydryl (-SH), amino, and carboxyl groups.
  - Intracellular free copper drives Fenton-like chemical reactions, generating high levels of hydroxyl free radicals ($\cdot\text{OH}$) and reactive oxygen species (ROS) that oxidize lipids, perforate plasma membranes, and fragment genomic DNA.
- **Formulation Chemistry**:
  - Micron-sized insoluble copper particulates are applied to foliar surfaces; atmospheric carbon dioxide, plant exudates, and rainwater slowly solubilize trace amounts of biologically active $\text{Cu}^{2+}$ ions over time.

## Molecular Mechanisms of Copper Resistance
The first scientific documentation of copper resistance in a plant-pathogenic bacterium occurred in Florida in *[[xanthomonas-euvesicatoria]]* (Marco & Stall, 1983; Stall et al., 1986).

### 1. Plasmid-Borne *copLAB* / *pco* Operons
- Resistance in *Xanthomonas* and *Pseudomonas* is predominantly encoded on large, self-transmissible conjugative plasmids (e.g., pXvCu in *X. euvesicatoria*):
  - **CopA**: Periplasmic multi-copper oxidase that oxidizes more toxic cuprous ions ($\text{Cu}^+$) into less toxic cupric ions ($\text{Cu}^{2+}$) and binds excess copper ions in the periplasmic space.
  - **CopB**: Outer membrane protein involved in periplasmic copper compartmentalization or extrusion.
  - **CopC**: Periplasmic chaperone protein that selectively binds single $\text{Cu}^{2+}$ ions, transferring them to CopA.
  - **CopD**: Inner membrane transporter mediating regulated copper uptake or efflux in concert with CopC.
  - **CopR / CopS**: Two-component regulatory system consisting of an inner-membrane histidine kinase sensor (CopS) and a DNA-binding response regulator (CopR) that induces operon transcription upon sensing elevated periplasmic copper concentrations.
- **Sequestration Phenotype**: Copper-resistant xanthomonad colonies turn bright turquoise or blue-green when grown on copper-amended agar media due to dense intra-periplasmic binding and sequestration of copper complexes, preventing ions from poisoning cytoplasmic enzymes.

### 2. Genetic Linkage to Avirulence and Antimicrobial Resistance
- Plasmids bearing *cop* operons frequently harbor transposable elements encoding resistance to other antibiotics, particularly **streptomycin** (*strAB* phosphotransferases).
- In some historical strains, *cop* operons were physically linked on self-transmissible plasmids to avirulence genes (e.g., *avrBs1*), meaning chemical selection for copper resistance inadvertently maintained or shifted host-range avirulence alleles.

## Field Resistance Crisis and Environmental Impact
- **Ubiquitous Field Resistance**: In commercial tomato and pepper basins across the United States (Florida, Alabama, California), South America (Brazil), and Asia (Taiwan), 70% to 100% of surveyed *[[xanthomonas-perforans]]* and *[[xanthomonas-gardneri]]* isolates now test insensitive or highly resistant to standard copper concentrations.
- **Environmental Phytotoxicity & Residue**: Decades of weekly prophylactic copper sprays lead to heavy copper accumulation in agricultural topsoils, reducing beneficial mycorrhizal and rhizosphere microbiomes, inducing micronutrient imbalances, and causing phytotoxicity on sensitive foliage.

## 21st-Century Alternatives & Non-Copper Horizons

| Alternative Strategy | Chemistry / Organism | Mechanism of Action | Advantages & Limitations |
|---|---|---|---|
| **Advanced Nanocomposites** | Core-shell copper (CS-Cu), Multivalent Cu (MV-Cu), Nano-MgO, Cu/Zn hybrids, TiO2/Ag | Controlled ultra-small particulate penetration; photocatalytic generation of ROS | Superior efficacy at 10-fold lower active ingredient rates; MV-Cu exhibits zero plant phytotoxicity |
| **Systemic Acquired Resistance (SAR) Inducers** | Acibenzolar-S-methyl (ASM / BTH) | Priming host salicylic acid (SA) defense pathway; up-regulates *PR* genes | Host-mediated defense; no direct chemical resistance selection; requires preventive application |
| **Microbial Biocontrol Agents** | *[[bacillus-velezensis]]* (GF267, QST713, FZB42), *B. pumilus* S2-3-2 | Multi-site lipopeptide antagonism ([[cyclic-lipopeptides]]), apoplastic niche competition, [[induced-systemic-resistance]] (ISR) | Environmentally benign; requires careful tank-mix compatibility with residual coppers |
| **Phage Therapy** | Specific lytic bacteriophages (e.g., phage cocktail KФ1) | Pathogen-specific bacterial lysis | Highly targeted; degrades rapidly under solar ultraviolet (UV) radiation; best applied in evenings |
| **Synergistic Adjuvants & Small Molecules** | Carvacrol, N-acetylcysteine, 3-indolylacetonitrile | Membrane permeabilization, ROS modulation, resensitizing copper-tolerant strains | Enhances efficacy of low-dose copper bactericides |

## References & Sources
- Osdaghi, E., et al. (2021). A centenary for bacterial spot of tomato and pepper. *Molecular Plant Pathology*, 22(9), 1500–1519. [[raw/papers/osdaghi2021centenary.pdf]]
- Marco, G. M., & Stall, R. E. (1983). Control of bacterial spot of pepper initiated by strains of *Xanthomonas campestris* pv. *vesicatoria* that differ in sensitivity to copper. *Plant Disease*, 67(7), 779–781.
- Stall, R. E., Loschke, D. C., & Jones, J. B. (1986). Linkage of copper resistance and avirulence loci on a self-transmissible plasmid in *Xanthomonas campestris* pv. *vesicatoria*. *Phytopathology*, 76(2), 240–243.
- Lamichhane, J. R., et al. (2018). Thirteen decades of antimicrobial copper compounds applied in agriculture. A review. *Agronomy for Sustainable Development*, 38(3), 28.
- Strayer-Scherer, A., et al. (2018). Advanced copper composites against copper-tolerant *Xanthomonas perforans* and tomato bacterial spot. *Phytopathology*, 108(2), 196–205.
