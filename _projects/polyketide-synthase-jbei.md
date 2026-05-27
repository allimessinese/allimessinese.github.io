---
title: "Non-Canonical Amino Acid Biosynthesis"
year: 2024
role: "Research Affiliate"
institution: "Joint BioEnergy Institute (Keasling Lab)"
summary: "Research Affiliate in Jay Keasling's lab at JBEI, under Sarah Klass. Engineered PKS pathways in Pseudomonas putida for non-canonical amino acid biosynthesis. Pre-publication."
tags: [synthetic biology, metabolic engineering, research]
gradient: grad-6
image: "/assets/images/jbei-lab.jpg"
image_position: "center 28%"
category: research
city: "Emeryville"
lat: 37.8309
lng: -122.2854
links:
  - label: "Joint BioEnergy Institute"
    url: "https://www.jbei.org"
  - label: "Keasling Lab"
    url: "https://keaslinglab.lbl.gov"
---

## What I Learned

Working in a DOE national lab is different from working in a university lab. The scale of the science, the number of people working on adjacent problems, and the institutional pressure to demonstrate translational impact all shape how the work gets done. It was the first time I worked inside a project that was explicitly pointed at a commercial endpoint: engineering biology to replace petrochemical manufacturing. That framing changed how I thought about experimental choices. Every decision had a "and then what?" attached to it.

The project also gave me a concrete sense of how pathway engineering differs from genetic engineering of individual parts. Building a non-canonical amino acid biosynthesis pathway in a new chassis is not one problem: it is a sequence of problems that each generate new constraints for the next, from gene integration strategy to codon optimisation to analytical validation. The iteration is slower and the failure modes are more numerous than when you are working with a single well-characterised component.

## The Lab

**Jay Keasling's lab** at the **Joint BioEnergy Institute (JBEI)** in Emeryville is one of the leading groups in metabolic engineering and synthetic biology. The lab is DOE-funded, with a central focus on engineering microorganisms to produce fuels and bio-based chemicals from renewable feedstocks.

I worked directly under **Sarah Klass**, whose project centres on engineering **polyketide synthases (PKSs)** to biosynthesise small molecule monomers that can be polymerised into recyclable 3D-printable plastics. PKSs are large, modular enzyme complexes that naturally produce a wide range of bioactive compounds including antibiotics and antifungals. Their modularity makes them attractive targets for rewiring: by swapping the loading and extension modules, you can in principle redirect the biosynthetic output toward new chemical structures.

## The Project

My project sat within the broader PKS engineering effort: the **biosynthesis of non-canonical amino acids (ncAAs) in *Pseudomonas putida* and *Bacillus subtilis***, in collaboration with Chenyi.

Non-canonical amino acids are structural analogues of the 20 standard amino acids, with altered or added chemical functionalities: click chemistry handles, altered hydrophobicity, bulky side chains, cross-linking groups. They have two main applications in protein engineering: as **bioconjugation handles** for antibody-drug conjugates and other protein-payload fusions, and as **structural perturbations** that can improve enzyme thermostability or activity.

The PKS connection: by swapping the **loading modules (LMs)** of a PKS, you can change the starter unit for polyketide biosynthesis and generate structurally distinct ncAA products. The long-term vision goes further: by coupling ncAA production to **auxotrophic recovery** in strains lacking the ability to synthesise a standard amino acid (ΔpheA, ΔleuB, ΔthrC), the production titre becomes directly tied to cell viability. This creates a selection pressure that can be used to drive **directed evolution of PKS systems** at high throughput.

## My Work

I focused on building the ncAA biosynthesis pathway in ***Pseudomonas putida***, chosen for its established genome engineering protocols, codon-optimised loading modules, and well-characterised media for expression.

The pathway construction used a **multi-site integration strategy**, sequencing plasmid insertions across four genomic loci: the ZmaHIGJ biosynthetic cluster at the RV site, ZmaF at the TG1 site, the PKS extension module ZmaA-eryTE at the BxB1 site, and the loading modules at the R4 site. Integration was tracked and validated using the **SAGE** (iterative site-specific genome integration) framework, following Elmore et al. (2023). The integrated ZmaHIGJ strain was submitted for **proteomics** and **LC-MS** to assess amino malonate production.

Alongside the *P. putida* work, the project was establishing a parallel track in *B. subtilis*, which offers complementary tools for ncAA incorporation into heterologous proteins but presents its own challenges: slower integration, no codon-optimised LMs, and limited proteomics.

## Status

This work is ongoing and a manuscript is in preparation.
