# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Branch structure

- `master` — deployed static HTML (GitHub Pages serves this directly). Do **not** edit source content here.
- `src` — Jekyll source. All content editing happens on `src`.

The current working directory is on `master` (pre-built output). Switch to `src` to make content changes.

## Development (Jekyll source on `src` branch)

```bash
git checkout src
bundle install          # first time only
bundle exec jekyll serve
```

Site available at `http://localhost:4000`.

## Deploy

```bash
./bin/deploy
```

Must be run from `src` branch. Script builds Jekyll, replaces `master` contents with `_site/`, and force-pushes to origin.

## Site structure

Personal academic portfolio (al-folio Jekyll theme) for Amin (David) Fadaeinejad. Pages: About, CV, Publications, Projects, Teaching, News, Presentations.

On the `src` branch:
- `_config.yml` — site-wide settings (title, author, social links, theme color)
- `_pages/` — Markdown source for each section
- `_bibliography/papers.bib` — publications (auto-rendered)
- `_data/coauthors.yml` — co-author link metadata
- `_sass/base.scss` line 40 — theme color variable
- `assets/` — CSS, JS, images, PDFs (shared between branches)

## CSS / styling

Custom styles go in `assets/css/style.css`. The stack is Bootstrap 4 + MDB + FontAwesome + Academicons. `assets/css/main.css` is compiled Bootstrap — don't edit it directly.
