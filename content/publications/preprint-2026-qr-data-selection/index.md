---
title: "Efficient Full-Waveform Inversion via QR-Based Data Selection"
date: 2026-04-28
pubtype: preprint
venue: "EarthArXiv preprint (2026), under review"
tags: ["full-waveform inversion","data selection","QR factorization","wavelets"]
author: ["Arnaud Mercier","Hansruedi Maurer","Christian Boehm"]
description: "Rank-revealing QR selection of FWI data to reduce linear-system size or the number of forward and adjoint simulations. EarthArXiv preprint, 2026."
summary: "Choosing which data to invert, via QR factorisation of the Jacobian, cuts the cost of elastic FWI with little loss in model quality."
editPost:
    URL: "https://doi.org/10.31223/X5PJ4N"
    Text: "EarthArXiv"
---

---

##### Links

+ [Preprint on EarthArXiv](https://doi.org/10.31223/X5PJ4N)
+ [Code: MODJO](https://gitlab.com/armercier/MODJO)

---

##### Summary

Full-waveform inversion is expensive because of the number of measurements, simulations and unknowns involved, and realistic acquisition geometries often make the resulting systems highly redundant. This preprint frames data selection as row selection on the Jacobian using rank-revealing QR factorisation. One variant preserves the conditioning of the linear system; another reduces the number of distinct forward and adjoint simulations. Combined with wavelet compression of the model, tests on synthetic elastic crosshole and surface geometries show that QR-based selection outperforms random subsampling, and that achievable compression depends on how well the acquisition illuminates the model.

---

##### Citation

Mercier, A., Maurer, H., & Boehm, C. (2026). Efficient Full-Waveform Inversion via QR-Based Data Selection. *EarthArXiv* (preprint). https://doi.org/10.31223/X5PJ4N

```bibtex
@misc{Mercier2026QR,
  author = {Mercier, Arnaud and Maurer, Hansruedi and Boehm, Christian},
  title  = {Efficient Full-Waveform Inversion via QR-Based Data Selection},
  year   = {2026},
  note   = {EarthArXiv preprint},
  doi    = {10.31223/X5PJ4N}
}
```
