---
title: "Teaching at TU Delft"
year: 2024
role: "Head Teaching Assistant"
institution: "Delft University of Technology"
summary: "Head TA for Computational Biology at TU Delft, responsible for designing course projects on GitHub, grading deliverables, and running weekly 4-hour practicals. Also TA for Physics 2 (Optics and Quantum Physics)."
tags: [teaching, computational biology, Python, numerical methods]
gradient: grad-5
image: "/assets/images/tudelft-library.jpg"
image_position: "center 55%"
category: teaching
city: "Delft"
lat: 52.0116
lng: 4.3571
---

## What I Learned

Designing a problem is a different skill from solving one. When you solve a problem someone else wrote, you work within a structure that already knows where it is going. When you design the problem, you have to make every structural choice yourself: what prior knowledge to assume, where to put the scaffolding, how much to reveal in the assignment text and how much to leave for the student to discover. Getting that balance wrong in either direction produces either boredom or paralysis. The six course projects I helped create were a continuous exercise in threading that needle.

The second year taught me something the first year could not. I ran the same course with a different cohort, using largely the same materials, and watched concepts that had landed cleanly the first time fail to register with the second group. The students were different. Their prior preparation was different. What read as clear scaffolding to one cohort read as ambiguous to the next.

I rewrote sections of assignments between years not because the content was wrong but because the framing was wrong for who was in the room. That distinction — between an idea being sound and the framing being right for this specific audience — is one I have carried into every communication problem since.

The role also clarified what it actually means to understand something. Students would ask questions I thought I knew the answer to, and then, mid-explanation, I would find a gap I had not noticed before. The Euler method, finite difference schemes, Monte Carlo convergence: each of them has an edge case that only surfaces when someone who does not yet understand it forces you to re-derive it from first principles in real time.

## The Course

**Modelling and Simulation in Science and Engineering** is a core course in the Nanobiology bachelor at TU Delft. Students work through numerical methods and their implementation in Python, with problems drawn from biology and biophysics. The format is practical-first: four-hour sessions each week where students work through assignments, with TAs providing real-time support and code review.

The course covers four main skill areas, each corresponding to a project:

**Project 1: Numerical Function Analysis.** Forward, backward, and central difference methods for numerical differentiation; composite rectangle, midpoint, trapezoid, and Simpson's 1/3 rule for integration; bisection and Newton-Raphson methods for root finding. Students investigate how accuracy scales with step size using log-log analysis.

**Project 2: Vectors, Matrices and Linear Algebra.** Matrix operations, linear systems, eigenvalues and eigenvectors. Emphasis on using matrix algebra as a computational primitive rather than operating element-by-element.

**Project 3: Random Variables and Monte Carlo.** Probability distributions, random number generation, Monte Carlo simulation. Students model stochastic systems and reason about how many simulations are needed to characterise a distribution.

**Project 4: Parameter Fitting.** Least-squares linear regression, weighted fitting with variable measurement uncertainty, and generalised polynomial fitting via the pseudo-inverse. Students implement the full chi-square minimisation from scratch before using library functions.

## The Final Projects

At the end of the course, students chose one of two longer projects as a final assessment. These were designed to require synthesis across all four skill areas.

**Final Project A: Deterministic and Stochastic Models of Epidemic Spread (SIR Model).** Students first implemented the classic SIR model as an initial value problem solved by the Euler method, producing stacked area plots of susceptible, infected, and removed populations over 150 days. They then built a stochastic version: a 1,000-person social network encoded as an adjacency matrix, with infection propagating through the network probabilistically at each discrete time step. A Monte Carlo loop of 100 runs produced a distribution of outcomes. Students estimated R0 at the day of peak infection across simulations and fitted a gamma distribution to the R0 distribution using SciPy.

**Final Project B: Worm-like Chain Model.** A biophysical model of polymer mechanics, applied to DNA and other semiflexible polymers. Students implemented the worm-like chain force-extension relationship and fitted it to simulated experimental data, combining numerical methods, parameter estimation, and physical reasoning.

## My Role

As Head TA for Computational Biology, I was responsible for the full TA operation on the course:

**Project design and maintenance.** I created and maintained the course projects on GitHub. This included writing assignment text, scaffolding code templates, designing grading rubrics, and iterating on projects between years based on where students consistently struggled.

**Grading and feedback.** I reviewed and graded student deliverables hosted on GitHub, providing code-quality feedback on correctness, vectorisation, and structure. The emphasis was on feedback that taught rather than feedback that just scored.

**Weekly practicals.** I ran four-hour practical sessions each week, circulating between students to debug code, clarify concepts, and identify when a question was revealing a structural gap in the assignment rather than in the student.

<p class="press-table-note">Hero image: TU Delft Library. <a href="https://commons.wikimedia.org/wiki/File:TU_Delft_Universiteitsbibliotheek.jpg">Choinowski via Wikimedia Commons</a>, CC BY-SA 4.0.</p>

