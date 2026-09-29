# STEP-09b — Close the empty gap after the cenote (Ivana, 2026-09-29)

Only this fix. Touch nothing else.

## What's wrong
Between the last cenote beat (OMé Spa) and the Surface heading ("Begin your Casa Árbol journey") there is about 1.5 screens of empty chukum. It adds up from:
1. `.cenote-scroll` (640svh desktop / 560svh phone): the OMé beat ends at p = 0.95, then p 0.95→1 only fades `.cenote-out` to chukum — about 27svh of nothing.
2. When the sticky `.cenote-pin` releases, its last frame is a full chukum screen (cenote-out at opacity 1) that scrolls away — another ~100svh of nothing.
3. `.surface-inner` starts with padding-top 20vh (14vh on phones).

## Fix
- The Surface slides up over the fading cenote instead of after it: give `.cenote-scroll` a negative bottom margin of −100svh, and `.surface` `position:relative; z-index:2` with a background that is transparent at the top and chukum below (the existing `.surface-rise` glow can sit in that transparent part).
- Beats: OMé window ends at 0.9; `--co` fade runs 0.88 → 1, so the dark water turns to chukum exactly as the Surface heading arrives.
- `.surface-inner` padding-top: 10vh desktop, 8vh phone.
- Recheck the anchors #wine-cellar / #ome-spa (top: calc(.37 / .69 …)) still land on their beats; adjust if the window change moves them.

## Done when
At 1440×900 and 390×844, scrolling slowly from the OMé beat to the enquiry form, no frame shows more than about a third of the screen empty. The cenote still fades to light; nothing else changes.

Also: RUN-ORDER.md's Done list has STEP-06/07/08 written several times — keep one line each.
