# Before Greatness - GitHub Pages Static Site

This directory contains a static HTML/CSS/JavaScript version of the Before Greatness website, ready to be deployed on GitHub Pages.

## Directory Structure

```
github-pages/
├── index.html          # Main landing page
├── about.html          # About page
├── css/
│   └── style.css       # Custom styles
├── images/
│   ├── BG_MTN_LOGO_WHITE-256w.png
│   ├── bg_mtn_logo_black_circle_white_logo_icon.ico
│   └── BG_MTN_LOGO_horizontal-white-words.png
└── js/                 # JavaScript files (if needed)
```

## Features

- **Minimal Dependencies**: Uses CDN-hosted libraries (Bulma CSS, Font Awesome)
- **Responsive Design**: Mobile-friendly layout using Bulma framework
- **Fast Loading**: No backend processing, pure static files
- **Easy to Customize**: Simple HTML structure with separated CSS

## Deployment to GitHub Pages

### Option 1: Deploy from Main Branch

1. Create a new GitHub repository
2. Copy all files from this `github-pages` directory to the root of your new repository
3. Commit and push to GitHub:
   ```bash
   git init
   git add .
   git commit -m "Initial commit - static site"
   git branch -M main
   git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO-NAME.git
   git push -u origin main
   ```
4. Go to your repository settings on GitHub
5. Navigate to **Settings > Pages**
6. Under "Source", select **main** branch and **/ (root)** folder
7. Click **Save**
8. Your site will be available at: `https://YOUR-USERNAME.github.io/YOUR-REPO-NAME/`

### Option 2: Deploy from gh-pages Branch

1. Create a new GitHub repository
2. Create a `gh-pages` branch:
   ```bash
   git init
   git checkout -b gh-pages
   git add .
   git commit -m "Initial GitHub Pages deployment"
   git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO-NAME.git
   git push -u origin gh-pages
   ```
3. Go to repository settings and enable GitHub Pages from the `gh-pages` branch
4. Your site will be available at: `https://YOUR-USERNAME.github.io/YOUR-REPO-NAME/`

### Option 3: Custom Domain

If you want to use a custom domain like `beforegreatness.com`:

1. Follow either Option 1 or 2 above
2. Add a file named `CNAME` to the root directory with your domain:
   ```
   beforegreatness.com
   ```
3. Configure your domain's DNS settings to point to GitHub Pages:
   - Add an A record pointing to GitHub's IP addresses
   - Or add a CNAME record pointing to `YOUR-USERNAME.github.io`
4. More details: https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site

## Customization

### Changing Colors
Edit `css/style.css` to modify the background color and other styles.

### Updating Content
- **Home page**: Edit `index.html`
- **About page**: Edit `about.html`

### Adding Pages
1. Create a new HTML file (e.g., `contact.html`)
2. Copy the structure from `index.html` or `about.html`
3. Add navigation links in both `index.html` and the new page

### Changing Fonts
The site currently uses the B612 Mono font from Google Fonts. To change:
1. Browse fonts at https://fonts.google.com
2. Replace the font link in the `<head>` section of HTML files
3. Update the `.b612-mono` class in `css/style.css`

## External Dependencies (CDN)

- **Bulma CSS** (v0.9.2): https://cdn.jsdelivr.net/npm/bulma@0.9.2/css/bulma.min.css
- **Bulma Social**: https://cdn.jsdelivr.net/npm/bulma-social@2/css/all.min.css
- **Font Awesome**: https://kit.fontawesome.com/27ddd86667.js
- **Google Fonts (B612 Mono)**: https://fonts.googleapis.com/css2?family=B612+Mono

All external resources are loaded via CDN, so no local installation is required.

## Local Development

To test locally before deploying:

1. Simply open `index.html` in your web browser
2. Or use a simple HTTP server:
   ```bash
   # Python 3
   python -m http.server 8000

   # Python 2
   python -m SimpleHTTPServer 8000

   # Node.js (if you have npx)
   npx http-server
   ```
3. Navigate to `http://localhost:8000`

## Browser Support

This site supports all modern browsers:
- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## License

[Add your license information here]

## Credits

- **Bulma CSS Framework**: https://bulma.io
- **Font Awesome Icons**: https://fontawesome.com
- **Google Fonts**: https://fonts.google.com

---

For questions or support, contact: [Add contact information]
