---
layout: page
permalink: /research/
title: Research
description:
nav: true
nav_order: 1
---

Full electromagnetic simulations of complex systems — wireless power transfer (WPT) chargers, human-body exposure models, planetary electromagnetic cavities — are too costly to run thousands of times for sensitivity analysis, optimization, or uncertainty quantification. My work builds *surrogate models* (metamodels, e.g. polynomial-chaos Kriging) that approximate these simulations at a fraction of the cost, while retaining the accuracy needed for real design and safety decisions. The same toolbox now spans three settings: high-power WPT/human-exposure systems, RF-EMF exposure from telecommunications networks, and Titan's electromagnetic cavity.

### Surrogate modeling for fast electromagnetic prediction

Applied to inductive power transfer systems for electric vehicles: a polynomial-chaos Kriging (PCK) surrogate is fit adaptively to a full 3D electromagnetic model of the coupled coils, reproducing quantities like the mutual inductance across the full range of geometric variability at a fraction of the simulation cost.

{% include figure.liquid path="assets/img/research/surrogate_wpt.jpg" class="img-fluid rounded z-depth-1" zoomable=true alt="PCK surrogate model of a WPT coil's mutual inductance, next to the underlying vehicle/coil finite-element mesh" caption="PCK surrogate of a WPT coil's mutual inductance (left) and the underlying vehicle/coil finite-element mesh (right)." %}

### Human exposure assessment around high-power systems

The same surrogate lets exposure levels be mapped around a WPT charger far faster than direct simulation allows, so safety margins can be checked across the full range of geometric and physical variability rather than a handful of worst cases.

{% include figure.liquid path="assets/img/research/human_exposure.jpg" class="img-fluid rounded z-depth-1" zoomable=true alt="Dosimetric human body model next to a predicted exposure-factor map around a WPT system" caption="Dosimetric human body model (left) and predicted exposure-factor map around a WPT system (right)." %}

### RF-EMF exposure prediction for telecommunications networks

At the Chaire C2M (Télécom Paris), this approach is applied to spatial and temporal prediction of RF-EMF exposure from telecommunications networks: a spatial component (level) is combined with a temporal component (daily/weekly shape) learned from drive-test and sensor data, giving continuous exposure maps that evolve over the day.

{% include figure.liquid path="assets/img/research/massy_24h_cycle.gif" class="img-fluid rounded z-depth-1" avoid_scaling=true alt="Animated 24-hour cycle of predicted RF-EMF exposure over Massy, combining a spatial exposure level map with a learned temporal shape" caption="Predicted RF-EMF exposure over Massy across a 24-hour cycle: E(x, y, t) = Level(x, y) × Shape(t)." %}

### Titan's electromagnetic cavity and Schumann resonances

At LATMOS, I developed a numerical and surrogate model of Titan's electromagnetic cavity — bounded by the ionosphere and a possible subsurface water ocean — to re-assess PWA/Huygens observations and predict the performance of the EFIELD experiment on board NASA's Dragonfly mission for constraining the ocean's depth.

{% include figure.liquid path="assets/img/research/titan_schumann_modes.png" class="img-fluid rounded z-depth-1" zoomable=true alt="Simulated electric field amplitude of the first three Schumann resonance modes in Titan's electromagnetic cavity" caption="Simulated |E| field of the first three Schumann resonance modes in Titan's electromagnetic cavity." %}

## Supervision

- *2025 – present*&nbsp;&nbsp;**Yukun Liu** (Ph.D. student), LTCI, Télécom Paris — "Uncertainty quantification in predicting EMF exposure with artificial neural networks", with Prof. Shanshan Wang
- *June – December 2026*&nbsp;&nbsp;**Saif Meftah** (M2 internship), LTCI, Télécom Paris — "Boosting methods for predicting temporal and spatial variations of E-field levels in urban environments", with Prof. Shanshan Wang
- *April – July 2025*&nbsp;&nbsp;**Ethan Reuchin** (M1 internship), LATMOS, Université Paris-Saclay — "Data acquisition for the DIEL Sensor from the Dragonfly mission: sensitivity analysis and optimization of design parameters", with Prof. Alice Le Gall
- *April – September 2024*&nbsp;&nbsp;**Bruno Martin Peña** (M1 internship), LATMOS, Université Paris-Saclay — "Sensitivity analysis of the EFIELD sensors aboard the Dragonfly mission to Titan for measuring Schumann resonances", with Prof. Alice Le Gall
- *May – July 2024*&nbsp;&nbsp;**Pierrot Cadeilhan** (Bachelor internship), LATMOS, Université Paris-Saclay — "Feasibility of Schumann Resonances' measuring using multimodal measurements from the EFIELD experiment on-board Dragonfly", with Prof. Alice Le Gall
- *May – June 2019*&nbsp;&nbsp;**Sahil Deshmukh** (Bachelor internship), GeePs, Université Paris-Saclay — "Assessment of human exposure with stochastic models for wireless charging of electrical vehicles", with Prof. Lionel Pichon

## Teaching

- *2016 – present*&nbsp;&nbsp;**Physics oral examiner**, Lycée Buffon, Paris — oral examiner for CPGE pre-bachelor students in Physics (PSI)
- *2020 – 2022*&nbsp;&nbsp;**Physics teacher**, IUT de Cachan, Université Paris-Saclay — introduction course to general physics (mechanics, electromagnetics, thermodynamics) for first-year students
- *2016 – 2017*&nbsp;&nbsp;**Mathematics assistant teacher**, Lycée Buffon, Paris — lessons and tutoring for high school students
- *April – August 2017*&nbsp;&nbsp;**French assistant teacher**, Massey University, Palmerston North, New Zealand
