# No Brand Baseball Analytics — Pitch Grip Database

An internal, filterable reference of 104 pitch grips for pitch-design work.

## How to use it
- **Open it:** double-click `index.html` — it runs in any browser, no internet needed.
- **Host it:** drop this whole folder on the No Brand web server (or an internal share).
  `index.html` must sit next to the `grips/` folder.
- Everything is self-contained: the grip data is baked into `index.html`; photos and
  clips live in `grips/`.

## What's in it
- **104 grips** across 13 shape families (slider, slurve, sweeper, gyro, death ball,
  curveball, changeup, splitter, forkball, cutter, sinker, four-seam, modifiers).
- **Filters:** shape, bias fit (pronator / supinator / neutral), and movement goal
  (velo, sweep, depth, tighter/kill HB, command). Plus free-text search and per-card
  "Details" that show grip / movement / when to use / what to watch for.
- **Media:** 72 grip photos and 31 short grip clips (marked `CLIP` — hover or click to
  play; each shows a still frame until then).
- Lefty-specific grips are tagged with an **LHP** badge.

## Notes
- **Descriptions are original No Brand write-ups** — written from the grip mechanics and
  movement behavior in our own voice and framework (SSW, IVB/HB, gyro, spin efficiency,
  etc.), not copied from anywhere. Edit freely; they're ours.
- **Photos/clips** are used with permission and kept for internal reference. One grip
  ("Tilt — inward") has no image available.
- **No movement plots are included.** The source's plots were left out on purpose — those
  are better regenerated from No Brand's own TrackMan data so the shapes reflect our arms.
  The tool has room to add a plot image per grip later.

## Editing / extending
- To add or change a grip, edit the `DATA` object near the bottom of `index.html`
  (or ask Claude to regenerate it). Each grip is:
  `{ id, name, bias[], goal[], media, mediaType, hand, grip, movement, when, watch }`.
- To swap in a No Brand photo, drop the image in `grips/` and point the grip's `media`
  at it. Clips can get a poster still named `<clip>-poster.jpg` in `grips/`.

Built for No Brand Baseball Analytics.
