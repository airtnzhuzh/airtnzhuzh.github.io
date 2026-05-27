# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a single-page static academic homepage for Zhihan Zhu, hosted on GitHub Pages at `airtnzhuzh.github.io`. There is no build step — the site deploys directly from the repository.

## Architecture

The entire site is one self-contained file: `index.html`. It contains:
- All HTML structure
- All CSS (in a `<style>` block in `<head>`)
- All JavaScript (a small bilingual toggle function at the bottom)

Content is organized into sections within `<div class="section">` blocks: Bio, Education, Publications, Patents, Honors, and Skills.

**Bilingual support**: English and Chinese content coexist in the same DOM. Chinese elements use `class="zh"` and are hidden by default (`display: none`). The `toggleLanguage()` function at the bottom switches visibility between `.en` and `.zh` elements.

**Assets**:
- `images/` — profile photo (`me.png`) and paper/project preview thumbnails (`paper1-4.png`, `project1-2`)
- `assets/` — CV PDF files. The current CV is `zhihanzhu_cv_en_26-5-27.pdf` (dated 2026-05-27)

## Deployment

Push to `main` branch → GitHub Pages automatically serves the updated site. No CI, no build pipeline.

## Common Edits

- **Update CV link**: search for `zhihanzhu_cv_en` in `index.html` to find the `<a href>` pointing to the PDF, update the filename to match the newly uploaded asset.
- **Add a publication**: copy an existing publication `<div>` block in the Publications section and update the thumbnail (`images/paperN.png`), title, authors, venue, links, and badges.
- **Add a Chinese translation**: add a sibling element with `class="zh"` next to the corresponding `class="en"` element.
