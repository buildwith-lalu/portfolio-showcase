# Lalu Prasad - Portfolio Website

A modern, responsive portfolio website showcasing full-stack development expertise with 10+ years of experience.

## 🌟 Features

- **Responsive Design** - Works perfectly on desktop, tablet, and mobile devices
- **Modern UI/UX** - Clean, professional design with smooth animations
- **Fast Loading** - Optimized performance with minimal dependencies
- **SEO Friendly** - Proper meta tags and semantic HTML
- **Easy to Customize** - Well-organized code structure

## 📁 Project Structure

```
portfolio-website/
├── index.html          # Main HTML file
├── styles.css          # CSS styling
├── script.js           # JavaScript functionality
└── README.md           # This file
```

## 🚀 Quick Start

### Option 1: GitHub Pages (Recommended)

1. **Create a GitHub Repository**
   ```bash
   cd portfolio-website
   git init
   git add .
   git commit -m "Initial commit: Portfolio website"
   ```

2. **Create a new repository on GitHub**
   - Go to https://github.com/new
   - Name it: `your-username.github.io` (for user site) or any name (for project site)
   - Don't initialize with README

3. **Push to GitHub**
   ```bash
   git remote add origin https://github.com/your-username/your-repo-name.git
   git branch -M main
   git push -u origin main
   ```

4. **Enable GitHub Pages**
   - Go to repository Settings → Pages
   - Source: Deploy from a branch
   - Branch: main, folder: / (root)
   - Click Save

5. **Access Your Site**
   - User site: `https://your-username.github.io`
   - Project site: `https://your-username.github.io/repo-name`

### Option 2: Netlify

1. **Install Netlify CLI** (optional)
   ```bash
   npm install -g netlify-cli
   ```

2. **Deploy via Drag & Drop**
   - Go to https://app.netlify.com/drop
   - Drag the `portfolio-website` folder
   - Your site is live!

3. **Or Deploy via CLI**
   ```bash
   cd portfolio-website
   netlify deploy --prod
   ```

### Option 3: Vercel

1. **Install Vercel CLI**
   ```bash
   npm install -g vercel
   ```

2. **Deploy**
   ```bash
   cd portfolio-website
   vercel --prod
   ```

## ✏️ Customization Guide

### 1. Update Personal Information

**In `index.html`:**

- **Line 7**: Update meta description
- **Line 8**: Update page title
- **Lines 30-40**: Update hero section text
- **Lines 200-220**: Update contact information (email, LinkedIn, GitHub)

### 2. Update Contact Links

Replace placeholder links with your actual profiles:

```html
<!-- Email -->
<a href="mailto:your.actual.email@example.com">your.actual.email@example.com</a>

<!-- LinkedIn -->
<a href="https://linkedin.com/in/your-actual-profile">linkedin.com/in/your-actual-profile</a>

<!-- GitHub -->
<a href="https://github.com/your-actual-username">github.com/your-actual-username</a>
```

### 3. Customize Colors

**In `styles.css` (lines 2-15):**

```css
:root {
    --primary-color: #2563eb;      /* Main brand color */
    --secondary-color: #7c3aed;    /* Secondary brand color */
    --accent-color: #f59e0b;       /* Accent color */
    /* ... other colors ... */
}
```

### 4. Add Your Projects

Edit the projects section in `index.html` (lines 60-150) to add or modify projects:

```html
<div class="project-card">
    <div class="project-icon">
        <i class="fas fa-your-icon"></i>
    </div>
    <h3 class="project-title">Your Project Name</h3>
    <p class="project-description">Description</p>
    <!-- Add features, tech stack, etc. -->
</div>
```

### 5. Update Skills

Modify the skills section in `index.html` (lines 160-190) to reflect your actual skills.

### 6. Add Profile Image (Optional)

Replace the icon with an actual image:

```html
<!-- In index.html, replace the profile-icon div with: -->
<img src="your-photo.jpg" alt="Lalu Prasad" class="profile-image">
```

Add this CSS:
```css
.profile-image {
    width: 100%;
    height: 100%;
    object-fit: cover;
    border-radius: 20px;
}
```

## 🎨 Advanced Customization

### Add Google Analytics

Add before closing `</head>` tag:

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_MEASUREMENT_ID');
</script>
```

### Add Favicon

Add in `<head>` section:

```html
<link rel="icon" type="image/png" href="favicon.png">
```

### Add Open Graph Tags (for social sharing)

```html
<meta property="og:title" content="Lalu Prasad - Full-Stack Developer">
<meta property="og:description" content="Portfolio of a Full-Stack Developer with 10+ years experience">
<meta property="og:image" content="https://your-site.com/preview-image.jpg">
<meta property="og:url" content="https://your-site.com">
```

## 🔧 Troubleshooting

### GitHub Pages not showing

- Wait 5-10 minutes after enabling GitHub Pages
- Check that the repository is public
- Verify the branch and folder settings

### Styles not loading

- Check file paths are correct
- Ensure all files are in the same directory
- Clear browser cache (Ctrl+F5)

### Mobile menu not working

- Ensure `script.js` is loaded
- Check browser console for errors
- Verify Font Awesome is loading

## 📱 Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## 📄 License

This project is open source and available for personal and commercial use.

## 🤝 Support

If you need help customizing your portfolio:
- Check the comments in the code
- Review this README
- Search for similar issues online

## 🎯 Next Steps

1. ✅ Customize all personal information
2. ✅ Update contact links
3. ✅ Add your actual projects
4. ✅ Deploy to GitHub Pages or Netlify
5. ✅ Share your portfolio link!

---

**Built with ❤️ by Lalu Prasad**

*Last updated: May 2026*