# Redwood Mobility

Official website for Redwood Mobility, Inc. - Building premium electric vehicle charging infrastructure across America's scenic corridors.

## Overview

This is a Jekyll-based static site designed for GitHub Pages hosting. The site showcases Redwood Mobility's infrastructure ownership approach and portfolio of EV charging assets.

## Site Structure

```
redwood-pages/
├── _config.yml           # Jekyll configuration
├── _layouts/             # Page layouts
│   └── default.html      # Main layout template
├── _includes/            # Reusable components
│   ├── header.html       # Navigation and meta tags
│   └── footer.html       # Footer content
├── assets/               # Static assets
│   ├── css/
│   │   └── main.css      # Main stylesheet
│   └── images/           # Logo and image files
├── index.html            # Homepage
├── CNAME                 # Custom domain configuration
└── Gemfile               # Ruby dependencies
```

## Local Development

### Prerequisites

- Ruby 2.6 or higher
- Bundler

### Setup

1. Install dependencies:
   ```bash
   bundle install --path vendor/bundle
   ```

2. Build the site:
   ```bash
   bundle exec jekyll build
   ```

3. Serve locally with live reload:
   ```bash
   bundle exec jekyll serve
   ```

4. View at `http://localhost:4000`

## GitHub Pages Deployment

### First-Time Setup

1. Push changes to the `main` branch
2. Go to repository Settings > Pages
3. Set source to "Deploy from a branch"
4. Select branch: `main` and folder: `/ (root)`
5. Click Save

### Custom Domain

The CNAME file is configured for `redwoodmobility.com`.

To set up the custom domain:
1. In repository Settings > Pages > Custom domain
2. Enter `redwoodmobility.com`
3. Click Save
4. Configure DNS records with your domain provider:
   - Add an A record pointing to GitHub Pages IPs:
     - 185.199.108.153
     - 185.199.109.153
     - 185.199.110.153
     - 185.199.111.153
   - Or add a CNAME record pointing to `[username].github.io`

### Automatic Deployment

GitHub Pages automatically rebuilds and deploys when you push to the `main` branch.

## Content Updates

### Editing Content

1. Edit `index.html` to update homepage content
2. Modify `assets/css/main.css` for styling changes
3. Update `_config.yml` for site-wide settings

### Adding New Pages

1. Create new HTML files with Jekyll front matter:
   ```yaml
   ---
   layout: default
   title: Page Title
   ---
   ```

2. Update navigation in `_includes/header.html`

## Architecture

This site follows the same Jekyll structure as other Rangeway portfolio sites:
- `rangeway-newsroom` (newsroom.rangeway.energy)
- `pathfinder` (pathfinder site)
- Main Rangeway site

This ensures consistency across the portfolio and makes maintenance easier.

## Technical Details

- **Jekyll Version**: 3.9 (GitHub Pages compatible)
- **Theme**: Custom (no theme gem)
- **Plugins**: jekyll-seo-tag
- **CSS**: Custom, responsive design
- **Browser Support**: Modern browsers, mobile-responsive

## Contact

For questions about this site, contact:
- **General**: info@redwoodmobility.com
- **Investor Relations**: investors@redwoodmobility.com
- **Real Estate**: realestate@redwoodmobility.com

## License

© 2025 Redwood Mobility, Inc. All rights reserved.
