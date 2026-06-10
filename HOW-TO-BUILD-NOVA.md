# How to build Nova — your 3D AI avatar

A simple guide to building this from scratch with AI (no coding background needed).
Nova is **one HTML file** that runs in any browser. That's the whole trick — no
install, no setup, no framework.

---

## The fastest path: copy this prompt into Claude / ChatGPT

Paste this, then keep asking for one feature at a time (see "Build it in steps" below).

> Build me a single self-contained `index.html` file — no build tools, no
> frameworks, works by just opening it in a browser.
>
> **The avatar:** Use Three.js (loaded from a CDN via an importmap) to render a
> glowing glass **octahedron** floating in the center on a dark background. Give
> it an iridescent cyan→violet look, soft inner glow, and a few drifting
> particles around it. It should slowly spin on its own, gently **tilt toward
> the mouse cursor**, and **breathe** (scale up and down slowly).
>
> **The face:** Draw two simple eyes on the front of the gem using a `<canvas>`
> texture. Make it **blink** every few seconds. Add a function
> `setExpression(name)` that swaps between: neutral, happy, sad, surprised,
> thinking, sleepy, wink, love (heart eyes), star. Expose it as `window.Nova`
> so other code can change the face.
>
> **Keep it one file. Comment the code simply. Make it look premium and calm.**

Then add the labs one at a time with follow-up prompts:

> Now add a tab bar with 3 tabs. Tab 2 is a **chat box** I can type into — it
> shows a "thinking" animation, then a reply. Let me change its color, bubble
> style, thinking animation, and text reveal, and copy the CSS.

> Tab 3 is a **"cozy loader"**: a small card with a bouncing tag, a line of text
> with one word highlighted, pulsing dots, and a shimmer bar. Let me edit the
> tone, tag, and lines, and copy it.

> Add a **"Copy everything"** button that copies the whole file to my clipboard.

---

## How it works (the simple version)

Nova is built from **5 small ideas** stacked together:

- **It's just one `.html` file.** HTML for structure, a `<style>` block for the
  look, and `<script>` blocks for the behavior. Open the file = it runs.

- **The 3D gem uses Three.js.** That's a free library for 3D in the browser. We
  load it from a link (a CDN) so there's nothing to install. It draws a glass
  shape, points a couple of colored lights at it, and re-draws it ~60 times a
  second — that loop is what makes it animate.

- **The face is a drawing, not a model.** We paint eyes onto a small square
  canvas, then stick that square on the front of the gem like a sticker. To
  change the expression, we just **re-draw the eyes** (a smile arc, a frown, a
  heart). Simple shapes, no 3D modeling.

- **Animations are pure CSS.** Each one (float, pulse, bounce…) is a
  `@keyframes` rule — a recipe that says "start here, end there, loop forever."
  You add a class to any element and it moves. No JavaScript needed.

- **Everything talks through one small function.** `window.Nova.setExpression()`
  lets any part of the page change the face. That's how the chat makes Nova look
  "happy" or "sad" based on its reply — it just calls that one function.

---

## Build it in steps (don't do it all at once)

The secret to building with AI is **small steps you can test**:

1. **Get the gem on screen.** Just a spinning shape on a dark page. Nothing else.
2. **Make it react to the mouse** and breathe. Now it feels alive.
3. **Add the face** (two eyes + blinking).
4. **Add expressions** (happy, sad, etc.) with the `setExpression` function.
5. **Add the CSS animation gallery** — tiles you click to preview.
6. **Add the chat box**, then wire it so sending a message changes Nova's face.
7. **Add the cozy loader.**
8. **Add "Copy everything."**

After each step: **open the file, check it works, then move on.** If something
breaks, paste the broken part back to the AI and say "this isn't working, fix it."

---

## The 3 things that make it feel premium

If you only copy the *vibe*, copy these:

- **Calm, slow motion.** Everything eases gently (slow spin, soft breathe). Fast =
  cheap; slow = expensive-feeling.
- **One accent color, dark background.** Restraint reads as polished. Let the
  glow and the gem be the only bright things.
- **It reacts to you.** The cursor tilt and the face changing on a prompt are
  what make people feel like it's *alive* instead of a static picture.

---

## Using it in your own dashboard

- **Plain HTML site?** Copy the whole file (the "Copy everything" button), save it
  as `nova.html`, open it. Done.
- **React / Next / Vue?** Use the small **copy ⧉** buttons inside each lab to grab
  just the piece you want (an animation, the chat box, the loader) and paste it
  into your project. Those pieces are plain CSS/JS — they drop in anywhere.
- The only part that needs the Three.js line is the **3D gem itself**. The
  animations, chat box, and loader work with no library at all.

---

*That's it. One file, five ideas, built in small steps. Open it, read the
comments, and change one thing at a time — that's how you'll actually learn it.*
