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

## How this project started

We came across passive dynamic walking and were struck by how elegant the idea is: a
machine that walks down a slope using nothing but its own mechanical design and gravity —
no motors, no control loop, nothing driving the gait at all. We wanted to build one
ourselves.

We started with the simplest model we could design, inspired by Tedrake's work — two legs,
a pin joint at the hip, curved feet. After a lot of tinkering with the model's design
parameters, we eventually reached a version that could take about 40 steps in its best
trial. Forty consecutive steps meant we'd actually found a real stable configuration, not
just gotten lucky for a step or two.

Once the walker actually worked, we wanted to understand *why* it worked rather than stop
at "it walks." That's what turned our attention to the feet specifically: we built a
novel swappable-foot mechanism so multiple foot curvatures could be tested on the exact
same physical body, and found consistent trends relating the feet's circular curvature to
measurable properties of the gait. Those trends, together with physical reasoning and
closed-form calculation, are what the rest of this research builds out.

## Where to go from here

- **[Build a Simple Passive Walker](/build-a-toy/)** — feel this physically with
  cardboard and a pin before reading anything more technical.
- **[The Research](/research/)** — skip straight to the actual robot, math, and data.
