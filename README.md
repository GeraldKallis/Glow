# Glow

A CSS animation study exploring keyframes, brightness filters, and layered radial gradients.

[Live video walkthrough](https://geraldkallis.com)

## What it does

A small, focused exploration of how far pure CSS can go for atmospheric visual effects — no canvas, no JavaScript animation libraries, no images. Three glowing orbs pulse and drift independently using `@keyframes`, layered `radial-gradient` backgrounds, and the `brightness()` filter, producing a soft, breathing motion rather than a mechanical loop.

This project is intentionally small in scope. It exists to demonstrate comfort with CSS animation timing, easing, and visual layering at a level beyond standard layout work — the kind of detail that shows up in polish, not in feature count.

## What's actually happening

- **Brightness pulse** — each orb cycles between `brightness(1)` and roughly `brightness(1.5–1.6)` using `ease-in-out` timing on an alternating infinite loop, so it breathes rather than flashes.
- **Layered radial gradients** — each orb is a `radial-gradient` fading from a saturated core to transparent, creating a soft halo rather than a hard-edged circle.
- **Independent timing per orb** — each orb has its own pulse duration (2.7s–4s) and drift duration (7s–9.5s), deliberately mismatched so the animation never falls into a visibly repeating pattern.
- **Subtle drift** — small `margin` shifts on a separate animation cycle give each orb gentle independent movement, layered on top of the brightness pulse.

## Tech stack

- **CSS3** — `@keyframes`, `radial-gradient`, `filter: brightness()`
- **HTML** — minimal structural markup
- **JavaScript** — light touch, mostly unused; this is a CSS-first study

## Running it locally

This is a static project with no build step.

```bash
git clone https://github.com/GeraldKallis/Glow.git
cd Glow
open index.html
```

Or serve it with any static file server, e.g.:

```bash
npx serve .
```

## License

MIT
