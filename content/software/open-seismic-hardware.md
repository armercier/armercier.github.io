---
title: "Geophysical Open Seismic Hardware"
date: 2022-01-01
tags: ["open hardware","instrumentation","vertical seismic profiling"]
description: "Open hardware and firmware for a multi-component borehole seismic array for vertical seismic profiling, developed at Université Laval."
summary: "Open hardware, firmware and control software for a multi-component borehole seismic array for vertical seismic profiling."
editPost:
    URL: "https://github.com/Geophysical-Instrumentation-Group-UL/Geophysical-Open-Seismic-Hardware"
    Text: "GitHub"
---

---

##### What it is

An open reference design for a multi-component borehole seismic array, developed with the Geophysical Instrumentation Group at Université Laval during my MSc. Downhole shuttles are lowered on a standard mineral-industry wireline winch. The aim is to make borehole seismic acquisition accessible and to encourage open development in geophysical instrumentation.

+ **Hardware:** printed circuit boards designed in KiCad around a Teensy 4.0 microcontroller, with a 3-channel 24-bit ADC sampling up to 32 kHz and a power-conditioning module for the downhole shuttle.
+ **Firmware** for acquisition and communication.
+ **Control software:** a basic GUI that configures a three-shuttle system and displays shot records and stacked traces.

Hardware is released under the TAPR Open Hardware License and firmware under GPLv3. The design and its first field validation are described in the [Journal of Open Hardware paper](/publications/joh-2023-open-seismic-hardware/).

---

##### Links

+ [Repository on GitHub](https://github.com/Geophysical-Instrumentation-Group-UL/Geophysical-Open-Seismic-Hardware)
+ [Paper: Journal of Open Hardware (2023)](https://doi.org/10.5334/joh.50)
