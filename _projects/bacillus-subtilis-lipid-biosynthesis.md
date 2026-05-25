---
title: "Lipid Biosynthesis Regulation in Bacillus subtilis - Bachelor Thesis"
year: 2024
role: "Bachelor Thesis Student"
institution: "Delft University of Technology"
summary: "Investigated the role of a poorly understood protein, YqhY, as a post-translational regulator of fatty acid synthesis in Bacillus subtilis - using Gibson Assembly, GFP tagging, and fluorescence microscopy."
tags: [microbiology, molecular biology, research, thesis]
gradient: grad-4
category: research
city: "Delft"
lat: 52.0116
lng: 4.3571
image: "/assets/images/bacillus-subtilis-microscopy.jpg"
---

## Overview

My bachelor thesis - completed in the [Bokinsky Lab](https://www.bokinksylab.nl) at TU Delft's Department of Bionanoscience between November 2023 and February 2024 - focused on a protein of almost entirely unknown function called **YqhY**, and its suspected role as a post-translational regulator of **fatty acid biosynthesis** in *Bacillus subtilis*.

Fatty acids are essential building blocks for bacterial membranes. Their synthesis is energetically expensive, so bacteria have evolved precise mechanisms to match production with demand. The committed step in this pathway is catalysed by **acetyl-CoA carboxylase (ACC)**, which converts acetyl-CoA into malonyl-CoA - the universal precursor for all fatty acid chain elongation. How this enzyme is regulated in gram-positive bacteria like *B. subtilis* remains largely uncharacterised, and that gap is where YqhY became interesting.

## The Protein: YqhY

YqhY belongs to the Asp23/Gls24 family and contains a **DUF322 domain** - a domain of unknown function found in diverse bacteria. It is expressed at remarkably high levels: roughly **22,500 molecules per cell** in *B. subtilis* under standard growth conditions, suggesting it plays a constitutive and important cellular role. Despite this abundance, its function had never been experimentally characterised.

Previous transcriptomic and computational work in the lab had raised a hypothesis: YqhY might act as a direct, post-translational inhibitor of ACC, switching off malonyl-CoA production when fatty acid synthesis is already saturated. If true, it would represent a novel regulatory mechanism for a critical metabolic checkpoint.

My thesis set out to test this hypothesis directly.

## Approach

The core idea was to tag YqhY with a fluorescent reporter (GFP) and observe whether it forms discrete **subcellular foci** - spatially concentrated spots within the cell - and whether those foci change under conditions that perturb fatty acid metabolism. Focal localisation is a hallmark of proteins that are actively engaged with a molecular target; diffuse cytoplasmic distribution would suggest inactivity or a structural/chaperone role.

Two model organisms were used:

- ***Escherichia coli* NCM3722** - a well-characterised model with conserved fatty acid pathway enzymes, used as a proxy for initial characterisation
- ***Bacillus subtilis* 168** - the native organism, where YqhY's biological role would ultimately matter

### Construct Design and Cloning

I designed plasmid constructs that fused **YqhY to GFP2** (an enhanced GFP variant optimised for bacterial imaging):

- **pBbE5k_yqhY_GFP2** for *E. coli* expression (IPTG-inducible, strong promoter)
- **pDR111_yqhY_GFP2** for chromosomal integration at the *amyE* locus in *B. subtilis* (IPTG-inducible)

All constructs were assembled using **Gibson Assembly** and verified by Sanger sequencing. Successful integration into the *B. subtilis* chromosome at *amyE* was confirmed by loss of amylase activity on starch plates.

### Fluorescence Microscopy

Imaging was performed on an **Olympus IX81F-ZDC2** widefield fluorescence microscope at 100x magnification (oil immersion). Cells were grown to mid-exponential phase, transferred to agarose pads, and imaged immediately to preserve native localisation patterns.

Foci were detected and quantified semi-automatically using custom **MATLAB scripts** that identified fluorescence intensity peaks above background in individual cells. Metrics extracted included foci count per cell, mean intensity, and localisation pattern (polar, septal, or diffuse cytoplasmic).

### Antibiotic Perturbations

To test whether YqhY foci respond to changes in the fatty acid pathway, I treated cells with a panel of antibiotics targeting different steps:

| Antibiotic | Target | Prediction |
|---|---|---|
| Triclosan | FabI (enoyl-ACP reductase) | Blocks fatty acid elongation - causes malonyl-CoA to accumulate upstream |
| Cerulenin | FabB/FabF (condensing enzymes) | Blocks elongation at condensation step |
| Mupirocin | IleRS (isoleucyl-tRNA synthetase) | Blocks translation - growth arrest |
| Chloramphenicol | 50S ribosome | Blocks translation - growth arrest |

The key comparison was between drugs that specifically perturb the **fatty acid pathway** (triclosan, cerulenin) versus drugs that cause **general growth arrest** without touching fatty acid metabolism (mupirocin, chloramphenicol). If YqhY foci increase only in the former group, it would support a malonyl-CoA-specific response.

## Results

### YqhY Forms Distinct Foci

The first result was confirmatory but important: YqhY-GFP2 forms **clear, discrete foci** in both *E. coli* and *B. subtilis* under standard growth conditions. This ruled out a purely structural or non-specific role and was consistent with YqhY interacting with a specific molecular partner - likely ACC.

Localisation differed between organisms. In *E. coli*, foci were concentrated at the **septal region** (the cell division plane). In *B. subtilis*, they appeared primarily at the **cell poles**.

### IPTG Overexpression Shifts Localisation to the Poles

When YqhY-GFP2 expression was induced with IPTG (increasing protein levels beyond the endogenous ~22,500 molecules/cell baseline), foci became more prominent and shifted distribution: **97% of cells had detectable foci**, with approximately 70% of foci localised at the poles. This suggests that polar localisation may reflect a saturated or inhibitory state, where excess YqhY cannot all be engaged at the septum.

### Triclosan Increases Foci Intensity

The most informative result came from the antibiotic panel. Triclosan treatment - which blocks FabI and causes malonyl-CoA to accumulate upstream of the block - led to a significant increase in foci fluorescence intensity: roughly **~7,500 AU compared to ~4,500 AU** in untreated controls.

This is the expected signature of a protein that responds to malonyl-CoA accumulation. When fatty acid elongation is blocked and malonyl-CoA builds up, more YqhY molecules transition from a diffuse cytoplasmic state into the focal (ACC-bound, inhibitory) state - reducing intensity at ACC to prevent further malonyl-CoA accumulation.

### Translation Inhibitors Do Not Increase Foci

Critically, neither mupirocin nor chloramphenicol - both of which arrest growth without targeting the fatty acid pathway - increased foci intensity. Values in treated cells were roughly **~1,200 AU**, well below the control baseline.

This was the key negative control. It demonstrated that the triclosan effect was **not simply a consequence of growth arrest** or global metabolic slowdown. The response was specific to perturbations in the fatty acid pathway, supporting the model that YqhY directly senses the status of malonyl-CoA availability.

### B. subtilis Experiments Remained Inconclusive

The *B. subtilis* experiments could not be completed within the 15-week project window. While constructs were successfully integrated into the chromosome, consistent imaging conditions were not achieved before the project deadline. This became the starting point for my follow-on research internship, where I continued this work through June 2024.

## Interpretation

Taken together, the data support a model in which **YqhY acts as a post-translational feedback regulator of ACC**:

- When fatty acid synthesis is running normally, YqhY exists in a diffuse cytoplasmic state - ACC is active and produces malonyl-CoA freely.
- When malonyl-CoA accumulates (either because elongation is blocked or because synthesis has outpaced demand), YqhY is recruited into a focal complex with ACC - inhibiting it and halting further malonyl-CoA production.
- This focal (inhibitory) state is visible as bright GFP foci concentrated at specific subcellular locations.

The model positions YqhY as a **molecular sensor and switch** - translating malonyl-CoA abundance into ACC activity through direct protein-protein interaction and subcellular relocalisation.

## Significance

Understanding how bacteria regulate fatty acid synthesis matters both fundamentally and practically. *B. subtilis* is a major platform organism in synthetic biology and industrial biotechnology - engineered strains are used to overproduce lipid-derived compounds ranging from biofuels to specialty chemicals. Knowing how ACC is naturally inhibited is critical for designing strains that can override this feedback and push flux toward desired products.

Beyond engineering, YqhY represents a class of poorly-characterised DUF proteins whose abundance suggests functional importance but whose roles remain unmapped. This work contributes to that annotation effort.

## What I Learned

This project was my first independent research experience - from literature review through experimental design to data analysis and presentation. Working in a department where most colleagues held PhDs meant I had to learn quickly, ask precisely, and iterate fast. The MATLAB image analysis pipeline was entirely new to me; I wrote the quantification scripts from scratch after teaching myself the basics during the first few weeks.

The incomplete *B. subtilis* arm was a useful lesson in research timelines: not every thread resolves within the project window, and knowing when to consolidate findings versus when to extend is a skill in itself.

**Duration:** November 2023 - February 2024  
**Supervisor:** Dr. Gregory Bokinsky  
**PI:** Jaïrus Beije  
**Department:** Bionanoscience, TU Delft
