# Deployment Guide for GitHub Pages

## 📋 Prerequisites

1. A GitHub account
2. Git installed on your computer
3. Your profile photo ready (recommended: 400x400px, JPG/PNG format)

## 🚀 Step-by-Step Deployment

### Step 1: Prepare Your Content

1. **Add your profile photo**:
   - Place your photo in the `images` folder
   - Rename it to `profile.jpg` (or update the path in `index.html`)

2. **Verify all information**:
   - Check your email address
   - Verify Google Scholar link
   - Confirm ResearchGate and GitHub URLs
   - Update publications if needed

### Step 2: Create GitHub Repository

1. Go to [GitHub](https://github.com)
2. Click the "+" icon → "New repository"
3. Repository name: `aster-ww.github.io` (replace `aster-ww` with your GitHub username)
4. Description: "My academic homepage"
5. Make it **Public**
6. Click "Create repository"

### Step 3: Upload Files

**Option A: Using GitHub Web Interface** (Easiest)

1. In your new repository, click "uploading an existing file"
2. Drag and drop all files from your `personal_site` folder
3. Add commit message: "Initial commit - Academic homepage"
4. Click "Commit changes"

**Option B: Using Git Command Line**

```bash
# Navigate to your project folder
cd d:\test_tclaw\personal_site

# Initialize git repository
git init

# Add all files
git add .

# Commit changes
git commit -m "Initial commit - Academic homepage"

# Add remote repository
git remote add origin https://github.com/aster-ww/aster-ww.github.io.git

# Push to GitHub
git push -u origin main
```

### Step 4: Enable GitHub Pages

1. Go to your repository on GitHub
2. Click "Settings" tab
3. Scroll down to "Pages" section (in the left sidebar)
4. Under "Source", select "main" branch
5. Click "Save"

### Step 5: Access Your Website

Your website will be live at:
```
https://aster-ww.github.io
```

It may take 1-2 minutes for the site to become available.

## 🔄 Updating Your Website

### To update content:

1. Edit the files locally
2. Commit and push changes:
   ```bash
   git add .
   git commit -m "Update content"
   git push
   ```
3. Changes will be reflected in 1-2 minutes

### To update profile photo:

1. Replace `images/profile.jpg` with new photo
2. Commit and push:
   ```bash
   git add images/profile.jpg
   git commit -m "Update profile photo"
   git push
   ```

## ✅ Checklist Before Deployment

- [ ] Profile photo added to `images/` folder
- [ ] Email address verified
- [ ] Google Scholar link working
- [ ] ResearchGate link working
- [ ] GitHub link working
- [ ] Publications up to date
- [ ] Awards section updated
- [ ] Tested locally in browser

## 🔧 Local Testing

Before deploying, test your site locally:

1. Open `index.html` in your browser
2. Check all sections display correctly
3. Test all links work
4. Verify responsive design (resize browser window)
5. Test on mobile device if possible

## 🐛 Troubleshooting

### Site not loading?
- Wait 2-3 minutes after enabling GitHub Pages
- Check repository name matches exactly: `username.github.io`
- Ensure index.html is in the root directory

### Styles not applying?
- Check `css/style.css` file exists
- Verify the link tag in `index.html` is correct

### Images not showing?
- Ensure images are in the `images/` folder
- Check file paths are correct
- Use forward slashes in paths: `images/profile.jpg`

## 📊 Analytics (Optional)

To add Google Analytics:

1. Create a Google Analytics account
2. Get your tracking ID
3. Add this code before `</head>` in `index.html`:

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=YOUR_TRACKING_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'YOUR_TRACKING_ID');
</script>
```

## 🎨 Custom Domain (Optional)

To use a custom domain:

1. Purchase a domain (e.g., from Namecheap, Google Domains)
2. In repository Settings → Pages → Custom domain, enter your domain
3. Configure DNS settings with your domain registrar:
   - Add CNAME record pointing to `aster-ww.github.io`
4. Wait for DNS propagation (can take up to 24 hours)

## 📝 Need Help?

- GitHub Pages Documentation: https://docs.github.com/en/pages
- Git Documentation: https://git-scm.com/doc

---

Good luck with your deployment! 🎉
