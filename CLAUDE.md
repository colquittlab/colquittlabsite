# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this is

A Jekyll 4.3 static site for the Colquitt Lab, built on the [Lab Website Template](https://greene-lab.gitbook.io/lab-website-template-docs) (greenelab, v1.3.1). The site is deployed to GitHub Pages at `colquitt-lab.com`.

## Commands

**Local dev with Docker (recommended — runs both Jekyll and the citation pipeline):**
```bash
bash .docker/run.sh
```
Site is served at `localhost:4000` with live reload.

**Local dev with bare Ruby (Jekyll only, no citations):**
```bash
bundle install
bundle exec jekyll serve
```

**Production build:**
```bash
JEKYLL_ENV=production bundle exec jekyll build
```

**Run the citation pipeline manually:**
```bash
pip install -r _cite/requirements.txt
python _cite/cite.py
```
Requires `GOOGLE_SCHOLAR_API_KEY` in `.env` for the Google Scholar plugin.

## Architecture

### Content structure

- **Pages:** `index.md`, `research/`, `team/`, `publications/`, `contact/`, `_posts/` — Markdown files with Liquid front matter
- **`_members/`** — One `.md` file per lab member (front matter: name, image, role, links, aliases). Auto-rendered by the team page.
- **`_data/`** — Site data:
  - `sources.yaml` — Hand-curated list of DOIs; this is the source of truth for publications
  - `citations.yaml` — **Auto-generated** by `_cite/cite.py`; never edit manually
  - `roles.yaml`, `funding.yaml`, `tools.yaml`, `links.yaml`, `projects.yaml`

### Citation pipeline

`_cite/cite.py` reads `_data/sources.yaml` and resolves each DOI via Manubot and optional source plugins (PubMed, ORCID, Google Scholar), writing full metadata to `_data/citations.yaml`. A disk cache (`.cache/`, gitignored) avoids re-fetching. To add or remove publications, edit `sources.yaml`; `citations.yaml` is regenerated automatically in CI on pushes to `main`.

### Layouts and components

- `_layouts/` — Thin shell layouts (`default.html`, `member.html`, `post.html`) that delegate to includes
- `_includes/` — Liquid component partials (`hero.html`, `feature.html`, `citation.html`, `portrait.html`, `card.html`, etc.) used in page content via `{% include %}`
- `_styles/` — SCSS compiled by Jekyll's built-in Sass; `custom.scss` is for local overrides
- `_scripts/` — Vanilla JS (dark mode, search, tooltips, etc.)
- `_plugins/` — Custom Ruby Liquid filters (`array.rb`, `file.rb`, `hash.rb`, `misc.rb`, `regex.rb`)

### CI/CD

GitHub Actions workflows in `.github/workflows/`:
- Push to `main` → update citations → build and deploy to `gh-pages` branch
- Weekly schedule → auto-update citations via PR
- PRs get a preview build

## Gotchas

- **`modern-theme/`** is a staging directory for a proposed redesign that has NOT been applied to the live site yet. Don't treat its files as current.
- **Tilde (`~`) files in `_members/`** (e.g., `alekhya-meduri.md~`) are editor autosave artifacts that Jekyll may attempt to process. They should be excluded or deleted.
- There is no `package.json` / Node tooling — this is intentional.
- `testbed.md` is a template test page that was never removed by the first-time setup workflow.
