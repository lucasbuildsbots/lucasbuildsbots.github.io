---
layout: default
title: What Is Passive Dynamic Walking?
---

[← Home](/)

# What Is Passive Dynamic Walking?

## The problem: legged robots run out of battery

Legged robots move over terrain that wheeled robots can't — disaster zones, rocky
ground, unstructured environments. But most legged robots today are highly actuated:
they rely on a large number of independently controlled motors to drive every motion,
and that costs energy. NASA's Valkyrie, a bipedal robot built for planetary exploration,
was limited by a battery life of about one hour. AgiBot 2, a humanoid that walked a
record 66 miles across multiple terrains, still needed its battery replaced every three
hours. Neither is a practical long-term solution.

## The insight: let gravity do the work

Passive dynamic walking (PDW) is a mode of legged locomotion where a robot walks down a
slope using only its own mechanical design and gravity — no motors driving the gait at
all. The idea takes its cue from human walking itself: EMG studies (McMahon) show that a
portion of human gait is not actually powered by muscle at any given instant — it's
semi-passive. Feet play a direct role in that efficiency, too. Adamczyk et al. showed
that in human gait, the foot behaves analogously to a rolling arc as the stance leg rolls
over it, rather than pivoting around a fixed point.

## Point feet vs. curved feet

Early passive walkers were built with point feet, but they suffer from a small basin of
attraction — the set of initial conditions from which the walker will actually settle
into stable passive walking, rather than falling over. Walkers built with curved feet
instead exhibit smoother, more anthropomorphic gaits. Collins, Wisse, and Ruina built a
curved-foot walker with knees and counter-swinging arms; notably, during development of
that relatively complex model, simulation could not find a design that produced stable
gait — the working design came out of iterative physical experimentation, not
simulation.

Simulation of curved feet is hard in a specific way: it requires coupling the frontal
plane (side-to-side rocking) and the sagittal plane (forward stepping) at once. Tehrani
recently made progress solving this coupling mathematically, but his simulation, using
spherical feet, could not find a set of design parameters producing a periodic gait, and
it didn't account for some dynamics present in a real physical walker, such as yaw
(twisting about the vertical axis).

## Where this project fits

The mechanics of passive dynamic walking, and the accurate simulation of fabricable
designs, are not yet fully understood. Given the limits of simulation-based approaches,
**physical experimentation** is a valuable complementary path for exploring curved-foot
geometries — which is the approach this project takes. Specifically, it investigates a
**toroidal** foot: independently curved in the frontal and sagittal directions, built
into a modular robot with feet that swap in and out, so each curvature parameter can be
isolated and tested directly on a physical slope rather than only in simulation.

## Where to go from here

- **[Build a Simple Passive Walker](/build-a-toy/)** — feel this physically with
  cardboard and a pin before reading anything more technical.
- **[The Research](/research/)** — skip straight to the actual robot, math, and data.
