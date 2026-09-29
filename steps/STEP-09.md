# STEP-09 — QA

1. Phones first: iPhone 12-size and a mid Android, in Chrome and inside the WhatsApp in-app browser. Poster visible under 2.5 s on throttled 4G; no jank while scrolling; the page never goes blank while WebGL loads.
2. Fallback mode (reduced motion on): the whole story still reads, every section has its image.
3. Desktop 1440 and 1920: 60 fps target; dispose off-screen chapters; no memory growth after a full scroll up and down three times.
4. applyLang('es') and ('fr'): every new key translated, nothing raw, long Spanish/French words don't overflow the huge type.
5. Forms send via mailto, admin panel opens (triple-click ⚙), Brokers Portal and #register-client deep links work.
6. No console errors. Update RUN-ORDER.md.
