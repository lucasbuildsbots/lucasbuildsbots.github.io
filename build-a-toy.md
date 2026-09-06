---
layout: default
title: Build a Simple Passive Walker (No CAD Needed)
---

[← Home](/)

# Build Your First Passive Walker: A Toy

You don't need CAD, a 3D printer, or bearings to see passive dynamic walking work. The
entire phenomenon — a two-legged mechanism walking down a slope using nothing but
gravity and its own geometry — can be built on a desk with cardboard and a couple of
pins. This page is the on-ramp before the [research-grade design](/research/design/): build this
first, feel why it walks, then go add curvature and rigor.

## Why this works at all

A passive walker doesn't need motors because gravity plus geometry can produce the same
alternating stance/swing motion that a motor would otherwise have to drive. Put the
walker on an incline: gravity pulls the center of mass forward and down, the stance leg
rocks over its foot, and the swing leg — free to pivot at the hip — swings forward under
its own weight, just like a pendulum released from an angle. If the geometry (leg
length, hip placement, foot shape, mass distribution) is right for the slope angle you've
chosen, the walker settles into a repeating gait instead of tipping over or grinding to a
stop. Get the geometry wrong for that slope, and it won't — this tuning relationship is
the entire subject of the [math](/research/derivation/) and [experiment](/research/experiment/) sections
later on this site.

## What you need

- Two legs — stiff material (cardboard, thin plywood, or acrylic), roughly equal length,
  straight.
- A hip joint — a single pin, small bolt, or brad through both legs at one end, loose
  enough to pivot freely with minimal friction. Friction at the hip is the enemy: it
  bleeds energy out of the gait every step, and if the slope isn't supplying enough
  gravitational energy to make up for it, the walker slows down and stops.
- Feet — curved arcs (a rocker shape) glued or screwed to the bottom of each leg, so the
  leg rolls over the foot instead of pivoting on a single point. Even a foot cut from a
  curved scrap of wood or a section of a circular disk works.
- A ramp — a board you can tilt to different shallow angles, ideally with some texture
  (sandpaper, felt, a rubber mat) rather than a slick surface.

## Assembly and why each choice matters

Connect the two legs at the hip so they can swing freely past each other, like a pair of
scissors that can open past straight. Attach a curved foot to the bottom of each leg,
oriented so the leg rocks forward-backward on the curve rather than sitting on a flat
sole. Keep the two legs and feet as close to identical in mass and shape as you can — an
asymmetric walker will pull to one side or twist (yaw) instead of walking straight.

## Testing it

Stand the walker at the top of the ramp with one leg forward as the "stance" leg, and
give it a very gentle push or just let go. Watch what happens:

- If it immediately falls forward or backward: the ramp angle is probably too steep or
  too shallow for this geometry, or the hip is too stiff.
- If it takes a step or two and then stops: energy is being lost somewhere it can't be
  recovered — usually hip friction, or feet not rolling cleanly.
- If it walks several steps and picks up speed until it topples: it's gaining more energy
  from the slope than it loses per step, which is one of the same gait regimes this
  project measured formally in its [results](/research/results/).

Try a few different ramp angles for the same walker. You'll find a narrow range where it
actually walks several steps consistently — that range is exactly what "basin of
attraction" means for physical geometry rather than just a simulation abstraction.

## Where to go from here

Once you've got a toy version walking reliably, the natural next questions are exactly
the ones this research addresses: what happens if you change the *shape* of the foot's
curvature independently in two different directions, and can you predict how that changes
the walker's timing before you build it?

- **[How the Robot Was Built](/research/design/)** — the research-grade version of the same idea.
- **[The Research](/research/)** — the full hub, if you'd rather pick a specific piece.
