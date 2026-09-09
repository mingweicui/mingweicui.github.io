# mingweicui.github.io

Personal homepage for Mingwei Cui, served at [https://mingweicui.github.io/](https://mingweicui.github.io/).

## Purpose

GitHub user page acting as the umbrella entry point for personal brand and products. Catches URL-hack traffic from product project pages (e.g. visitors editing `https://mingweicui.github.io/voxelvision/` down to the root domain).

## Structure

- `index.html` — single-page personal homepage (Hero + About + Products + Contact + Footer)
- `lightpad/` — LightPad product pages: `index.html` (marketing + support, the app's ASC support/marketing URL) and `privacy.html` (ASC privacy URL)
- `assets/` — shared design tokens (`site.css`, `site.js`), self-hosted fonts, product icons, hero imagery
- `publish.sh` — single-commit snapshot publisher to GitHub (excluded from the published tree)
- `.gitignore` — macOS / editor / secrets / Claude metadata

## Visual style

Inherits design tokens (color palette, font stack, hero gradient, light/dark mode adaptation) from the VoxelVision product landing page so that the user-page → product-page transition feels like one continuous brand experience.

## Maintenance

Lives in `/Users/cuim/Dev/Marketing/mingweicui.github.io/` on macOS. Pushed to GitHub repo `mingweicui/mingweicui.github.io`, deployed via GitHub Pages from the `main` branch root.

## Deployment

Dual-remote, mirroring the VoxelVision website repo: `origin` (NAS) holds the full
development history and is the history of record; `github` only ever holds one
snapshot commit, force-pushed by `publish.sh`.

After local edit:

```bash
cd /Users/cuim/Dev/Marketing/mingweicui.github.io
git add -A
git commit -m "feat: <change summary>"   # conventional commits govern NAS history
git push origin main                      # history of record
./publish.sh                              # single-commit snapshot -> github/main
```

GitHub Pages rebuilds within ~30 seconds. Verify at [https://mingweicui.github.io/](https://mingweicui.github.io/).

## Linked surfaces

- VoxelVision product page: [https://mingweicui.github.io/voxelvision/](https://mingweicui.github.io/voxelvision/)
- LinkedIn: [https://www.linkedin.com/in/mwcui/](https://www.linkedin.com/in/mwcui/)
- GitHub: [https://github.com/mingweicui](https://github.com/mingweicui)
- Email: mnwcui@gmail.com
