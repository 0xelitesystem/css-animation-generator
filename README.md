# CSS Animation Generator

Build CSS @keyframes animations visually. Set the name, duration, delay, timing function, iteration count, direction, and fill mode, edit keyframe stops with per-stop transform and opacity, preview the animation live, and copy the finished CSS with one click. Single HTML file, no external dependencies, works offline.

**Live demo:** https://0xelitesystem.github.io/css-animation-generator/

## Live demo

https://0xelitesystem.github.io/css-animation-generator/

## Features

- Full animation settings: name, duration, delay, timing function (ease, linear, ease-in, ease-out, ease-in-out, plus cubic-bezier presets), iteration count or infinite, direction, fill mode
- Keyframe editor: add and remove stops anywhere from 0% to 100%
- Per-stop controls: translate X/Y, scale, rotate, and opacity
- Live preview box with a replay button, so you can re-run the animation on demand
- Six common presets: fade-in, slide-in-left, bounce, pulse, shake, spin
- Complete generated CSS (the @keyframes block plus the animation property on a class) with a copy button
- Everything recomputes live as you type
- Light and dark theme toggle, keyboard-usable controls

## How it works

The keyframe stops live in a small JavaScript model. Every edit rebuilds the CSS text from that model: stops are sorted by percentage, each one emits a transform (translate, scale, rotate) and an opacity line, and the settings compose the animation shorthand on a class named after your animation. The same generated rules are injected into a style element on the page, so the preview box plays exactly the CSS you will copy. The replay button restarts the animation by removing and re-adding the class with a forced reflow in between.

## Use

1. Load one of the six presets (fade-in, slide-in-left, bounce, pulse, shake, spin) or start from the default animation.
2. Set the name, duration, delay, timing function, iteration count, direction and fill mode.
3. Add, remove and edit keyframe stops, adjusting translate, scale, rotate and opacity per stop, and press replay to rerun the preview.
4. Copy the generated `@keyframes` block and class rule.

## Why this exists

Hand-writing `@keyframes` means guessing at percentages and transforms, reloading, and guessing again. This tool previews exactly the CSS it will hand you, so you tune the motion by eye and copy the result. It is a single HTML file with no tracking and no network calls, and it is MIT licensed.

## Privacy

Everything runs client-side in your browser. Nothing you type leaves the page, no requests are made, no analytics, no cookies. You can open DevTools and watch the network tab to confirm.

The one thing the page saves is your light or dark theme choice, written to `localStorage` under the key `theme` when you press the theme toggle. Clearing site data removes it.

## Run locally

```
git clone https://github.com/0xelitesystem/css-animation-generator
cd css-animation-generator
```

Then open `index.html` in any modern browser, or serve the folder with `python -m http.server` and visit http://localhost:8000/.

## Build

No build step. The whole tool is one `index.html` file with inline CSS and JavaScript, and there is nothing to install or compile.

## More

Part of a catalog of single-file browser tools and plain-language references, all MIT licensed and dependency-free: [0xelitesystem.github.io](https://0xelitesystem.github.io/). Built by [elitesystem.ai](https://elitesystem.ai).

## License

MIT. Copyright 0xelitesystem 2026.
