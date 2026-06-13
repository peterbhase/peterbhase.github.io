# peterbhase.github.io

Personal website of Peter Hase, built with [Hugo](https://gohugo.io/) and a small custom theme (no external theme dependency). Tabs for Bio, Google Scholar, Blog Posts, Talks, CV, and an archived News timeline.

This site was designed and built with [Claude](https://www.anthropic.com/claude) (Anthropic), which scaffolded the Hugo project, wrote the layouts and CSS, migrated content from the previous Jekyll/academicpages site, and set up the GitHub Pages deployment.

## Structure

- `hugo.toml` — site config, params, and the top navigation menu
- `content/` — page content in Markdown (`_index.md` is the Bio/home page; `talks.md`, `blog.md`, `news.md`)
- `layouts/` — custom templates (`baseof.html`, `index.html`, partials for the header, nav, etc.)
- `assets/css/main.css` — all styling
- `static/` — images and files (e.g. `static/files/` for the CV and slides), served at the site root
- `_archive_jekyll/` — the previous Jekyll site, kept for reference

## Run locally

```
hugo server
```

Then open http://localhost:1313. The server live-reloads on changes to content, layouts, and CSS.

## Deploy

Pushing to `master` triggers the GitHub Actions workflow in `.github/workflows/hugo.yml`, which builds the site with Hugo and publishes it to GitHub Pages. The Pages source must be set to "GitHub Actions" (Settings → Pages). The live site is at https://peterbhase.github.io/.
