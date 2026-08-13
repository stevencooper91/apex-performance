# Logo Integration Guide

## 📸 Your Logo Files

You've uploaded two logo files:
1. **ChatGPT_Image_Dec_2__2025__11_28_46_AM.png** - Multiple color variations
2. **Screenshot_2025-10-09_at_17_00_35.png** - Black logo on white background

## 🎨 Which Logo to Use Where

### For Navigation Bar (Dark Background)
**Use: WHITE logo version**
- Background color: Dark (#1a1a1a)
- Logo should be: White version from your multi-color file
- File to extract: Top-right OR bottom-left version (white logo on dark background)

**Where in code**: LINE 259
```html
<img src="logo-white.png" alt="Apex Performance Logo">
```

### For Footer (Dark Background)
**Use: WHITE logo version** (same as navigation)
- Background color: Dark (#1a1a1a)
- Logo should be: White version

**Where in code**: LINE 570
```html
<img src="logo-white.png" alt="Apex Performance">
```

### Optional: Favicon (Browser Tab Icon)
**Use: Simple black mountain icon**
- Extract just the mountain symbol from your logo
- Save as 32x32 pixels
- Save as `favicon.ico` or `favicon.png`

**Add after LINE 7**:
```html
<link rel="icon" type="image/png" href="favicon.png">
```

## 🔧 How to Extract the Right Logo Version

### Option 1: Use Your Original Design File
If you have the original design files (AI, PSD, Figma), export:
- White logo on transparent background → `logo-white.png`
- Black logo on transparent background → `logo-black.png` (optional)

### Option 2: Extract from Your Uploaded File
From `ChatGPT_Image_Dec_2__2025__11_28_46_AM.png`:

**For white logo:**
1. Crop the top-right section (dark background with white logo)
2. Or crop bottom-left section
3. Make background transparent if possible
4. Save as `logo-white.png`

Recommended size: 200-300px wide, maintaining aspect ratio

## 📐 Recommended Logo Dimensions

For best quality on all devices:
- **Width**: 200-300px
- **Height**: Let it scale proportionally (should be ~80-120px)
- **Format**: PNG with transparent background (best)
- **File size**: Try to keep under 50KB

## 🖼️ Files You Need to Create

Based on your uploads, create these files:

```
📁 Your Website Folder
├── index.html
├── logo-white.png         ← Extract white version from your multi-color file
├── hero-mountain.png      ← Use the standalone mountain icon OR create a hero visual
├── about-image.jpg        ← Add later (placeholder for now)
└── favicon.png            ← Optional: Small icon for browser tab
```

## 🎨 Your Brand Colors (From Logo)

I've already integrated these into the CSS:

```css
--apex-black: #1a1a1a;     ✓ Used for text and dark sections
--apex-white: #ffffff;      ✓ Used for light backgrounds
--apex-yellow: #FFD700;     ✓ Used for accents and highlights
--apex-blue: #2B4B8C;       ✓ Used for secondary accents
```

These match your logo perfectly!

## 🚀 Quick Setup Steps

1. **Extract white logo:**
   - Open `ChatGPT_Image_Dec_2__2025__11_28_46_AM.png`
   - Crop the section with white logo on dark background
   - Save as `logo-white.png`

2. **Create hero image (optional):**
   - Use your black mountain icon
   - Or create a larger graphic with the mountain
   - Save as `hero-mountain.png`

3. **Place in folder:**
   - Put logo files in same folder as `index.html`

4. **Test:**
   - Open `index.html` in browser
   - Check if logos appear correctly

## 💡 Pro Tips

### Logo Not Showing?
Check these common issues:
- File name matches exactly: `logo-white.png` (case-sensitive!)
- File is in same folder as `index.html`
- PNG format with transparent background works best

### Logo Too Big/Small?
**Change LINE 242-245** in CSS:
```css
.logo img {
    height: 50px;  /* Increase/decrease this number */
    width: auto;
}
```

### Logo Quality Poor?
- Use a larger source image (300px+ wide)
- Export at 2x size for retina displays
- Use PNG format, not JPG

## 🎯 Alternative: Use Your Existing Files

### If you want to use your files AS-IS:

**Option A: Use the multi-color logo file**
```html
<!-- Change LINE 259 to: -->
<img src="ChatGPT_Image_Dec_2__2025__11_28_46_AM.png" alt="Apex Performance Logo">
```
Note: This will show all 4 color variations. Better to extract just the white one.

**Option B: Use the black logo file**
```html
<!-- Change LINE 259 to: -->
<img src="Screenshot_2025-10-09_at_17_00_35.png" alt="Apex Performance Logo">
```
Note: Black logo won't show well on dark navigation bar. Only use if you change nav background to light.

## ✅ Recommended Workflow

1. ✅ Use your multi-color file to extract WHITE logo → save as `logo-white.png`
2. ✅ Place in same folder as index.html
3. ✅ Keep filenames simple: `logo-white.png` not `ChatGPT_Image_Dec_2...`
4. ✅ Test in browser
5. ✅ Deploy!

---

**Need help extracting the logo?** 
Let me know and I can guide you through it or provide specific instructions for your image editing software!
