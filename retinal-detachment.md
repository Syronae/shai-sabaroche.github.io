---
layout: page
title: "Mechanics of Retinal Detachment (PhD Dissertation)"
permalink: /retinal-detachment/
---

> **Doctoral Dissertation – Rutgers University, Oct 2024**

## Overview
Retinal detachment jeopardises sight by separating the neurosensory retina (NSR) from its retinal‑pigmented epithelium (RPE) and blood supply.  
My dissertation presents the **first physics‑complete, time‑domain model** that tracks the eye’s response to **low‑velocity blunt impacts** and quantifies when a nascent detachment grows or self‑arrests.

## Modelling Approach
- **Geometry & Kinematics** – Retina and sclera are Kirchoff–Love spherical shells, the vitreous a nearly incompressible viscoelastic solid; azimuthal symmetry reduces the problem to \(r,\theta,t\).
- **Variational Formulation** – A propagating‑boundary, calculus‑of‑variations framework yields governing PDEs and a **transversality condition** for the moving detachment front.  
- **Spectral Solution** – Modal fields use spherical Bessel and associated Legendre functions; impulse loading is decomposed with Blackman‑windowed integrals.

## Key Results
- **Stress Hot‑Spots** – Peak membrane stress, bending moment, and shear concentrate at the **peripapillary region**, matching clinical tear incidence.  
- **Energy‑Release‑Rate Envelope** – Small initial detachments experience the **highest energy release**, making them the most unstable.  
  Plotting maximum \(G_{max}(a)\) against detached percent reveals three regimes:  
  1. **\(\gamma < G_{max}\)** → runaway detachment (catastrophic).  
  2. **intermediate \(\gamma\)** → tunnelling then arrest at a larger stable size.  
  3. **\(\gamma > G_{max}\)** → no propagation.  
- **Implication** – Adhesive energy \(\gamma\) is the critical patient‑specific material property; measuring it could stratify trauma risk.

## Representative Figures
Insert the exported images from your dissertation in `assets/images/` and reference them here:

```markdown
![Energy release rate vs. time for selected detachments](/assets/images/energy_release_rate.png)
![Maximum energy release rate locus](/assets/images/max_energy_release_locus.png)
