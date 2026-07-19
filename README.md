# resume

Michael W. Knox's resume, published via GitHub Actions to GitHub Pages.

## Viewing locally

The resume is a single self-contained `index.html` (no build step, no external assets), so either works:

```sh
# Open directly in your default browser
open index.html

# Or serve it locally (closer to how Pages serves it)
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deployment

Pushing to `main` triggers `.github/workflows/deploy.yml`, which publishes `index.html` to GitHub Pages via GitHub's Actions-based deployment (no `gh-pages` branch needed). Pages source must be set to **GitHub Actions** in the repo's Settings → Pages.

The workflow also generates `resume.pdf` on every deploy (headless Chrome printing `index.html`), which the "Download PDF" button links to. That file only exists on the deployed site — it isn't committed to the repo, so the Download PDF button will 404 when viewing `index.html` locally.
