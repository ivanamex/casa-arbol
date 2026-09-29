# RUN-ORDER — Casa Árbol "From canopy to cenote" (branch: redesign-webgl)

## Now
- STEP-09c — text colliding with images: hero subtitle + price, gallery title vs ribbon

## Next
- STEP-10 — the cellar: wine moves out of the cenote into its own chapter, the wall opens, the backlight fills up (needs Ivana's 2 Gemini photos)

## Done
- STEP-09b — Surface slides up over the fading cenote (−100svh overlap, transparent-to-chukum top, beats end 0.90 / fade 0.88→1, padding 10vh/8vh): no frame more than a third empty at 1440 and 390; vault beat on suite-vault-front (web versions, top-anchored crop); 9th ribbon photo suite-sculpted-wall with img.suite-sculpted EN/ES/FR; honest alt for the ground-floor room; anchors re-tuned
- STEP-09 — QA pass (iPhone 12 / mid Android / 1440 / 1920 / fallback both sizes, throttled 4G): poster paints in 0.5–1.1 s, page never blank while WebGL loads, no console errors, flat memory over 3 up/down cycles, heavy chapters (ground, inside, cenote) now sleep off screen and wake from cache; ES/FR: no raw keys, no overflow (beat titles hyphenate); mailto forms, admin ⚙, Brokers Portal, #register-client and ?portal=brokers deep links all work. Open, scheduled: cenote→surface gap (09b), hero/gallery text vs images (09c). Not testable here: real-GPU fps, WhatsApp in-app browser
- STEP-08 — Surface: light rising into chukum, lead.h2 huge, price + lines, two virtual-experience buttons, underline form with a Corten submit; enquiry + broker modals as a right-side chukum drawer; footer in sand with the small particle tree, contacts, portal, socials, EN/ES/FR, bottom line + 20°N signature; chapter menu on earth with contacts and languages on the side; WhatsApp Corten on hover
- STEP-07 — Cenote: full-screen water shader (earth-dark, pool photo as the surface seen from below, Voronoi caustics, radial light shafts, dust drifting up), ping-pong ripple sim stirred by the pointer, wine cellar in a rippling window; three floating beats (pool, wine, OMé perks); fades back to chukum; SVG-turbulence fallback; no sound toggle (no loop available)
- STEP-06 — Roots: procedural root system (4 main roots + branches + 2 minors) grows with scroll as soft ribbons, wood → Corten → earth; systems (feat.f2/f1/f3/f9) appear where roots land; arch.btn; page darkens to earth into the cenote; SVG stroke-dash fallback; plans section folded in
- STEP-05 — Inside: 8 photos on a curved WebGL ribbon (scroll turns it, velocity bends it + RGB split, hover/tap straightens with caption + index), vault beat with rising light (feat.f7), kitchen + brand list close; phone swipe ribbon; scroll-snap fallback
- STEP-04c — earth palette: chukum/sand/wood/Corten/earth/lilac tokens, legacy tokens remapped, old teal/petrol removed; line-art mark as the hero poster, seed-coloured particles (normal blending), ground beats in earth on a chukum band, wood/Corten gauge, earth WhatsApp disc; videos, lead and footer light (only the cenote stays dark), small text in deep wood #6F4E38 for AA
- STEP-04b — Sora 300/400/500 for all reading text (subtitles 300, gauge 12 px); Geist Mono reserved for the footer 20°N signature (--font-coords); coordinates removed from the hero
- STEP-04 — Ground: facade on a cover-fit plane, golden-hour sweep + grain, scroll push-in to the door, three pinned beats (x.r1–3, EN/ES/FR), facts line, noise dissolve into the first interior; CSS push-in/crossfade fallback
- STEP-03 — Canopy: mark sampled into 30k/10k particles, pollen → tree assembly, wordmark, pointer spring, scroll dissolve; SVG stroke-draw fallback
- STEP-02 — foundation: images/web, palette + fonts, three/gsap/lenis, #gl stage + CA_STAGE scene manager, no-gl fallback, depth gauge
- STEP-01 — compare setup (old.html + compare.html)

## Rules
- Branch `redesign-webgl` only. Never push to main. One step at a time.
- One file: index.html. Vanilla JS modules from CDN (Three.js, GSAP + ScrollTrigger, Lenis). No build, no npm, no React.
- Concept: one continuous descent — canopy → house → rooms → roots → cenote (pool, OMé) → cellar → back to the surface.
- Palette (2026-09-29, from the renders): chukum #EFE8DC · sand #DFC9AB · wood #8D6846 · Corten #9A4A26 (only accent) · earth #2A1E15 · dusk lilac #8F95C4 (rare). Light site; the cenote is the one dark chapter. No teal, no petrol, no gold, no serif.
- Type: Unbounded (display) + Sora (everything you read). Geist Mono only for the footer coordinates.
- 20°N signature: the property's coordinates, small and quiet, in the footer next to "Site by 20°N" — never in the header or hero.
- Phone first: the link goes out on WhatsApp. Poster image visible in < 2.5 s on 4G; WebGL loads after.
- Text never overlaps a photo or WebGL image unless it sits on a panel; check 1440×900, 1280×720, 390×844.
- Keep every data-i18n key, EN/ES/FR, both enquiry forms, Brokers Portal, admin leads panel, WhatsApp button.
- Metric units. Surname "Buric". Agency "Weber-Buric Real Estate".
- Before merge: delete old.html, compare.html, steps/, RUN-ORDER.md.
