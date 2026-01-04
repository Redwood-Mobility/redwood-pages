# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Redwood Mobility corporate website - a Jekyll-based static site hosted on GitHub Pages at redwoodmobility.com. The site showcases EV charging infrastructure portfolio brands (Rangeway, Altara Energy, ChargeVia).

## Common Commands

```bash
# Install dependencies
bundle install --path vendor/bundle

# Build site
bundle exec jekyll build

# Serve locally with live reload (http://localhost:4000)
bundle exec jekyll serve
```

## Architecture

This is a single-page Jekyll site with a simple structure:

- **`_config.yml`** - Site configuration, organization contact emails, SEO settings
- **`_layouts/default.html`** - Main layout wrapper (includes header + content + footer)
- **`_includes/header.html`** - Navigation bar and all meta tags (OG, Twitter, SEO)
- **`_includes/footer.html`** - Copyright footer
- **`index.html`** - All page content (Hero, About, Portfolio, Contact sections)
- **`assets/css/main.css`** - All styles using CSS custom properties

### CSS Custom Properties

```css
--redwood-copper: #A14E2B;
--forest-green: #2E473B;
--light-sand: #F3E5C8;
--slate-charcoal: #3B3B3B;
```

### Jekyll Templating

Uses Liquid templating. Site-wide variables are in `site.organization`:
- `site.organization.name`
- `site.organization.email`
- `site.organization.investor_email`
- `site.organization.realestate_email`

## Deployment

Pushes to `main` branch auto-deploy to GitHub Pages. Custom domain configured via CNAME file.

## Related Repositories

This site follows the same Jekyll structure as other portfolio sites: rangeway-newsroom, pathfinder, and the main Rangeway site.
