# Conscious Mama Website

This is the landing page and support website for the Conscious Mama app.

## Setup Instructions

### 1. Push to GitHub

```bash
# Navigate to this folder
cd website

# Initialize git (if not already done)
git init

# Add all files
git add .

# Commit
git commit -m "Initial website setup"

# Add your GitHub repository as remote
git remote add origin https://github.com/YOUR_USERNAME/consciousmama.github.io.git

# Push to main branch
git push -u origin main
```

### 2. Enable GitHub Pages

1. Go to your repository on GitHub
2. Click **Settings**
3. Scroll to **Pages** in the left sidebar
4. Under "Source", select **main** branch and **/ (root)** folder
5. Click **Save**
6. Wait a few minutes for deployment

Your site will be live at: `https://consciousmama.github.io`

## Files

- `index.html` - Main landing page
- `privacy.html` - Privacy Policy (required for App Store)
- `support.html` - Support/Help Center (required for App Store)
- `terms.html` - Terms of Service
- `images/` - Folder for screenshots and images

## Adding Screenshots

1. Take screenshots from your app
2. Save them in the `images/` folder with names like:
   - `screenshot-home.png`
   - `screenshot-learning.png`
   - `screenshot-activities.png`
   - etc.

3. Update `index.html` to replace the placeholder divs with actual images:

```html
<!-- Replace this -->
<div class="placeholder-phone">...</div>

<!-- With this -->
<img src="images/screenshot-home.png" alt="Home Screen" class="phone-mockup">
```

## URLs for App Store Submission

- **Privacy Policy URL**: https://consciousmama.github.io/privacy.html
- **Support URL**: https://consciousmama.github.io/support.html

## Customization

### Update Contact Email
Search and replace `support@consciousmama.app` with your actual email address in:
- `privacy.html`
- `support.html`
- `terms.html`

### Add App Store Links
When your app is live, update the store button links in `index.html`:
```html
<a href="https://apps.apple.com/app/your-app-id" class="store-btn apple">
<a href="https://play.google.com/store/apps/details?id=your.app.id" class="store-btn google">
```
