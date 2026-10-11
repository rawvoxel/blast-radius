# Blast Radius site

The front page for [Blast Radius](https://rawvoxel.github.io/blast-radius/), served by GitHub Pages
from the root of `main`. The product itself is sold on Gumroad; this repo holds only the page.

| File | What it is |
|---|---|
| `index.html` | The whole page: styles, content and the hero drawing inline |
| `favicon.svg` | Browser-tab icon |
| `.nojekyll` | Tells Pages to serve the files as they are, without a Jekyll build |

## Before launch

Replace `#TODO-GUMROAD` with the Gumroad product URL. It appears in three links in `index.html`
(top bar, hero, closing section); the `TODO-GUMROAD` comment above the first one marks it.

## Preview locally

Open `index.html` in a browser, or serve the folder:

```bash
python -m http.server 8000
```
