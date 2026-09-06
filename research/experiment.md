---
layout: default
title: How We Tested It
---

[← Back to The Research](/research/)

# Experimental Setup

## The ramp

All trials were run on the same 8-foot wooden ramp described in
[How the Robot Was Built](/research/design/), tilted at 0.0663 rad (3.80°), with a textured surface to
control yaw. Starting from the same baseline configuration ($R_f = 120$ mm,
$R_s = 100$ mm), only the curvature of the feet was changed between trials — every other
geometric and mass parameter was held fixed by design.

## What was varied

Two separate sweeps were run:

- **Frontal radius sweep:** $R_f$ tested at 110 mm, 120 mm, 130 mm, and 140 mm, while
  $R_s$ was held constant at 100 mm.
- **Sagittal radius sweep:** $R_s$ tested at 80 mm, 100 mm, and 120 mm, while $R_f$ was
  held constant at 120 mm.

Each configuration was run for **3 trials**.

## What was measured, and how

For each trial, four things were recorded: rocking period, step length, step count, and
walking speed, along with their standard deviations across trials — this is what lets
the walking cycle actually be characterized and compared between configurations rather
than just observed once.

Measurements were taken through **video analysis**, using two synchronized camera angles
— one positioned above the walker, one from the side — recording at **4K, 60 fps**. Foot
collisions (which mark the start/end of a rocking or stepping cycle) were identifiable
frame-by-frame from this footage, which is what rocking period and step length were
extracted from.

<!-- ADD: photo or diagram of your actual two-camera rig setup -->

## A real limitation, stated plainly

The two-camera video method could reliably identify foot collisions — enough to measure
rocking period and step length — but it could **not** precisely measure angles, such as
the inter-leg angle at heel strike or the walker's yaw during the gait cycle. That's a
real constraint on what this dataset can answer, not just a caveat: it's why yaw is
discussed qualitatively (see [Lessons Learned](/research/lessons/)) rather than quantified
directly in the results, and it's the direct motivation for planned sensor-based data
acquisition in future work.

## Where to go from here

- **[What We Found](/research/results/)** — what came out of this setup.
- **[The Math](/research/derivation/)** — the prediction being checked, if you haven't read it
  yet.
