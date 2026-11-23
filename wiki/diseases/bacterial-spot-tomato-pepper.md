---
type: disease
name: "Bacterial Spot of Tomato and Pepper"
aliases: ["番茄與甜椒細菌性斑點病", "Bacterial spot", "Bacterial leaf spot", "BSTP"]
causal_agents: ["[[xanthomonas-euvesicatoria]]", "[[xanthomonas-perforans]]", "[[xanthomonas-vesicatoria]]", "[[xanthomonas-gardneri]]"]
primary_hosts: ["[[solanum-lycopersicum]]", "[[capsicum-annuum]]"]
tags: ["disease", "bacterial-disease", "foliar", "seedborne", "solanaceae", "copper-resistance"]
last_updated: 2026-11-20
---

# Bacterial Spot of Tomato and Pepper

## Overview
Bacterial spot of tomato (*[[solanum-lycopersicum]]*) and pepper (*[[capsicum-annuum]]*) is one of the most destructive and economically damaging bacterial diseases affecting field- and greenhouse-grown solanaceous crops worldwide. It is caused by a complex of four distinct species within the genus *Xanthomonas*: *[[xanthomonas-euvesicatoria]]*, *[[xanthomonas-perforans]]*, *[[xanthomonas-vesicatoria]]*, and *[[xanthomonas-gardneri]]*. Severe epidemics result in extensive foliar defoliation, blighting of flowers, blossom drop, and disfiguring lesions on developing fruit, leading to direct yield losses of 23% to 44% and catastrophic indirect losses from sunscald. The pathogens are listed on the EPPO A2 high-risk quarantine catalog (EPPO codes: XANTEU, XANTGA, XANTPF, XANTVE).

## Symptomology & Progression
- **Foliage**:
  - Initial symptoms appear as tiny (1–3 mm), dark, water-soaked, circular to angular lesions on leaves.
  - As lesions expand, centers turn necrotic, brownish-black, often surrounded by a conspicuous chlorotic halo.
  - In *[[xanthomonas-perforans]]* infections, lesions often dry and drop out, creating a characteristic "shot-hole" or perforating pattern.
  - Severe foliar infections coalesce into blighted patches, leading to scorching, chlorosis, and rapid defoliation.
- **Stems and Petioles**:
  - Elongated, dark brown to black cankers develop, weakening plant branches and predisposing them to wind breakage. Pith necrosis has also been documented in greenhouse crops (Aiello et al., 2013).
- **Fruit**:
  - On green, immature fruit, symptoms begin as small, pale green water-soaked spots with greenish-white halos that become slightly raised, blister-like or scabby (3–6 mm).
  - Spots eventually turn brown, cracked, and sunken, destroying commercial marketability.
  - Extensive foliage loss exposes fruit directly to solar radiation, causing severe **sunscald**.

## Causal Pathogen Complex
The disease is incited by four genetically distinct *Xanthomonas* lineages:

| Species (Current Consensus) | Phylogenomic Status | Historical Group | Primary Hosts | Distinctive Trait |
|---|---|---|---|---|
| *[[xanthomonas-euvesicatoria]]* | *X. euvesicatoria* pv. *euvesicatoria* | Group A | Tomato, Pepper | Non-amylolytic; model for T3SS and TALE (*avrBs2*, *avrBs3*) |
| *[[xanthomonas-perforans]]* | *X. euvesicatoria* pv. *perforans* | Group C | Tomato, Pepper | Strongly amylolytic; bacteriocins; expanding host range |
| *[[xanthomonas-vesicatoria]]* | *X. vesicatoria* | Group B | Tomato, Pepper | Amylolytic; dominant in temperate / subtropical regions |
| *[[xanthomonas-gardneri]]* | *X. hortorum* pv. *gardneri* | Group D | Tomato, Pepper | Cold-adapted; clonal global spread via seed |

## Disease Cycle & Epidemiology
1. **Seedborne Transmission & Blossom Infection**:
   - The pathogens survive in and on seed coats and internal seed tissues. Contamination levels in pepper seeds infected with *X. euvesicatoria* range from 34 to 100 CFU/g, transmitting into 16% to 39% of seed lots (Giovanardi et al., 2018).
   - Once disease is established during the flowering stage, blossoms serve as an open entrance portal for bacteria to invade ovary tissues and infest subsequent seed generations (Dutta et al., 2014).
2. **Transplant Nursery Dissemination**:
   - High planting densities, overhead sprinkler irrigation, and warm temperatures create an ideal incubator in commercial transplant greenhouses.
   - Newly infected seedlings exhibit a 5- to 7-day incubation lag before symptoms appear. Consequently, asymptomatic transplants are unwittingly shipped to open fields. Studies show that **60% to 100% of field infections are direct extensions of nursery transplant populations** (Abrahamian et al., 2019).
3. **In-Field Dispersal & Microclimate Dynamics**:
   - Splashing rain and wind-driven droplets drive intra-field spread.
   - Bacterial genetic traits influence transmission speed: strains carrying functional T3SS effector **XopJ2** disperse through tomato fields **three times faster** than non-functional mutants (Sharma et al., 2021).
   - Pathogens survive epiphytically on volunteer solanaceous weeds (*Solanum americanum*, *Physalis pubescens*, *Euphorbia heterophylla*).
4. **Spatiotemporal Foliar Infection Stages & Stomatal Egression Dynamics**:
   - In planta transcriptomics ([[in-planta-bacterial-transcriptomics]]) demonstrates that foliar infection proceeds through coordinated molecular stages (Kaur et al., 2026):
     - **Epiphytic Phase (8–24 h)**: Pathogens actively swim across the phyllosphere via flagella and methyl-accepting chemotaxis proteins, pre-arming themselves against environmental stress via anticipatory induction of the oxidative stressome (*katB*, *ahpCF*, *ohr*, *sodA*). At 24 h, c-di-GMP triggers the *ycgR* "wheel lock" brake, cellulose synthesis (*bcsABC*), and Type IV pili to establish adherent microcolonies near stomata.
     - **Early Apoplastic Phase (24 h)**: Upon stomatal entry, bacteria shut off motility, upregulate the Type III secretion system (*hrp* cluster) to deliver effectors ([[avrbs2]], *xopV*, *xopN*, *xopZ*), and deploy high-affinity nutrient scavengers (*citM*, *pstSCAB*, *cysJIH*).
     - **Late Apoplastic Phase & Egression (72 h)**: As tissues undergo water-soaking and necrosis, the bacteria adapt to hypoxia (*cioAB*) and **reactivate flagellar synthesis and chemotaxis** (*fliA*, *fliC*, *cheY*). This allows bacteria to swim out through open stomata back to the leaf surface, fueling secondary inoculum pools for rapid rain-splash dispersal across the crop canopy.

## Antimicrobial Resistance Crisis (Copper & Streptomycin)
For over half a century, the primary chemical tactic for bacterial spot has been preventive sprays of copper bactericides mixed with ethylene-bis-dithiocarbamate (EBDC / mancozeb). 
- **Copper Resistance**: First discovered in *X. euvesicatoria* in Florida in 1983 (Marco & Stall, 1983), copper resistance is mediated by self-transmissible conjugative plasmids carrying the ***copLAB* operon**, which encodes periplasmic copper oxidases and efflux transporters (see [[copper-bactericides-and-resistance]]).
- **Streptomycin Resistance**: Chromosomal mutations in *rpoB* emerged following historical agricultural antibiotic applications.
- In intensive production regions (e.g., Florida, Brazil, Taiwan), over 90% of field isolates are resistant to copper, resulting in widespread failure of conventional chemical spray programs.

## Host Resistance & Gene-for-Gene Genetics
Host resistance follows classic [[gene-for-gene-resistance]]:
- **Pepper (*Capsicum annuum*)**:
  - **Bs1**: Dominant resistance gene recognizing effector AvrBs1.
  - **Bs2**: Widely deployed CC-NB-LRR receptor conferring resistance against strains expressing [[avrbs2]]; durable because *avrBs2* is critical for bacterial virulence and fitness.
  - **Bs3**: Unique executor resistance gene encoding a flavin-dependent monooxygenase-like protein, directly activated by the promoter-binding TALE [[avrbs3]].
  - **Bs4**: TIR-NB-LRR receptor recognizing AvrBs4.
- **Tomato (*Solanum lycopersicum*)**:
  - Tomato lacks single durable dominant R-genes comparable to pepper *Bs2*. Three independent quantitative trait loci (QTLs) for resistance on chromosome 11 have been mapped from wild accessions: Hawaii 7998 (QTL-11A), PI 114490 (QTL-11B), and LA2533 (QTL-11C) (Bernal et al., 2020).
  - Transgenic expression of pepper *Bs2* in tomato confers robust field resistance against all bacterial spot xanthomonads carrying functional AvrBs2.

## Diagnostics & Molecular Detection
- **Multiplex Real-Time TaqMan PCR**: A diagnostic assay targeting a 420-bp fragment of the *hrpB7* gene simultaneously discriminates all four lineages using lineage-specific fluorogenic probes (Strayer et al., 2016).
- **Isothermal Field Assays**:
  - Recombinase polymerase amplification (RPA) allows rapid, inhibitor-tolerant detection in fields without thermocyclers.
  - Loop-mediated isothermal amplification (LAMP) targeting the *recG* gene enables point-of-care discrimination of *X. euvesicatoria*.

## Integrated Disease Management (IPM)
1. **Pathogen-Free Seed & Transplant Sanitation**:
   - Hot-water seed disinfestation (50°C for 25 min for tomato; 50°C for 30 min for pepper) or chemical disinfection.
   - Aggressive rogueing in nurseries: when a symptomatic seedling is found, rogue all seedlings within a 1- to 3-meter radius to remove latent infections (Abrahamian et al., 2021).
2. **Cultural Practices**:
   - Strict transition to drip irrigation to avoid foliar moisture and splashing.
   - Minimum 2- to 3-year crop rotations away from solanaceous plants.
3. **Advanced Alternatives to Copper**:
   - **Engineered Nanocomposites**: Multivalent copper (MV-Cu), nano-magnesium oxide (Nano-MgO), and core-shell copper (CS-Cu) achieve high bactericidal efficacy at 10-fold lower active ingredient concentrations with no phytotoxicity.
   - **Systemic Acquired Resistance (SAR)**: Foliar applications of acibenzolar-S-methyl (ASM / BTH) prime plant defense genes (*PR-1*, *PR-2*).
   - **Biocontrol & Phage Therapy**: Multi-site antagonists like *[[bacillus-velezensis]]* GF267 combine rapid in vitro bactericidal activity (eradicating viable *X. perforans* in broth within 5 hours), preemptive nutritional niche competition ($\text{NOI} = 0.8\text{--}1.0$), and root-mediated [[induced-systemic-resistance]] that triggers accelerated peroxidase and polyphenoloxidase bursts (Mates et al., 2019). When combined with lytic bacteriophages (e.g., KФ1), biocontrol provides synergistic control when integrated into IPM schedules.

## References & Sources
- Kaur, A., Ramamoorthy, S., Ghosh, P., Weis, K., & Potnis, N. (2026). Spatiotemporal coordination of virulence, metabolism, and stress responses shapes infection dynamics of *Xanthomonas perforans*. *Applied and Environmental Microbiology*, 92(8), e00681-26. [[raw/papers/kaur2026spatiotemporal.pdf]]
- Mates, A. K., Pontes, N. C., & Halfeld-Vieira, B. A. (2019). *Bacillus velezensis* GF267 as a multi-site antagonist for the control of tomato bacterial spot. *Biological Control*, 137, 104013. [[raw/papers/mates2019bacillus.pdf]]
- Osdaghi, E., et al. (2021). A centenary for bacterial spot of tomato and pepper. *Molecular Plant Pathology*, 22(9), 1500–1519. [[raw/papers/osdaghi2021centenary.pdf]]
- Potnis, N., et al. (2015). Bacterial spot of tomato and pepper: diverse *Xanthomonas* species with a wide variety of virulence factors posing a worldwide challenge. *Molecular Plant Pathology*, 16(9), 907–920. [[raw/papers/potnis2015bacterial.pdf]]
- Abrahamian, P., et al. (2021). Dynamics and spread of bacterial spot epidemics in tomato transplants grown for field production. *Plant Disease*, 105(3), 566–575.
- Strayer, A., et al. (2016). A multiplex real-time PCR assay differentiates four *Xanthomonas* species associated with bacterial spot of tomato. *Plant Disease*, 100(8), 1660–1668.
- Strayer-Scherer, A., et al. (2018). Advanced copper composites against copper-tolerant *Xanthomonas perforans* and tomato bacterial spot. *Phytopathology*, 108(2), 196–205.
