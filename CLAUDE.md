# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a static HTML/CSS website for "Before Greatness" deployed via GitHub Pages. The site features a minimal black-and-white design with two pages: a landing page with ASCII art branding, and an about page using the Bulma CSS framework.

## Architecture

The site has two distinct design approaches:

1. **Landing Page (index.html)**: Pure custom CSS with centered layout, minimal dependencies. Features logo image and ASCII art text rendering.

2. **About Page (about.html)**: Bulma CSS framework with hero layout, social sharing capabilities, and Font Awesome icons. Uses B612 Mono font from Google Fonts.

This architectural split means:
- Main page is completely standalone (no external CSS dependencies)
- About page relies on CDN resources (Bulma, Font Awesome, Google Fonts)
- Both pages share the same custom CSS file (css/style.css)

## Development Commands

### Local Testing

Start a local server to test the site:

```bash
# Python 3
python -m http.server 8000

# Python 2
python -m SimpleHTTPServer 8000

# Node.js
npx http-server
```

Then navigate to `http://localhost:8000`

### Deployment

The site is deployed to GitHub Pages with custom domain `beforegreatness.com` (configured in CNAME file).

Push to main branch to deploy:
```bash
git add .
git commit -m "Description of changes"
git push origin main
```

## Key Files

- **index.html**: Landing page with minimal dependencies and ASCII art
- **about.html**: Secondary page using Bulma framework
- **css/style.css**: Custom styles for both pages (black background, white text, responsive design)
- **CNAME**: Contains `beforegreatness.com` for custom domain configuration
- **images/**: Contains three logo assets (white logo, horizontal logo, favicon)

## External Dependencies

The about page uses CDN-hosted resources:
- Bulma CSS v0.9.2
- Bulma Social v2
- Font Awesome kit (ID: 27ddd86667)
- Google Fonts: B612 Mono

The landing page has NO external dependencies except for the logo image.

## Design System

- **Color scheme**: Pure black (#000000) background, white (#ffffff) text
- **Typography**: Courier New/monospace for landing page, B612 Mono for about page
- **Responsive breakpoint**: 768px (mobile adjusts ASCII art font size and logo dimensions)
- **Layout**: Centered flex container with fullheight hero sections

## Important Constraints

- Keep the landing page dependency-free (no framework imports)
- Maintain the minimal black/white aesthetic
- ASCII art on landing page must remain properly formatted
- All logo images are white-on-transparent and require dark backgrounds
- Font Awesome kit is linked to a specific account - avoid changing kit ID
