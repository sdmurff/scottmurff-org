# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is Scott Murff's personal academic website built with Quarto. The site showcases teaching, research, student resources, essays, and ventures. It's a static website deployed to GitHub Pages.

## Site Architecture

**Quarto Website Project**: This is a `type: website` Quarto project (not a book or document), configured in `_quarto.yml`.

**Content Structure**:
- Root-level `.qmd` files are primary pages (index, about, teaching, research, students, ventures)
- `essays/` subdirectory contains essay content with its own `index.qmd`
- Navigation is controlled through `_quarto.yml` navbar configuration
- Output directory is `_site/` (git-tracked for GitHub Pages deployment)

**Styling System**:
- Base theme: `flatly` (Bootstrap-based Quarto theme)
- Custom CSS in `styles.css` with specific typography choices:
  - Body text: Georgia serif at 1.05rem with 1.7 line-height
  - Headings: Inter sans-serif at 600 weight
  - Navbar: Inter sans-serif at 500 weight
- Images stored in `images/` directory (included via resources in `_quarto.yml`)

## Common Commands

**Preview site locally**:
```bash
quarto preview
```

**Check Quarto version** (currently 1.7.32):
```bash
quarto --version
```

## Content Development Notes

- The site uses Bootstrap card components and grid layout (see `index.qmd` for examples)
- Essays are standalone `.qmd` files in the `essays/` directory
- The `page-layout: full` option is used on index.qmd for wider content
- TOC is enabled globally but positioned left via `_quarto.yml`
- Footer includes copyright notice centered at page bottom

## GitHub Pages Deployment

The site is deployed via GitHub Pages using the `_site/` directory. The CNAME file in the root maps to the custom domain. Changes to `_site/` directory are tracked in git (not ignored) for GitHub Pages deployment.
