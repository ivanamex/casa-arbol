# STEP-05 — Spaces: pinned horizontal scroll

Replace the gallery with an ERA-style horizontal walk through the rooms.

- Section height = track width − viewport width + viewport height. Inner container sticky, 100svh.
- Vertical scroll moves the track sideways (translateX). Thin progress bar under it in pink-ink.
- First panel: heading "Crafted in every detail" + hint "Scroll to walk through" (touch: "Swipe").
- Then 8 photos, each with caption (existing img.* keys) and "01/08"-style index on the right of the caption: exterior (narrow/portrait), ground floor bedroom, guest suite ×2, upper suite ×3, guest bathroom.
- Below 820 px, or with reduced motion: no pinning — native horizontal swipe with scroll-snap.
- Keep the nav link #gallery pointing here.
