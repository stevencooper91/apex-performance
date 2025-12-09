# QUICK START GUIDE - Apex Performance Website

## 🚀 Get Your Site Live in 3 Steps

### STEP 1: Add Your Images (5 minutes)

1. Save your logo files in the same folder as `index.html`:
   - White logo → save as `logo-white.png`
   - Hero mountain image → save as `hero-mountain.png`
   - About section image → save as `about-image.jpg`

2. If your files have different names, update these lines in `index.html`:

**LINE 259** - Navigation Logo:
```html
<img src="logo-white.png" alt="Apex Performance Logo">
```
Change `logo-white.png` to your actual filename

**LINE 373** - Hero Image:
```html
<img src="hero-mountain.png" alt="Mountain Peak Visualization">
```
Change `hero-mountain.png` to your actual filename

**LINE 322** - About Image:
```html
<img src="about-image.jpg" alt="Data analysis visualization">
```
Change `about-image.jpg` to your actual filename

---

### STEP 2: Test Locally (2 minutes)

1. Open `index.html` in your web browser (double-click the file)
2. Check that everything looks good
3. Click through all the sections
4. Test the mobile view (make your browser window narrow)

---

### STEP 3: Deploy to GitHub Pages (15 minutes)

#### A. Create GitHub Account
- Go to: https://github.com/signup
- Create your free account

#### B. Create New Repository
1. Click the "+" in top-right corner
2. Select "New repository"
3. Repository name: `apex-performance`
4. Make it **Public**
5. Click "Create repository"

#### C. Upload Your Files
1. Click "uploading an existing file"
2. Drag and drop:
   - index.html
   - logo-white.png
   - hero-mountain.png
   - about-image.jpg
   - README.md
3. Click "Commit changes"

#### D. Enable GitHub Pages
1. Click "Settings" tab
2. Click "Pages" in left sidebar
3. Under "Source": select **main** branch
4. Click "Save"
5. Wait 2-3 minutes
6. Your site is live at: `https://YOUR-USERNAME.github.io/apex-performance`

#### E. Connect Your GoDaddy Domain

**In GitHub:**
1. Still in Pages settings
2. Type your domain in "Custom domain" box
3. Click "Save"

**In GoDaddy:**
1. Log into GoDaddy
2. Go to "My Products" → "DNS" for your domain
3. Add these DNS records:

```
Record Type: A
Name: @
Value: 185.199.108.153
TTL: 600 seconds

Record Type: A
Name: @
Value: 185.199.109.153
TTL: 600 seconds

Record Type: A
Name: @
Value: 185.199.110.153
TTL: 600 seconds

Record Type: A
Name: @
Value: 185.199.111.153
TTL: 600 seconds

Record Type: CNAME
Name: www
Value: YOUR-USERNAME.github.io
TTL: 1 Hour
```

**Wait 24-48 hours** for DNS to propagate. Then your domain will work!

---

## 📝 Most Common Edits

### Change Colors
**LINES 15-23** - Color Variables:
```css
--apex-yellow: #FFD700;    /* Change to any color code */
--apex-blue: #2B4B8C;      /* Change to any color code */
```

### Change Main Headline
**LINE 276**:
```html
<h1>Performance, <span class="highlight">Seen Clearly</span></h1>
```

### Change Tagline
**LINE 277**:
```html
<p class="tagline">— From the peak of experience</p>
```

### Change Hero Description
**LINES 278-281**:
```html
<p>
    Bespoke data analysis for sports clubs and organisations. 
    With 13 years navigating elite environments, we've done the hard yards so you don't have to.
</p>
```

### Update Contact Email
**LINE 497**:
```html
<a href="mailto:contact@apex-perf.com">contact@apex-perf.com</a>
```

### Update Phone Number
**LINE 505**:
```html
<a href="tel:+33788373486">+33 7 88 37 34 86</a>
```

### Change Button Text
**LINE 284** - Primary button:
```html
<a href="#contact" class="btn btn-primary">Schedule Consultation</a>
```

**LINE 285** - Secondary button:
```html
<a href="#services" class="btn btn-secondary">Explore Services</a>
```

---

## 🎨 Customization Tips

### Want Different Fonts?
**LINE 9** - Replace with any Google Font:
```html
<link href="https://fonts.googleapis.com/css2?family=YOUR-FONT-HERE&display=swap" rel="stylesheet">
```

Then update **LINES 25-27**:
```css
--font-heading: 'YOUR-FONT-HERE', sans-serif;
--font-body: 'YOUR-FONT-HERE', sans-serif;
```

### Want to Remove a Section?
Simply delete everything between the `<section>` and `</section>` tags.

For example, to remove Testimonials:
- Delete **LINES 454-493**

### Want to Add Social Media Links?
**After LINE 515**, add:
```html
<div class="contact-item">
    <div class="contact-item-icon">🔗</div>
    <div>
        <strong>Social Media</strong><br>
        <a href="https://linkedin.com/company/your-company">LinkedIn</a> | 
        <a href="https://twitter.com/your-handle">Twitter</a>
    </div>
</div>
```

---

## ✉️ Make the Contact Form Work

### Option 1: Formspree (Easiest - Takes 5 minutes)

1. Go to https://formspree.io
2. Sign up for free
3. Create a new form
4. Copy your form ID
5. Change **LINE 540** to:
```html
<form action="https://formspree.io/f/YOUR-FORM-ID" method="POST">
```

### Option 2: If Using Netlify
Change **LINE 540** to:
```html
<form name="contact" method="POST" data-netlify="true">
```

---

## 🔍 Testing Checklist

Before going live:
- [ ] All images showing correctly
- [ ] Contact info is correct
- [ ] All links work (especially mailto: and tel:)
- [ ] Mobile version looks good
- [ ] Form submission works
- [ ] Colors match your brand
- [ ] All text is updated (no placeholder text)

---

## 💡 Pro Tips

1. **Browser Cache**: If changes don't show, press `Ctrl+F5` (Windows) or `Cmd+Shift+R` (Mac)

2. **Save Often**: Press `Ctrl+S` or `Cmd+S` frequently when editing

3. **Keep Backup**: Before major changes, make a copy of the working file

4. **Test on Phone**: Use your actual phone to check mobile view

5. **Small Changes First**: Make one change at a time and test

---

## 🆘 Troubleshooting

**Images not showing?**
- Check file names match exactly (including capitalization)
- Make sure images are in same folder as index.html
- Try clearing browser cache

**Site not updating?**
- GitHub Pages takes 2-3 minutes to rebuild
- Clear your browser cache
- Try incognito/private browsing mode

**Form not submitting?**
- Set up Formspree (see above)
- Check that all required fields have the `required` attribute

**Domain not working?**
- DNS changes take 24-48 hours
- Double-check DNS records in GoDaddy
- Make sure you saved GitHub Pages custom domain

---

## 📞 Need Help?

Just ask! Tell me:
- What you want to change
- What's not working
- What new section you want to add

I'll give you the exact code and line numbers to edit.

---

## 🎯 Next Steps After Launch

1. Test form submissions
2. Monitor site speed at https://pagespeed.web.dev
3. Set up Google Analytics (if desired)
4. Share your new site!
5. Keep README.md for future reference

**Your site is production-ready and cost: $0!** 🎉
