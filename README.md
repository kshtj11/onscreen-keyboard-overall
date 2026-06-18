# onscreen-keyboard-overall

A single-file on-screen keyboard prototype for testing cursor-movement gestures.

The keyboard (alpha/num layouts, shift-row, trackpoint, size sliders, three
variants) is unchanged from the original prototype. The terminal has been
replaced with a **simple text editor** so the spacebar-swipe and trackpoint
cursor movements can be tried out directly on real, multi-line text.

## Cursor movement
- **Spacebar swipe (variant 2)** — drag the spacebar to move the caret: left/right
  by character, up/down between lines.
- **Trackpoint** — drag the centre nub for ← → ↑ ↓ (hold to repeat).
- **Arrow keys** — `Shift` extends a selection, `Ctrl` moves by word.
- `Ctrl+A` select all · `Ctrl+W` delete word · `Ctrl+U` clear to line start · `Ctrl+L` clear all.

## Run
```
python -m http.server 5501
```
Then open <http://localhost:5501/>. No build step, no dependencies.

## Font
[JetBrains Mono](https://github.com/JetBrains/JetBrainsMono) (latin subset) is
self-hosted in `jetbrains-mono.woff2` — same-origin, no third-party request. It
is licensed under the [SIL Open Font License 1.1](https://github.com/JetBrains/JetBrainsMono/blob/master/OFL.txt).
The CSS falls back to the platform monospace if the file is unavailable.
