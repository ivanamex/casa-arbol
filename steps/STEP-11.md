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

## 5. OMé inside the water, seamlessly
New photos: `images/ome-entrance.jpg`, `images/ome-sign-wall.jpg`, `images/ome-lounge-lantern.jpg` (portrait, 1320 px wide; make web versions as in STEP-02).
- In the cenote the view through the surface is the pool photo. During the OMé beat it crossfades, through the ripples, into `ome-entrance` (the stone wall, wooden letters, jungle): same distortion, same caustics, so it's the same water showing a different place. No hard cut, no frame.
- `ome-sign-wall` as a second surface image late in the OMé beat (slow drift between the two). `ome-lounge-lantern` is the lamp-lit lounge: use it as the image that bridges to the fire (item 6).
- The OMé beat's perk list shows five perks; the temazcal gets its own beat (item 6).

## 6. Water → fire: the temazcal
New photo: `images/temazcal-stones.jpg` (glowing volcanic stones).
- New cenote beat after OMé, text keys `ome.p6.name` + `ome.p6.note` (already in EN/ES/FR).
- The water warms: the shader's palette slides from turquoise/earth to amber/ember; the caustic network turns into glowing ember cracks; the rising bubbles/dust become sparks; a heat shimmer (vertical refraction wobble) replaces the ripples. The surface image goes ome-lounge-lantern → temazcal-stones through the shimmer.
- All scroll-driven and reversible. Phones: fewer sparks, shimmer at quarter resolution. Fallback: crossfade the photos with a warm CSS overlay.

## 7. Fire → cellar
- The ember glow is the last light of the cenote; it hands over directly to the cellar's dark-by-candle state (item 4), so the colour never jumps: amber → amber.
- Sparks rise and become the champagne bubbles of the cellar reveal.
- New photo `images/champagne-pour.jpg` (a hand pouring champagne in front of the lit wine wall): on the cellar text panel, above the text, 16:9, once the light is up. Grade it with the wine-wall photo.

## Order check after this step
canopy → ground → inside → roots (drops) → cenote: pool → OMé → temazcal (fire) → cellar (bubbles, light) → surface.
