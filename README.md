# Jacob's Exercise Library

A browsable, mobile-friendly library of reformer exercises with spring-load suggestions.

Each move shows its category (Core / Lower Body / Oblique / Upper Body), the suggested
**Winter Park** spring load (Gray / Black / Blue), a setup cue, a typical duration, and
how many source classes it appears in. Live search and category filters are built in.

## Viewing it

- **Live site:** published via GitHub Pages (see the repo's Pages settings / the link in the repo description).
- **Locally:** open `index.html` in any browser — it's a single self-contained file, no build step.

## Editing

Everything lives in `index.html`. The exercise data is a JSON array in the `DATA`
constant inside the `<script>` tag near the bottom — add, edit, or remove moves there.
Each entry looks like:

```js
{ "name": "Runners Lunge", "category": "Lower Body", "wp": "3 Black",
  "setup": "Right foot on front platform…", "time": "2 minutes", "n": 4 }
```

- `wp` — Winter Park spring load. Comma-separate to stack springs (e.g. `"1 Gray, 1 Black"`).
  Leave empty for bodyweight moves.
- `n` — how many source classes the move came from (shown as a small count on each card).

## Source

Moves were extracted and deduplicated from the *Level 2 — Lower Templates* class workbook.
