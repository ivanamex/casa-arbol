# STEP-13 — Go live: merge to main, keep the classic site for brokers (Ivana, 2026-09-29)

Ivana's decisions: the redesign goes to main. The current (old) site stays online as a full site brokers can use to sell. OMé photos are cleared (Ivana has The Reef's OK). The credit links to Instagram until 20north.art is public.

## 0. First, before merging: the empty brown stretch before the cellar
- On the way from the temazcal into the cellar there is about a screen of plain brown (#4D331F) with nothing on it. Causes: `.cellar-lead` (100svh of lead-in) plus the start of the 800svh `.cellar-scroll` before the bubbles begin.
- Remove the lead-in gap: the cellar starts where the fire ends (overlap the cenote's tail as STEP-09b did for Surface). The first bubbles must be on screen the moment the brown appears — sparks from the fire turn into bubbles in the same frame, never a blank one.
- Tighten `.cellar-scroll` so act 1 (bubbles) is about 1 screen, act 2 (pour) about 2, act 3 (wall + text) about 3.
- Check at 1440×900 and 390×844: scrolling slowly from the temazcal to the wine wall, no frame is ever plain brown.

## 1. Keep the classic site
- Move `old.html` to `classic/index.html`. Fix its relative paths (`./images/…` → `/images/…`) so it works from the folder. Keep `noindex` and add `<link rel="canonical" href="https://casaarbolplayacar.com/">`.
- Make sure every image it uses still exists in `images/` (don't delete originals the classic site needs).
- Its Brokers Portal, forms and ?portal=brokers deep link keep working at `/classic/`.
- Tag the pre-merge main as `classic-2026-09` so the old version is also recoverable from git.

## 2. Routing (vercel.json)
- The catch-all rewrite sends everything to /index.html. Keep it for the SPA-style hash links, but let real files and `/classic` through: put an explicit rule first, `{"source":"/classic","destination":"/classic/index.html"}` and `{"source":"/classic/(.*)","destination":"/classic/index.html"}`, then the catch-all.
- Check: `/`, `/classic`, `/classic/`, `/?portal=brokers`, `/#register-client`, `/classic/?portal=brokers`, `/robots.txt`, `/sitemap.xml`, an image URL.

## 3. Credit link
- "20.6296°N 87.0739°W by 20°N" links to `https://www.instagram.com/20north.art/` for now (target _blank, rel noopener). Leave a one-line HTML comment-free note in RUN-ORDER: switch to https://20north.art when it's public.

## 4. Nothing internal ships
- Delete `compare.html`.
- Keep `RUN-ORDER.md` and `steps/` in the repo (it's how we work) but keep them off the website: add a `.vercelignore` with `RUN-ORDER.md`, `steps/`, `compare.html`, `*.md`.
- `sitemap.xml`: only `/` (not /classic).

## 5. Merge
- Merge `redesign-webgl` into `main` (a merge commit, not a squash, so the steps' history stays), push main, and check the production deploy at casaarbolplayacar.com on desktop and phone: the canopy loads, the WebGL chapters run, the enquiry form opens, /classic works.
- Afterwards the working branch is main again; update RUN-ORDER's first line and the "Branch" rule accordingly, and move the Open items that are settled to Done.
