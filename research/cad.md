---
layout: default
title: Foot Geometry & CAD Files
---

[← Back to The Research](/research/)

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
[How the Robot Was Built](/research/design/) and [Lessons Learned](/research/lessons/)).

## CAD files

GitHub natively renders `.stl`, `.obj`, and `.glb` files if someone clicks on them
directly in the repo's file browser — so even before any `model-viewer` embeds below are
wired up, the raw files themselves are viewable to anyone browsing the repo.


<!--
  ADD: Full Assembly — this is the final prototype as one model. Export a .glb from
  Fusion 360 (File > Export) and put it at assets/models/full_assembly.glb, then
  uncomment:

<model-viewer src="/assets/models/full_assembly.glb" alt="Full walker assembly"
  auto-rotate camera-controls style="width: 100%; height: 450px;">
</model-viewer>

[Download STEP file](/assets/models/full_assembly.step)
-->

### Foot curvature variants

Six distinct feet were tested in total: four across the frontal-radius sweep
($R_f$ = 110, 120, 130, 140 mm, all at $R_s$ = 100 mm), plus two more from the
sagittal-radius sweep ($R_s$ = 80 mm and $R_s$ = 120 mm, both at $R_f$ = 120 mm — the
$R_f$=120/$R_s$=100 foot is shared between both sweeps, so it isn't counted twice).

<!--
  ADD: export a .glb for each of the six feet and put them in assets/models/, then
  duplicate this block once per foot (six times total), changing the filename, alt
  text, and heading each time:

#### R_f = 110 mm, R_s = 100 mm

<model-viewer src="/assets/models/foot_110_100.glb" alt="Rf=110mm, Rs=100mm foot"
  auto-rotate camera-controls style="width: 100%; height: 350px;">
</model-viewer>
-->

<p class="note">Once your six .glb files are in assets/models/, uncomment and duplicate
the block above for each foot: (110,100), (120,100), (130,100), (140,100), (120,80),
(120,120).</p>

### Foot attachment mechanism

This is the mechanism that lets feet swap in and out on the same leg while holding
length, width, and standing-height contribution constant across every foot (see
[How the Robot Was Built](/research/design/) for why that matters).

<!-- ADD: a still render or photo of the attachment mechanism, e.g.:
![Foot attachment mechanism](/assets/img/foot-attachment.png)
-->


<!-- The full paper PDF is not linked here yet — pending MIT URTC / IEEE publication
     clearance on public posting. Add it back once that's confirmed, e.g.:
[Download the full paper (PDF)](/assets/paper.pdf)
-->

## Where to go from here

- **[How the Robot Was Built](/research/design/)** — the physical build these files came from.
- **[The Research](/research/)** — back to the full hub.
