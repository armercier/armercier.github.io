---
title: "Research"
description: "Arnaud Mercier's research: designing efficient full-waveform inversion problems through experimental design, data selection, model compression and differentiable physics, from synthetic studies to field campaigns."
---

Seismic full-waveform inversion (FWI) can image the subsurface in remarkable detail, but it is expensive: every source requires wave simulations, every model parameter adds to the size of the problem, and much of the data collected in the field is redundant. My research asks a simple question: **instead of only solving inverse problems faster, can we design them to be cheaper and more informative from the start?**

I approach this from several angles:

+ **Experimental design**: choosing where to place sources and receivers so that each one adds new information about the subsurface.
+ **Data selection**: keeping only the measurements that matter, using rank-revealing QR factorisation of the sensitivity matrix.
+ **Model compression**: describing the subsurface with wavelets so that only the parameters the data can actually resolve are inverted for.
+ **Differentiable physics**: writing the wave solver in JAX so that the survey layout itself can be optimised with gradients, through the inversion.

These methods are tested on synthetic benchmarks and then taken to the field, from a 1,000-node 3D survey for CO₂ storage monitoring to a fibre-optic deployment on an avalanche slope. Before my PhD, I designed open seismic hardware, which still shapes how I think about the link between instruments, data and models.

The posts below describe each project, with figures from the papers and photos from the field.
