---
title: "Open Seismic Hardware for Borehole Seismics"
date: 2022-06-01
weight: 6
tags: ["open hardware","instrumentation","vertical seismic profiling"]
summary: "An open-source, multi-component borehole seismic instrument: electronics, firmware and software designed from scratch during my MSc at Université Laval."
cover:
    image: "cover.jpg"
    alt: "Sensor module and acquisition electronics of the open seismic instrument"
    relative: true
---

Before working on inversion, I worked on the instruments that collect the data. During my MSc at Université Laval, with the Geophysical Instrumentation Group, I designed the **Geophysical Open Seismic Hardware**: an open reference design for a multi-component borehole seismic array for vertical seismic profiling, deployable on a standard mineral-industry wireline winch.

{{< figure src="hardware.jpg" caption="Sensor module with three orthogonal accelerometers, the acquisition board (24-bit ADC, microcontroller, communication) and the power supply. The whole shuttle fits in a 40 mm tube. From Mercier, Dupuis & Giroux (2023), *Journal of Open Hardware*, CC BY 4.0." >}}

I designed the printed circuit boards, wrote the firmware and acquisition libraries, built test benches for the sensors, and processed the field data from the first validation surveys. Everything (hardware, firmware and documentation) is released openly, so that other groups can build, adapt and improve the instrument.

This experience still shapes my research: knowing how data are physically recorded makes it much easier to reason about which data are worth recording.

---

##### Read more

+ Paper: [Geophysical Open Seismic Hardware](/publications/joh-2023-open-seismic-hardware/), *Journal of Open Hardware* (2023)
+ Project: [hardware and firmware](/software/open-seismic-hardware/)
+ Talks: [IMAGE 2022](/talks/2022-image/), [GeoConvention 2022](/talks/2022-geoconvention/)
