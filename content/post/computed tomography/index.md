---
title: CT Inverse Radon Implementation
description: Quick little Matlab side quest
slug: computed-tomography
date: 2025-05-03 14:50:00+0000
lastmod: 2025-10-13 14:50:00+0000
image: rde.png
categories:
    - Sidequest
tags:
    - Matlab
    - Programming
    - Image Processing
weight: 1       # You can add weight to some posts to override the default sorting (date descending)
---


## Background

Rotating Detonation Engines (RDEs) are a relatively novel form of rocket propulsion that takes advantage of pressure-gain combustion. Conventional rocket engines use constant-pressure combustion cycles. RDEs theoretically produce better performance by taking better advantage of the energy stored chemically in the propellants. There is a fine line between detonating in the way that yields the performance advantage, and detonating in the way that destroys the engine. Due to the speeds involved in the process, these engines have only recently began gaining traction now that computers and sensors allow for the extremely fast sampling rates necessary for reliable data output. Their compact size allows for storable propellants to be used more effectively in missile and defense applications.

The goals of this project at the beginning were beyond creating a working air breathing lab scale engine, to lay the foundation for further research to be done at UCF. This involved creating a test stand equipped with a capable and robust data acquisition system and control system. With the tight budget for a project of this ambition we had to get creative.

## Design

## Ignition

Lighting an RDE involves precise timing and a strong enough relese of energy to induce a detonation mode within the engine. A fast burst (in tens of micro seconds) with not a lot of energy is more likely to induce a detonation compared to a longer burst with a ton more energy. Typically predets are used where an explosive mixture of gases are lit on one end of a long tube and over that length of tube the energy release is structured in such a way a shock is developed by the time the combusting gases exit. Due to the mechanism of operation, these have careful geometry that is hard to package into a system with compact and flight in mind. This is where my approach comes in, conventional torch. If the annulus can act as the constriction that focuses the energy towards a shock, the igniter can be more compact and allow for smaller designs for flight vehicles. 


## Humbled by Testing

## Senior Design Showcase

## Future Plans

### SciTech

## Final Thoughts and Acknowledgements

Taha Dr. Burke, Teammates and UCF's Senior Design Support System



