# portfolio

Personal portfolio site — a single static page, hand-written HTML and CSS with no build step
and no dependencies.

## Run locally

```
python3 -m http.server 8000
```

Then open http://localhost:8000.

Opening `index.html` directly via `file://` also works, since nothing is fetched relative to a
server origin.

## Before publishing

- Replace the placeholder email `you@example.com` in the footer of `index.html`
- Add `resume.pdf` at the repo root, or repoint the Resume link in the nav
- Fill in the `og:url` / add an `og:image` if you want link previews
