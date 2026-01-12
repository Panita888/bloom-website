# GitHub Setup Guide for Bloom Website

## Step 1: Create GitHub Account (if you don't have one)
1. Go to https://github.com
2. Click "Sign up"
3. Follow the instructions

## Step 2: Create New Repository

1. Click the "+" icon in the top right corner
2. Select "New repository"
3. Repository name: `bloom-website` (or any name you want)
4. Description: "Bloom - Where Businesses Bloom"
5. Select "Public"
6. ✅ Check "Add a README file"
7. Click "Create repository"

## Step 3: Upload Your Files

**Option A: Using Web Interface (Easiest)**

1. In your repository, click "Add file" → "Upload files"
2. Drag and drop ALL these files:
   - index.html
   - about.html
   - contact.html
   - Bloom_logo.png
   - CNAME
   - .gitignore
3. Write commit message: "Initial commit - Bloom website"
4. Click "Commit changes"

**Option B: Using Git Command Line**

```bash
# 1. Initialize git in your website folder
git init

# 2. Add all files
git add .

# 3. Commit
git commit -m "Initial commit - Bloom website"

# 4. Link to your GitHub repository
git remote add origin https://github.com/YOUR_USERNAME/bloom-website.git

# 5. Push
git branch -M main
git push -u origin main
```

## Step 4: Enable GitHub Pages (Free Hosting!)

1. Go to your repository
2. Click "Settings" (top navigation)
3. Click "Pages" in left sidebar
4. Under "Source":
   - Branch: Select "main"
   - Folder: Select "/ (root)"
5. Click "Save"
6. Wait 2-3 minutes
7. Your site will be live at: `https://YOUR_USERNAME.github.io/bloom-website/`

## Step 5: Connect Your Custom Domain (joinbloom.tech)

### A. In GitHub:
1. Still in Settings → Pages
2. Under "Custom domain", enter: `joinbloom.tech`
3. Click "Save"
4. ✅ Check "Enforce HTTPS" (after DNS propagates)

### B. In GoDaddy (or your domain registrar):

1. Log into your domain registrar
2. Find DNS settings for joinbloom.tech
3. Delete any existing A or CNAME records
4. Add these records:

**A Records** (for root domain):
```
Type: A
Name: @
Value: 185.199.108.153
TTL: 600

Type: A
Name: @
Value: 185.199.109.153
TTL: 600

Type: A
Name: @
Value: 185.199.110.153
TTL: 600

Type: A
Name: @
Value: 185.199.111.153
TTL: 600
```

**CNAME Record** (for www):
```
Type: CNAME
Name: www
Value: YOUR_GITHUB_USERNAME.github.io
TTL: 600
```

5. Save changes
6. Wait 24-48 hours for DNS to propagate

## Step 6: Test Your Website

1. After DNS propagates, go to: https://joinbloom.tech
2. Test all pages work
3. Test the calculator
4. Test FAQ accordion

## Updating Your Website

Whenever you want to make changes:

1. Edit files locally
2. Go to GitHub repository
3. Click on the file you want to edit
4. Click the pencil icon (Edit)
5. Make changes
6. Scroll down, write commit message
7. Click "Commit changes"
8. Changes will go live in 1-2 minutes!

## Important Notes

✅ Your website is now hosted for FREE on GitHub Pages
✅ It will be available 24/7
✅ HTTPS is automatic after DNS setup
✅ You can update anytime through GitHub

## Need Help?

- GitHub Pages docs: https://docs.github.com/en/pages
- GoDaddy DNS help: Search "GoDaddy custom domain GitHub Pages"

## Contact Form Setup

Don't forget to set up your contact form! In `contact.html`, replace:
```html
action="https://formspree.io/f/YOUR_FORM_ID"
```

With your actual form service:
- **Formspree**: https://formspree.io (easiest)
- **Netlify Forms**: If you switch to Netlify hosting
- **Custom backend**: If you have your own server

---

**You're all set! 🎉**

Your website will be live at https://joinbloom.tech within 24-48 hours after DNS propagation.
