# greghcarr.github.io

Personal website for Greg Carr. Built with Jekyll and hosted on GitHub Pages.

## Stack

- **Jekyll** (v3.10.0) static site generator
- **Theme:** `pages-themes/minimal` via `jekyll-remote-theme`
- **Deployment:** GitHub Pages (auto-deploys from `main`)

## Local Development

```bash
bundle exec jekyll serve
# → http://127.0.0.1:4000
```

## Site Structure

- `index.md` — Homepage (intro, projects, recipes, cats, music)
- `cats.md` — Cat photo gallery (auto-populated from `assets/images/cats/`)
- `recipes/` — Bread recipe pages, each in markdown
- `recipes/_recipe-template.md` — Template for new recipes (git-ignored)
- `_config.yml` — Jekyll config (title, description, theme, plugins)
- `_includes/head-custom.html` — Favicon overrides for the theme
- `assets/images/` — Logo, favicons, and cat photos
- `export_cats_photos.sh` — Script to export cat photos from Apple Photos (git-ignored)

## External Dependencies

- **Resume** — linked via Google Docs preview (`docs.google.com/document/d/1pIQPG5e1VB5pgUajiucgQq12x4w_YK2B/preview`). The filename and content of this Google Doc are public-facing. Sharing must stay set to "anyone with the link can view."

## Conventions

- Content is markdown with Liquid templating — no custom Jekyll plugins.
- Page-specific CSS goes in inline `<style>` tags at the top of each `.md` file.
- Recipe pages follow the structure in `_recipe-template.md`.
- Cat photos are bulk-exported via `export_cats_photos.sh` into `assets/images/cats/`.
- External links use `{:target="_blank"}` to open in new tabs.
