# Static Assets Directory

This directory contains static assets for the Wolverine Masters Water Polo Club website.

## Directory Structure

- `/public` - Root directory for all static assets (directly accessible at the site root)
  - `/images` - Store site images here
  - `/icons` - Store icons including favicon variations here
  - `favicon.svg` - Main favicon in SVG format
  - `global.css` - Global CSS styles

## Usage Guide

### Adding Images

1. Place image files in the `/public/images` directory
2. Reference them in your `.astro` files using: 
   ```html
   <img src="/images/your-image-file.jpg" alt="Description" />
   ```

### Using the Favicon

The site is set up to use `/favicon.svg` as the default favicon. To change it:

1. Place your new favicon file in the `/public/icons` directory
2. Update the reference in the BaseLayout.astro file:
   ```html
   <link rel="icon" type="image/png" href="/icons/your-favicon.png" />
   ```

### Favicon Formats

For the best cross-browser compatibility, consider creating multiple favicon formats:

- `favicon.ico` - 16x16, 32x32, 48x48 (ICO format)
- `favicon.svg` - Scalable vector (modern browsers)
- `favicon-16x16.png` - 16x16 PNG
- `favicon-32x32.png` - 32x32 PNG
- `apple-touch-icon.png` - 180x180 PNG (for iOS devices)

You can use a tool like [Favicon Generator](https://realfavicongenerator.net/) to create these files. 