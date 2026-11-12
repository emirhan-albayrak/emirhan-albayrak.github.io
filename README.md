# Personal site — Emirhan B. Albayrak

Static site. No build step, no dependencies. `index.html` plus an `assets/` folder.

## Putting it on GitHub Pages

1. Create a repo named **`emirhan-albayrak.github.io`** (that exact name — it makes the site live at the root URL rather than under a subfolder).
2. Upload `index.html`, `assets/`, and `.nojekyll` to the root of the repo.
3. Settings → Pages → Source: **Deploy from a branch**, branch `main`, folder `/ (root)`.
4. Wait ~1 minute. The site is at **https://emirhan-albayrak.github.io/**

## Before you publish — one thing to check

`index.html` has two tags near the top that assume the URL above:

```html
<meta property="og:url"   content="https://emirhan-albayrak.github.io/" />
<meta property="og:image" content="https://emirhan-albayrak.github.io/assets/og-image.png" />
```

These must be the **real, absolute** URL or link previews break in email, Slack and X.
If you use a project repo (`.../some-repo/`) or a custom domain, update both lines.

## Files

| File | What it is |
|---|---|
| `index.html` | The whole page: markup, styles, and a small script for the figure lightbox |
| `assets/photo.jpg` | Profile photo (450×450) |
| `assets/fig-1.png` | Aim 1 — encoding time courses and stimulation windows |
| `assets/fig-2.png` | Aim 2 — UMAP of the five physiological clusters |
| `assets/fig-3.png` | Aim 3 — model architecture |
| `assets/CV-Emirhan-Albayrak.pdf` | CV, linked from the hero button and from the Talks section |
| `assets/og-image.png` | 1200×630 social preview card |
| `.nojekyll` | Tells Pages to serve the files as-is |

## Updating things later

- **CV**: replace `assets/CV-Emirhan-Albayrak.pdf`, keeping the filename. Nothing else changes.
- **Figures**: replace the file, keep the name. Captions live in `index.html` in each `<figcaption>`.
- **Colors**: every color is a variable in the `:root` block at the top of the `<style>` section.
- **Fonts**: IBM Plex Sans and Serif are loaded from Google Fonts in the `<head>`.

## Known choices

- Figures open full size on click (Esc or a second click closes).
- The Research section runs wider than the rest of the page so the figures get room; its heading is pulled back so all section headings share a left edge.
- The Twitter/X link is commented out in the hero, ready to uncomment.
