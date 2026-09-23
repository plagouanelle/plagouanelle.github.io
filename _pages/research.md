---
layout: page
permalink: /research/
title: Research
description:
nav: true
nav_order: 1
---

### Surrogate modeling for complex electromagnetic problems

Full electromagnetic simulations of complex systems — wireless power transfer (WPT) chargers, human-body exposure models, planetary electromagnetic cavities — are too costly to run thousands of times for sensitivity analysis, optimization, or uncertainty quantification. My work builds *surrogate models* (metamodels, e.g. polynomial-chaos Kriging) that approximate these simulations at a fraction of the cost, while retaining the accuracy needed for real design and safety decisions. The same toolbox now spans three settings: RF-EMF exposure from telecommunications networks, Titan's electromagnetic cavity, and high-power WPT/human-exposure systems.

<figure>
<svg viewBox="0 0 920 220" xmlns="http://www.w3.org/2000/svg" style="width:100%; height:auto;">
  <rect x="10" y="50" width="230" height="120" rx="12" style="fill:none; stroke:var(--global-divider-color); stroke-width:1.5;" />
  <text x="125" y="86" text-anchor="middle" style="fill:var(--global-text-color); font-size:16px; font-weight:600;">Full 3D</text>
  <text x="125" y="106" text-anchor="middle" style="fill:var(--global-text-color); font-size:16px; font-weight:600;">electromagnetic</text>
  <text x="125" y="126" text-anchor="middle" style="fill:var(--global-text-color); font-size:16px; font-weight:600;">simulation</text>
  <text x="125" y="152" text-anchor="middle" style="fill:var(--global-text-color-light); font-size:13px;">FEM / circuit model</text>

  <line x1="240" y1="110" x2="335" y2="110" style="stroke:var(--global-theme-color); stroke-width:2;" marker-end="url(#arrowhead)" />
  <text x="287" y="97" text-anchor="middle" style="fill:var(--global-text-color-light); font-size:12px;">a few expensive</text>
  <text x="287" y="132" text-anchor="middle" style="fill:var(--global-text-color-light); font-size:12px;">samples</text>

  <rect x="345" y="50" width="230" height="120" rx="12" style="fill:none; stroke:var(--global-divider-color); stroke-width:1.5;" />
  <text x="460" y="76" text-anchor="middle" style="fill:var(--global-text-color); font-size:16px; font-weight:600;">Surrogate model</text>
  <text x="460" y="95" text-anchor="middle" style="fill:var(--global-text-color-light); font-size:13px;">(Kriging / PCK)</text>
  <path d="M365,155 C 400,112 430,100 465,115 C 500,130 520,150 545,140" style="fill:none; stroke:var(--global-theme-color); stroke-width:2;" />
  <circle cx="375" cy="148" r="3.5" style="fill:var(--global-theme-color);" />
  <circle cx="405" cy="118" r="3.5" style="fill:var(--global-theme-color);" />
  <circle cx="440" cy="104" r="3.5" style="fill:var(--global-theme-color);" />
  <circle cx="478" cy="118" r="3.5" style="fill:var(--global-theme-color);" />
  <circle cx="518" cy="145" r="3.5" style="fill:var(--global-theme-color);" />

  <line x1="575" y1="110" x2="670" y2="110" style="stroke:var(--global-theme-color); stroke-width:2;" marker-end="url(#arrowhead)" />
  <text x="622" y="97" text-anchor="middle" style="fill:var(--global-text-color-light); font-size:12px;">instant,</text>
  <text x="622" y="132" text-anchor="middle" style="fill:var(--global-text-color-light); font-size:12px;">everywhere</text>

  <rect x="680" y="50" width="230" height="120" rx="12" style="fill:none; stroke:var(--global-divider-color); stroke-width:1.5;" />
  <text x="795" y="76" text-anchor="middle" style="fill:var(--global-text-color); font-size:16px; font-weight:600;">Fast predictions</text>
  <text x="795" y="102" text-anchor="middle" style="fill:var(--global-text-color-light); font-size:13px;">sensitivity analysis</text>
  <text x="795" y="124" text-anchor="middle" style="fill:var(--global-text-color-light); font-size:13px;">optimization</text>
  <text x="795" y="146" text-anchor="middle" style="fill:var(--global-text-color-light); font-size:13px;">exposure maps</text>

  <defs>
    <marker id="arrowhead" markerWidth="8" markerHeight="8" refX="6" refY="3" orient="auto">
      <path d="M0,0 L6,3 L0,6 Z" style="fill:var(--global-theme-color);" />
    </marker>
  </defs>
</svg>
<figcaption class="caption">The principle behind all three research settings below: fit a cheap surrogate to a handful of expensive simulations, then use it wherever the real model would be too costly to run.</figcaption>
</figure>

### Prediction of radio-frequency electromagnetic fields exposure induced by cellular networks

The fast deployment of 5G technologies along with new bands, beamforming technologies, and denser deployments, motivated the careful exposure characterization and compliance assessment. At the Chaire C2M (Télécom Paris), my work on surrogate modeling is applied to spatial and temporal prediction of RF-EMF exposure correlated to the complexity of urban environments (population density, street network, infrastructure...). Costly ray-tracing simulation results are combined with measurement data coming from drive-tests and fixed sensors in order to estimate continuous exposure maps that evolve over the day. This allows local authorities to accurately estimate RF-EMF exposure without the need of expensive large-scale measurement campaigns.

{% include figure.liquid path="assets/img/research/massy_24h_cycle.gif" class="img-fluid rounded z-depth-1" avoid_scaling=true alt="Animated map of predicted RF-EMF exposure over Massy across 2-hour windows of the day, with drive-test route, fixed sensors, and base stations shown" caption="Predicted RF-EMF exposure map over Massy, animated across 2-hour windows of the day, with drive-test route, fixed sensors, and base station locations." %}

**Related publications:**

<div class="publications">
{% bibliography --query @article[topic=massy] --group_by none --template bib_compact %}
</div>

### Titan's electromagnetic cavity and Schumann resonances

At LATMOS, I developed a numerical and surrogate model of Titan's electromagnetic cavity — bounded by the ionosphere and a possible subsurface water ocean — to re-assess PWA/Huygens observations and predict the performance of the EFIELD experiment on board NASA's Dragonfly mission for constraining the ocean's depth.

{% include figure.liquid path="assets/img/research/titan_schumann_modes.png" class="img-fluid rounded z-depth-1" zoomable=true alt="Simulated electric field amplitude of the first three Schumann resonance modes in Titan's electromagnetic cavity" caption="Simulated |E| field of the first three Schumann resonance modes in Titan's electromagnetic cavity." %}

**Related publications:**

<div class="publications">
{% bibliography --query @article[topic=titan] --group_by none --template bib_compact %}
</div>

### Human exposure assessment around high-power systems

The same surrogate lets exposure levels be mapped around a WPT charger far faster than direct simulation allows, so safety margins can be checked across the full range of geometric and physical variability rather than a handful of worst cases.

{% include figure.liquid path="assets/img/research/human_exposure.jpg" class="img-fluid rounded z-depth-1" zoomable=true alt="Dosimetric human body model next to a predicted exposure-factor map around a WPT system" caption="Dosimetric human body model (left) and predicted exposure-factor map around a WPT system (right)." %}

**Related publications:**

<div class="publications">
{% bibliography --query @article[topic=human_exposure] --group_by none --template bib_compact %}
</div>

### Surrogate modeling for fast electromagnetic prediction

Applied to inductive power transfer systems for electric vehicles: a polynomial-chaos Kriging (PCK) surrogate is fit adaptively to a full 3D electromagnetic model of the coupled coils, reproducing quantities like the mutual inductance across the full range of geometric variability at a fraction of the simulation cost.

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
