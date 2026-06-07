# CSS 3D Card Gallery

Six **distinct** CSS 3D card effects — not the same card six times. Each card isolates one technique so you can see it on its own, and **flips to reveal the exact code** that powers it.

**Live demo:** https://danielt69.github.io/css-3d-card-gallery/

![Pure CSS + tiny vanilla JS](https://img.shields.io/badge/stack-CSS%203D%20%2B%20vanilla%20JS-7c5cff) ![No build step](https://img.shields.io/badge/build-none-00d1ff)

## The six effects

| # | Card | What's different |
|---|------|------------------|
| 01 | **Cursor Tilt** | Pure `rotateX`/`rotateY` toward the pointer — no glare, no parallax, just the rotation. |
| 02 | **Holographic Foil** | A rainbow gradient blended with `color-dodge` that slides under the cursor like a real holo trading card. Flat, no tilt. |
| 03 | **Glare Sweep** | A `soft-light` specular highlight that rides across the surface following the pointer — the glossy look. |
| 04 | **Parallax Depth** | Layers placed at different `translateZ`; as the card tilts, the emoji floats far above the text. Real depth, not a drop shadow. |
| 05 | **Flip Reveal** | A 180° `rotateY` swapping two faces that share one transform, with `backface-visibility` hiding the far side. |
| 06 | **Cursor Spotlight** | A radial spotlight that follows the pointer plus a spinning `conic-gradient` border ring. No tilt — pure light. |

Flip any card (click **View code**, the card body, or press Enter) to read the implementation, with a **Copy** button on each snippet.

## How it works

- **One `perspective` scene per card**, with `transform-style: preserve-3d` so child layers keep their depth.
- **A single pointer handler** writes CSS custom properties (`--mx`, `--my`, `--rx`, `--ry`) and each effect reads only what it needs — tilt uses the rotation vars, glare/holo/spotlight use the pointer position.
- **The back face is the code** — a small, dependency-free syntax tinter colors comments, selectors, properties, and values; no highlighting library.
- **Accessible & responsive** — keyboard-activatable, clean from 390px up, tap-to-flip on touch (live tilt disabled), and `prefers-reduced-motion: reduce` turns off tilt/spotlight/ring motion while keeping every card usable and readable.

Everything lives in a single self-contained `index.html` with inline `<style>` and a small inline `<script>` — no libraries, no frameworks, no build step.

## Run locally

Open `index.html` in any modern browser. That's it.
