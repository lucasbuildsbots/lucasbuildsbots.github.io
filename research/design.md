---
layout: default
title: How the Robot Was Built
---

[← Back to The Research](/research/)

# Prototype & Design

## Overall model

The walker's design is inspired by the model introduced by Tedrake et al.: two legs
connected by a pin joint at the hip, with toroidal curved feet that provide foot
clearance through lateral rocking. The feet are the whole point of the design — their
surface profile is defined by the toroidal equation covered on the [math](/research/derivation/)
and [CAD](/research/cad/) pages, with independent frontal-plane radius $R_f$ and sagittal-plane
radius $R_s$.

<!-- ADD: Fig. 1 visual render of the model
![Visual render of model description](/assets/img/fig1-render.png)
-->

The walker descends a shallow slope by rocking laterally onto one stance leg, lifting the
opposite (swing) leg off the ground and letting it swing forward. As the walker returns
to upright, the swing leg contacts the ground and becomes the new stance leg, starting
the next step with the opposite leg. This alternating stance/swing sequence lets the
robot descend the slope: gravitational potential energy converts to kinetic energy each
step, while energy is lost to foot-ground collisions and friction.

## Physical build

<!-- ADD: Fig. 3, the designed walker
![The designed walker](/assets/img/fig3-walker.jpg)
-->

Legs and feet were 3D-printed, designed in Fusion CAD. Design choices for the walker
body were guided directly by physical experimentation, informed by insights from prior
passive dynamic walkers — not purely derived from simulation.

**Friction at the hip.** McGeer's finding that hip friction should be minimal and
consistent — since damping causes the walk to decay if energy losses aren't balanced by
gravitational input from the slope — was addressed with ball bearings at the hip, along
with 3D-printed inner bearing spacers and shaft collars to keep them seated correctly.

**Physical tuning.** Beyond total energy dynamics, physical parameters (proportions,
slope, and surface) were calibrated experimentally until the walker showed a reasonably
stable gait with consistent step length, period, and a straight trajectory.

**Yaw control.** A major source of instability beyond total energy was yaw — twisting
about the vertical axis. Collins et al. used counter-swinging arms to solve this on their
larger robot. At this walker's smaller scale, yaw turned out to be reduced enough that a
simpler fix worked: covering the wooden slope in a **textured surface**, which produces
enough scrubbing torque at the contact patch to suppress yaw without adding the mechanical
complexity of counter-swinging arms.

**Swappable feet.** To isolate the effect of toroidal curvature specifically, a
swappable foot mechanism was designed so different feet could be tested on the same
body.

<!-- ADD: Fig. 4, modular robot with swappable feet
![Modular robot model with swappable feet](/assets/img/fig4-swappable-feet.jpg)
-->

Every foot's other geometric variables — length, width, and contribution to the walker's
overall standing height — were held constant across configurations, so that only
curvature changed between trials. Foot length specifically has to be long enough that the
walker doesn't roll onto the foot's edge during normal gait (once that happens, the
[rolling assumption in the derivation](/research/derivation/) no longer holds). Center of mass
was also held fixed across feet by keeping every foot's mass consistent at
**27.45 ± 0.26 g**, achieved by adjusting 3D-print infill density rather than geometry.

## Baseline configuration

A baseline walker — feet with $R_f = 120$ mm and $R_s = 100$ mm — could walk relatively
consistently for about 40 steps down an 8-foot ramp tilted at 0.0663 rad (3.80°), started
by hand. The walker weighs **450.9 g**, has a leg length of **12.87 cm**, and a center of
mass height $h_0$ of approximately **61.5 mm**. This baseline is what the swappable feet
were tested against — see [Experimental Setup](/research/experiment/).

<!-- ADD: Fig. 5, physical walker on the inclined ramp
![Physical passive walker on inclined ramp](/assets/img/fig5-ramp.jpg)
-->

<!-- ADD: link to your 8-foot walk video, e.g.:
[Watch the 8-foot walk](/assets/8-foot-walk.mov)
-->

## Video

<!--
  ADD: your actual walker video, using ONE of the two options below depending on file
  size. GitHub blocks any file over 100MB outright and warns above 50MB, so check your
  file's size first (right-click it in File Explorer > Properties).

  OPTION A — small clip (well under 50MB, e.g. a short compressed .mp4), hosted directly
  in the repo. Put the file at assets/video/8-foot-walk.mp4, then uncomment:

  <video controls width="100%" src="/assets/video/8-foot-walk.mp4"></video>

  OPTION B — larger or raw phone footage. Upload it to YouTube (an "Unlisted" video works
  fine — it won't show up in search or on your channel, but anyone with the link, or
  anyone visiting this page, can watch it), then uncomment and replace VIDEO_ID with the
  ID from the video's URL (the part after watch?v=):

  <iframe width="100%" height="400" src="https://www.youtube.com/embed/VIDEO_ID"
    title="8-foot walk" frameborder="0" allowfullscreen></iframe>
-->


## Where to go from here

- **[The Math](/research/derivation/)** — why this design predicts a specific relationship
  between $R_f$ and rocking period.
- **[Foot Geometry & CAD Files](/research/cad/)** — the exact surface equation and files for the
  feet described above.
