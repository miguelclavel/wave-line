# Wave Line

A line that bends toward your cursor, from [miguelclavel.com](https://miguelclavel.com/?utm_source=github&utm_medium=wave-line).

<img src="assets/demo.gif" width="720" alt="A line that bends toward your cursor: a screen recording">

**[Try it live](https://miguelclavel.github.io/wave-line/)** · one file, `index.html`, no libraries, no build step.

There's a thin line on my site that bends toward your mouse.

Get close and it leans to you. Move away and it wobbles back like a plucked string.

Nobody needs this. That's sort of the point.

A page can be completely correct and still feel flat. The gap between flat and expensive is usually a few small moments where the page notices you're there. This is one of them, and it's about twenty lines of code.

The line isn't really a line. It's a curve with a single control point, and that control point is your cursor. Move sideways and it slides with you. Move closer and it pushes further out, so the bend gets deeper. One point doing two jobs.

What makes it feel real is the letting go. It doesn't snap flat. It overshoots, comes back, overshoots less, and settles. Each bounce keeps 86 percent of the one before it, which is roughly what a real piece of string does.

There's no invisible box over the line catching your mouse either. It just listens to where your pointer is on the page. That matters, because a box would sit on top of the links next to it and eat the clicks.

Small thing. Go and pester it for a minute, it's oddly satisfying.

## Use it on your site

Give any divider this SVG: `<svg data-wave viewBox="0 0 1000 300" preserveAspectRatio="none"><path d="M0 150 Q500 150, 1000 150"/></svg>`. Copy the `<script>` from `index.html` and every `[data-wave]` on the page starts listening. Change `0.86` to make the string stiffer or looser.

## Or build your own from the prompt

Copy it as it is and paste it into Claude, or any AI coding tool.

```text
Draw a flat horizontal line as an SVG quadratic curve with one control point in the middle. Listen for mouse movement on the whole page, with no overlay element over the line. When the pointer comes within about 100 pixels vertically and inside the line's width, move the control point to the pointer's horizontal position and push it toward the pointer vertically. When the pointer leaves, spring the line back with a decaying oscillation, keeping about 86 percent of the amplitude each bounce, until it settles flat.
```

More like this in [interaction-recipes](https://github.com/miguelclavel/interaction-recipes).

---

MIT licensed. Made by [Miguel Clavel](https://miguelclavel.com/?utm_source=github&utm_medium=wave-line) with Claude Code. If you build one of these, send it to me. I'd genuinely like to see it.
