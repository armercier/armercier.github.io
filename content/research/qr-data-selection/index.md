---
title: "Choosing Which Data to Invert: QR-Based Selection"
date: 2026-04-28
weight: 2
tags: ["full-waveform inversion","data selection","QR factorization","wavelets"]
summary: "Rank-revealing QR factorisation of the Jacobian picks the most informative measurements, so elastic FWI needs fewer simulations for almost the same result."
cover:
    image: "cover.jpg"
    alt: "Crosshole inversion results with 50% and 25% of the data"
    relative: true
---

Field surveys record far more data than an inversion really needs: neighbouring receivers and sources see nearly the same part of the subsurface. Inverting all of it costs memory and simulations without adding much information. This project treats data selection as a **linear-algebra problem**: which rows of the sensitivity (Jacobian) matrix are the most independent?

**Rank-revealing QR factorisation** answers exactly that question. We developed two variants:

+ a **row-wise** selection that keeps the best-conditioned subset of data points, shrinking the linear system;
+ a **cost-aware** selection that groups data by source, so that fewer forward and adjoint simulations are needed.

Combined with wavelet compression of the model, these reduce both sides of the problem.

{{< figure src="crosshole-model.png" caption="Synthetic crosshole test: true elastic model with sources (dots) in one borehole and receivers (crosses) in the other. From Mercier, Maurer & Boehm (2026), EarthArXiv preprint, CC BY 4.0." >}}

{{< figure src="crosshole-inversions.png" caption="Inverted P- and S-wave velocities as the fraction of selected data decreases from 50% to 3.2% (rows), and their difference from the full-data result (right columns). Half of the data already gives an almost identical model. From Mercier, Maurer & Boehm (2026), EarthArXiv preprint, CC BY 4.0." >}}

In both crosshole and surface geometries, QR selection consistently beats random subsampling. How far the data and model can be compressed depends on how well the acquisition illuminates the subsurface: the well-illuminated crosshole case tolerates aggressive reduction, while the surface case needs more data before the inversion converges. The same tools are now being applied to a [real 3D field survey](/research/co2-3d-survey/).

---

##### Read more

+ Preprint: [Efficient Full-Waveform Inversion via QR-Based Data Selection](/publications/preprint-2026-qr-data-selection/) (EarthArXiv, under review)
+ Related: [Combined inversion of active and passive data with optimised data selection](/publications/preprint-2026-combined-inversion/) (Behnen et al., 2026)
+ Code: [MODJO](/software/modjo/)
