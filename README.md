# Blast Radius site

The front page for [Blast Radius](https://rawvoxel.github.io/blast-radius/), served by GitHub Pages
from the root of `main`. The product itself is sold on Gumroad; this repo holds only the page.

| File | What it is |
|---|---|
| `index.html` | The whole page: styles, content and scripts inline |
| `shots/<theme>/` | The page's seven screenshots, taken in that theme |
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

## Screenshots

The hero and each feature section show a screenshot of the app: `<img data-shot="<name>">`, in a
16:9 frame. The names are `hero`, `node-graph`, `thermal`, `flow`, `health`, `structure` and
`workflow`.

Each is taken in every theme the page offers. A script sets the source to
`shots/<theme>/<name>.webp` for the page's current theme, and swaps it when the theme changes.

Clicking a screenshot opens it full size.

The screenshots are 1920×1080 lossless WebP. They are captured from two sample workspaces by
scripts kept outside this repo, beside the samples, in `blast-radius-samples/capture`; its README
has the steps.

A new theme needs a full set of seven before its chip goes on the page.
