# The all-in-one prompt

Copy everything in the box below and paste it into Claude or ChatGPT. It builds
the whole Nova kit — 3D avatar, animation gallery, expression picker, chat box
lab, and cozy loader — in **one HTML file**.

> Tip: if the model runs out of room, just say *"keep going from where you
> stopped"* — it'll continue the same file.

---

```
Build me a single, self-contained index.html file — no frameworks, no build
tools, no installs. It must work by just opening it in a browser. Load Three.js
from a CDN using an importmap. Comment the code simply so a beginner can follow
it. Style everything dark, calm, and premium.

Make a sticky TAB BAR at the top with: "Avatar + Animations", "Chat Box Lab",
"Cozy Loader", and a bright "Copy everything" button that copies the entire
page source to the clipboard.

=== TAB 1: THE AVATAR ("Nova") ===
Use Three.js to render a glowing glass OCTAHEDRON floating on a dark cosmic
background. Give it:
- An iridescent cyan → violet → pink look (physical material with transmission +
  iridescence) over a procedurally generated environment (no image downloads).
- A soft inner glow sphere and a halo of ~70 drifting particles. NO rings or
  wireframe borders.
- Always-alive motion: slow rotation, a gentle "breathe" (scale up/down), and a
  spring-eased tilt that follows the mouse cursor.
- A face drawn on a <canvas> texture, placed in FRONT of the gem so it never
  gets clipped (use depthTest:false + a high renderOrder). It should blink
  randomly.
- 9 expressions: neutral, happy, sad, surprised, thinking, sleepy, wink,
  love (heart eyes), star-eyed — each just a few canvas strokes/shapes.
- Expose a tiny global API: window.Nova.setExpression(name, holdSeconds) and
  window.Nova.setPalette(a, b, c). Expressions auto-return to neutral after
  their hold time, with a little "pop" bounce when they change.
- A serif-italic "Nova" name label with "your companion" underneath.
- A row of color-swatch buttons at the top that recolor the whole avatar live
  by calling setPalette (offer ~8 palettes like Nebula, Mint, Ember, Ocean).

Below the avatar, an ANIMATION KIT: 15 pure-CSS animations (float, pulse, spin,
wobble, glow, bounce, shimmer, flip, 3D tilt, heartbeat, jelly, drift, swing,
pop-in, ripple). Show each in a clickable card with a small live preview.
Clicking a card PLAYS that animation on the real Nova above; a small "copy" chip
on each card copies that animation's exact, self-contained CSS to the clipboard
with a toast confirmation.

Then an EXPRESSION KIT: a card per expression. Clicking plays it on Nova; the
copy chip hands over the JS to drive it from any app, with a worked example
(show "thinking" while calling the model, then happy/sad based on the reply).

=== TAB 2: CHAT BOX LAB ===
A live, restyleable AI-coach chat box. The user types a message, a THINKING
indicator shows, then the reply REVEALS with animation. A side panel changes it
live and every option writes a CSS custom property so the live box and the
exported code are identical:
- Accent color (swatches)
- Bubble design: glass / solid / outline / glow
- Corner radius (slider)
- Thinking animation: dots / bars / pulse / shimmer
- Text reveal: fade / word-rise / typewriter
Use a few canned replies (no real backend); each reply carries a "mood" so it
calls Nova.setExpression to make the avatar's face react. A "Copy this chat box
CSS" button exports the styling baked with the current options.

=== TAB 3: COZY LOADER LAB ===
A playful "pop" loading card: a tag bounces in, a line springs up with one
phrase highlighted, dots pulse, a shimmer bar slides, and the whole card tints
to a tone. Use overshoot cubic-bezier easing so it feels cozy. Let me edit the
title, the rotating tags (one per line), and the lines (written as
"text | highlighted phrase"), pick a tone (mint / blue / amber / violet / rose),
set the rotation speed, and toggle the shimmer bar / dots / thumbnail. A copy
button exports a fully self-contained HTML + CSS + JS loader.

=== GLOBAL RULES ===
- Respect prefers-reduced-motion everywhere (turn looping animation off).
- Use navigator.clipboard with a textarea fallback for all copy buttons.
- Keep it ONE file. Make it feel expensive: slow easing, one accent color on a
  dark background, and reactions to the user (cursor + face) so it feels alive.
```

---

## Build it in steps instead?

The prompt above builds everything at once. If it's too much, paste just the
**TAB 1: THE AVATAR** section first, get it working, then add each tab with a
follow-up message. See `HOW-TO-BUILD-NOVA.md` for the recommended order.
