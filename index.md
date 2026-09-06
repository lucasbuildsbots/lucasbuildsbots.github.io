---
layout: default
title: Home
---
{% include nav.html %}

# Investigating a Toroidal Foot Curvature Design in a 3D Passive Dynamic Walker

**Lucas Malachovsky · Lucas Mkheidze · Donna Leonardi · Weitian Wang**
Bergen County Academies / Montclair State University

<!-- ADD: a photo or short clip of the physical walker on the ramp, e.g.:
![The physical walker on the ramp](/assets/img/walker.jpg)
-->

This site is two things at once: the code/CAD repository for this research, and a
self-contained guide for building a passive dynamic walker (PDW) from nothing. If you
don't already know what passive dynamic walking is, start at the top and read down —
each page builds on the last. If you already know the field and want the research
directly, jump straight to the math, the experiment, or the results.

## What this project did

There has been little exploration of a crucial component of passive legged systems: the
feet. This project proposes a **toroidal foot curvature design** for a passive walker and
builds a modular robot with swappable feet to experimentally test variations in foot
curvature. A closed-form prediction relating the frontal radius of curvature to the
rocking period is derived, and validated against physical trial data to within **1%**
across all frontal-radius pairings tested. Variations in both the frontal and sagittal
radii were tested during passive gait on a fixed slope, revealing distinct gait
regimes — increasing step length and speed for smaller radii, decreasing step length and
speed for larger radii.

## A path through this site

1. **[Intro to PDW](/intro/)** — what passive dynamic walking is, why it matters, and
   where curved feet fit in.
2. **[Build a Toy](/build-a-toy/)** — build the simplest possible passive walker with
   basic materials, no CAD or 3D printer required, to feel the physics in your hands
   before touching any of the research.
3. **[Prototype & Design](/design/)** — how the actual research-grade robot was built:
   toroidal feet, swappable-foot mechanism, bearings, yaw control.
4. **[The Math](/derivation/)** — the closed-form derivation of the frontal-radius /
   rocking-period relationship, from energy conservation to the final formula.
5. **[Experimental Setup](/experiment/)** — the ramp, the trial protocol, how
   measurements were actually taken.
6. **[Results](/results/)** — the data: rocking period vs. $R_f$, the sagittal-radius
   findings, and the gait-speed regimes.
7. **[Lessons Learned](/lessons/)** — the practical things that only became clear from
   actually building and running the walker.
8. **[CAD Files](/cad/)** — the toroidal foot geometry and the actual model files.

## Read the paper

[Download the full paper (PDF)](/assets/paper.pdf)
