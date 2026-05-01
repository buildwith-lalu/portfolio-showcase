# ⚡ Quick Start Guide

Get your portfolio live in 10 minutes!

## 🎯 Step 1: Customize Your Info (5 minutes)

Open `index.html` and update:

### Your Name & Title
Find line 30-40 and change:
```html
<h1 class="hero-title">
    Hi, I'm <span class="highlight">YOUR NAME HERE</span>
</h1>
```

### Your Email
Find all instances of `your.email@example.com` and replace with your actual email.

**Quick Find & Replace:**
- Press `Ctrl + H` in your editor
- Find: `your.email@example.com`
- Replace: `your.actual.email@example.com`
- Click "Replace All"

### Your LinkedIn
Find `linkedin.com/in/yourprofile` and replace with your actual LinkedIn username.

### Your GitHub
Find `github.com/yourusername` and replace with your actual GitHub username.

## 🚀 Step 2: Deploy to GitHub Pages (5 minutes)

### A. Open PowerShell in portfolio folder
```powershell
cd C:\Users\LaluPrasad\Desktop\portfolio-website
```

### B. Initialize Git
```powershell
git init
git add .
git commit -m "Initial commit: My portfolio"
```

### C. Create GitHub Repository
1. Go to: https://github.com/new
2. Name: `your-username.github.io` (replace `your-username` with your GitHub username)
3. Make it **Public**
4. Click "Create repository"

### D. Push to GitHub
```powershell
git remote add origin https://github.com/your-username/your-username.github.io.git
git branch -M main
git push -u origin main
```

**Note:** If asked for password, use a Personal Access Token:
- Go to: https://github.com/settings/tokens
- Generate new token (classic)
- Select `repo` scope
- Copy token and use as password

### E. Enable GitHub Pages
1. Go to repository Settings → Pages
2. Source: `main` branch, `/ (root)` folder
3. Click Save
4. Wait 2-5 minutes

### F. Visit Your Site! 🎉
Your portfolio is live at: `https://your-username.github.io`

## 🎨 Optional: Customize Colors

Open `styles.css` and change colors at the top:

```css
:root {
    --primary-color: #2563eb;      /* Change this */
    --secondary-color: #7c3aed;    /* And this */
    --accent-color: #f59e0b;       /* And this */
}
```

Popular color schemes:
- **Blue/Purple** (current): `#2563eb`, `#7c3aed`
- **Green/Teal**: `#10b981`, `#14b8a6`
- **Orange/Red**: `#f97316`, `#ef4444`
- **Pink/Purple**: `#ec4899`, `#a855f7`

## 📱 Test Your Portfolio

After deployment, check:
- ✅ All links work
- ✅ Mobile responsive (test on phone)
- ✅ Contact information is correct
- ✅ No placeholder text remains

## 🔄 Making Updates

After changing files:

```powershell
cd C:\Users\LaluPrasad\Desktop\portfolio-website
git add .
git commit -m "Update: describe your changes"
git push
```

Wait 2-5 minutes for changes to appear online.

## 🆘 Troubleshooting

### Site shows 404
- Wait 5-10 minutes after enabling Pages
- Check repository is Public
- Verify file is named `index.html` (lowercase)

### Can't push to GitHub
- You need a Personal Access Token (not password)
- See step D above

### Styles not loading
- Clear browser cache (Ctrl + F5)
- Check all files are in same folder

## 📞 Need More Help?

See the full guides:
- `README.md` - Complete documentation
- `DEPLOYMENT-GUIDE.md` - Detailed deployment steps

---

**That's it! Your portfolio is live! 🚀**

Share it on:
- LinkedIn
- Resume
- Email signature
- Job applications