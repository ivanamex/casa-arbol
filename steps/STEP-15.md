# STEP-15 — Phone: no chapter ever shows a plain brown screen (Ivana, 2026-09-30)

Ivana's iPhone, after the "Phone fixes" push (17:23, ES): the cenote screen is plain earth — no pool photo, no water, no movement, only the beat text on brown. Other backgrounds are missing too.

## Why (found in the code)
- The chapter photos (`.cenote-fallback`, `.cellar-fb`, `.rib-fallback`, roots SVG, …) only show under `html.no-gl`.
- `failChapter()` only removes `<name>-live`, so a chapter that throws shows its bare base colour, not its photo. The comment says "hands its screen back to its photo" — it doesn't.
- `boot()`: if `init()` rejects (shader compile, texture load, iOS memory), it sets `inited = false` but not `failed`, so it retries on every scroll in and stays brown forever. No photo, no warning on screen.
- While a chapter is still initialising (or re-waking after `dispose()`), there's nothing but the base colour.

## Do
1. **Per-chapter photo mode.** Add `html.<name>-fb` (canopy, ground, inside, roots, cenote, cellar, surface). Every `html.no-gl …` rule for a chapter also matches `html.<name>-fb …`. The chapter's canvas output is skipped while `-fb` is on.
2. **Set `-fb` when:** `init()` rejects → mark `failed`, add `-fb`, no retry · `update`/`render` throws (`failChapter`) → add `-fb` · the chapter is on screen and not `initDone` after 1.2 s → add `-fb`; remove it with a 0.6 s crossfade once it goes live (a slow wake shows the photo, then the water fades in).
3. **Wake from sleep on phones:** start `init()` when the chapter is within one screen (ScrollTrigger `start: 'top bottom+=100%'`), not when it enters.
4. **Find the real cause on iOS.** Add `?debug` → a small fixed panel bottom-left (monospace, 11 px, above everything) listing each chapter: `live / init / fb / failed / sleeping`, plus the last 5 `[stage]` warnings with the error text, WebGL2 yes/no, `MAX_TEXTURE_SIZE`, device pixel ratio. Ivana opens casaarbolplayacar.com/?debug on her iPhone and sends a screenshot. Remove nothing else; the panel never shows without `?debug`.
5. Fix anything obvious the panel would show on iOS: every fragment shader that runs on phones compiles under `mediump` where it can (4 shaders use `highp`); textures ≤ 2048 px on phones; pixel ratio capped at 2.

## Check
390×844 with WebGL forced to fail per chapter (throw in `init` and in `render`): each shows its photo, never plain brown · slow scroll and fast fling top → bottom → top on 390×844: no frame of plain earth where a photo or WebGL image should be · `?debug` panel works, hidden without it · 1440×900 unchanged · no console errors.

## Then
Push to main. Ivana checks on her iPhone (normal + `?debug`) and says "ok" or sends the panel screenshot.
