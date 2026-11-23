---
type: concept
name: "Gene-for-Gene Resistance"
aliases: ["基因對基因抗性", "Flor's hypothesis", "Gene-for-gene hypothesis", "GfG model"]
tags: ["concept", "immunity", "eti", "genetics", "r-gene", "avr-gene"]
last_updated: 2026-11-20
---

# Gene-for-Gene Resistance

## Overview
The **Gene-for-Gene (GfG) Hypothesis**, originally formulated by Harold H. Flor in the 1940s through his studies on flax rust (*Melampsora lini* on *Linum usitatissimum*), is one of the most foundational concepts in plant pathology and molecular plant-microbe interactions. The model posits that for each dominant or semi-dominant gene conditioning resistance in the host plant (*R* gene), there is a corresponding specific gene conditioning avirulence in the pathogen (*Avr* gene). Resistance is only manifested when both complementary genes are present.

## Classical Flor Matrix
The genetic outcome of host-pathogen interactions is governed by the presence or absence of functional alleles:

| | Pathogen: *Avr* (Avirulent) | Pathogen: *avr* (Virulent allele / mutant) |
|---|---|---|
| **Host: *R* (Resistant)** | **Incompatible (Resistance / HR)** | Compatible (Disease) |
| **Host: *r* (Susceptible)** | Compatible (Disease) | Compatible (Disease) |

- **Incompatible interaction**: Pathogen recognition triggers localized programmed cell death (the **Hypersensitive Response**, HR), rapid generation of reactive oxygen species (ROS), cell wall fortification, and expression of pathogenesis-related (PR) proteins, arresting pathogen proliferation.
- **Compatible interaction**: If either the host lacks the specific *R* gene ($r$) or the pathogen carries a non-recognized allele or deletion ($avr$), disease ensues.

## Molecular Mechanisms of GfG Perception
In the modern molecular era, Flor's genetic abstraction has been elucidated as diverse biochemical mechanisms of **Effector-Triggered Immunity (ETI)**:

1. **Direct Receptor-Ligand Interaction**:
   - The host NLR (Nucleotide-binding Leucine-rich Repeat) receptor binds directly to the pathogen effector (e.g., rice Pi-ta directly binding *Magnaporthe oryzae* AVR-Pita).
2. **Indirect Guard and Decoy Models**:
   - The host NLR monitors the integrity or modification state of an endogenous host virulence target ("guardee") or a specialized structural mimic ("decoy"). When the pathogen effector cleaves or phosphorylates the target, the NLR detects this alteration and triggers HR (e.g., tomato Pto/Prf system).
3. **Transcriptional Executor Model**:
   - Distinct from NLRs, executor resistance genes encode cytotoxic proteins under the control of promoters containing specific effector-binding elements (EBEs). When a modular bacterial Transcription Activator-Like Effector (TALE) binds the promoter, it directly activates expression of the killer gene (e.g., the pepper **Bs3** gene activated by *[[xanthomonas-euvesicatoria]]* **[[avrbs3]]**).

## Paradigmatic MPMI Case Study: Pepper vs. *Xanthomonas*
The solanaceous pathosystem featuring *[[capsicum-annuum]]* and the bacterial spot complex illustrates both classical and cutting-edge facets of the gene-for-gene model:
- **Pepper *Bs1* vs. AvrBs1**: Classical single dominant R-gene interaction.
- **Pepper *Bs2* vs. [[avrbs2]]**:
  - Encodes a CC-NB-LRR receptor.
  - AvrBs2 is an essential virulence factor with glycerophosphoryl diester phosphodiesterase activity.
  - Pathogen strains that mutate or drop *avrBs2* escape *Bs2* recognition, but suffer a major fitness penalty (10- to 100-fold reduction in apoplastic bacterial load). Hence, *Bs2* provides durable field resistance.
- **Pepper *Bs3* vs. [[avrbs3]]**:
  - The premier example of an executor R-gene, where the effector's own transcription factor activity turns on host defense suicide mechanisms.

## Evolutionary Dynamics & R-Gene Pyramiding
- **Selection Pressure & Virulence Evolution**: Monogenic deployment of single *R* genes creates strong selective pressure in the field, rapidly selecting for rare *Xanthomonas* mutants harboring single amino acid substitutions, transposon insertions, or deletions in the matching *avr* locus.
- **Resistance Pyramiding**: Combining multiple non-allelic *R* genes (e.g., stacking *Bs2* + quantitative resistance loci) forces pathogens to undergo multiple simultaneous loss-of-function mutations in essential virulence factors, dramatically reducing the likelihood of resistance breakdown.

## References & Sources
- Flor, H. H. (1971). Current status of the gene-for-gene concept. *Annual Review of Phytopathology*, 9(1), 275–296.
- Potnis, N., et al. (2015). Bacterial spot of tomato and pepper: diverse *Xanthomonas* species with a wide variety of virulence factors posing a worldwide challenge. *Molecular Plant Pathology*, 16(9), 907–920. [[raw/papers/potnis2015bacterial.pdf]]
- Jones, J. D. G., & Dangl, J. L. (2006). The plant immune system. *Nature*, 444(7117), 323–329.
- Römer, P., et al. (2007). Plant pathogen recognition by the pepper *Bs3* protein requires transcription of the *Bs3* gene. *Science*, 318(5848), 261–263.
