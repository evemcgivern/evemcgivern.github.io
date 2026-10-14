# AGENTS.md

Workspace-wide rules (commits, security, plan-before-code, approval gates) live in the `AGENTS.md` at the root of the Projects workspace folder; this file only adds what is specific to this project.

## Project Overview

Eve McGivern's personal landing page. Public-facing. Plain static HTML/CSS, no build step, served by GitHub Pages from `main` (per `README.md`).

## Development Commands

None. Open `index.html` in a browser.

## Architecture

- `index.html`: the page, with canonical and Open Graph metadata in `<head>`.
- `og-image.png`: Open Graph image referenced from `index.html`.
- `sitemap.xml`: lists the root URL only.
- `robots.txt`: allows all; points at this site's sitemap and at `app-governance-kit/sitemap.xml`.
- `llms.txt`: plain-text summary and link list for AI crawlers.

## Common Gotchas

- Keep `index.html`, `llms.txt`, `sitemap.xml`, and `robots.txt` consistent. The project links in `index.html` and `llms.txt` are maintained separately and must match (names, URLs, descriptions, bio).
- Do not delete Search Console verification files (typically `google*.html`) if they are ever added. None are present now.
- `robots.txt` references the `app-governance-kit` sitemap, which is served from another repository.
- Changes publish publicly on push to `main`.
