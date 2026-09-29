# STEP-10 — The cellar: the wall opens (Ivana, 2026-09-29)

Do after STEP-09b. Needs two new photos from Ivana (Gemini): `images/wine-wall-off.jpg` and `images/wine-wall-on.jpg` — same frame, backlight off and on. Until they exist, use the current wine-cellar.jpg for both and ship the motion anyway.

## Order
- Cenote beats become: pool → OMé Spa. Remove the wine beat and the rippling wine window from the cenote (keep its text keys).
- New chapter `cellar` right after the cenote, before Surface. Add it to the depth gauge between cenote and surface. Keep the id `wine-cellar` on it so nav links still work.

## The moment (pinned, about 300svh)
1. The cenote fades up into chukum as it does now. The chukum page *is* the wall: a vertical seam appears in the middle of the screen (a 1 px wood line drawing top to bottom).
2. Scroll: the wall splits along the seam and both halves slide apart (two WebGL planes in chukum with a subtle plaster noise texture and a soft shadow on the inner edges, so it reads as thick plaster, not a curtain). Behind them: the wine wall, backlight off (`wine-wall-off`).
3. Scroll on: the backlight comes on row by row from the floor up, like wine filling a glass — shader wipe from `off` to `on` with a soft, warm leading edge. Tiny delay per rack row; slight bloom on the lit edge.
4. Text appears on the left once the light is up: wine.ey, wine.h2a + wine.h2b, wine.body, then wine.s1 / s3 / s5 as three lines.
5. Pointer: a gentle parallax between the glass front and the bottles behind it (two layers from the same photo: split with a depth-ish mask, max 8 px).
6. Exit: the halves slide back closed over the lit wall and the page continues in chukum into Surface (the STEP-09b overlap rule applies here now: cellar → Surface without an empty screen).

## Phones
Same sequence, halves slide top/bottom instead of left/right if the photo is used in portrait crop; wipe stays floor-up.

## Fallback
Two stacked images, CSS clip-path wipe from bottom to top on scroll; the wall halves as two chukum divs sliding apart.
