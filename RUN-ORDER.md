# RUN-ORDER — Casa Árbol "From canopy to cenote" (branch: redesign-webgl)

## Now
- STEP-03 — Canopy: tree of life particles + wordmark (hero)

## Next
- STEP-04 — Ground: the house, light sweep, three reasons
- STEP-05 — Inside: rooms ribbon (curved WebGL gallery)
- STEP-06 — Roots: the systems beneath (solar, water, windows) + descent
- STEP-07 — Cenote: water, caustics, light shafts, ripples (pool, wine, OMé)
- STEP-08 — Surface: closing CTA, price, enquiry drawer, footer "Site by 20°N"
- STEP-09 — mobile, fallback, performance, ES/FR QA

## Done
- STEP-02 — foundation: images/web, palette + fonts, three/gsap/lenis, #gl stage + CA_STAGE scene manager, no-gl fallback, depth gauge
- STEP-01 — compare setup (old.html + compare.html)

## Rules
- Branch `redesign-webgl` only. Never push to main. One step at a time.
- One file: index.html. Vanilla JS modules from CDN (Three.js, GSAP + ScrollTrigger, Lenis). No build, no npm, no React.
- Concept: one continuous descent — canopy → house → rooms → roots → cenote → back to the surface.
- Palette: abyss #03161B, deep water #0A3440, cenote #2FD4C4, limestone #EDE6D8, sunlight #FFE3AE. No green, no gold, no serif.
- Type: Unbounded (display, 200–400) + Geist (body) + Geist Mono (gauge, coordinates, small labels).
- Phone first: the link goes out on WhatsApp. Poster image visible in < 2.5 s on 4G; WebGL loads after.
- Keep every data-i18n key, EN/ES/FR, both enquiry forms, Brokers Portal, admin leads panel, WhatsApp button.
- Metric units. Surname "Buric". Agency "Weber-Buric Real Estate".
- Before merge: delete old.html, compare.html, steps/, RUN-ORDER.md.
