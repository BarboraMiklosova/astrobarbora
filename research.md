---
layout: page
title: Research
description: >
  Overview of my current research interests, focusing on AGN feedback and shocks in the cosmic web.
permalink: /research/
---

My current research focuses on how energy from active galactic nuclei (AGN)  
and large-scale shock structures in the cosmic web shape the evolution of  
galaxies and their surrounding gas. On this page you can find a short overview
of my work on [AGN feedback](#agn-feedback) and [shocks in the cosmic web](#shocks).

## Probing the radio-mechanical AGN feedback using multi-cavity systems 
#### AGN feedback in hot atmospheres

In an active galactic nucleus (AGN), found in a giant elliptical galaxy (gE), the cen- tral supermassive black hole (SMBH) prevents the surrounding hot gas from cooling. If some gas cools, it can get accreted onto the SMBH’s in the form of radiatively inefficient disc, launching relativistic jets. These jets inject energy into the gas, creat- ing X-ray cavities that heat the atmosphere as they rise. This cycle repeats, forming a self-regulating feedback loop that suppresses radiative cooling and thus also star formation [1].

#### X-ray cavities
X-ray cavities, formed by AGN jets displacing hot gas, appear as regions of **reduced** X-ray emission. From their volumes and the thermodynamic properties of the X-ray–emitting gas, we can derive the jet power $P_{\text{jet}}$ that inflated them, which allows us to **quantify the AGN feedback history** if multiple generations are present.

Jet power $P_{\text{jet}}$ was calculated as  
$$ P_{\text{jet}} = \dfrac{E_{\text{inj}}}{t_{\text{age}}} = \dfrac{1}{t_{\text{age}}} E_{\text{mea}} \left( \dfrac{p_{0}}{p(d)} \right)^{1 - 1/\gamma}$$,

where $t_{\text{age}}$ is the cavity age, $E_{\text{mea}}$ is the measured energy approximated by $4\,p(d)\,V$, $V$ is the cavity volume, $p_{0}$ is the central pressure, and $p(d)$ is the pressure at the cavity’s distance $d$. The adiabatic index is $\gamma = 4/3$.

The cavity age $t_{\text{age}}$ can be estimated as:

- **sound-speed time:**  
  $t_{\text{ss}} \sim d (kT)^{-1/2}$, suitable for an attached cavity expanding mildly supersonically (innermost generation)

- **buoyancy time:**  
  $t_{\text{buo}} \sim d^{3/2} R_{\text{l}}^{-1/2}$, suitable for a cavity rising buoyantly (outer generations)


#### Data analysis
Archival *Chandra X-ray Observatory* data were analysed for four gEs: NGC 5813, NGC 5044, NGC 4649, and NGC 4472. The goal was to obtain an image of the galaxy to identify cavities and establish their parameters, and to obtain spectra to derive electron density $n_\text{e}$ and $kT$ radial profiles.

Spectral analysis was performed in XSPEC, where spectra were extracted from concentric annuli disecting the atmosphere, fitted with a model corresponding to X-ray emission and correctly deprojected. Cavities were identified in the residual images after subtraction of surface brightness model **$\beta$-model** or by deploying a machine-learning pipeline **CADET**. 

It is important to note that in our work, we reflected different physical
conditions in the **timescale corrections** and **energy corrections**
compared to the standard procedure.

<div class="galaxy-grid">
  <figure>
    <img src="{{ "/assets/img/thesis/galaxies/ngc5044.png" | relative_url }}" alt="NGC 5044">
    <figcaption>NGC 5044</figcaption>
  </figure>
  <figure>
    <img src="{{ "/assets/img/thesis/galaxies/ngc4472.png" | relative_url }}" alt="NGC 4472">
    <figcaption>NGC 4472</figcaption>
  </figure>
  <figure>
    <img src="{{ "/assets/img/thesis/galaxies/ngc5813.png" | relative_url }}" alt="NGC 5813">
    <figcaption>NGC 5813</figcaption>
  </figure>
  <figure>
    <img src="{{ "/assets/img/thesis/galaxies/ngc4649.png" | relative_url }}" alt="NGC 4649">
    <figcaption>NGC 4649</figcaption>
  </figure>
</div>

#### Toy model

To probe how the **inclination** affects our measurements, we calculated how
the jet power $P_\text{jet}$ changes with increasing inclination angle $i$ for
both **oblate** ($R_\text{l} < R_\text{w}$, e.g. NGC 5813 – G3) and
**prolate** cavities ($R_\text{l} > R_\text{w}$, e.g. NGC 4649 – G2). First,
we calculated the projected distance $d' = d \cos(i)$ and
$R'_\text{l} = R_\text{w} \sqrt{\sin^2 i + \tau^2 \cos^2 i}$, where
$\tau = R_\text{l}/R_\text{w}$ is the cavity's elongation, and recalculated
other cavity parameters accordingly at a given $i$ (following
Grange et al. 2020).

For systems showing an increasing $P_\text{jet}$ trend, we reversed the process
and calculated what would be the intrinsic $P_\text{jet}$ if we assumed that we
measured the $P'_\text{jet}$ at a given inclination angle $i$. In the thesis
this is illustrated by lighter-blue points for systems NGC 5044 (left) and
NGC 4472 (right).

### Key takeaways

- For aligned systems, the jet power seems to be roughly **constant**.  
- Inclination always causes the jet powers to be **overestimated**, and it can
  help explain the increasing $P_\text{jet}$ trend in two of the studied
  systems.  
- Jet powers are affected by inclination more in **oblate** cavities. In
  general, **buoyant** cavities are affected more than cavities expanding
  supersonically.  

**Bachelor thesis text**  
If you are interested in more detail, you can read the full thesis:  
[here](https://is.muni.cz/th/xdxlp/BM_thesis_agn_feedback.pdf).

### Figures from the thesis

I plan to add a few key figures here (e.g. cavity maps, profiles, or toy-model
illustrations). Once the images are exported from the thesis, they can be added
under `assets/img/research/` and included like this:

```md
![Cavity system example]({{ "/assets/img/research/agn_cavities.png" | relative_url }})
```

## Shocks in the cosmic web

For my master’s thesis, *Exploring Shock Structures in the Cosmic Web* (tentative
title), I am interested in how large-scale shocks trace the assembly of structure
in the Universe and how they affect the thermodynamic state of the intergalactic
medium.

Current directions include:

- Identifying and characterizing shock fronts in simulations of the cosmic web  
- Connecting shock properties to underlying large-scale structure and accretion  
- Exploring how shocks redistribute energy and entropy in diffuse gas  

This project is still in progress; over time, I plan to add figures, notes, and
selected results here as the work develops.
