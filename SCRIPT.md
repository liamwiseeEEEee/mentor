# 🎬 Video script — "I gave my dashboard a brain"

The verbal script for the Nova build video. Read it straight through — it maps
1:1 to the files in this repo. Rough runtime ~4 minutes.

---

**[0:00–0:20] Hook**

> "Most dashboards just sit there. Today I'm giving mine a brain — an AI mentor
> that reads my whole day and actually talks to me. I built it from scratch in
> one file, it costs less than a penny a question, and by the end you'll be able
> to do it to *your* dashboard too. Let's build it."

**[0:20–0:45] Show the finished thing**

> "This is it. I ask 'how's my week looking?' — and it already knows my workouts,
> my water, my sleep. I never told it any of that. And watch — Nova, the little
> crystal, looks when I ask and reacts when it answers. Looks alive. Now let me
> show you how I actually made this."

**[0:45–1:25] How I built it — the method**

> "Here's how fast this goes. I start with one blank HTML file — no installs, no
> setup, it just opens in a browser. Then I describe what I want in plain
> English, like a human. First I get it *working* and ugly — a box, type a
> question, get an answer. The second it works, the hard part's done. *Then* I
> make it beautiful. That's the whole secret to speed: skip the setup, and never
> polish something that doesn't work yet."

**[1:25–2:05] The one big idea**

> "And here's the trick that makes it feel smart. Before it answers, the app
> grabs my dashboard — workouts, water, sleep — turns it into plain text, and
> hands it to the AI with my question. That's it. The AI isn't magic — it just
> gets my day as a paragraph. Which means this works on *any* dashboard. You just
> change what data goes in."

**[2:05–2:40] The cost — and how it's basically free**

> "I'm using Claude Haiku, the cheap model — about a penny a question, hundreds
> for a dollar. And you don't need my key. You paste your *own*. New accounts get
> free starter credit, so you can film your whole setup without spending a cent."

**[2:40–3:00] The design lab**

> "Don't like how it looks? I built a lab too — open it, click any animation to
> copy it, drag the colors live, paste it back. Same engine, totally your style.
> It's optional — skip it if you love the default."

**[3:00–3:35] Make it yours — not just a repo**

> "And I'm not just throwing you a folder of code. I just walked you through every
> piece — the file, the AI, feeding it your data, the animations — so you can
> rebuild it on your own dashboard even if it looks nothing like mine. The repo's
> below as a head start, but now you actually understand it."

**[3:35–4:00] CTA**

> "Want it already wired to your real data, hosted, no setup? That's Vitality —
> link below. Otherwise grab the file, paste your key, and go give your dashboard
> a brain."

---

## Description-box timestamps

```
0:00  Intro
0:20  The finished mentor
0:45  How I build fast (the method)
1:25  The one idea that makes it smart
2:05  Cost + free starter credit
2:40  The design lab
3:00  Build it on your own dashboard
3:35  Get the hosted version
```

## Files referenced in the video

| In the video I say… | File to point at |
|---|---|
| "one blank HTML file… it just runs" | [`ai-avatar.html`](ai-avatar.html) |
| "I describe what I want in plain English" | [`all-in-one-prompt.md`](all-in-one-prompt.md) |
| "build it working first, then beautiful" | [`HOW-TO-BUILD-NOVA.md`](HOW-TO-BUILD-NOVA.md) |
| "the lab — click to copy, drag the colors" | the Chat Box Lab tab in `ai-avatar.html` |
