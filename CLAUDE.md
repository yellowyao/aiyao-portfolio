# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a single-page personal portfolio website (aiyao-portfolio) for a full-stack/AI agent developer. It's a static site with no build system, no framework, and no backend — a single `index.html` file containing all HTML, CSS (embedded in `<style>`), and JavaScript (embedded in `<script>`).

## Structure

```
aiyao-portfolio/
├── index.html          # Single file: all HTML, CSS, and JS
├── static/             # Asset directory (currently empty)
└── .gitignore
```

The `static/` directory is intended for images, videos, and other media assets.

## Page Sections

The site consists of the following sections (each is a `<section>` element in `index.html`):

| Section ID | Description |
|------------|-------------|
| `#about` (hero) | Full-viewport hero with name, title, contact info, and CTA buttons |
| `#experience` | Timeline/career history |
| `#projects` | Project showcase cards |
| `#skills` | Skills and technologies |
| (unnamed) | Technical sharing / blog posts |
| (unnamed) | Call-to-action / contact prompt |
| `#contact` (footer) | Footer with contact links |

## Development Workflow

There is no build, test, or lint process. To develop:

1. Edit `index.html` directly
2. Open the file in a browser to preview (e.g., `npx serve .` or open `index.html` directly)
3. Commit changes with conventional commit messages

## Design System

CSS custom properties are defined in `:root` and should be used for all styling:

- **Colors**: `--primary`, `--accent`, `--bg-*`, `--text-*`, `--border-*`
- **Spacing**: `--space-1` through `--space-24` (based on 0.25rem increments)
- **Typography**: `--text-xs` through `--text-6xl`
- **Shadows**: `--shadow-sm` through `--shadow-xl`, plus `--shadow-accent`
- **Radius**: `--radius-sm` through `--radius-2xl`, plus `--radius-full`
- **Theme**: Light theme (UI/UX Pro Max design system)

## Conventions

- All styles are embedded in a single `<style>` block in `<head>`
- All scripts are embedded in a single `<script>` block at the end of `<body>`
- Animations use `IntersectionObserver` for scroll-triggered fade-in effects
- The site uses Google Fonts (Inter + Noto Sans SC)
- Language is Chinese (`lang="zh-CN"`)
- No external JS libraries or frameworks are used
