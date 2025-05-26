---
layout: page
title: "Rotation‑Induced Beam‑Plate Detachment under Rotational Excitation"
permalink: /rotation-beam-detachment/
---

## Overview
An eccentrically cantilevered elastic beam‑plate bonded to a Winkler foundation inside a rotating housing is analysed to determine when rotational inertia causes peeling.  
A propagating‑boundary variational problem yields the energy‑release rate G.

## Modelling Framework
- **Geometry** – Kirchhoff/Euler‑Bernoulli beam‑plate offset from the rotation axis.  
- **Transversality condition** – kw = γ⁄2 for the bonded sector.  
- **Solution** – Modal expansion; natural frequencies nearly independent of detached length.

## Excitation Cases
| Case | Angular acceleration profile | G(a) trend | Behaviour |
|------|-----------------------------|-----------|-----------|
| Impulse | β₀ δ(t) | Peak at small a, then decreases | Arrests when G < γ |
| Harmonic | β₀ sin Ωt | Similar decreasing curve | Arrests beyond small a |
| Saccadic | Eye‑like polynomial | G increases with a | Catastrophic propagation |

## Representative Figures
```markdown
![Gmax vs a – impulse](/assets/images/beam_impulse_Gmax.png)
![Gmax vs a – harmonic](/assets/images/beam_harmonic_Gmax.png)
![Gmax vs a – saccade](/assets/images/beam_saccade_Gmax.png)
