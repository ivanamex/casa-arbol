# STEP-02 — Palette, fonts, day/night tokens

Reference CSS: `steps/ref/v2-reference.css` (copy from it, adapt as needed).

1. Replace the Google Fonts link with Syne (500, 600) + Instrument Sans (400, 500, 600). Remove Fraunces and Plus Jakarta Sans everywhere.
2. Add the token block from the reference `:root` and `html[data-mode="night"]`:
   - Day: bg #F7F9FA, ink #14302A, sky #B5CEDB, sky-2 #DCE8EF, pink #F8BBCB, pink-ink #B23A63, panel #EAF1F4.
   - Night: bg #0E1A26, ink #EEF3F6, sky #15263A, panel #132233, pink stays #F8BBCB.
3. Remap the legacy tokens (--gold, --gold-lt, --bg, --ink, --white, --teal…) to the new palette so the modal, broker and admin components keep working. No gold/brown anywhere.
4. Headings: Syne 500, letter-spacing −0.035em, sentence case. No italics, no single accented word in headlines.
5. Buttons: 6 px radius, solid ink or outline. Remove trailing → arrows from button labels.
6. Default `<html data-mode="day">`. Body background/colour transition 0.8 s.

Done when: whole site uses the new fonts/colours; layout unchanged.
