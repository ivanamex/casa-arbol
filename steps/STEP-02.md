# STEP-02 — Foundation

## Images
- The photos in images/ are 6–8 MB each. Make web versions with sharp or Python PIL in `images/web/`: long side 2400 px (desktop) and 1200 px (`-m` suffix, phone), WebP quality 80 + JPG fallback. Targets: under 400 KB desktop, under 150 KB phone.
- Also make a 64 px blurred placeholder of each, inlined as base64 for instant paint.

## Tokens
- Colours: abyss #03161B · deep #0A3440 · cenote #2FD4C4 · limestone #EDE6D8 · sunlight #FFE3AE. Text is limestone on abyss; body copy at 78% opacity.
- Remove every green (#14302A etc.), every gold/brown (#A07840, #C9A46A…) and the Syne / Instrument Sans / Fraunces fonts.
- Remap the legacy tokens (--gold, --gold-lt, --bg, --ink, --white, --teal…) so the modal, broker and admin components still render, in the new palette.
- Fonts (Google): Unbounded 200/300/400, Geist 400/500, Geist Mono 400.
- Display type: Unbounded 200–300, lowercase or sentence case, letter-spacing −0.04em, huge sizes (up to 16vw). Small labels in Geist Mono 12–13 px. No all-caps tracked eyebrows.

## Libraries (ES modules from jsdelivr, pinned versions)
- three (latest r17x), gsap + ScrollTrigger, lenis (smooth scroll, linked to ScrollTrigger).

## Stage
- One fixed full-screen `<canvas id="gl">` behind the HTML, one WebGLRenderer, DPR capped at 1.5 on phones and 2 on desktop.
- A small scene manager: each chapter (canopy, ground, inside, roots, cenote, surface) registers `init / update(progress, velocity) / dispose`, and only the chapters in view render.
- HTML content scrolls on top; chapters are `<section data-chapter="…">` with ScrollTrigger progress passed to the scene.

## Fallback (decide once, on load)
- No WebGL2, `prefers-reduced-motion`, `navigator.connection.saveData`, or deviceMemory < 3 → no canvas. Every chapter shows its poster image with CSS-only fades. The site must be complete and beautiful in this mode.

## Depth gauge (the scroll indicator)
- Fixed on the right edge (bottom on phones): a thin vertical line with layer names in Geist Mono — canopy · ground · inside · roots · cenote · surface — and a moving marker. The active layer brightens.
- Top-left: logo mark + "Casa Árbol". Top-right: EN/ES/FR, "Private Enquiry", "Menu".

## Content
- Keep the existing forms, modals, broker portal, admin panel, WhatsApp button and LANG object working. Sections below get rebuilt step by step; in this step you can leave the current body content in place under the new tokens.

Done when: new fonts and palette everywhere, canvas running an empty scene, fallback mode works, gauge moves with scroll.
