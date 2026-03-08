# Project Overview

Personal website for Riccardo Spada, PhD Candidate in Business Economics at Wageningen University. Built with [Quarto](https://quarto.org/) and deployed via GitHub Pages.

- **Live site:** <https://blade-sp.github.io/website/>
- **Repo:** `blade-sp/website` (branch `main` for production, `development` for WIP).

## Key Technologies

- **Quarto:** Static site generator for scientific/technical publishing. Content is written in `.qmd` (Quarto Markdown) files.
- **HTML/CSS/Bootstrap:** Rendered output uses the Flatly Bootstrap theme with custom styles in `styles.css`.
- **Font Awesome:** Icons use the `quarto-ext/fontawesome` extension via `{{< fa >}}` shortcodes.
- **Shinylive:** Interactive R Shiny apps embedded in the browser via the `quarto-ext/shinylive` extension.

## Project Structure

- `_quarto.yml` — Project configuration (site metadata, navbar, theme, output directory). Only `.qmd` files are rendered (`.md` files excluded via `render` key).
- `index.qmd` — Landing page with hero section (profile photo, bio) and social links (LinkedIn, GitHub, ORCID, ResearchGate, Google Scholar).
- `cv.qmd` — Curriculum vitae with downloadable PDF (`assets/cv.pdf`).
- `resources.qmd` — Resource hub with clickable cards linking to sub-pages (Research, Dashboards, Blog).
- `research.qmd` — Research page (placeholder).
- `dashboards.qmd` — Financial dashboards index page.
- `dashboards/` — Subdirectory for dashboard pages.
  - `compound_interest.qmd` — Interactive compound interest calculator (Shinylive R app).
- `blog.qmd` — Blog listing page (placeholder).
- `blogpost/` — Subdirectory for blog post `.qmd` files (currently empty).
- `styles.css` — Custom CSS: theming variables, navbar, hero section, project cards, buttons, footer.
- `assets/` — Images (`ProfilePic.jpg`), favicon (`favicon/`), logo variants (`RS_logo_*.png`), CV PDF.
- `_extensions/` — Quarto extensions (fontawesome, shinylive).
- `docs/` — Generated output (do not edit manually).
- `TODO.md` — Task tracking.

## Building and Running

Requires [Quarto](https://quarto.org/docs/get-started/) installed.

```bash
quarto render    # Build site to docs/
quarto preview   # Live preview with hot reload
```

## Conventions

- Icons: use Font Awesome shortcodes (`{{< fa brands linkedin >}}`), not Bootstrap Icons.
- Content goes in `.qmd` files; styling in `styles.css`.
- Output directory is `docs/` (configured in `_quarto.yml`), committed for GitHub Pages.
- CSS custom properties (e.g. `--color-primary`, `--color-accent`) are defined in `:root` in `styles.css` for theming.
- Fonts: Inter (sans-serif body text) and Playfair Display (serif headings), loaded via Google Fonts.
- Project cards in `resources.qmd` are fully clickable via wrapping `<a>` tags with the `.project-card-link` class.
- `.md` files (e.g. `CLAUDE.md`, `GEMINI.md`, `TODO.md`, `README.md`) are excluded from rendering in `_quarto.yml`.
