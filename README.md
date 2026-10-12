# Blast Radius site

The front page for [Blast Radius](https://rawvoxel.github.io/blast-radius/), served by GitHub Pages
from the root of `main`. The product itself is sold on Gumroad; this repo holds only the page.

| File | What it is |
|---|---|
| `index.html` | The whole page: styles, content and scripts inline |
| `shots/<name>.svg` | The page's seven screenshots, each carrying every theme's colors |
| `favicon.svg` | Browser-tab icon |
| `.nojekyll` | Tells Pages to serve the files as they are, without a Jekyll build |

## Before launch

Replace `#TODO-GUMROAD` with the Gumroad product URL. It appears in three links in `index.html`
(top bar, hero, closing section); the `TODO-GUMROAD` comment above the first one marks it.

## Preview locally

Serve the folder: the screenshots are fetched, which a page opened straight from disk cannot do.

```bash
python -m http.server 8000
```

## Screenshots

The hero and each feature section show a picture of the app in a 16:9 frame:
`<span data-shot="<name>">`, which a script fills with `shots/<name>.svg`. The names are `hero`,
`node-graph`, `thermal`, `flow`, `health`, `structure` and `workflow`.

Each one is the app's own SVG export, taken once in every theme the page offers. Its colors are CSS
variables, with a block of values for each theme, chosen by `data-theme`. The script puts the file
inline, because an `<img>` cannot be restyled by the page. It then sets each picture's `data-theme` to
the page's theme, so a theme change recolors the pictures in place.

Clicking one opens it full size.

They are exported from two sample workspaces by scripts kept outside this repo, beside the samples,
in `blast-radius-samples/capture` (`svgs.ps1`); its README has the steps. The themes an export
carries come from the app's `[export] themes` setting, written as `site-id=app-theme` pairs.

A new theme needs its pair added to that setting, and the seven shots exported again, before its chip
goes on the page.
