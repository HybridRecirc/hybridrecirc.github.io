---
title: Project Pegasus
description: N-Class Hybrid - IREC 2023
slug: project-pegasus
date: 2025-10-05 00:00:00+0000
image: pegasuscover.jpg
categories:
    - Spotlight
    - Major Project
    - Undergrad
tags:
    - Propulsion
    - R&D
    - Data Acquisition
    - Test Engineering
weight: 1       # You can add weight to some posts to override the default sorting (date descending)
---

## Major Achievements:
<ul>
    <li>Pioneered a novel fuel grain composition.</li>
    <li>Solved emulsification problems between fuel grain ingredients.</li>
    <li>Developed an modular injector plate, allowing for quick refurbishment in case of damage.</li>
    <li>Generated manufacturing procedures to guarantee repeatability and uniformity between fuel grain batches.</li>
    <li>Successfully static fired twice, both times gaining N-class impulse classification, outperforming previous generations by 60% in peak thrust.</li>
</ul>

## Background

This was my first major project in college, and I was in the position to spearhead an approach to hybrids that hadn't been tried before at UCF. At this point, I had messed around with Paraffin-based fuels on my own small backyard hybrid, but I encountered the typical issues with density, structural stability, and burn stability as every other amateur. I came into this project with the goal of finding a solution to these issues by dedicating a major part of the year to R&D and testing every single approach we could come up with, the Skunkworks Way.

Additionally, the previous hybrid projects at UCF all incorporated pyrotechnic valves, with zero control of oxidizer flow after ignition starts. I took it as a challenge to incorporate basic valve control to allow for finetuning of the burn, and most importantly, lay out the framework for in-flight burn control. The importance of being able to control how the motor performs during the flight comes from the ability to pinpoint the target apogee and maximize the points scored within the competition. 

## The Paraffin Problem

As mentioned before, paraffin has its issues, but what are its upsides? 

In order for a fuel to burn, it needs to first become a gas in order to react with the oxidizer, much like gasoline vapors are the part that actually burns. In hybrids, depending on the fuel, this mechanism can occur in two different ways, which allows us to separate fuels into two major categories: 

<ul>
<li><b>Plastic/Rubber (HTPB, ABS, any kind of epoxy, resins, etc.)</b></li>
For these, there's no intermediate phase.  Solid immediately turns into gas for combustion. These tend to be more energy dense, stable, and easier to handle. Downside comes down to mixing efficiency.

<li><b>Paraffins</b></li>
Paraffin has the unique trait of having an intermediate phase, where it turns into liquid before gasifying when burning. This allows it to develop an unstable liquid layer that flings droplets into the oxidizer stream, giving it an advantage when it comes to energy release and burn efficiency. However, it tends to be softer, prone to cracking, and carries a much lower energy density compared to the others. <b>Also, it won't withstand much time in the New Mexico Desert during the summer.</b>
</ul>

If we could solve paraffin's issues, we'd have a great middle ground with room for growth in future projects. My first instinct was to research candlemaking forums, books and every other piece of media I could get my hands on. As a society, we've been making candles for centuries and have grown pretty good at it. As it turns out, different waxes can increase paraffin's structural stability, melting point, hardness, and alleviate shrinkage/cracking issues. All this research led me towards adding Microcrystalline Wax and Stearic Acid to provide these benefits.

Our final problem comes down to energy density, and this is where Sorbitol comes in. It's a cheap, plentiful diet sugar replacement that's extensively used in amateur solid rocket motors, as well as some hybrids. It's easy to melt and very resilient towards caramelization, which reduces sugar fuels' performance. At this point, we came across the age old problem of trying to mix oil with water. See, paraffin is polar and sorbitol is non-polar, meaning we're ending up with a block split into two layers when everything cools down. <b>Suboptimal.</b> 

This is where emulsifiers come in. Mayo, for example, is oil and water mixed together, but no one thinks of two layers when thinking of mayo. See, in order for something like that to remain homogeneous, you need a third ingredient in order to "interface" between the two substances and keep them happy next to each other. In the case of mayonnaise, it's egg. In the case of our fuel mixture? We tried commercial grade emulsifiers and surfactants, Sodium Laureth Sulfate, namely. Pretty similar stuff to shampoo components. Ultimately we arrived at a super high-tech solution: <b>Dawn Dish Soap with Papaya Scent.</b> Remember, if it's stupid and it works then it's not stupid. It's incredible how effective a tiny bit of Dawn was at homogeinizing the ingredients and keeping them together when everything cooled back down. 

One more issue I wanted to solve wasn't really critical but instead a way to appease my lizard brain desire to push past 100%. In order to extract more performance out of this fuel, we need to make the best use out of the energy released by the chemical reaction. This fuel mix ended up being very white and semi-transluscent, traits which aren't ideal for two reasons: white things reflect instead of absorbing, and non-opaque things tend to let light thru them. We need the grain to absorb as much heat from the combusting gases as possible, and we need that heat to remain at the outermost layer of the fuel. In order to achieve this, we want to make the grain opaque somehow, and we want the reacting gases to radiate as much heat as possible. Carbon Black, Lampblack, or Soot was what we chose. Adding just 1-5%wt of Carbon Black to the mix made the fuel completely opaque and it created a very incandescent exhaust as expected, but the kicker was that we got about 10% more thrust out of this simple change. Free performance glitch.

## Combustion Chamber

Going from forward to aft, the major components of a typical hybrid combustion chamber are: Injector Carrier/Forward Closure, Casing, Thermal Liner, Nozzle, Nozzle Retainer. Designs may vary going from system to system but the basic components generally remain the same. While the concept of rocket propulsion remains relatively standard between solids, liquids, and hybrids, hybrids have a few particular quirks that drive the design of the combustion chamber in order to maximize performance.

Take a liquid engine, for example. Two propellants are injected into the chamber, mixed together and ignited. Straight forward enough. This involves careful timing and geometric design in order to guarantee that your propellants get to know each other as well as possible before they get the chance to burn. Inefficient mixing leads to loss of performance, so the art comes down to the injector design and chamber geometry (as well as other tricks involving preheating or preburning one or both of the propellants, not the focus of this discussion). On the other hand, you've got solids. Your propellants are mixed together homogeneously during manufacturing, meaning you have a mixture ratio and properties that are essentially set in stone. Major drawback is that potent fuels and oxidizers in close proximity to each other are a recipe for disaster. This is where hybrids come in and attempt to reach a goldilocks spot between these two. Conventionally, you've got a solid fuel and a liquid or gaseous oxidizer being injected. You still have the simplicity of solids and most of their form factor, but since your propellants are still separate from one another, you have the inherent safety of a liquid platform. The benefits truly end here, as they tend to inherit some of the worst performance issues of either counterpart. They're hard to ignite, since as mentioned above you need to vaporize that fuel in order for it to ignite, which is rendered borderline impossible when your oxidizer is undergoing a phase transition right upstream wicking a lot of your igniter's energy (we'll get into this soon, I promise). It's hard to ignite the whole grain face at once, mixing is a problem because fuel vapors are produced at the inner face of the grain white the oxidizer is injected flowing longitudinally,meaning a boundary layer forms where the two are supposed to be getting to know each other well. Diffusion is the primary mechanism driving mixing, and unfortunately without clever engineering it leads to horrible combustion performance and a ton of unburnt propellants being expelled without reacting. But this is where engineers thrive, with careful consideration, a lot of these issues can be mitigated to turn this into a somewhat tolerable platform for something like a sounding rocket. 

Getting started at the forward end with the oxidizer. In Pegasus, the oxidizer of choice is Nitrous Oxide. You might know this as laughing gas, or whippets. It's cheap, plentiful, and most importantly, it's part of the family of refrigerant gases. This last feature is a double edged sword, where it can be stored at a relatively low pressure as a liquid, it's self-pressurizing and it's got an awesome density at its ideal storage temperature, also it flashes into a gas the second that pressure drops below a threshold, which serves very well when you're trying to get it to atomize and mix with the fuel in the chamber. However, the refrigerant side of things comes in and it will devour all the heat around it in order to support the phase transition, think turning a can of keyboard duster upside down. Additionally, when the fluid speeds up, pressure drops, which leads to two phase flow and cavitation, both of which are headahces in trying to design something to run at steady state. 

In order to take care of these issues, in

 (Note: This did not happen in this narrative order in real life. Truth is, you need the rest of the system to be able to iterate on fuels and hone everything the way portrayed above)

## Valve Control

Oxidizer flow was controlled by a servo strapped to a ball valve. Simple enough for a team getting into valve control, robust enough not to introduce too much uncertainty into our design. Although we found out real quick what happens when you keep sending position information to an uncooled servo

Printed cage around valve

## Testing Campaign

Burn ban

Ground Support Issues

First Test
Second Test

## IREC 2023

Integration Nightmare

No Nitrous

## Acknowledgements and Final Thoughts

This article highlights primarily the work I was directly spearheading, but ultimately this is all the culmination of a team of equally talented people working towards a common goal. I'd like to thank my peers in the propulsion team for their help getting this from whiteboard drawings up into the air, as well as the people involved in every other supporting subsystem ranging from avionics to aerostuctures. 

Enjoy some pictures from IREC 2023 and the later launch in Florida!

Peggy pics


