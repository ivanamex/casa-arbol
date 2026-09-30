# STEP-11b — The 20°N credit (follows the 20north rule of 2026-09-29)

Tiny step, after STEP-11. Touch nothing else.

The agency rule (20north RUN-ORDER, 2026-09-29): the credit is plain `by 20°N` in the client's own footer style, linked to https://20north.art, no logo, no orange, no animation. For Casa Árbol Ivana keeps the coordinates beside it.

- Footer bottom line, Ivana's call for this site (2026-09-29): split it in two.
  - Left: "By Private Sale Only. © 2026 Casa Árbol · Weber-Buric Real Estate".
  - Right: the coordinates "20.6296°N 87.0739°W" (Geist Mono, as now), then `<a href="https://20north.art" rel="noopener">by 20°N</a>` in the footer's own font, colour and size. Coordinates + credit are one link to 20north.art.
  - Underline on hover/focus only, visible focus ring.
  - The right group must clear the WhatsApp float button: right padding of button size + 24 px, and on phones the right group wraps under the left one, left-aligned.
- Leave the geo meta tags in <head> alone (they're for search, not display).

Note: 20north.art is behind a login during its demo phase. Fine on this preview branch; before merging to main it must be public (see RUN-ORDER Open).

## Also: Brokers Portal button text vanishes on hover
- Three rule sets fight: line ~592 (`footer .f-broker:hover` fills Corten, text #FBF6EE), ~828–829 (old legacy `.f-broker`), and ~865–866 (`footer .f-broker:hover{color:var(--corten)}`), which wins and paints Corten text on a Corten fill.
- Keep one definition only (the ~591–592 pair: outline at rest, Corten fill + `--on-corten` text on hover and focus-visible). Delete the other two.
- Grep the file for any other button whose hover sets the text to the same colour as its fill (enquiry submit, drawer submit, portal options, language buttons) and fix the same way.
- The coordinates at bottom right also sit under the WhatsApp button; they go away with the credit change above.
