---
layout: default
title: CAD Files
---
{% include nav.html %}

# Foot Geometry and CAD Files

## The toroidal foot surface

The whole point of this design is that $R_f$ (frontal-plane curvature) and $R_s$
(sagittal-plane curvature) can be set independently, rather than being tied to a single
spherical radius as in prior models. The foot's surface profile, in the foot's own local
frame with $x$ along the frontal direction and $y$ along the sagittal direction, is:

\[
z(x,y) = \sqrt{\left((R_f - R_s) + \sqrt{R_s^2 - y^2}\right)^2 - x^2} - R_f
\]

This is what actually gets modeled in CAD and printed — every other foot dimension
(length, width, contribution to standing height) is held constant across configurations
so that curvature is the only thing changing between trials (see
[Prototype & Design](/design/) and [Lessons Learned](/lessons/)).

## CAD files

<!--
  ADD: for each foot configuration tested (Rf = 110/120/130/140 mm at Rs = 100 mm, and
  Rs = 80/100/120 mm at Rf = 120 mm), export a .glb from Fusion 360 (File > Export) and
  drop it in assets/models/, then duplicate the block below. GitHub also natively renders
  .stl/.obj/.glb files if someone clicks on them directly in the repo file browser, so the
  raw files are viewable even before model-viewer is wired up for any given foot.
-->

<!--
### R_f = 110 mm, R_s = 100 mm

<model-viewer src="/assets/models/foot_110_100.glb" alt="Rf=110mm, Rs=100mm foot"
  auto-rotate camera-controls style="width: 100%; height: 400px;">
</model-viewer>

[Download STEP file](/assets/models/foot_110_100.step)
-->

<p class="note">Once your .glb files are in assets/models/, uncomment and duplicate the
block above for each of the seven tested configurations.</p>

## The paper

[Download the full paper (PDF)](/assets/paper.pdf) — this is the actual manuscript this
entire site is built from.
