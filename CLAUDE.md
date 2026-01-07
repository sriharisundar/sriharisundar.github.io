# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Personal portfolio website for Srihari Sundar, built with Hugo static site generator and deployed to GitHub Pages at https://sriharisundar.github.io.

## Build Commands

```bash
# Local development server
hugo server

# Production build (with garbage collection and minification)
hugo --gc --minify
```

## Architecture

- **Static Site Generator**: Hugo (version 0.153.2 extended)
- **Theme**: hugo-coder (personal fork at git@github.com:sriharisundar/hugo-coder.git)
- **Deployment**: GitHub Actions → GitHub Pages (triggers on push to `main` branch)

### Directory Structure

- `content/` - Markdown pages with TOML frontmatter (`+++` delimiters)
- `static/images/` - Static assets (avatar, favicon)
- `themes/hugo-coder/` - Active theme (git submodule)
- `themes/hugo-bearblog/` - Archived theme (not in use)
- `hugo.toml` - Main Hugo configuration

### Content Pages

Pages use `weight` in frontmatter to control menu order:
- about.md (weight: 1)
- codes.md (weight: 2)
- research.md (weight: 3)
- contact.md (weight: 5)

### Theme Customization

To override theme templates, create corresponding files in the root `layouts/` directory (currently empty, using theme defaults).
