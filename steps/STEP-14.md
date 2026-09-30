# STEP-14 — Back to the top (Ivana, 2026-09-29)

The page is very long (the whole descent). Give people a way back up, without making them scroll back through every WebGL chapter.

## Where
1. **Footer**: a text link at the top of the footer, centred under the small particle tree: "Back to the canopy" (EN) / "Volver a la copa" (ES) / "Retour à la canopée" (FR), key `x.top`. Footer type, underline on hover/focus, visible focus ring.
2. **Header logo**: it already scrolls to top (smooth, through every chapter). Keep it as the main way up, but route it through the quick veil below. The header is fixed, so it's always there — no floating button (keeps the corner clear for WhatsApp).
3. **Depth gauge**: make the layer names clickable (buttons, keyboard-reachable). "canopy" goes to the top; each other name jumps to its chapter.

## How it goes up
- Not a long smooth scroll through 3000+ svh of WebGL. Instead: a quick veil in chukum fades in (300 ms), jump to top instantly (Lenis `scrollTo(0, {immediate:true})`), the canopy particles re-assemble the tree as on first load (short version, ~1.2 s), veil fades out.
- Same veil for gauge jumps to other chapters (land at the chapter's start).
- Reduced motion: instant jump, no veil animation.
- Remove the dead `btt` script (`bttBtn` refers to an element that no longer exists).

## Check
1440×900, 390×844, EN/ES/FR; keyboard: Tab reaches the logo, the footer link and the gauge names, Enter works; no console errors.
