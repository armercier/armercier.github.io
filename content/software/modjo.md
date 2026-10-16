---
title: "MODJO — Model and Data Optimisation for FWI"
date: 2024-05-29
tags: ["scientific software","full-waveform inversion","experimental design","data selection"]
description: "MODJO: a Python package for model and data optimisation in full-waveform inversion — sequential experimental design, wavelet compression and QR data selection."
summary: "Python package for sequential experimental design, wavelet model compression and QR-based data selection in FWI workflows."
editPost:
    URL: "https://gitlab.com/armercier/MODJO"
    Text: "GitLab"
---

---

##### What it does

MODJO is a Python package for optimising both the data and the model parametrisation of full-waveform inversion problems. It implements the methods behind my [GJI paper](/publications/gji-2025-designing-fwi/) and the [QR data-selection preprint](/publications/preprint-2026-qr-data-selection/):

+ sequential optimal experimental design for selecting source layouts;
+ tools to load and reshape sensitivity (Jacobian) matrices, built on NumPy and xarray;
+ Haar and wavelet transform-domain compression of the model;
+ QR and sketch-based row selection for compressing the design problem.

The repository is set up as maintained research software, with unit and integration tests, linting and type checks in GitLab CI, and Sphinx documentation published to GitLab Pages.

---

##### Links

+ [Source code on GitLab](https://gitlab.com/armercier/MODJO)
+ [Documentation](https://armercier.gitlab.io/MODJO/)
