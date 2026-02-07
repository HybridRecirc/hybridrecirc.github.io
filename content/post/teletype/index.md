---
title: Teletypewriter Retrofit
description: Taking advantage of 80s simplicity to get a Linux Terminal + other goodies
slug: teletype
date: 2026-02-07 14:50:00+0000
lastmod: 2026-02-07 14:50:00+0000
image: cover.jpeg
categories:
    - In-Progress
    - Sidequest
tags:
    - Electronics
    - Radio
    - Reverse Engineering
    - R&D
#weight: 1       # You can add weight to some posts to override the default sorting (date descending)
---

## Background

I got a Smith Corona SL600 off eBay for $3 + shipping, the seller said it had an unfixable error that prevented it from starting up and only showed a rapid blinking light on the CapsLock indicator. I love taking gambles at anything on eBay with a clueless seller so I bought it. When it came in, I cleaned it, plugged it in and saw the same error as the seller. However, I had bought an extra set of ribbon cartridges and the one that came with the machine looked off to me, so I swapped it. To my surprise the very well designed typewriter sprung to life with the correct ribbon installed. I've been using it to type letters and journaling but I'm retiring it in favor of a model with a better keyboard. As you'll see below from my teardown, the 80s were a period of cost reduction and optimization, sometimes at the detriment of user experience. 

## Goals

    - Intercepting keystrokes between the keyboard and the rest of the typewriter in order to control/hear what's being typed
    - Developing a serial interface for the typewriter to act as a Linux terminal, much like early terminals of the 50s and 60s.
    - Acting as a packet radio transceiver, putting the tele in teletypewriter

## Preliminary Exploration

I took the typewriter apart to clean it and gaze at its insides. To my surprise, it's probably the best model to modify for this project. As far as I can tell, logic listens out for which circuits are being closed as the operator types, and signals to type the corresponding letters. 

Taking it apart further revealed that the keyboard is composed of a film PCB similar to modern membrane keyboards, where the keys press down a tree of stamped sheet metal levers that close exposed pads on the film surface via carbon-coated plungers. Essentially an ancestor of modern membrane keyboards, except that the PCB is optimized to be a ribbon across the center of the keyboard. My educated guess for this is the early restrictions on film PCBs would drive costs much higher if they had a PCB matching the footprint of the keyboard itself. Much cheaper to have the levers do the heavy lifting of connecting the outer keys to the center.  

## Current Work