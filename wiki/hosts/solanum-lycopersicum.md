---
type: host
scientific_name: "Solanum lycopersicum"
common_name: "Tomato"
family: "Solanaceae"
aliases: ["番茄", "Lycopersicon esculentum", "Tomato", "西紅柿"]
major_pathogens: ["[[xanthomonas-euvesicatoria]]", "[[xanthomonas-perforans]]", "[[xanthomonas-vesicatoria]]", "[[xanthomonas-gardneri]]"]
major_diseases: ["[[bacterial-spot-tomato-pepper]]"]
tags: ["host", "crop", "solanaceae", "model-host"]
last_updated: 2026-11-20
---

# Solanum lycopersicum

## Overview
*Solanum lycopersicum* (cultivated tomato; formerly *Lycopersicon esculentum*) is one of the world's most widely grown and economically significant vegetable crops. In addition to its agricultural value, tomato serves as a premier dicot model organism in Molecular Plant-Microbe Interactions (MPMI), genetics, fruit ripening biology, and plant defense signaling.

## Agronomic Significance & Production
- Cultivated across tropical, subtropical, and temperate zones in open-field and protected greenhouse systems.
- Susceptible to a broad spectrum of pathogens, including bacteria, fungi, oomycetes, and viruses, necessitating intense integrated disease management.

## Interactions with Bacterial Spot (*Xanthomonas* Complex)
- **Causal Agents**: In nature, tomato foliage and fruit are vulnerable to all four bacterial spot xanthomonads:
  - *[[xanthomonas-perforans]]* (predominant in modern warm, open-field production systems)
  - *[[xanthomonas-euvesicatoria]]*
  - *[[xanthomonas-vesicatoria]]*
  - *[[xanthomonas-gardneri]]*
- **Symptom Profile**: Causes water-soaked lesions that brown and necrose, shot-hole foliar perforations, severe defoliation, and fruit scabbing (see [[bacterial-spot-tomato-pepper]]).

## Immune System & Resistance Genetics
- **Receptor Kinases & PRRs**: Tomato possesses cell-surface pattern recognition receptors (e.g., FLS2, CORE) that recognize conserved bacterial PAMPs (flagellin flg22, cold-shock protein csp22) triggering pattern-triggered immunity (PTI).
- **Effector-Triggered Immunity (ETI) & R-genes**:
  - **Bs4**: An intracellular TIR-NB-LRR resistance gene that recognizes the bacterial spot effector AvrBs4 (derived from *X. euvesicatoria*), triggering an arrest of pathogen multiplication.
  - **Rxv / Rx3**: Hypersensitivity locus introgressed from wild tomato relatives (*Solanum pimpinellifolium* Hawaii 7998) conferring hypersensitive resistance against race T3 of *X. perforans*.
  - **Transgenic Resistance (Bs2 Introgression)**: While wild tomatoes lack a direct homolog to the pepper *Bs2* NB-LRR gene, transgenic tomato expressing pepper *Bs2* confers robust field resistance against xanthomonads harboring [[avrbs2]].
  - Other landmark MPMI defense systems in tomato include Pto/Prf (recognizing *Pseudomonas syringae* effectors AvrPto and AvrPtoB) and Cf-4/Cf-9 (recognizing *Cladosporium fulvum* apoplastic effectors).
- **Biocontrol-Mediated Systemic Immunity & Dual Pest/Pathogen Defense**:
  - Inoculation with beneficial bacilli, notably *[[bacillus-thuringiensis]]* (Bt) and *[[bacillus-velezensis]]*, stimulates tomato systemic defenses.
  - Pre-treatment with Bt primes the tomato apoplastic **Reactive Oxygen Species (ROS) oxidative burst**, amplifying flg22- and EIX-elicited ROS generation by up to 300% (measured via HRP-luminol chemiluminescence).
  - Concurrently coordinates the expression of salicylic acid markers (***PR1a***, ***PR1b***, ***Pi-1***) and jasmonate/ethylene markers (***Pti-5***, ***ERF1***, ***LoxD***), suppressing *[[xanthomonas-euvesicatoria]]* bacterial populations by ~40% while controlling fungal blights (*Botrytis cinerea*, powdery mildew) and sap-feeding pests (*Bemisia tabaci*, *Tuta absoluta*).
  - Significantly, this defense priming uncouples the growth-defense tradeoff, resulting in increased node formation and higher total marketable fruit yields (Gupta et al., 2024).

## Model Cultivars & Wild Germplasm
- **Model Research Cultivars**: Moneymaker, Heinz 1706 (genome reference), Castlemart, Rio Grande-PtoR.
- **Differential Cultivars for Xanthomonas Spot**: Bonny Best (susceptible), Hawaii 7998 (differential resistance bearer).
- **Wild Relatives**: *Solanum pimpinellifolium*, *Solanum pennellii*, *Solanum habrochaites* (critical germplasm donors for introgressing disease resistance loci).

## References & Sources
- Gupta, R., Keppanan, R., Leibman-Markus, M., Matveev, S., Rav-David, D., Shulhani, R., Elad, Y., Ment, D., & Bar, M. (2024). *Bacillus thuringiensis* promotes systemic immunity in tomato, controlling pests and pathogens and promoting yield. *Food Security*, 16(3), 675–690. [[raw/papers/gupta2024bacillus.pdf]]
- Potnis, N., et al. (2015). Bacterial spot of tomato and pepper: diverse *Xanthomonas* species with a wide variety of virulence factors posing a worldwide challenge. *Molecular Plant Pathology*, 16(9), 907–920. [[raw/papers/potnis2015bacterial.pdf]]
- The Tomato Genome Consortium. (2012). The tomato genome sequence provides insights into fleshy fruit evolution. *Nature*, 485(7400), 635–641.
- Tai, T. H., et al. (1999). Expression of the *Bs2* pepper gene confers resistance to *Xanthomonas campestris* pv. *vesicatoria* in tomato. *Proceedings of the National Academy of Sciences*, 96(24), 14153–14158.
