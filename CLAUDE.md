# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Jekyll-based academic personal website using the "Minimal Light" theme. The site is hosted on GitHub Pages and showcases publications, CV, and research information for Soyoung Lee, a Ph.D. student at the University of Michigan.

## Development Commands

### Local Development
```bash
# Install dependencies
bundle install
bundle add webrick

# Run local development server
bundle exec jekyll server
```
The site will be available at `http://localhost:4000`

### Building
Jekyll automatically builds the site when using GitHub Pages. For local builds:
```bash
bundle exec jekyll build
```
Generated files are placed in the `_site` folder.

## Project Architecture

### Key Configuration
- `_config.yml` - Main Jekyll configuration with personal information, theme settings, and site metadata
- `Gemfile` - Ruby dependencies (Jekyll ~3.8.5, webrick ~1.8)
- Uses `remote_theme: yaoyao-liu/minimal-light` instead of local theme files

### Content Structure
- `index.md` - Main homepage content using the `homepage` layout
- `_data/publications.yml` - YAML file containing publication data with fields like title, authors, conference, PDF links, etc.
- `_includes/publications.md` - Template for rendering publications from the YAML data
- `_includes/services.md` - Services section (currently commented out)

### Theme Files
- `_layouts/homepage.html` - HTML template for the main page layout
- `_sass/` - SCSS files for styling (both dark mode and no-dark-mode versions)
- `assets/` - Static assets including images, PDFs, CSS, and JavaScript

### Content Management
Publications are managed through `_data/publications.yml`. Each publication entry can include:
- title, authors, conference details
- PDF links, code repositories, project pages
- Poster/presentation files, BibTeX
- Conference abbreviations and notes

### Styling and Themes
- Supports both light and dark modes (configurable via `auto_dark_mode`)
- Font selection between Serif and Sans Serif
- Custom SCSS in `_sass/minimal-light.scss` for style modifications
- Academic icons and Font Awesome for social links

### Deployment
- Automatically deploys via GitHub Pages when changes are pushed to the main branch
- Uses Jekyll's exclude configuration to omit development files from the built site

## Commit Guidelines
- When creating git commits, do not include the standard Claude Code attribution or co-author tags
- Use simple, descriptive commit messages without AI tool attribution