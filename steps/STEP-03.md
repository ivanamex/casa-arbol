# STEP-03 — Canopy (hero)

The Casa Árbol mark is a tree of life. The site opens by growing it.

- Sample `images/casa-arbol-logo/casa-arbol-mark.svg` (draw it to an offscreen canvas and read the filled pixels) into points: 30 000 on desktop, 10 000 on phones.
- Particles start as scattered drifting pollen (curl-noise motion, sunlight #FFE3AE to limestone, additive blending, tiny soft round sprites).
- Preloader = the assembly: while the fonts and first images load, the particles gather into the tree over about 2.5 s. When it's complete, "casa árbol" fades up under it in Unbounded 200, about 14vw.
- Mouse/touch: particles near the pointer push away softly and return (spring).
- Scroll 0 → 1 through this chapter: the tree breaks apart upward like leaves in wind, the camera sinks, and the particles turn into light falling through a canopy onto the next chapter.
- Small text, bottom left, Geist Mono: "20.6°N · 87.1°W — Playacar Fase II, Riviera Maya". Bottom right: "$1.675M USD".
- One line of copy under the wordmark: hero.sub (existing key).
- Fallback: the mark as SVG, drawn with stroke-dash animation, over the blurred exterior photo.

Done when: load → tree assembles → wordmark; scroll → tree dissolves into light. 60 fps on a mid laptop, smooth on an iPhone 12.
