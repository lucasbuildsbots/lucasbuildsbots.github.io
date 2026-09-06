---
layout: default
title: Results
---
{% include nav.html %}

# Results

## Rocking period vs. frontal radius

As $R_f$ increased from 110 mm to 140 mm (with $R_s$ held at 100 mm), the rocking period
decreased — exactly the direction predicted by the derivation on
[The Math](/derivation/) page.

<!-- ADD: Fig. 6 chart, Rf vs average rocking period
![Increasing Rf decreases rocking period](/assets/img/fig6-rf-vs-period.png)
-->

The standard deviation of rocking period across trials was low at every $R_f$ tested,
which is itself a finding: it means the rocking motion behaves like a simple harmonic
oscillator with a relatively constant period, even though step-to-step amplitude can
vary.

**Table I. Standard deviation of rocking periods across $R_f$, per trial**

| $R_f$ (mm) | Trial 1 (s) | Trial 2 (s) | Trial 3 (s) |
|---|---|---|---|
| 110 | 0.02 | 0.02 | 0.01 |
| 120 | 0.01 | 0.01 | 0.02 |
| 130 | 0.02 | 0.02 | 0.02 |
| 140 | 0.03 | 0.02 | 0.02 |

## Checking the prediction directly

The predicted ratio $T_2/T_1$ from Eq. (15) on [The Math](/derivation/) page was
calculated for every possible pairing among the four frontal radii tested, and compared
against the measured ratio from trial data. Across all six pairings, predicted and
measured ratios differ by **at most 1.0%**.

**Table II. Predicted vs. measured ratio of rocking periods across frontal radii pairs**

| Radii (mm) | Predicted Ratio | Measured Ratio | Difference |
|---|---|---|---|
| 110 vs 120 | 0.910 | 0.908 | 0.2% |
| 110 vs 130 | 0.841 | 0.846 | 0.5% |
| 110 vs 140 | 0.786 | 0.792 | 0.6% |
| 120 vs 130 | 0.924 | 0.932 | 0.9% |
| 120 vs 140 | 0.863 | 0.873 | 1.0% |
| 130 vs 140 | 0.934 | 0.936 | 0.2% |

This agreement is notable precisely because the theoretical model assumes smooth rocking
on a level surface, while actual gait introduces foot-ground collisions, yaw motion, and
a time-varying inertia contribution from the swinging leg — none of which are in the
derivation. The fact that measured ratios stay within 1% of the prediction anyway
suggests these unmodeled dynamics don't substantially change the $R_f$-period
relationship over the conditions tested.

## What about the sagittal radius?

While holding $R_f$ fixed at 120 mm, $R_s$ was tested at 80 mm, 100 mm, and 120 mm across
three trials each.

**Table III. Rocking period across $R_s$ values**

| $R_s$ (mm) | Mean Rocking Period (s) | Intra-Trial SD (s) | Inter-Trial SD (s) |
|---|---|---|---|
| 80 | 0.36 | 0.01 | 0.01 |
| 100 | 0.35 | 0.01 | 0.02 |
| 120 | 0.34 | 0.01 | 0.01 |

$R_s$ has a minimal effect on rocking period compared to $R_f$ — but because there's
currently no mathematical model of the frontal/sagittal coupling for a non-spherical
foot, no decisive conclusion can be drawn about whether $R_s$ truly has *zero* effect on
rocking period, or just a small one. This is reported as an open question, not resolved
one way or the other.

## Gait speed and step length regimes

Beyond timing, the toroidal curvature visibly changes gait *behavior*: step length and
walking speed both develop clear trends over the course of a walk, and the direction of
that trend depends on which radius is small vs. large.

**Frontal radius ($R_s$ fixed at 100 mm):**

<!-- ADD: Fig. 7 (speed) and Fig. 8 (step length) charts here -->

- $R_f = 110$ mm — speed trend: $y = 1.156x + 15.848$ (increasing)
- $R_f = 140$ mm — speed trend: $y = -0.6983x + 17.328$ (decreasing)
- $R_f = 110$ mm — step length trend: $y = 0.4147x + 6.5317$ (increasing)
- $R_f = 140$ mm — step length trend: $y = -0.2711x + 5.7454$ (decreasing)

**Sagittal radius ($R_f$ fixed at 120 mm):**

<!-- ADD: Fig. 9 (speed) and Fig. 10 (step length) charts here -->

- $R_s = 80$ mm — speed trend: $y = 1.745x + 13.432$ (increasing)
- $R_s = 120$ mm — speed trend: $y = -0.6079x + 20.948$ (decreasing)
- $R_s = 80$ mm — step length trend: $y = 0.5667x + 5.1$ (increasing)
- $R_s = 120$ mm — step length trend: $y = -0.2021x + 7.175$ (decreasing)

**Interpretation:** these two opposite regimes can be explained by an energy balance
between what the slope supplies and what the walker loses per step. At the smaller
radii tested, the walker gains more energy from the slope per step than it loses to
damping — steps get longer and faster until the walker eventually topples forward. At
the larger radii tested, the opposite happens: an energy deficit means the walker loses
more to damping than it gains from the slope, so steps get shorter and slower until it
shuffles to a stop. This is proposed as a logical interpretation of the observed data,
not a derived result — a theoretical model capturing it directly is future work (see
[Lessons Learned](/lessons/)).

Practically, this also explains why the smaller-radius walkers took *fewer* steps before
the trial ended: they speed up until they fall, while the larger-radius walkers slow to a
stop on their own, in a statically stable configuration, without falling.
