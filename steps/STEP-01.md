# STEP-01 — Compare setup

Goal: see current site and redesign side by side on the branch preview.

1. Copy current `index.html` to `old.html`. In old.html only, add `<meta name="robots" content="noindex">` in head.
2. Extract the 3 base64 JPEGs embedded in index.html into files, and point both index.html and old.html at them:
   - about section image → `images/master-suite.jpg`
   - pool section image → `images/cenote-pool.jpg`
   - virtual tour video thumbnail → `images/tour-preview.jpg`
3. Create `compare.html` (noindex):
   - Two iframes side by side, labelled "Current" (`/old.html`) and "Redesign" (`/`).
   - Top bar with width toggle: Desktop (1440 px scaled to fit) / Mobile (390 px).
   - Checkbox "Sync scroll" that scrolls both frames to the same percentage.
   - Plain sans-serif styling, nothing decorative.
4. Do not change the design of index.html in this step.

Done when: `/compare.html` on the Vercel preview shows both versions, identical for now.
