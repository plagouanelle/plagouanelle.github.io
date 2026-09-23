---
layout: page
permalink: /research/
title: Research
description:
nav: true
nav_order: 1
---

### Surrogate modeling for complex electromagnetic problems

Across many electromagnetic problems, the physical model of interest is either too costly to evaluate many times or only partially known, better described by scattered field measurements, sensor readings, or past campaigns than by any closed-form model. Surrogate modeling addresses both situations: a compact statistical model (e.g., Kriging, ANN, boosting methods) is trained on whichever data is available — costly simulations, real measurements, or both — in order to approximate the underlying physics. Once an accurate surrogate has been built, it can be used at a low computation cost wherever the use of the direct model would fail due to incomplete data or huge computation time: sensitivity analysis, optimization, inverse problems...

<figure>
<svg viewBox="0 0 1000 540" xmlns="http://www.w3.org/2000/svg" style="width:100%; height:auto;">
  <!-- Design parameters -->
  <rect x="20" y="130" width="180" height="200" rx="14" style="fill:none; stroke:var(--global-text-color); stroke-width:2;" />
  <text x="110" y="163" text-anchor="middle" style="fill:var(--global-text-color); font-size:18px; font-weight:600;">Design</text>
  <text x="110" y="184" text-anchor="middle" style="fill:var(--global-text-color); font-size:18px; font-weight:600;">parameters</text>
  <line x1="20" y1="196" x2="200" y2="196" style="stroke:var(--global-text-color); stroke-width:2;" />
  <text x="110" y="228" text-anchor="middle" style="fill:var(--global-text-color-light); font-size:16px; font-style:italic;">x&#8321;</text>
  <text x="110" y="256" text-anchor="middle" style="fill:var(--global-text-color-light); font-size:16px; font-style:italic;">x&#8322;</text>
  <text x="110" y="284" text-anchor="middle" style="fill:var(--global-text-color-light); font-size:16px;">&#8942;</text>
  <text x="110" y="312" text-anchor="middle" style="fill:var(--global-text-color-light); font-size:16px; font-style:italic;">x&#8345;</text>

  <!-- Simulations -->
  <rect x="300" y="20" width="180" height="90" rx="12" style="fill:none; stroke:var(--global-text-color); stroke-width:2;" />
  <text x="390" y="50" text-anchor="middle" style="fill:var(--global-text-color); font-size:18px; font-weight:600;">Simulations</text>
  <line x1="300" y1="62" x2="480" y2="62" style="stroke:var(--global-text-color); stroke-width:2;" />
  <text x="390" y="86" text-anchor="middle" style="fill:var(--global-text-color-light); font-size:15px; font-style:italic;">y = f(x)</text>

  <!-- Measurements -->
  <rect x="520" y="20" width="180" height="90" rx="12" style="fill:none; stroke:var(--global-text-color); stroke-width:2;" />
  <text x="610" y="50" text-anchor="middle" style="fill:var(--global-text-color); font-size:18px; font-weight:600;">Measurements</text>
  <line x1="520" y1="62" x2="700" y2="62" style="stroke:var(--global-text-color); stroke-width:2;" />
  <text x="610" y="86" text-anchor="middle" style="fill:var(--global-text-color-light); font-size:15px;">sensors, campaigns</text>

  <!-- Surrogate model -->
  <rect x="360" y="350" width="280" height="110" rx="14" style="fill:none; stroke:var(--global-theme-color); stroke-width:2;" />
  <text x="500" y="382" text-anchor="middle" style="fill:var(--global-text-color); font-size:18px; font-weight:600;">Surrogate model</text>
  <line x1="360" y1="394" x2="640" y2="394" style="stroke:var(--global-theme-color); stroke-width:2;" />
  <text x="500" y="420" text-anchor="middle" style="fill:var(--global-text-color-light); font-size:15px; font-style:italic;">y &#8776; f&#770;(x)</text>
  <text x="500" y="443" text-anchor="middle" style="fill:var(--global-text-color-light); font-size:13px;">Kriging, polynomial chaos, ...</text>

  <!-- Predictions -->
  <rect x="800" y="130" width="180" height="200" rx="14" style="fill:none; stroke:var(--global-text-color); stroke-width:2;" />
  <text x="890" y="163" text-anchor="middle" style="fill:var(--global-text-color); font-size:18px; font-weight:600;">Predictions</text>
  <line x1="800" y1="176" x2="980" y2="176" style="stroke:var(--global-text-color); stroke-width:2;" />
  <text x="890" y="205" text-anchor="middle" style="fill:var(--global-text-color-light); font-size:14px;">sensitivity analysis</text>
  <text x="890" y="233" text-anchor="middle" style="fill:var(--global-text-color-light); font-size:14px;">optimization</text>
  <text x="890" y="261" text-anchor="middle" style="fill:var(--global-text-color-light); font-size:14px;">field / exposure maps</text>

  <!-- Expensive (dashed) arrows -->
  <line x1="201" y1="185" x2="295" y2="90" style="stroke:#e0575a; stroke-width:2.5; stroke-dasharray:7,5;" marker-end="url(#arrow-expensive)" />

  <!-- Cheap (solid, theme color) arrows -->
  <line x1="201" y1="290" x2="358" y2="400" style="stroke:var(--global-theme-color); stroke-width:2.5;" marker-end="url(#arrow-cheap)" />
  <line x1="365" y1="112" x2="450" y2="348" style="stroke:var(--global-theme-color); stroke-width:2.5;" marker-end="url(#arrow-cheap)" />
  <line x1="600" y1="112" x2="540" y2="348" style="stroke:var(--global-theme-color); stroke-width:2.5;" marker-end="url(#arrow-cheap)" />
  <text x="505" y="255" text-anchor="middle" style="fill:var(--global-text-color-light); font-size:14px;">training</text>
  <line x1="642" y1="400" x2="798" y2="280" style="stroke:var(--global-theme-color); stroke-width:2.5;" marker-end="url(#arrow-cheap)" />

  <!-- Legend -->
  <line x1="40" y1="495" x2="90" y2="495" style="stroke:#e0575a; stroke-width:2.5; stroke-dasharray:7,5;" />
  <text x="100" y="500" style="fill:var(--global-text-color-light); font-size:14px;">Expensive &#8212; many simulation or measurement campaigns</text>
  <line x1="40" y1="523" x2="90" y2="523" style="stroke:var(--global-theme-color); stroke-width:2.5;" />
  <text x="100" y="528" style="fill:var(--global-text-color-light); font-size:14px;">Cheap &#8212; training and querying the surrogate</text>

  <defs>
    <marker id="arrow-expensive" markerWidth="9" markerHeight="9" refX="6.5" refY="3.5" orient="auto">
      <path d="M0,0 L7,3.5 L0,7 Z" style="fill:#e0575a;" />
    </marker>
    <marker id="arrow-cheap" markerWidth="9" markerHeight="9" refX="6.5" refY="3.5" orient="auto">
      <path d="M0,0 L7,3.5 L0,7 Z" style="fill:var(--global-theme-color);" />
    </marker>
  </defs>
</svg>
<figcaption class="caption">The principle behind all three research settings below: train a cheap surrogate on whichever data is available — costly simulations, real measurements, or both — then use it wherever the true model would be too slow or too incomplete to query directly.</figcaption>
</figure>

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

{% include figure.liquid path="assets/img/research/human_exposure.jpg" class="img-fluid rounded z-depth-1" zoomable=true alt="Dosimetric human body model next to a predicted exposure-factor map around a WPT system" caption="Dosimetric human body model (left) and predicted exposure-factor map around a WPT system (right)." %}

**Related publications:**

<div class="publications">
{% bibliography --query @article[topic=human_exposure] --group_by none --template bib_compact %}
</div>

### Metamodel-based design optimization of wireless power transfer systems

Designing an inductive power transfer (IPT) system for electric vehicles means navigating a large space of geometric and material parameters (coil shape, ferrite core, air gap...) under competing objectives: maximizing power transfer and efficiency while minimizing cost, weight, and stray magnetic field. Exploring this space with full 3D finite-element simulations is far too slow for multi-objective optimization or global sensitivity analysis. During my PhD at GeePs and Politecnico di Torino, I developed an adaptive sampling algorithm that builds a polynomial-chaos Kriging (PCK) surrogate of the coupled-coil electromagnetics using far fewer simulations than classical designs of experiments, by concentrating new samples where the surrogate is most uncertain. The resulting model reproduces quantities like the mutual inductance across the full design space at a fraction of the simulation cost, and can be plugged directly into gradient-based or multi-objective optimization routines.

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
