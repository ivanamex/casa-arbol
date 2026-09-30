# RUN-ORDER — Casa Árbol "From canopy to cenote" (branch: redesign-webgl)

## Now
- Nothing queued. Next: Ivana's review round 2, or the device check + pre-merge clean-up listed under Later

## Next
- STEP-11b — footer: credit + coordinates on the right, linked to 20north.art, clear of the WhatsApp button; Brokers Portal hover text fixed

## Open (Ivana) — before going live
- Written OK from The Reef Playacar / OMé to use their spa photos and logo on the site.
- 20north.art public before this merges (it's behind a login in its demo phase).

## Later
- Nothing queued. Next: a device check of STEP-10 on a real phone and a real GPU (the wall's seam, the light wipe, the closing before Surface), then the pre-merge clean-up (delete old.html, compare.html, steps/, RUN-ORDER.md)

## Done
- STEP-11 — review round 1: ground 480svh with the dissolve over 0.70→1 (slow through the middle, coarser frontier); facade stage 84svh/66svh with the three beats on a chukum panel lower-left, the band keeps the facts line; roots → cenote: 8 drops (4 on phones) swell at the root tips, fall and ring on the water, the rings feed the cenote's ripple sim and the water arrives as they spread (fallback: 3 CSS drops + rings); cenote 640svh: pool → OMé → temazcal, the place through the surface crossfades pool → ome-entrance → ome-sign-wall → ome-lounge-lantern → temazcal-stones through the same ripples, the fire slides the palette to ember, caustics become ember cracks, dust becomes sparks, a heat shimmer replaces the ripples, exit fades to the ember-dark wall; cellar: wine-wall-off dropped, the dark state built from wine-wall-on in the shader (−70 % exposure, earth/amber shadows), the wall is dark by candle with a seam of light until the LED comes on (+10 % lit), champagne pop + bubble stream from the seam, champagne-pour on the text panel; web versions of the five new photos
- STEP-10 — Cellar chapter (id wine-cellar) between cenote and surface, in the gauge and menu: wood seam draws, two plaster halves part (top/bottom on portrait), the backlight washes down the stone off → on with a warm leading edge, text on a chukum panel, pointer parallax glass/bottles ≤ 8 px, halves close and hand to Surface; cenote is pool → OMé; graded web versions of wine-wall-on/off; CSS clip-path fallback
- STEP-09c — hero block anchored from the bottom (wordmark min(12.6vw, 22vh)), price clears the gauge; the rooms ribbon hangs from the measured title bottom (+32 px, shrinks on short screens), title on one line on desktop when it fits; rule added: text never overlaps a photo or WebGL image unless set on a panel
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
- Concept: one continuous descent — canopy → house → rooms → roots → cenote (pool, OMé, temazcal fire) → cellar → back to the surface.
- Palette (2026-09-29, from the renders): chukum #EFE8DC · sand #DFC9AB · wood #8D6846 · Corten #9A4A26 (only accent) · earth #2A1E15 · dusk lilac #8F95C4 (rare). Light site; the cenote is the one dark chapter. No teal, no petrol, no gold, no serif.
- Type: Unbounded (display) + Sora (everything you read).
- Credit: footer bottom line, right side: the coordinates + "by 20°N", one link to https://20north.art, in the footer's own style (Ivana, 2026-09-29).
- Phone first: the link goes out on WhatsApp. Poster image visible in < 2.5 s on 4G; WebGL loads after.
- Text never overlaps a photo or WebGL image unless it sits on a panel; check 1440×900, 1280×720, 390×844.
- Keep every data-i18n key, EN/ES/FR, both enquiry forms, Brokers Portal, admin leads panel, WhatsApp button.
- Metric units. Surname "Buric". Agency "Weber-Buric Real Estate".
- Before merge: delete old.html, compare.html, steps/, RUN-ORDER.md.
