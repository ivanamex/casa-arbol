# STEP-08 — Menu, enquiry drawer, translations, QA

1. Header: logo mark + "Casa Árbol", EN/ES/FR, "Private Enquiry", "Menu". Transparent over hero, solid blurred background after it.
2. Menu: full-screen pink panel (navy at night), large Syne links left, hero.sub + languages + WhatsApp contacts + enquiry button right.
3. Enquiry modal becomes a right-side drawer (slides in, 22 px left radius, full height). Broker modals keep their current behaviour, restyled with new tokens.
4. Add every new x.* key in EN/ES/FR. Run applyLang('es') and ('fr') and check no key shows raw.
5. QA at 1440 / 1024 / 390 px, day and night, reduced motion. No console errors. Forms still send via mailto; admin panel still opens (triple-click ⚙).
6. Update RUN-ORDER.md.
