---
type: host
scientific_name: "Citrullus lanatus"
common_name: "Watermelon"
family: "Cucurbitaceae"
aliases: ["西瓜", "Watermelon", "Citrullus vulgaris"]
major_pathogens: ["[[acidovorax-citrulli]]", "Fusarium oxysporum f. sp. niveum", "Colletotrichum orbiculare", "Podosphaera xanthii"]
major_diseases: ["[[bacterial-fruit-blotch]]"]
tags: ["host", "crop", "cucurbitaceae", "pti-model"]
last_updated: 2026-11-20
---

# Citrullus lanatus

## Overview
*Citrullus lanatus* (cultivated watermelon) is an economically vital annual vine belonging to the gourd family Cucurbitaceae. Originating from northeastern Africa, watermelon is now grown globally across tropical, subtropical, and warm temperate regions for its large, sweet, edible fruits. In molecular plant pathology, *C. lanatus* serves as a primary model for investigating cucurbit vascular wilt diseases and seedborne bacterial infections, most notably **[[bacterial-fruit-blotch]] (BFB)** caused by *[[acidovorax-citrulli]]*.

## Agronomic Significance & Production
- Grown extensively in open fields and protected tunnel/greenhouse structures. In major producing countries (including China, Turkey, India, and Brazil), watermelon represents one of the highest-volume horticultural commodities.
- Cultivars range from large diploid seeded varieties (e.g., cv. 華寶 / Hua-Bao, Charleston Gray, Crimson Sweet) to triploid seedless hybrids.
- Highly vulnerable to seedborne bacterial outbreaks and soil-borne fungal pathogens (*Fusarium oxysporum* f. sp. *niveum*), often requiring grafting onto resistant cucurbit rootstocks (e.g., bottle gourd *Lagenaria siceraria* or squash hybrids *Cucurbita maxima* $\times$ *C. moschata*).

## Interactions with Bacterial Fruit Blotch (*Acidovorax citrulli*)
- **Primary Target Tissue**: All aerial tissues are susceptible. Cotyledons show water-soaked lesions that rapidly collapse seedlings. Rinds of developing fruits develop dark, expanding oil-soaked blotches that crack and rot (see [[bacterial-fruit-blotch]]).
- **Pathogen Transmission**: Contaminated seeds act as the primary disease vehicle, carrying bacteria internally beneath the seed coat.

## Cucurbit Immune System & PTI Dynamics
Watermelon possesses an active, inducible innate immune system centered on **[[pamp-triggered-immunity]] (PTI)** (Chang et al., 2019):
1. **PAMP Perception**:
   - Watermelon leaf and cotyledon cells express pattern recognition receptors (PRRs) that perceive conserved bacterial elicitors, including flagellin peptide **flg22** from *Acidovorax* and *Pseudomonas*.
2. **The Oxidative Burst (NADPH Oxidase / RBOH)**:
   - Perception of *A. citrulli* or flg22 triggers apoplastic generation of reactive oxygen species (ROS) mediated by plant plasma membrane-bound **NADPH oxidases** (Respiratory Burst Oxidase Homologs, RBOHs).
   - In unprimed watermelon leaves, the ROS burst elicited by *A. citrulli* is modest ($\sim 313$-fold above baseline).
   - Co-treatment with plant-beneficial *[[bacillus-velezensis]]* / *B. amyloliquefaciens* (strains PMB04 and PMB05) massively intensifies this oxidative burst by **up to 2,733-fold within 1 hour**, accelerating antimicrobial cytotoxicity and vascular signaling.
   - Pharmacological inhibition of plant NADPH oxidases using **diphenyleneiodonium chloride (DPI, 80 $\mu\text{M}$)** abolishes this ROS surge and completely reverses the biocontrol efficacy of *Bacillus*, increasing watermelon leaf spot severity from 11.1% to 91.1%, proving that plant-derived ROS is essential for resistance execution.
3. **Callose Papillae Fortification**:
   - Activated watermelon mesophyll cells synthesize $\beta$-1,3-glucan polymer (**callose**) via callose synthases.
   - Aniline blue fluorometric microscopy reveals dense callose deposition around stomata and mesophyll cell walls within 8 hours of *Bacillus* priming, forming a physical barrier that prevents *A. citrulli* intercellular multiplication.

## References & Sources
- Chang, C. J., Wu, Y. H., Lin, Y. H., Deng, W. L., & Lin, C. H. (2019). Intensification of PAMP-triggered immunity in watermelon by *Bacillus* spp. strains as a strategy for controlling bacterial fruit blotch disease. *Journal of Plant Medicine*, 61(1), 39–48. [[raw/papers/chang2019intensification.pdf]]
- Burdman, S., & Walcott, R. (2012). *Acidovorax citrulli*: generating basic and applied knowledge to tackle a global threat to the cucurbit industry. *Molecular Plant Pathology*, 13(8), 805–815.
- Guo, S., et al. (2013). The draft genome of watermelon (*Citrullus lanatus*) and resequencing of 20 diverse accessions. *Nature Genetics*, 45(1), 51–58.
