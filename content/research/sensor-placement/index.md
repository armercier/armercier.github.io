---
title: "Moving Sensors with Gradients: Differentiable Survey Design"
date: 2026-10-01
weight: 3
tags: ["full-waveform inversion","experimental design","differentiable physics","JAX"]
summary: "A differentiable wave solver in JAX lets source and receiver positions be optimised by gradient descent through the full-waveform inversion itself."
cover:
    image: "cover.jpg"
    alt: "Source positions moving during gradient-based optimisation, with the FWI loss decreasing"
    relative: true
---

Choosing where to put sensors is usually a combinatorial problem: try candidate positions, keep the best, repeat. That scales poorly and only explores a fixed grid. If the whole pipeline (wave simulation and inversion) is **differentiable**, the positions themselves become continuous variables that can be optimised with gradients.

I implemented an acoustic wave solver in **JAX**, so that the quality of the final FWI model can be differentiated with respect to where the sources and receivers sit. This turns survey design into a **bilevel optimisation**: the inner problem is the inversion, the outer problem moves the instruments to make that inversion as good as possible.

{{< video src="sources.mp4" poster="poster.jpg" caption="Source positions (red, with their trajectories) move through a layered velocity model while receivers (green stars) stay fixed. Each step updates the layout using gradients through the inversion; the FWI loss (right) drops by more than half." >}}

Because the positions are continuous, the optimiser is free to find layouts no grid search would have tried, and the same framework extends naturally to adaptive designs, where the next measurement is chosen from what has already been learned. Possible applications range from seismic monitoring of CO₂ storage sites to other imaging problems governed by PDEs.

This work is a collaboration with Ben Moseley (Imperial College London).

---

##### Read more

+ Paper: [Differentiable Physics for Sensor Placement in Full-Waveform Inversion](/publications/neurips-2026-sensor-placement/), NeurIPS 2026 workshop *Sim2Science*
+ Code: [Hybrid-OED on GitHub](https://github.com/armercier/Hybrid-OED)
