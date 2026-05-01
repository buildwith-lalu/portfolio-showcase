# 🚀 Portfolio Deployment Guide

Complete step-by-step guide to deploy your portfolio website.

## 📋 Pre-Deployment Checklist

Before deploying, make sure you've customized:

- [ ] Personal information (name, title, description)
- [ ] Contact details (email, LinkedIn, GitHub)
- [ ] Project descriptions
- [ ] Skills section
- [ ] All placeholder links

## 🎯 Method 1: GitHub Pages (Recommended - FREE)

### Step 1: Create GitHub Account
If you don't have one, sign up at https://github.com

### Step 2: Initialize Git Repository

Open PowerShell in the `portfolio-website` folder:

```powershell
# Navigate to portfolio folder
cd C:\Users\LaluPrasad\Desktop\portfolio-website

# Initialize git
git init

# Add all files
git add .

# Create first commit
git commit -m "Initial commit: My portfolio website"
```

### Step 3: Create GitHub Repository

1. Go to https://github.com/new
2. Repository name: Choose one of these options:
   - **Option A (User Site)**: `your-username.github.io` 
     - Example: `laluprasad.github.io`
     - URL will be: `https://laluprasad.github.io`
   
   - **Option B (Project Site)**: `portfolio` or any name
     - Example: `my-portfolio`
     - URL will be: `https://your-username.github.io/my-portfolio`

3. Description: "My professional portfolio website"
4. Make it **Public**
5. **DO NOT** check "Initialize with README"
6. Click "Create repository"

### Step 4: Connect and Push to GitHub

Copy the commands from GitHub (they'll look like this):

```powershell
# Add remote repository
git remote add origin https://github.com/your-username/your-repo-name.git

# Rename branch to main
git branch -M main

# Push to GitHub
git push -u origin main
```

**If you get authentication error:**
- GitHub no longer accepts passwords
- You need a Personal Access Token (PAT)

**To create a PAT:**
1. Go to GitHub → Settings → Developer settings → Personal access tokens → Tokens (classic)
2. Click "Generate new token (classic)"
3. Name: "Portfolio Deployment"
4. Expiration: 90 days (or your preference)
5. Select scopes: Check `repo` (all sub-options)
6. Click "Generate token"
7. **COPY THE TOKEN** (you won't see it again!)
8. Use this token as your password when pushing

### Step 5: Enable GitHub Pages

1. Go to your repository on GitHub
2. Click **Settings** (top menu)
3. Click **Pages** (left sidebar)
4. Under "Source":
   - Branch: `main`
   - Folder: `/ (root)`
5. Click **Save**
6. Wait 2-5 minutes
7. Refresh the page - you'll see: "Your site is live at https://..."

### Step 6: Visit Your Site! 🎉

Your portfolio is now live at:
- User site: `https://your-username.github.io`
- Project site: `https://your-username.github.io/repo-name`

---

## 🌐 Method 2: Netlify (Alternative - FREE)

### Option A: Drag & Drop (Easiest)

1. Go to https://app.netlify.com/drop
2. Drag the entire `portfolio-website` folder onto the page
3. Wait for upload to complete
4. Your site is live! You'll get a URL like: `random-name-123.netlify.app`

### Option B: Connect to GitHub (Better for updates)

1. Sign up at https://netlify.com (use GitHub to sign in)
2. Click "Add new site" → "Import an existing project"
3. Choose "GitHub"
4. Authorize Netlify
5. Select your portfolio repository
6. Build settings:
   - Build command: (leave empty)
   - Publish directory: (leave empty or put `/`)
7. Click "Deploy site"
8. Your site is live!

### Customize Netlify Domain

1. Go to Site settings → Domain management
2. Click "Options" → "Edit site name"
3. Change to: `your-name-portfolio.netlify.app`

---

## ☁️ Method 3: Vercel (Alternative - FREE)

### Deploy via Website

1. Go to https://vercel.com
2. Sign up with GitHub
3. Click "Add New" → "Project"
4. Import your GitHub repository
5. Click "Deploy"
6. Your site is live!

### Deploy via CLI

```powershell
# Install Vercel CLI
npm install -g vercel

# Navigate to portfolio folder
cd C:\Users\LaluPrasad\Desktop\portfolio-website

# Deploy
vercel --prod
```

---

## 🔄 Updating Your Portfolio

After making changes to your portfolio:

### If using GitHub Pages:

```powershell
# Navigate to portfolio folder
cd C:\Users\LaluPrasad\Desktop\portfolio-website

# Check what changed
git status

# Add changes
git add .

# Commit changes
git commit -m "Update: describe what you changed"

# Push to GitHub
git push
```

Wait 2-5 minutes for changes to appear on your live site.

### If using Netlify/Vercel with GitHub:

Just push to GitHub (same commands as above). Netlify/Vercel will automatically rebuild and deploy!

### If using Netlify Drag & Drop:

1. Go to https://app.netlify.com
2. Find your site
3. Drag the updated folder to deploy a new version

---

## 🎨 Custom Domain (Optional)

### Buy a Domain

Popular registrars:
- Namecheap: https://namecheap.com
- GoDaddy: https://godaddy.com
- Google Domains: https://domains.google

Recommended: `yourname.dev` or `yourname.com`

### Connect to GitHub Pages

1. Buy domain (e.g., `laluprasad.dev`)
2. In your repository, create a file named `CNAME` (no extension)
3. Content: just your domain name
   ```
   laluprasad.dev
   ```
4. In your domain registrar, add DNS records:
   ```
   Type: A
   Name: @
   Value: 185.199.108.153
   
   Type: A
   Name: @
   Value: 185.199.109.153
   
   Type: A
   Name: @
   Value: 185.199.110.153
   
   Type: A
   Name: @
   Value: 185.199.111.153
   
   Type: CNAME
   Name: www
   Value: your-username.github.io
   ```
5. Wait 24-48 hours for DNS propagation

### Connect to Netlify

1. Go to Site settings → Domain management
2. Click "Add custom domain"
3. Enter your domain
4. Follow Netlify's instructions to update DNS

---

## 🐛 Common Issues & Solutions

### Issue: "Permission denied" when pushing to GitHub

**Solution:** You need a Personal Access Token (see Step 4 above)

### Issue: GitHub Pages shows 404

**Solutions:**
- Wait 5-10 minutes after enabling Pages
- Check repository is Public
- Verify branch is `main` and folder is `/`
- Check file is named `index.html` (lowercase)

### Issue: Styles not loading on GitHub Pages

**Solution:** If using project site, update paths in HTML:
```html
<!-- Change from: -->
<link rel="stylesheet" href="styles.css">

<!-- To: -->
<link rel="stylesheet" href="/repo-name/styles.css">
```

### Issue: Site works locally but not online

**Solutions:**
- Check browser console for errors (F12)
- Verify all file paths are correct
- Ensure all files are committed and pushed
- Clear browser cache (Ctrl + F5)

---

## 📊 Add Analytics (Optional)

### Google Analytics

1. Go to https://analytics.google.com
2. Create account and property
3. Get Measurement ID (looks like: G-XXXXXXXXXX)
4. Add to `index.html` before `</head>`:

```html
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-XXXXXXXXXX');
</script>
```

---

## ✅ Post-Deployment Checklist

After deployment:

- [ ] Visit your live site and test all links
- [ ] Test on mobile device
- [ ] Test all navigation links
- [ ] Verify contact links work
- [ ] Check site loads quickly
- [ ] Test on different browsers
- [ ] Share your portfolio link!

---

## 🎯 Where to Share Your Portfolio

Once deployed, share your portfolio on:

- LinkedIn profile (Featured section)
- GitHub profile README
- Resume/CV
- Email signature
- Twitter/X bio
- Dev.to profile
- Stack Overflow profile
- Job applications
- Freelance platforms (Upwork, Fiverr)

---

## 💡 Pro Tips

1. **Keep it updated** - Add new projects regularly
2. **Monitor analytics** - See what visitors are interested in
3. **Get feedback** - Ask colleagues to review
4. **SEO optimize** - Use proper meta tags (already included!)
5. **Mobile first** - Most visitors will be on mobile
6. **Fast loading** - Optimize images if you add them
7. **Professional email** - Use custom domain email if possible

---

## 🆘 Need Help?

If you encounter issues:

1. Check this guide again
2. Search the error message on Google
3. Check GitHub Pages documentation
4. Ask on Stack Overflow
5. Check repository Issues tab

---

**Good luck with your portfolio! 🚀**

*Remember: Your portfolio is your digital business card. Keep it updated and professional!*