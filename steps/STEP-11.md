# STEP-11 — Review round 1 (Ivana, 2026-09-29)

Ivana is still sending notes; more items may be added below before you build. Touch nothing outside these items.

## 1. Ground → Inside dissolve is too fast to see
- Now `uMix = smooth(0.86, 1, p)` over a 400svh chapter: about 40svh of scroll, so it's gone in one flick.
- Make the chapter 480svh and run the dissolve over `smooth(0.70, 1, p)` (about 110svh of scroll). Ease it (easeInOutSine) so the middle, where both rooms are mixed, lingers.
- Slow the noise frontier a little too (lower displacement frequency) so the blobs read as a deliberate melt, not glitches.

## 2. The facade is a stripe, not a picture
- `.ground-stage` is 60svh with a chukum band below; on a 1440×900 screen the house reads as a strip.
- Stage to 84svh desktop / 66svh phone. The chukum band below keeps only the facts line.
- The three beats move off the band onto a chukum panel over the lower-left of the photo (same panel style as the vault beat). Panel max 44% of the width on desktop, full width minus gutters on phones, never covering the front door (the push-in target).
- The hero → ground hand-off: the facade should enter as a picture, top edge rising from below, not as a band under the hero text.

## 3. Roots → cenote: the dark screen is empty
The page goes to earth and nothing happens for about a screen. Fill it with water:
- The root tips from the roots chapter keep going for a moment and each one forms a drop of water at its tip (the roots bring water down to the cenote).
- Drops swell, detach and fall with a slight stretch; 6–9 drops, staggered, driven by scroll (not time), so scrolling up reverses them.
- Each drop hits a surface near the bottom of the screen and makes a thin ring ripple in sand/chukum at low opacity. The rings spread and overlap until they become the cenote surface: the cenote shader's ripple sim receives these impacts, so the transition is continuous.
- A faint caustic shimmer starts on the dark as the rings spread.
- Shorten the pure-dark scroll to about half a screen.
- Phones: 4 drops. Fallback: 3 CSS drops (animated SVG) and a ring.

## 4. The cellar is too cold (Ivana's only dislike)
- Stop using `wine-wall-off.jpg` (the blue one). Build the dark state from `wine-wall-on` in the shader: exposure down about 70%, shadows pushed to deep earth/amber, never blue. It should look like the same room at dusk by one candle, not a switched-off freezer.
- The reveal becomes a champagne moment: as the wall halves part, a fine burst of bubbles escapes from the seam (the pop), then a stream of tiny bubbles rises up the screen in light chukum/sand, catching light. When they reach the ceiling slot, the LED light comes on and washes down the stone as it does now, warmer and brighter than now (lift the lit state about 10%).
- Bubbles ties back to the water bubbles of the cenote (and, after the fire beat, sparks turn back into bubbles).
- Phones: fewer bubbles. Fallback: a CSS bubble rise and the warm crossfade.
