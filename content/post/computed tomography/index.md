---
title: CT Inverse Radon Implementation
description: Looking inside of things without breaking them open
slug: computed-tomography
date: 2025-06-14 14:50:00+0000
lastmod: 2025-12-11 14:50:00+0000
#image: rde.png
categories:
    - In-Progress
    - Sidequest
tags:
    - Matlab
    - Programming
    - Image Processing
#weight: 1       # You can add weight to some posts to override the default sorting (date descending)
hidden: true
---


## Premise

Having spent a ton of time in manufacturing for aerospace applications, particularly my work regarding Gas Turbines, I'm no stranger to Non-Destructive Engineering (NDE). CT draws my attention because, fundamentally, it's just a conventional X-Ray machine (for the most part) with a ton of image processing slapped on top. I decided to challenge myself to learn more about it and implement the image processing pipeline necessary to reconstruct an object in 3D space as a slice stack using only side projections. 

## Approach

Before I go on to explain the MATLAB script I cobbled together, I owe you a crash course in computed tomography.

Computed tomography is the denser a material is, the more light it absorbs. This effect is also achieved with a lower density material if there's more of it for light to travel through before coming out of the other side. If we are to take a singular projection of our test subject, the luminosity along the projection line varies depending on how much stuff it has to cross in order to make it to our detector. 

Intermediate space of the sinogram, 



### The Radon Transform and its Inverse

### MATLAB


### Python Translation


### I can't believe it's not X-Ray!

I'm sure that at some point in time, I'll cave in and buy a decommissioned dental imaging setup. But for the scope of this project and my current desire to not give myself cancer at 24, we'll have to figure out a way to generate close enough data to feed into MATLAB.

The best thing I could come up with is essentially recreating the setup in Blender, projecting a light source through a 3D model and capturing it on a camera at the other side. The 3D model has to scatter light, so a volumetric shader was used. Ray tracing and stuff Looked close enough to the naked eye

I decided to be even more faithful to reality and continue on by redoing the blender setup. instead of using a volumetric shader, I'll have the model actually absorb light as it passes through it and it is projected onto a screen, much like conventional xray setups project the shade of an object onto a detector or illuminating screen. The camera then looks at this screen to generate our renders

## Results









