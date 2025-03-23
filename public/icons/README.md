# Favicon Guide

This directory is for storing favicon files for the website. Here's how to create and implement favicons:

## Complete Favicon Setup

For the best cross-browser support, you'll want to create multiple favicon formats:

1. **favicon.ico** - 16x16, 32x32, 48x48 pixels (multi-size ICO file)
2. **favicon.svg** - Vector format for modern browsers
3. **favicon-16x16.png** - 16x16 pixel PNG
4. **favicon-32x32.png** - 32x32 pixel PNG
5. **apple-touch-icon.png** - 180x180 pixel PNG for iOS devices
6. **android-chrome-192x192.png** - 192x192 pixel PNG for Android
7. **android-chrome-512x512.png** - 512x512 pixel PNG for Android

## Creating Favicon Files

### Option 1: Online Favicon Generator (Recommended)

1. Create your logo/icon as a high-resolution square image
2. Visit [Real Favicon Generator](https://realfavicongenerator.net/)
3. Upload your image
4. Configure settings for each platform
5. Download the package
6. Place all files in this `/public/icons/` directory

### Option 2: Manual Creation

If you prefer to create the files yourself:

1. Start with a square SVG or high-resolution image
2. Use a tool like Inkscape, Adobe Illustrator, or Photoshop
3. Export in the various formats and sizes listed above
4. Place the files in this directory

## Implementing Favicons

The `BaseLayout.astro` file already includes references to favicon files. Once you've added your custom favicon files, uncomment the relevant lines in the head section:

```html
<link rel="icon" href="/favicon.svg" type="image/svg+xml" />
<link rel="icon" href="/icons/favicon.svg" type="image/svg+xml" />
<link rel="apple-touch-icon" sizes="180x180" href="/icons/apple-touch-icon.png" />
<link rel="icon" type="image/png" sizes="32x32" href="/icons/favicon-32x32.png" />
<link rel="icon" type="image/png" sizes="16x16" href="/icons/favicon-16x16.png" />
```

For a complete implementation, you might want to add a webmanifest file and more, which the Real Favicon Generator will provide. 