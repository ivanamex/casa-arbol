# RUN-ORDER — Casa Árbol "From canopy to cenote" (branch: redesign-webgl)

## Now
- STEP-05 — Inside: rooms ribbon (curved WebGL gallery)

## Next
- STEP-06 — Roots: the systems beneath (solar, water, windows) + descent
- STEP-07 — Cenote: water, caustics, light shafts, ripples (pool, wine, OMé)
- STEP-08 — Surface: closing CTA, price, enquiry drawer, footer "Site by 20°N"
- STEP-09 — mobile, fallback, performance, ES/FR QA

## Done
- STEP-04c — earth palette: chukum/sand/wood/Corten/earth/lilac tokens, legacy tokens remapped, old teal/petrol removed; line-art mark as the hero poster, seed-coloured particles (normal blending), ground beats in earth on a chukum band, wood/Corten gauge, earth WhatsApp disc
- STEP-04b — Sora 300/400/500 for all reading text (subtitles 300, gauge 12 px); Geist Mono reserved for the footer 20°N signature (--font-coords); coordinates removed from the hero
- STEP-04 — Ground: facade on a cover-fit plane, golden-hour sweep + grain, scroll push-in to the door, three pinned beats (x.r1–3, EN/ES/FR), facts line, noise dissolve into the first interior; CSS push-in/crossfade fallback
- STEP-03 — Canopy: mark sampled into 30k/10k particles, pollen → tree assembly, wordmark, pointer spring, scroll dissolve; SVG stroke-draw fallback
- STEP-02 — foundation: images/web, palette + fonts, three/gsap/lenis, #gl stage + CA_STAGE scene manager, no-gl fallback, depth gauge
- STEP-01 — compare setup (old.html + compare.html)

## Rules
- Branch `redesign-webgl` only. Never push to main. One step at a time.
- One file: index.html. Vanilla JS modules from CDN (Three.js, GSAP + ScrollTrigger, Lenis). No build, no npm, no React.
- Concept: one continuous descent — canopy → house → rooms → roots → cenote → back to the surface.
- Palette (2026-09-29, from the renders): chukum #EFE8DC · sand #DFC9AB · wood #8D6846 · Corten #9A4A26 (only accent) · earth #2A1E15 · dusk lilac #8F95C4 (rare). Light site; the cenote is the one dark chapter. No teal, no petrol, no gold, no serif.
- Type: Unbounded (display) + Sora (everything you read). Geist Mono only for the footer coordinates.
- 20°N signature: the property's coordinates, small and quiet, in the footer next to "Site by 20°N" — never in the header or hero.
- Phone first: the link goes out on WhatsApp. Poster image visible in < 2.5 s on 4G; WebGL loads after.
- Keep every data-i18n key, EN/ES/FR, both enquiry forms, Brokers Portal, admin leads panel, WhatsApp button.
- Metric units. Surname "Buric". Agency "Weber-Buric Real Estate".
- Before merge: delete old.html, compare.html, steps/, RUN-ORDER.md.
