# STEP-07 — Cenote

The extravagant moment. We are below the water, looking up.

- Full-screen shader: the underwater view of a cenote. Deep water gradient (#0A3440 → #03161B), animated caustics (layered Voronoi/noise), volumetric light shafts from an opening above (radial blur of a bright disc), floating particles (dust/bubbles drifting up).
- Pointer/touch makes ripples on the surface above: a small ripple simulation (ping-pong render targets) that bends the light shafts and caustics.
- The cenote-pool photo (aerial) appears as the view through the surface when you look up: mix it in at the top of the frame, distorted by the ripples.
- Chapters inside the cenote, text floating in the water, one after another:
  1. the pool — pool.intro, chips: natural stone edges · waterfall · beach entry · tropical landscaping
  2. the wine cellar — wine.body (the cellar photo in a window whose edges ripple), wine.s1 / s3 / s5
  3. OMé Spa for two — ome.body + the 6 perks in a list
- Optional, off by default: a sound toggle bottom-left ("sound on") for a soft water ambience. Only if a royalty-free loop under 300 KB is available; otherwise skip.
- Phones: half the particles, ripple sim at a quarter resolution, light shafts simplified.
- Fallback: the pool photo with a CSS caustic overlay (animated SVG turbulence) and the same text.
