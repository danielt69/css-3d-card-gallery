# CSS 3D Card Gallery

An interactive 3D card gallery showcasing CSS 3D transforms — cards tilt toward your cursor with a moving glare, lift content in real depth, and flip on click to reveal a styled back face.

**Live demo:** https://danielt69.github.io/css-3d-card-gallery/

![Pure CSS + tiny vanilla JS](https://img.shields.io/badge/stack-CSS%203D%20%2B%20vanilla%20JS-7c5cff) ![No build step](https://img.shields.io/badge/build-none-00d1ff)

## How it works

- **Cursor-tracked tilt** — a tiny pointer handler maps the cursor position to `rotateX`/`rotateY` CSS variables, so each card leans toward your hand. It springs back with an expressive easing curve when the pointer leaves.
- **Moving glare** — a radial sheen blended in `soft-light` follows the same pointer position for a glossy, physical surface.
- **Real depth** — the card sits in a `perspective` scene with `transform-style: preserve-3d`; the content layers are pushed forward on `translateZ` for genuine parallax, plus a soft contact shadow underneath.
- **Flip to reveal** — clicking (or tapping) rotates an inner `flipper` 180° to expose a fully styled back face; tilt and flip compose cleanly.
- **Accessible & responsive** — keyboard-activatable, clean from 390px up, a tap-to-flip fallback on touch (tilt disabled), and `prefers-reduced-motion: reduce` turns off tilt/flip motion while keeping the cards usable.

Everything lives in a single self-contained `index.html` with inline `<style>` and a small inline `<script>` — no libraries, no frameworks, no build step.

## Run locally

Open `index.html` in any modern browser. That's it.
