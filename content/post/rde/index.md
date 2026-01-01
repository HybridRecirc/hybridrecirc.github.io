---
title: Project SABR
description: Small-Scale Air-Breathing Rotating Detonation Engine - Senior Design 2025
slug: project-sabr
date: 2025-05-03 14:50:00+0000
lastmod: 2025-10-13 14:50:00+0000
image: rde.png
categories:
    - Spotlight
    - Senior Design
    - Undergrad
tags:
    - Propulsion
    - R&D
    - Data Acquisition
    - Test Engineering
    - Electronics
weight: 1       # You can add weight to some posts to override the default sorting (date descending)
---

## Major Achievements:
<ul>
    <li>Developed a fully-fledged testing platform for air-breathing RDEs at UCF</li>
    <li>Laid the foundation for a future senior design teams</li>
    <li>Produced data for several AIAA SciTech 2025 papers</li>
</ul>

## Background

Rotating Detonation Engines (RDEs) are a relatively novel form of rocket propulsion that takes advantage of pressure-gain combustion. Conventional rocket engines use constant-pressure combustion cycles. RDEs theoretically produce better performance by taking better advantage of the energy stored chemically in the propellants. There is a fine line between detonating in the way that yields the performance advantage, and detonating in the way that destroys the engine. Due to the speeds involved in the process, these engines have only recently began gaining traction now that computers and sensors allow for the extremely fast sampling rates necessary for reliable data output. Their compact size allows for storable propellants to be used more effectively in missile and defense applications.

The goals of this project at the beginning were beyond creating a working air breathing lab scale engine, to lay the foundation for further research to be done at UCF. This involved creating a test stand equipped with a capable and robust data acquisition system and control system. With the tight budget for a project of this ambition we had to get creative. 

## Design

### Ignition

Lighting an RDE involves precise timing and a strong enough relese of energy to induce a detonation mode within the engine. A fast burst (in tens of micro seconds) with not a lot of energy is more likely to induce a detonation compared to a longer burst with a ton more energy. Typically predets are used where an explosive mixture of gases are lit on one end of a long tube and over that length of tube the energy release is structured in such a way a shock is developed by the time the combusting gases exit. Due to the mechanism of operation, these have careful geometry that is hard to package into a system with compact and flight in mind. This is where my approach comes in, conventional torch. If the annulus can act as the constriction that focuses the energy towards a shock, the igniter can be more compact and allow for smaller designs for flight vehicles. 

I was in charge of both mechanical and electrical aspects of the ignition system. In terms of the mechanical side of things, I prioritized cost and ease of manufacturing over anything else, arriving at what is essentially a modified stainless steel 1/4 NPT cross fitting, as pictured below. 

The torch body is then connected to the rest of the RDE via a thick-walled stainless steel pipe nipple. 

In practice, the concept of lighting the RDE was a lot easier said than done. I go more into detail about the outcome under Testing.

### Structure

Before pivoting towards my work in ignition, I helped with the first handful of iterations of the combustor. I focused on packaging and routing alongside my buddy Hunter, essentially figuring out how to efficiently route propellants from their respective ports coming from the fluids system and into the injectors. 

Initially, we weighed the our options for manufacturing methods. We could push for an additively manufactured design, which would allow for complex geometry and reduce the number of critical seals to worry about, but had the drawback of very money, timeline, and risk intensive. On the other hand, we could go for something doable with the resources available at the UCF Machine Shop: reliable and free access to 3 and 5 axis machining, turning, EDM hole drilling and wire cutting. All we'd have to source is our required material. Regardless of whether we printed it or machined it conventionally, the RDE would be exposed to extreme conditions surrounding the detonation wave as it propagates, which means high pressures and temperatures sweeping around in a circle. Compared to a conventional engine, the cyclic failure modes began rearing their ugly head in all of our analysis. 

![Transient conditions within the combustor. Source: Wikipedia](waveswipe.gif)

The only saving grace was that the timescales for all this energy release were minuscule, although they compounded over time. Based on the fact we were targetting a very short runtime of only a couple seconds (and much more engineering analysis I will not go into here), we decided to go for 304 Stainless Steel. The reasoning came down to the fact we wanted the ability to fail and iterate without being dead in the water trying to source another brick of material to machine or a whole new printed part. Much of the research behind RDEs is uncharted territory, so even with all of our calculations and analysis double, triple, and quadruple checked, we wanted a large margin of safety on top of the ability to return to the drawing board and modify our design without crippling the project. So with all that being said, we settled on a conventionally manufactured combustor. From all the discussion, preliminary analysis, and talking to researchers both at UCF labs and across the US in places like Purdue and Johns Hopkins, we went for a modular design based on a stack of plates. Below are some of the first iterations of our combustor, initially by me and later modified by Hunter. 

![The First Assembly of the Project](EarlyIterationOfRDE.png) ![A section view better showing our initial plenum design](OtherViewEarlyu.png) ![Combustor in context of its thrust-bearing mounting plate](EarlyMount.png)

A great start, but with any engineering project, we quickly started spotting flaws in terms of component integration, manufacturing, and especially in terms of final assembly in the stand. Looking back while writing this knowing how the project turned out as a whole makes the original design look extra alien. 

Plate design after ruling out 3d printing due to timeline and thankfully tariffs confirmed out option

Hard to route taps for pressure and igniter channel using conventional machining methods

### The Rest Of It

I would love to keep writing much more about all that this project entailed, but it ultimately was a deeply intertwined group contribution. I am highlighting my direct work on getting this RDE off the ground, so it wouldn't be fair to any of my teammates to mention it all without also highlighting their achievements. A major part of senior design at UCF are these "Milestone Reports" where we, as a team, got together and tracked our work in a format similar to a design review. Milestone 6, the final one, contains a snapshot of the past year of our work leading up to the results we got and how we'd improve upon our work if we were to hypothetically continue testing after the semester ended. I feel it's the best way to provide a curious reader, perhaps someone looking to base their research on our work, with the necessary in-depth info about the combustor, test stand, and our results. Please reach out to me directly if you have any questions. Email is best, all available over on the sidebar. 

[Here it is, weighing in at 134 pages.](/docs/rdereport.pdf) 

To go along with the report, I'd also like to provide a quick slidestack that we used to give an overview about the project. I can't embed it as a .pptx, so unfortunately, gifs will not work on this version. Enjoy!

[Showcase Slides](/docs/showcaseslides.pdf) 

However, I'd like to still cover what we experienced taking the design from a whiteboard/Solidworks to a real, working prototype. I'll also be covering my contribution to our combined in-the-field problem solving and troubleshooting. Just know it'll all be in a very simplified manner because, after all, we wrote that document precisely to act as a self-contained reference guide to our system. 


## Testing

## Senior Design Showcase

{{< youtube srb3Dv_vAVQ >}}

## Final Thoughts and Acknowledgements

Thicker annulus, overestimated pressures, ignition may be easier with the torch, testing necessary

things id fix

better thrust calibration, possibly using a pneumatic/hydraulic cylinder to calibrate load cells

less rigid plumbing, alternatively, put the whole thrust bearing frame on linear bearings, measure thrust there


I'd like to thank and congratulate Dr. Rezzag-Lebza, Dr. Burke, Dr. Stresau, and of course, my teammates. All our hard work paid off, and I hope we left a solid foundation for future detonation combustion research at UCF for both future senior design teams and researchers. Additionally, all the work before us that inspired the project as a whole: Fiorino, Dechert, among the many researchers across the US pioneering RDEs as a platform for future vehicles.

As a machinist, I'd also like to highlight the crucial role that UCF's Office of Research Machine Shop played in helping us not only bring the project to life, but also playing a role as a major contributor in optimizing the manufacturability of our system. The latter, along with their hard work, allowed us to achieve a quick turnaround between iterations. We were able to go from testing and reviewing data to firing a modified engine in the span of a week. Reader, remember to thank your manufacturing team as often as you can.  



