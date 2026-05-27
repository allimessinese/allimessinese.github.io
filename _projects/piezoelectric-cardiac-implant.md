---
title: "Piezoelectric Cardiac Implant"
year: 2025
role: "Project Manager"
institution: "UC Berkeley"
summary: "Led a cross-functional bioengineering team at UC Berkeley to design and validate a piezoelectric PVDF implant that converts cardiac motion into electrical stimulation to promote tissue regeneration after myocardial infarction."
tags: [biomedical engineering, cardiac, piezoelectric, tissue engineering, UC Berkeley]
gradient: grad-1
category: research
featured: true
city: "Berkeley"
lat: 37.8716
lng: -122.2727
image: "/assets/images/piezoelectric-team.jpg"
image_position: "center 30%"
pdf: "/assets/piezoelectric-capstone-report.pdf"
links:
  - label: "Coleman Fung Institute"
    url: "https://funginstitute.berkeley.edu"
  - label: "UC Berkeley Bioengineering"
    url: "https://bioeng.berkeley.edu"
---

## What I Learned

This project was where systems thinking became a practical requirement rather than an abstract concept. As Project Manager across a nine-month capstone, I was responsible for keeping four distinct workstreams (materials characterisation, mechanical engineering, electronics, and cell biology) moving together on a single shared timeline. Each one had different cadences, different failure modes, and different definitions of progress. Holding them in coordination without collapsing into micromanagement was the central challenge.

The other thing this project taught me was how to work at the interface between engineering and biology. The biological experiments placed constraints on the engineering design: the device had to fit inside a standard cell culture incubator, maintain sterility, and avoid thermal damage to cells. Every design decision had a downstream biological implication, and understanding those implications well enough to make good engineering trade-offs required genuinely learning the biology, not just deferring to the team members who knew it.

I also learned what it means to validate a hypothesis rigorously. The stretch system achieving 9.1% strain, within the physiological range of 5 to 15% experienced by cardiomyocytes, was not a result we assumed. It was a result we measured, characterised, and confirmed. That discipline of grounding every claim in evidence carried through the whole project.

## The Problem

Cardiovascular diseases are the leading cause of death worldwide, responsible for approximately 17.9 million deaths annually. When a myocardial infarction occurs, the affected cardiomyocytes die and are replaced by non-contractile fibrotic scar tissue. Unlike other tissues, the heart has almost no regenerative capacity in adult mammals. The scar weakens the heart's pumping function and increases the risk of arrhythmia and heart failure.

Existing treatments manage symptoms and restore blood flow but do not reverse the underlying cardiomyocyte loss. Stem cell therapies have shown promise but face persistent problems: low cell engraftment rates, immune rejection, and limited functional integration with native cardiac tissue.

## The Hypothesis

Electrical stimulation is known to activate voltage-gated ion channels in cardiomyocytes, driving calcium influx that triggers proliferation, structural maturation, and contractility. It also upregulates cardiac transcription factors and enhances extracellular matrix remodelling. The question our project set out to answer was whether a self-powered implant could deliver that stimulation continuously, without batteries or external wires, by harvesting energy directly from the motion of the beating heart.

The material we built around was **polyvinylidene difluoride (PVDF)**, a biocompatible, flexible piezoelectric polymer. When mechanically deformed, PVDF generates a localised electrical potential. A thin PVDF film placed on the infarct region of the heart would undergo cyclic deformation with every heartbeat, generating continuous electrical stimulation to the surrounding tissue without any external power source.

## The Device

The core engineering challenge was not the film itself but building a platform that could validate it. To test whether PVDF-generated electrical stimulation promotes cardiomyocyte proliferation, we needed to recreate the mechanical environment of a beating heart in a controlled laboratory setting, running continuously, inside a standard cell culture incubator.

We designed and built a **custom automated stretch system** from the ground up:

- A **PDMS (polydimethylsiloxane) membrane** serves as the flexible substrate, bonded to a 3D-printed acrylic chamber
- A **solenoid valve** controlled by an **Arduino microcontroller** modulates pressurised airflow to inflate and deflate the membrane cyclically
- A **ramped frequency protocol** starts at 0.2 Hz and increases to 1 Hz over four hours, mimicking progressive cardiomyocyte adaptation and reducing the risk of cellular detachment
- The entire assembly is **compact and incubator-compatible**, maintaining sterile conditions with all electronics housed externally
- The platform supports **parallel testing** across a standard 6-well plate format

<div class="project-video-wrap">
  <video controls playsinline>
    <source src="{{ '/assets/videos/piezoelectric-stretch-demo.mp4' | relative_url }}" type="video/mp4">
  </video>
</div>

## Results

**Measured strain: 9.1%.** The stretch system delivered a strain output of 9.1% to the PVDF film during cyclic actuation, falling within the physiological range of 5 to 15% experienced by cardiomyocytes during native cardiac contraction. This confirmed that the platform replicates the mechanical conditions required to generate physiologically relevant piezoelectric stimulation.

**Material characterisation.** Differential Scanning Calorimetry (DSC) confirmed the biocompatibility and thermal stability of the PVDF film and adhesive materials. The characterisation established the material's suitability for long-term implantation and for *in vitro* culture environments.

**Biological testing.** Initial biocompatibility experiments used primary mouse myoblasts, followed by hiPSC-derived cardiomyocytes (hiPSC-CMs). Cell viability under both static and stretch conditions was confirmed. Full cardiomyocyte contractility experiments were constrained by cell availability, and scaling down to 24-well plate formats is identified as the next step for achieving the cell densities needed to observe spontaneous beating.

**Design validation.** All six functional requirements were met: biocompatible materials, stable PVDF characterisation, continuous cyclic stretching at physiological frequency, incubator compatibility, parallel experimental throughput, and physiologically relevant strain levels.

## My Role

I led the project as **Project Manager**, coordinating across materials science, mechanical engineering, electronics, and cell biology over nine months (September 2024 to May 2025) under the supervision of Dr. Syed Hossainy, Dr. Dorian Liepmann, and Dr. Michael J. Conboy at the Coleman Fung Institute for Engineering Leadership.

My responsibilities spanned timeline management across four workstreams, design reviews, stakeholder communications, integration testing, and ensuring that engineering decisions accounted for biological constraints. The project reached over 90% milestone completion within the allocated timeframe.

Team: Ali Habbal, Yizhen Jia, Jacqueline Mejia, and Allegra Messinese.

<a href="{{ '/assets/piezoelectric-capstone-report.pdf' | relative_url }}" class="pdf-download-link" target="_blank">Full Capstone Report (PDF)</a>
