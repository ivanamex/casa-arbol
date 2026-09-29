# STEP-03 — Hero: sky, clouds, day/night

Replace the current hero (and remove marquee + stats strip + horizontal scroll text).

Layout, top to bottom:
- Sky gradient background (sky → sky-2 → bg). 4 soft CSS clouds drifting slowly left→right (radial-gradient ellipses, 95–170 s loops). Night mode: clouds fade to 10%, small star dots appear.
- Corners: "Playacar Fase II / Riviera Maya" left, price "$1.675M USD" right (hidden on mobile).
- Huge centred title "Casa Árbol" (Syne 500, ~14vw desktop, stacked two lines on mobile, −0.055em).
- One line under it: "A home [by day | by night] to return to" — the bracket is a segmented toggle (aria-pressed). Clicking sets `html[data-mode]` for the whole page.
- Large rounded image (22 px radius, 16:9 desktop, 4:5 mobile): exterior photo, subtle scale 1.08→1 on scroll.
- Below image: hero.sub text left, buttons "Schedule a Visit" / "View Gallery" right.

Day image slot: add `<img class="img-day" src="/images/casa-arbol-exterior-day.jpg">`. Only when it loads, add class `has-day` so day mode shows it and night mode shows the current dusk render. If it fails to load, remove it silently.

i18n keys (EN/ES/FR): x.hero.a "A home" / "Un hogar" / "Une maison"; x.hero.day "by day" / "de día" / "de jour"; x.hero.night "by night" / "de noche" / "de nuit"; x.hero.b "to return to" / "al que volver" / "où revenir".

Note for Ivana — Gemini prompt for the day render (upload the current exterior):
"Same house, same camera angle and composition, shown at 11 am on a clear sunny day: bright blue sky with a few soft white clouds, warm natural sunlight on the stone and Corten steel facade, lush green tropical garden, crisp daytime shadows, photorealistic architectural render."
Save as images/casa-arbol-exterior-day.jpg.

Done when: toggle switches the whole page day↔night; clouds drift; mobile looks right.
