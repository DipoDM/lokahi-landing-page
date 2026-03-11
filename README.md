# Lōkahi Landing Page

Official landing page for the Lōkahi app at [lokahiapp.io](https://lokahiapp.io)

## Structure

```
ohana-landing-page/
├── index.html          # Main landing page with download buttons
├── privacy.html        # Privacy policy
├── support.html        # Support & FAQ page
├── terms.html          # Terms of use
├── styles.css          # Stylesheet for all pages
└── assets/
    └── app-logo.png    # App logo
```

## Before Publishing

### 1. Update App Store Links

Edit `index.html` and replace the placeholder URLs:

**Line 26 (App Store):**
```html
<a href="https://apps.apple.com/us/app/your-app-id" ...>
```

**Line 29 (Google Play):**
```html
<a href="https://play.google.com/store/apps/details?id=your.app.id" ...>
```

### 2. Verify Email Address

The support email is set to: `support@lokahiapp.io`

Make sure this email is configured and monitored.

## Deployment

### Option 1: GitHub Pages

1. Create a new repository (e.g., `lokahi-landing-page`)
2. Push these files to the repository
3. Go to Settings → Pages
4. Set source to main branch
5. Configure custom domain: `lokahiapp.io`
6. Add CNAME record in your DNS:
   ```
   CNAME  @  <your-github-username>.github.io
   ```

### Option 2: Vercel

1. Install Vercel CLI: `npm i -g vercel`
2. Run `vercel` in this directory
3. Follow prompts to deploy
4. Configure custom domain in Vercel dashboard

### Option 3: Netlify

1. Drag and drop this folder to [Netlify Drop](https://app.netlify.com/drop)
2. Or use Netlify CLI:
   ```bash
   npm install -g netlify-cli
   netlify deploy --prod
   ```
3. Configure custom domain in Netlify dashboard

### Option 4: Traditional Hosting (cPanel, etc.)

1. Upload all files via FTP/SFTP
2. Ensure `index.html` is in the root directory
3. Point domain to hosting server

## DNS Configuration

For `lokahiapp.io`, you'll need:

1. **A Record** (if using IP-based hosting):
   ```
   A  @  <server-ip-address>
   ```

2. **CNAME Record** (if using GitHub Pages/Vercel/Netlify):
   ```
   CNAME  @  <platform-url>
   ```

3. **WWW Redirect** (optional):
   ```
   CNAME  www  lokahiapp.io
   ```

## URLs Referenced in App

The following URLs will be used by your app and should match your domain:

- Privacy Policy: `https://lokahiapp.io/privacy.html`
- Support: `https://lokahiapp.io/support.html`
- Terms of Use: `https://lokahiapp.io/terms.html`

## Testing Locally

Simply open `index.html` in a browser, or run a local server:

```bash
# Python 3
python3 -m http.server 8000

# Python 2
python -m SimpleHTTPServer 8000

# Node.js (if you have npx)
npx serve

# PHP
php -S localhost:8000
```

Then visit: `http://localhost:8000`

## Maintenance

### Updating Content

All content is in HTML files. Edit directly:
- `index.html` - Main page
- `privacy.html` - Privacy policy
- `support.html` - FAQ and support
- `terms.html` - Legal terms

### Updating Styles

Edit `styles.css` to change colors, fonts, or layout.

### Updating Logo

Replace `assets/app-logo.png` with a new logo (recommended: 512x512px or larger, PNG format).
