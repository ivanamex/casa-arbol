# STEP-09c — Text colliding with images (Ivana, 2026-09-29)

Only these fixes. Check each at 1440×900, 1280×720 (short laptop) and 390×844.

## 1. Canopy: subtitle cut by the facade photo, price cut at the right edge
- `.hero-content` sits at `top:60vh`; with the huge wordmark + three lines of hero.sub it runs past the bottom of the hero and the ground chapter's facade photo covers the last line.
- Anchor the block from the bottom instead (`bottom: max(10vh, 72px)`, no `top`), and let the wordmark size also respect height: `font-size: min(12.6vw, 22vh)`. The whole subtitle must be fully visible above the facade photo on every size above.
- `.hero-meta` price ("$1.675M USD") is clipped by the right edge / depth gauge. Give it right padding that clears the gauge (gauge width + 24 px), or move it to the left corner. Never clipped.

## 2. Inside: "Crafted in every detail" runs into the ribbon photos
- `.rib-hd` sits at `top:11vh`; the ribbon planes start higher than the title's bottom on shorter screens.
- Measure the title's bottom (getBoundingClientRect) on load and resize, and place/scale the ribbon so its top edge is always at least 32 px below it. On desktop let the title run on one line if it fits (max-width 80vw).
- The same rule on phones.

## 3. The general rule (add to RUN-ORDER Rules)
- Text never overlaps a photo or WebGL image unless it's intentionally set on a panel. Check every chapter at the three sizes above before saying done.
