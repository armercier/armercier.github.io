---
title: "Differentiable Physics for Sensor Placement in Full-Waveform Inversion"
date: 2026-10-01
pubtype: workshop
venue: "Sim2Science: ML with Imperfect Scientific Models, NeurIPS 2026 Workshop"
tags: ["full-waveform inversion","experimental design","differentiable physics","JAX"]
author: ["Arnaud Mercier","H. R. Thomsen","Ben Moseley"]
description: "A differentiable acoustic wave solver in JAX used to optimise receiver placement through full-waveform inversion. NeurIPS 2026 workshop paper."
summary: "Receiver positions are optimised by differentiating through a full-waveform inversion built on a JAX wave solver."
editPost:
    URL: "https://openreview.net/forum?id=OjMk7CZoOG"
    Text: "OpenReview"
---

---

##### Links

+ [Paper on OpenReview](https://openreview.net/forum?id=OjMk7CZoOG)
+ [Related code: Hybrid-OED](https://github.com/armercier/Hybrid-OED)

---

##### Summary

Where sensors are placed controls how well full-waveform inversion can recover the subsurface. This work implements a differentiable acoustic wave solver in JAX, so that the quality of the inversion result can be differentiated with respect to receiver positions. The receiver layout is then optimised with gradients, in a bilevel problem where the inner level is the inversion itself.

---

##### Citation

Mercier, A., Thomsen, H. R., & Moseley, B. (2026). Differentiable Physics for Sensor Placement in Full-Waveform Inversion. *Sim2Science: ML with Imperfect Scientific Models, NeurIPS Workshop*. https://openreview.net/forum?id=OjMk7CZoOG

```bibtex
@inproceedings{Mercier2026NeurIPSW,
  author    = {Mercier, Arnaud and Thomsen, H. R. and Moseley, Ben},
  title     = {Differentiable Physics for Sensor Placement in Full-Waveform Inversion},
  booktitle = {Sim2Science: ML with Imperfect Scientific Models, NeurIPS Workshop},
  year      = {2026},
  url       = {https://openreview.net/forum?id=OjMk7CZoOG}
}
```
