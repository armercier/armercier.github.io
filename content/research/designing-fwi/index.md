---
title: "Designing Full-Waveform Inverse Problems"
date: 2025-03-27
weight: 1
tags: ["full-waveform inversion","experimental design","wavelets","model compression"]
summary: "Choosing the source layout and the model parametrisation together: about half the sources and a 90% smaller model, with almost no loss of information."
cover:
    image: "cover.jpg"
    alt: "Ratio of retained wavelet coefficients for four subsurface models and 2, 6 and 12 sources"
    relative: true
---

Full-waveform inversion in 3D, with several physical parameters, is limited above all by cost: the number of sources sets the number of wave simulations, and the number of model parameters sets the size of the system to solve. Classical experimental design only optimises the first; model compression only tackles the second. In this project we optimise **both at once**.

The idea is to express the sensitivity of the data to the subsurface in a **wavelet basis**. Wavelet coefficients the data cannot "see" can be dropped from the model, and a source is valuable if it makes new coefficients visible. This gives a single criterion that grows the source layout one source at a time and, at the same time, tells us how small the model can be.

{{< figure src="wavelet-ratio.png" caption="Fraction of wavelet coefficients retained, relative to the full survey, for four subsurface models (columns) and 2, 6 and 12 sources (rows). With 12 sources the layout already resolves almost everything the full survey does. From Mercier et al. (2025), *GJI*, CC BY 4.0." >}}

Across homogeneous, layered, block and Marmousi models, the number of sources could be reduced from 20 to about 6, and the number of model parameters by around 90%, without significantly degrading resolution. The compressed model makes fast Gauss–Newton inversion practical, and computing the design itself becomes cheaper.

{{< figure src="wavelet-coefficients.png" caption="Number of wavelet coefficients retained across the domain for an optimised 10-source layout, for (a) homogeneous, (b) layered, (c) block and (d) Marmousi models. The profiles on the right follow the dashed red lines. From Mercier et al. (2025), *GJI*, CC BY 4.0." >}}

The same criterion also works **after acquisition**: from a large existing dataset, it selects compact subsets of source–receiver pairs that keep most of the information while cutting the number of simulations.

---

##### Read more

+ Paper: [Designing full waveform inverse problems: a combined data and model approach](/publications/gji-2025-designing-fwi/), *Geophysical Journal International* (2025)
+ Talk: [EGU General Assembly 2024](/talks/2024-egu/)
+ Code: [MODJO](/software/modjo/)
