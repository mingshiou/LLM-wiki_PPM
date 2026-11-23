---
type: molecular-biology
category: "effector"
aliases: ["AvrBs3", "TALE AvrBs3", "TAL effector AvrBs3"]
organism: "[[xanthomonas-euvesicatoria]]"
target_host_proteins: ["upa20 promoter", "Bs3 promoter"]
corresponding_r_gene: ["[[bs3]]"]
tags: ["molecular-biology", "effector", "tale", "t3ss", "transcription-factor", "executor-r-gene"]
last_updated: 2026-11-20
---

# AvrBs3

## Overview
**AvrBs3** is the seminal prototype of the **Transcription Activator-Like Effector (TALE)** family, delivered by *[[xanthomonas-euvesicatoria]]* through its Type III Secretion System into the nuclei of host plant cells. In susceptible plants, AvrBs3 mimics eukaryotic transcription factors to hijack the host transcriptional machinery, inducing plant cell hypertrophy (swelling and enlargement) to favor bacterial colonization. In resistant pepper (*[[capsicum-annuum]]*), AvrBs3 inadvertently triggers lethal programmed cell death by transcriptionally turning on the "executor" resistance gene **Bs3**.

## Function & Biochemical Activity
- **Structural Architecture**:
  - **N-terminal Translocation Domain**: Directs effector secretion and translocation through the bacterial T3SS apparatus.
  - **Central Repeat Domain**: Contains 17.5 tandem repeats of a highly conserved 34-amino-acid motif. Residues at positions 12 and 13 within each repeat are hypervariable—known as **Repeat-Variable Diresidues (RVDs)**—which dictate base-specific binding to major groove sequences of host DNA:
    - `NI` $\rightarrow$ Adenine (A)
    - `HD` $\rightarrow$ Cytosine (C)
    - `NG` $\rightarrow$ Thymine (T)
    - `NN` $\rightarrow$ Guanine / Adenine (G/A)
  - **C-terminal Functional Domain**: Contains canonical eukaryotic **Nuclear Localization Signals (NLS)** that import the protein into the plant nucleus, followed by an acidic **Activation Domain (AD)** that recruits plant RNA polymerase II transcription initiation complexes.

## Host Interaction & Target
- **Susceptibility Target (*upa20*)**: In susceptible hosts, AvrBs3 specifically binds an effector-binding element (EBE) in the promoter of the host gene *upa20* (an upregulation of *AvrBs3*-dependent gene), which encodes a basic helix-loop-helix (bHLH) master transcription factor.
- **Pathological Consequence**: Activation of *upa20* orchestrates downstream auxinic and cell-expansion pathways, culminating in massive hypertrophy of mesophyll cells. This creates the visible blister-like, water-soaked pustules characteristic of *X. euvesicatoria* infections, providing an expanded apoplastic niche for bacterial colonization.

## Host Immune Recognition (Executor Resistance Paradigm)
- **Executor R-Gene Mechanism**:
  - Rather than encoding a classical intracellular NB-LRR sensor, the pepper resistance gene **Bs3** acts as an **executor resistance gene**.
  - The *Bs3* promoter evolved an EBE (`UPPAvg`) that perfectly matches the DNA-binding specificity encoded by the RVD array of AvrBs3.
  - Upon translocation into the host nucleus, AvrBs3 binds the *Bs3* promoter and activates transcription of the *Bs3* coding region, which produces a flavin-dependent monooxygenase-like protein.
  - Accumulation of the Bs3 protein immediately triggers an explosive hypersensitive response (HR), halting further bacterial ingress.
- **Biotechnological Legacy**: The discovery of the modular AvrBs3 RVD DNA-recognition code laid the conceptual and mechanistic foundation for engineered TALEs and TALEN (TALE nuclease) genome editing technology.

## References & Sources
- Potnis, N., et al. (2015). Bacterial spot of tomato and pepper: diverse *Xanthomonas* species with a wide variety of virulence factors posing a worldwide challenge. *Molecular Plant Pathology*, 16(9), 907–920. [[raw/papers/potnis2015bacterial.pdf]]
- Boch, J., et al. (2009). Breaking the code of DNA binding specificity of TAL-type III effectors. *Science*, 326(5959), 1509–1512.
- Kay, S., et al. (2007). A bacterial effector acts as a plant transcription factor and induces a cell expansion gene. *Science*, 318(5850), 648–651.
- Römer, P., et al. (2007). Plant pathogen recognition by the pepper *Bs3* protein requires transcription of the *Bs3* gene. *Science*, 318(5848), 261–263.
