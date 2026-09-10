# portfolio

Personal portfolio site — a single static page, hand-written HTML and CSS with no build step
and no dependencies.

Live at https://adibashaikh.is-a.dev

## Run locally

```
python3 -m http.server 8000
```

Then open http://localhost:8000.

Opening `index.html` directly via `file://` also works, since nothing is fetched relative to a
server origin.

## Deploying

GitHub Pages serves `main` at the repo root, on the custom domain `adibashaikh.is-a.dev`
(configured via the `CNAME` file — do not delete it). Pushing to `main` rebuilds the site
automatically.

The subdomain is registered through [is-a.dev](https://github.com/is-a-dev/register); the record
lives in `domains/adibashaikh.json` in that repo and CNAMEs to `adibashaikh000.github.io`.
