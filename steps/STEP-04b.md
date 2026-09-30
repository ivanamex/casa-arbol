# STEP-04b — Type and coordinates fix (Ivana's review, 2026-09-29)

1. Body and subtitle font: Geist doesn't belong next to Unbounded. Replace Geist everywhere with **Sora** (Google, 300/400/500):
   - Subtitles (hero.sub, beat copy, lede lines): Sora 300, clamp(1.05rem, 1.4vw, 1.35rem), line-height 1.5, max 40ch.
   - Body text, buttons, form fields, menu: Sora 400/500.
   - Depth gauge labels: Sora 400, 12 px (not mono).
   - Unbounded stays for display type.
2. Coordinates: remove the "20.6°N · 87.1°W — Playacar Fase II, Riviera Maya" line from the canopy/hero. The coordinates live only in the footer (STEP-08), as the 20°N signature.
3. Geist Mono is used only for that footer coordinates line. Remove it from everywhere else.
4. Check the hero at 1440, 1024 and 390 px: the subtitle sits cleanly under the wordmark and nothing overlaps it.

Done when: one display face (Unbounded) + one reading face (Sora), no coordinates above the footer.
