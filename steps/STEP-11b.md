# STEP-11b — The 20°N credit (follows the 20north rule of 2026-09-29)

Tiny step, after STEP-11. Touch nothing else.

The agency rule (20north RUN-ORDER, 2026-09-29): on every client site the last line of the footer reads `by 20°N`, plain text in the client's own font, colour and footer size, linked to https://20north.art. No logo, no orange, no coordinates, no animation.

- Footer bottom line: replace "Site by 20°N" with `<a href="https://20north.art" rel="noopener">by 20°N</a>`, as the last item on the line. Same font, colour and size as the rest of the line; underline on hover/focus only, visible focus ring.
- Remove the coordinates signature (Geist Mono "20.6296°N 87.0739°W") from the footer, and drop the Geist Mono font load entirely if nothing else uses it.
- Leave the geo meta tags in <head> alone (they're for search, not display).

Note: 20north.art is behind a login during its demo phase. Fine on this preview branch; before merging to main it must be public (see RUN-ORDER Open).

## Also: Brokers Portal button text vanishes on hover
- Three rule sets fight: line ~592 (`footer .f-broker:hover` fills Corten, text #FBF6EE), ~828–829 (old legacy `.f-broker`), and ~865–866 (`footer .f-broker:hover{color:var(--corten)}`), which wins and paints Corten text on a Corten fill.
- Keep one definition only (the ~591–592 pair: outline at rest, Corten fill + `--on-corten` text on hover and focus-visible). Delete the other two.
- Grep the file for any other button whose hover sets the text to the same colour as its fill (enquiry submit, drawer submit, portal options, language buttons) and fix the same way.
- The coordinates at bottom right also sit under the WhatsApp button; they go away with the credit change above.
