---
title: "Field Campaign: A 3D Seismic Survey for CO₂ Storage Monitoring"
date: 2025-07-01
weight: 4
tags: ["field work","3D seismic","full-waveform inversion","CO2 storage"]
summary: "1,000 seismic nodes, 150 shots and a vibroseis truck: acquiring a near-surface 3D dataset to test data selection and FWI on real data."
cover:
    image: "cover.jpg"
    alt: "Vibroseis truck being unloaded from a low-loader trailer"
    relative: true
---

Methods developed on synthetic models have to survive real data. In 2025 I led the completion of a **near-surface 3D seismic survey** in the context of CO₂ storage monitoring: about **1,000 seismic nodes** and **150 shots**, acquired with a four-person team while coordinating with contractors for the heavy equipment.

<div class="photo-row">
<figure><img src="sledgehammer.jpg" alt="A sledgehammer shot on a field track, with two team members recording"><figcaption>Sledgehammer shot along a field track.</figcaption></figure>
<figure><img src="vibroseis.jpg" alt="Vibroseis truck on a low-loader trailer"><figcaption>The vibroseis source arriving on site.</figcaption></figure>
</div>

Every node position has to be known precisely, so a large part of the work is surveying: walking the layout with a GNSS receiver, including through fields of maize taller than the crew.

{{< video src="gps-survey.mp4" poster="gps-survey.jpg" portrait="true" caption="GNSS surveying of node positions in a maize field." >}}

The dataset is now the testbed for the rest of my work: 3D elastic FWI with Salvus, and the [QR-based data selection](/research/qr-data-selection/) applied at field scale. With this many sources and receivers, the full sensitivity matrix is too large to assemble, so I am building an HPC workflow that selects data without ever forming it explicitly.

---

##### Read more

+ Methods: [QR-based data selection](/research/qr-data-selection/), [designing FWI problems](/research/designing-fwi/)
