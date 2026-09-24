---
layout: page
permalink: /research/
title: Research
description:
nav: true
nav_order: 1
---

### Surrogate modeling for complex electromagnetic problems

Across many electromagnetic problems, the physical model of interest is either too costly to evaluate many times or only partially known, better described by scattered field measurements, sensor readings, or past campaigns than by any direct model. Surrogate modeling addresses both situations: a statistical model (e.g., Kriging, ANN, boosting methods) is trained on whichever data is available (costly simulations, real measurements, mathematical equations...) in order to approximate the underlying physics. Once an accurate surrogate has been built, it can be used at a low computation cost wherever the use of the direct model would fail due to incomplete data or huge computation time: sensitivity analysis, optimization, inverse problems... My work focuses on the design, the training and the use of such surrogate models for complex electromagnetic problems. 

{% include figure.liquid path="assets/img/research/surrogate_model_principle.png" class="img-fluid rounded z-depth-1" zoomable=true alt="Diagram of the surrogate modeling principle: design parameters feed expensive simulations, which train a cheap surrogate model used for sensitivity analysis, optimization, and risk analysis" caption="Principle of a surrogate model and its training. Image credit: Shuai Guo." %}

**Related publications:**

<div class="publications">
{% bibliography --query @article[topic=intro] --group_by none --template bib_compact %}
</div>

### Prediction of radio-frequency electromagnetic fields exposure induced by cellular networks

The fast deployment of 5G technologies along with new bands, beamforming technologies, and denser deployments, motivated the careful exposure characterization and compliance assessment. At the Chaire C2M (Télécom Paris), my work on surrogate modeling is applied to spatial and temporal prediction of RF-EMF exposure correlated to the complexity of urban environments (population density, street network, infrastructure...). Costly ray-tracing simulation results are combined with measurement data coming from drive-tests and fixed sensors in order to estimate continuous exposure maps that evolve over the day. This allows local authorities to accurately estimate RF-EMF exposure without the need of expensive large-scale measurement campaigns.

{% include figure.liquid path="assets/img/research/massy_24h_cycle.gif" class="img-fluid rounded z-depth-1" avoid_scaling=true alt="Animated map of predicted RF-EMF exposure over Massy across 2-hour windows of the day, with drive-test route, fixed sensors, and base stations shown" caption="Predicted RF-EMF exposure map over Massy, animated across 2-hour windows of the day, with drive-test route, fixed sensors, and base station locations." %}

**Related publications:**

<div class="publications">
{% bibliography --query @article[topic=massy] --group_by none --template bib_compact %}
</div>

### DraGMet/EFIELD experiment on-board the Dragonfly mission on Titan

Titan, Saturn's biggest moon, is an ocean world, covered by organic materials and therefore one of the most promising astrobiological targets in the Solar System, likely holding clues on the origin of life on Earth. That is why NASA has selected the Dragonfly mission to send in 2027 a rotorcraft lander to Titan in order to investigate its prebiotic chemistry and habitability. At LATMOS, my work focused on modeling and optimizing the design of the EFIELD experiment (measurement of the time-varying electric field) on board the DraGMet (Dragonfly Geophysical and Meteorological) package. Schumann resonances (SRs) might appear on Titan, which the EFIELD experiment will aim at measuring. If such resonances exist, they could provide information on Titan's electromagnetic cavity dimensions (notably the thickness of the ice crust). Due to the size of the planetary cavity and the complete chain of measurement (drone and probe modeling, electronics, atmosphere effects...), the solving of the inverse problem is impossible through a direct approach. Thus, I managed to develop an accurate predictor for SRs on Titan by developing a new surrogate model fed by both simulation and measurement data from the Cassini/Huygens mission.

{% include figure.liquid path="assets/img/research/titan_schumann_modes.png" class="img-fluid rounded z-depth-1" zoomable=true alt="Simulated electric field amplitude of the first three Schumann resonance modes in Titan's electromagnetic cavity" caption="Simulated |E| field of the first three Schumann resonance modes in Titan's electromagnetic cavity." %}

**Related publications:**

<div class="publications">
{% bibliography --query @article[topic=titan] --group_by none --template bib_compact %}
</div>

### Human exposure assessment around inductive power transfer systems

Inductive power transfer (IPT) systems for electric vehicles rely on strong, low-frequency magnetic fields circulating between the transmitter and receiver coils, raising the question of compliance with international guidelines on human exposure to electromagnetic fields (ICNIRP, IEEE). Because exposure depends on the exact position of the driver or a bystander relative to the coils, and this position varies with vehicle geometry, ground clearance, and coil misalignment, the worst-case exposure cannot be captured by a handful of simulated scenarios. During my PhD at GeePs, I built a surrogate-model-based dosimetric methodology that maps exposure levels around IPT systems as a continuous function of these geometric and physical parameters, using realistic human body models. This makes it possible to identify the true worst-case exposure configuration and to check compliance margins across the full range of variability, rather than relying on a few conservative test points.

{% include figure.liquid path="assets/img/research/human_exposure.jpg" class="img-fluid rounded z-depth-1" zoomable=true alt="Dosimetric human body model next to a predicted exposure-factor map around a WPT system" caption="3D human body model (left) and predicted exposure-factor map around a WPT system (right)." %}

**Related publications:**

<div class="publications">
{% bibliography --query @article[topic=human_exposure] --group_by none --template bib_compact %}
</div>

### Metamodel-based design optimization of wireless power transfer systems

Designing an inductive power transfer (IPT) system for electric vehicles means navigating a large space of geometric and material parameters (coil shape, ferrite core, air gap...) under competing objectives: maximizing power transfer and efficiency while minimizing cost, weight, and stray magnetic field. Exploring this space with full 3D finite-element simulations is far too slow for multi-objective optimization or global sensitivity analysis. During my PhD at GeePs and Politecnico di Torino, I developed an adaptive sampling algorithm that builds a polynomial-chaos Kriging (PCK) surrogate model of various finite-element simulations using far fewer calls of the expensive model than classical designs of experiments, by concentrating new samples where the surrogate is most uncertain. The resulting model reproduces quantities like the mutual inductance across the full design space at a fraction of the simulation cost, and can be plugged directly into gradient-based or multi-objective optimization routines.

{% include figure.liquid path="assets/img/research/surrogate_wpt.jpg" class="img-fluid rounded z-depth-1" zoomable=true alt="PCK surrogate model of a WPT coil's mutual inductance, next to the underlying vehicle/coil finite-element mesh" caption="PCK surrogate of a WPT coil's mutual inductance (left) and the underlying vehicle/coil finite-element mesh (right)." %}

**Related publications:**

<div class="publications">
{% bibliography --query @article[topic=wpt_surrogate] --group_by none --template bib_compact %}
</div>

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
