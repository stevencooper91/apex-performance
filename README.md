# Apex Performance Landing Page

Welcome to your professional landing page! This guide will help you customize and deploy your website.

## 📁 What You Have

- `index.html` - Your complete landing page (HTML, CSS, and JavaScript all in one file)
- This README file with setup instructions

## 🎨 Quick Customization Guide

### 1. Adding Your Logo Images

You have two logo images to add:
1. **White logo** (for dark navigation bar) - Save as `logo-white.png`
2. **Hero image** (mountain visualization) - Save as `hero-mountain.png`

Place these images in the same folder as your `index.html` file.

**In VS Code:**
- Find lines 259 and 373 in the HTML
- Update the `src` attributes to match your actual file names

```html
<!-- Line 259 - Navigation logo -->
<img src="logo-white.png" alt="Apex Performance Logo">

<!-- Line 373 - Hero section image -->
<img src="hero-mountain.png" alt="Mountain Peak Visualization">
```

### 2. Changing Colors

All colors are defined at the top of the file (lines 15-23). Easy to modify:

```css
:root {
    --apex-black: #1a1a1a;      /* Main dark color */
    --apex-white: #ffffff;       /* White */
    --apex-yellow: #FFD700;      /* Yellow accent */
    --apex-blue: #2B4B8C;        /* Blue accent */
    --apex-gray: #f5f5f5;        /* Light background */
    --apex-dark-gray: #3a3a3a;   /* Dark gray text */
}
```

### 3. Editing Text Content

All text is easy to find and change:

**Tagline (Line 277):**
```html
<p class="tagline">— From the peak of experience</p>
```

**Main headline (Line 276):**
```html
<h1>Performance, <span class="highlight">Seen Clearly</span></h1>
```

**About section (Lines 290-310)**
**Services (Lines 340-450)**
**Contact info (Lines 500-520)**

### 4. Adding Your Own Images

**About Section Image (Line 322):**
```html
<img src="about-image.jpg" alt="Data analysis visualization">
```

**Placeholder images you'll need:**
- `logo-white.png` - Your white logo for navigation
- `hero-mountain.png` - Hero section visual
- `about-image.jpg` - About section image

## 🚀 Deployment Options

### Option 1: GitHub Pages (Recommended - FREE)

1. **Create GitHub Account** (if you don't have one)
   - Go to github.com and sign up

2. **Create a New Repository**
   - Click "+" in top right → "New repository"
   - Name it: `apex-performance-website`
   - Make it Public
   - Click "Create repository"

3. **Upload Your Files**
   - Click "uploading an existing file"
   - Drag and drop your `index.html` and all images
   - Click "Commit changes"

4. **Enable GitHub Pages**
   - Go to Settings (in your repository)
   - Scroll to "Pages" (left sidebar)
   - Under "Source", select "main" branch
   - Click "Save"
   - Your site will be live at: `https://yourusername.github.io/apex-performance-website`

5. **Connect Your GoDaddy Domain**
   - In GitHub Pages settings, enter your domain in "Custom domain"
   - In GoDaddy DNS settings, add these records:
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
     Value: yourusername.github.io
     ```

### Option 2: Netlify (Also FREE)

1. **Go to Netlify.com**
   - Sign up with GitHub or email

2. **Drag and Drop Deploy**
   - On your dashboard, drag your folder into the deploy zone
   - Your site goes live instantly!

3. **Connect Your Domain**
   - Go to Domain settings
   - Add your GoDaddy domain
   - Follow the DNS instructions provided

### Option 3: Vercel (Also FREE)

1. **Go to Vercel.com**
   - Sign up with GitHub

2. **Deploy**
   - Click "Add New Project"
   - Upload your files
   - Site goes live immediately

3. **Add Custom Domain**
   - Go to Project Settings → Domains
   - Add your GoDaddy domain
   - Update DNS as instructed

## 🔧 Making Changes

### In VS Code:

1. **Open the file**: `File → Open → select index.html`

2. **Find what you want to change**: Use `Ctrl+F` (Windows) or `Cmd+F` (Mac) to search

3. **Edit and save**: Make your changes and save (`Ctrl+S` or `Cmd+S`)

4. **Test locally**: Right-click the file → "Open with" → Your browser

5. **Upload changes**: Re-upload to GitHub/Netlify/Vercel

### Quick Edit Examples:

**Change phone number (Line 505):**
```html
<a href="tel:+33788373486">+33 7 88 37 34 86</a>
```

**Change email (Line 497):**
```html
<a href="mailto:contact@apex-perf.com">contact@apex-perf.com</a>
```

**Add social media icons** (after line 510, add):
```html
<div class="contact-item">
    <div class="contact-item-icon">📱</div>
    <div>
        <strong>Follow Us</strong><br>
        <a href="https://twitter.com/yourhandle">Twitter</a> | 
        <a href="https://linkedin.com/company/yourcompany">LinkedIn</a>
    </div>
</div>
```

## 📝 Form Setup

The contact form currently logs to console. To receive actual emails:

### Option 1: Formspree (Easiest)
1. Go to formspree.io
2. Create a free account
3. Create a new form
4. Replace line 540 with:
```html
<form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
```

### Option 2: Netlify Forms (if using Netlify)
1. Add `netlify` to the form tag:
```html
<form name="contact" netlify>
```

### Option 3: Custom Email Script
You'll need a backend service. I can help you set this up separately.

## 🎯 SEO Tips

1. **Update the title** (Line 6):
```html
<title>Apex Performance - Sports Data Analysis | Contact</title>
```

2. **Update the description** (Line 7):
```html
<meta name="description" content="Your custom description here">
```

3. **Add keywords**:
```html
<meta name="keywords" content="sports analytics, performance analysis, data analysis">
```

## 📱 Mobile Friendly

Your site is already fully responsive! It will automatically adjust for:
- Desktop computers
- Tablets
- Mobile phones

## 🆘 Need Help?

### Common Issues:

**Q: Images aren't showing?**
A: Make sure image files are in the same folder as index.html and filenames match exactly (case-sensitive!)

**Q: Colors look wrong?**
A: Check the CSS variables at the top of the file (lines 15-23)

**Q: Form not working?**
A: Set up Formspree or Netlify Forms (see Form Setup section above)

**Q: Can't connect domain?**
A: DNS changes take 24-48 hours. Be patient!

### Getting Updates:

Just tell me what you want to change:
- "Make the header bigger"
- "Change the yellow to orange"
- "Add a pricing section"
- "Remove the testimonials"

I'll give you the exact code to update!

## 📦 File Structure

```
your-website-folder/
├── index.html          (Your main page - this is the only required file!)
├── logo-white.png      (Your logo - white version)
├── hero-mountain.png   (Hero section image)
├── about-image.jpg     (About section image)
└── README.md          (This instructions file)
```

## ✅ Pre-Launch Checklist

Before going live, make sure to:

- [ ] Add all your logo images
- [ ] Update contact email and phone
- [ ] Customize the About section text
- [ ] Review all service descriptions
- [ ] Add real testimonials (or remove the section)
- [ ] Set up form submission (Formspree/Netlify)
- [ ] Test on mobile device
- [ ] Check all links work
- [ ] Update page title and meta description
- [ ] Add social media links (if you have them)

## 🎓 Learning Resources

Want to learn more about editing HTML/CSS?

- **W3Schools**: https://www.w3schools.com
- **MDN Web Docs**: https://developer.mozilla.org
- **CSS-Tricks**: https://css-tricks.com

## 💡 Tips for Success

1. **Start Simple**: Get the basic page live first, then improve it
2. **Test Everything**: Click all links and buttons before launch
3. **Mobile First**: Check how it looks on your phone
4. **Ask Questions**: Come back anytime you need help making changes
5. **Backup**: Keep a copy of working versions before making big changes

---

**Ready to Launch?** Follow the GitHub Pages instructions above - it's the easiest free option!

**Need Changes?** Just tell me what you want different and I'll help you update it!
