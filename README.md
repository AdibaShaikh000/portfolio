# portfolio

Personal portfolio site — a single static page, hand-written HTML and CSS with no build step
and no dependencies.

Live at https://adibashaikh000.github.io/portfolio/

## Run locally

```
python3 -m http.server 8000
```

Then open http://localhost:8000.

Opening `index.html` directly via `file://` also works, since nothing is fetched relative to a
server origin.

## Deploying

GitHub Pages serves `main` at the repo root. Pushing to `main` rebuilds the site automatically.
