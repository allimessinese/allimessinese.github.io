---
title: "Lipid Biosynthesis Regulation in Bacillus subtilis"
year: 2024
role: "Bachelor Thesis"
institution: "Delft University of Technology"
summary: "Investigated the role of a poorly understood protein, YqhY, as a post-translational regulator of fatty acid synthesis in Bacillus subtilis using Gibson Assembly, GFP tagging, and fluorescence microscopy."
tags: [microbiology, molecular biology, research, thesis]
gradient: grad-4
category: research
city: "Delft"
lat: 52.0116
lng: 4.3571
image: "/assets/images/bacillus-subtilis-microscopy.jpg"
pdf: "/assets/bacillus-subtilis-thesis.pdf"
---

## What I Learned

This was my first fully independent research experience, from literature review through experimental design, data analysis, and a final presentation. Working in a department where most colleagues held PhDs meant learning quickly, asking precisely, and iterating fast. I built the MATLAB image quantification pipeline from scratch after teaching myself the basics in the first few weeks.

I also learned to **translate very complex biology into clear, accessible language.** The thesis defense required explaining malonyl-CoA feedback loops and subcellular protein dynamics to a mixed audience, and finding the right level of abstraction without losing scientific rigour was one of the most valuable skills I took from this project.

The incomplete *B. subtilis* arm was a useful lesson in research timelines: not every thread resolves within the project window, and knowing when to consolidate versus extend is a skill in itself.

## Overview

Completed in the Bokinsky Lab at TU Delft's Department of Bionanoscience (November 2023 to February 2024), my bachelor thesis focused on a protein of almost entirely unknown function called **YqhY** and its suspected role as a post-translational regulator of **fatty acid biosynthesis** in *Bacillus subtilis*.

Fatty acids are essential building blocks for bacterial membranes. Their synthesis is energetically expensive, so bacteria have evolved precise mechanisms to match production with demand. The committed step in this pathway is catalysed by **acetyl-CoA carboxylase (ACC)**, which converts acetyl-CoA into malonyl-CoA, the universal precursor for all fatty acid chain elongation. How this enzyme is regulated in gram-positive bacteria like *B. subtilis* remains largely uncharacterised, and that gap is where YqhY became interesting.

## The Protein: YqhY

YqhY belongs to the Asp23/Gls24 family and contains a domain of unknown function found in diverse bacteria. It is expressed at remarkably high levels (roughly **22,500 molecules per cell** in *B. subtilis* under standard growth conditions), suggesting a constitutive and important cellular role. Despite this abundance, its function had never been experimentally characterised.

Previous work in the lab raised a hypothesis: YqhY might act as a direct, post-translational inhibitor of ACC, switching off malonyl-CoA production when fatty acid synthesis is already saturated. My thesis set out to test this hypothesis directly.

## Approach

The core idea was to tag YqhY with a fluorescent reporter (GFP) and observe whether it forms discrete **subcellular foci** (spatially concentrated spots within the cell), and whether those foci change under conditions that perturb fatty acid metabolism. Focal localisation is a hallmark of proteins actively engaged with a molecular target; a diffuse cytoplasmic signal suggests inactivity.

I worked in two organisms: *E. coli* as a well-characterised initial model, and *B. subtilis* as the native host.

**Methods used:** Gibson Assembly, GFP2 fusion constructs, chromosomal integration, Sanger sequencing, widefield fluorescence microscopy, MATLAB-based foci quantification, antibiotic perturbation experiments.

To test pathway specificity, I compared two classes of antibiotics: drugs that block fatty acid elongation directly (causing malonyl-CoA to accumulate upstream), and drugs that cause general growth arrest without touching the fatty acid pathway. The prediction was that only the first group would increase YqhY foci.

## Results

YqhY-GFP forms **clear, discrete foci** in both organisms under standard conditions, ruling out a structural or non-specific role and pointing toward interaction with a specific molecular partner.

When fatty acid elongation was blocked with triclosan, foci fluorescence intensity increased significantly (roughly **7,500 AU compared to 4,500 AU** in untreated controls). This is the expected signature of a protein responding to malonyl-CoA accumulation: more YqhY molecules transitioning from a diffuse state into the focal, ACC-bound inhibitory state.

Critically, translation inhibitors that arrest growth without touching fatty acid metabolism did **not** increase foci intensity (roughly 1,200 AU). This ruled out a general growth-arrest response and pointed specifically to malonyl-CoA as the signal.

Overexpression with IPTG showed that 97% of cells had detectable foci, with approximately 70% localised at the cell poles, consistent with a saturated inhibitory state under excess protein.

The *B. subtilis* arm could not be completed within the 15-week window and became the starting point for my follow-on research internship.

![Thesis defense at TU Delft. Greg presenting the final slide showing GFP foci data and his written recommendation for Allegra.](/assets/images/bacillus-subtilis-defense.jpg)

## Interpretation

Taken together, the data support a model in which **YqhY acts as a post-translational feedback regulator of ACC.** When malonyl-CoA accumulates, YqhY transitions from a diffuse cytoplasmic state into a focal complex that inhibits ACC, halting further malonyl-CoA production. When the pathway runs normally, YqhY remains inactive and distributed. The focal state is visible as bright GFP spots concentrated at specific subcellular locations.

## Significance

*B. subtilis* is a major platform organism in synthetic biology, with engineered strains used to produce lipid-derived compounds ranging from biofuels to specialty chemicals. Knowing how ACC is naturally inhibited matters for designing strains that can override this feedback and push flux toward desired products. More broadly, YqhY belongs to a class of abundant but poorly characterised proteins whose roles remain unmapped; this work contributes to that annotation effort.

**PI:** Dr. Gregory Bokinsky &nbsp;·&nbsp; **Daily supervisor:** Jairus Beije &nbsp;·&nbsp; **Department:** Bionanoscience, TU Delft &nbsp;·&nbsp; Nov 2023 to Feb 2024

<a href="{{ '/assets/bacillus-subtilis-thesis.pdf' | relative_url }}" class="pdf-download-link" target="_blank" rel="noopener">Download thesis PDF</a>
