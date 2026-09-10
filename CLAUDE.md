# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this is

A personal portfolio site: one static page, hand-written HTML and CSS. Deliberately no build step,
no package manager, no dependencies. Keep it that way unless there is a concrete reason not to —
the whole site is `index.html` + `styles.css`.

## Running it

```
python3 -m http.server 8000
```

There is no build, lint, or test command; there is nothing to compile.

## Design system

All visual decisions flow from the custom properties at the top of `styles.css`. Change colors and
fonts there, not at call sites.

- Warm off-white ground (`--bg`) with near-black ink and a forest-green accent (`--accent`)
- Fraunces (serif) for display headings, Inter for everything else, both via Google Fonts
- Structure is expressed with hairline rules (`--rule`) and generous whitespace — no cards, no
  shadows, no borders-as-boxes. Preserve this when adding sections.
- Two radial-gradient washes (hero, footer) are the only decoration

Full-bleed bands inside the `920px` `.wrap` container use the `padding:… 32px; margin:0 -32px`
pattern to escape the container's own padding. The hero and footer both rely on this.

## Layout notes

- The "Selected work" ledger is an `<ol>` on CSS grid (`64px 1fr 180px`), not a table — it renders
  as aligned columns but is semantically a list of projects.
- Single breakpoint at `640px`: hero and about collapse to one column, and the ledger's metric
  column is hidden rather than wrapped.
- Avoid descendant selectors like `.hero p` for styling — they silently capture new elements added
  to the section. Use an explicit class (see `.hero-lede`).

## Content accuracy

Project descriptions and the resume PDF describe real client work. Client names are deliberately
generalised ("a Fortune 500 bank") rather than named — keep it that way when editing copy.
