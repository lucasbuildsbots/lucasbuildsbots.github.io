---
layout: default
title: Lessons Learned
---
{% include nav.html %}

# Lessons Learned

Things that only became clear from actually building and running the walker, rather
than from the theory alone.

## Friction is the enemy, and it's manageable

McGeer's observation holds in practice: hip friction has to be minimal *and* consistent,
because any damping there has to be paid back by gravitational energy from the slope
every single step, or the walk decays. Ball bearings at the hip, with 3D-printed inner
spacers and shaft collars to keep them properly seated, were enough to get consistent
gait — no active compensation needed.

## Yaw doesn't always need counter-swinging arms

Collins et al. solved yaw (twisting about the vertical axis) on their larger walker with
counter-swinging arms — a real mechanical addition. At this walker's smaller scale, yaw
turned out to be small enough that a much simpler fix worked: **texturing the ramp
surface** so the contact patch generates a scrubbing torque that resists twisting. Scale
matters here — what's a necessary mechanism at one size may be an unnecessary
complication at another. Worth checking before adding complexity by default.

## Foot geometry has a hard constraint: don't roll off the edge

Foot length has to be long enough that the walker never rolls onto the foot's actual
edge during normal gait. Once that happens, the rolling-contact assumption underlying
the entire [derivation](/derivation/) breaks — the physical foot stops behaving like the
math describes it. This is a design constraint that has to be checked for *every* foot
configuration tested, not just assumed to hold.

## Isolate one variable, or the comparison means nothing

To test curvature specifically, every other foot variable — length, width, contribution
to standing height, and mass — had to be held fixed across configurations. Mass in
particular was matched to **27.45 ± 0.26 g per foot** by adjusting 3D-print infill
density rather than geometry, so that the center of mass didn't shift as a side effect of
swapping feet. Any of these being left uncontrolled would have made it impossible to
attribute a change in gait to curvature specifically.

## The measurement method has a real, stated limit

Two-camera 4K video analysis reliably identified foot collisions — enough to extract
rocking period and step length — but it could not precisely measure angles, like the
inter-leg angle at heel strike or yaw during the cycle. That's a genuine gap in what this
dataset can speak to, and it's the direct reason a sensor-based data acquisition system
is the top item for future work, rather than just refining the current video method.

## Open questions this work leaves on the table

- **Does $R_s$ actually affect rocking period, or not?** The data shows a small effect,
  but with no existing mathematical model of frontal/sagittal coupling for a
  non-spherical foot, "small" can't be distinguished from "zero" with confidence.
- **A theoretical model of the frontal/sagittal coupling itself.** This work
  deliberately sidesteps that coupling to get a clean closed-form result for timing —
  actually modeling it is the natural next step.
- **Knees.** Adding them would move the design toward a more anthropomorphic gait, at the
  cost of added complexity.
- **Human applications.** Adamczyk et al. showed that rigid rocker arcs attached to the
  bottom of human shoes can make walking more energy-efficient by exploiting the same
  passive mechanics. Understanding how frontal/sagittal foot curvature affects gait here
  could eventually inform curvature designs that help guide natural walking for people
  with injuries or gait disabilities.

## Acknowledgments

Thanks to Michael Liva and Arend L. Schwab for advice on constructing the walker, and to
Carlos Nodarse at Bergen County Academies for providing 3D printers and lab space.
