# STEP-11b — The 20°N credit (follows the 20north rule of 2026-09-29)

Tiny step, after STEP-11. Touch nothing else.

The agency rule (20north RUN-ORDER, 2026-09-29): on every client site the last line of the footer reads `by 20°N`, plain text in the client's own font, colour and footer size, linked to https://20north.art. No logo, no orange, no coordinates, no animation.

- Footer bottom line: replace "Site by 20°N" with `<a href="https://20north.art" rel="noopener">by 20°N</a>`, as the last item on the line. Same font, colour and size as the rest of the line; underline on hover/focus only, visible focus ring.
- Remove the coordinates signature (Geist Mono "20.6296°N 87.0739°W") from the footer, and drop the Geist Mono font load entirely if nothing else uses it.
- Leave the geo meta tags in <head> alone (they're for search, not display).

Note: 20north.art is behind a login during its demo phase. Fine on this preview branch; before merging to main it must be public (see RUN-ORDER Open).
