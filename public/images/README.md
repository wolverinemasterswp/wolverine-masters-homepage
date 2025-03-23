# Image Assets Guide

This directory is for storing website images. Here's how to use them:

## Adding Images

1. Upload your image files to this directory
2. For organization, consider creating subdirectories for different categories:
   - `team/` - Team photos
   - `events/` - Event photos
   - `facility/` - Facility/pool photos

## Using Images in Pages

Reference images in your `.astro` files by using the path from the root:

```html
<!-- Basic image -->
<img src="/images/team-photo.jpg" alt="Team photo" />

<!-- With additional attributes -->
<img 
  src="/images/team-photo.jpg" 
  alt="Team photo" 
  width="600" 
  height="400"
  loading="lazy" 
  class="team-image"
/>
```

## Image Best Practices

1. **Optimize before uploading**: Use tools like [TinyPNG](https://tinypng.com/) or [Squoosh](https://squoosh.app/) to compress images
2. **Use descriptive filenames**: `2023-team-nationals.jpg` is better than `IMG_12345.jpg`
3. **Always include alt text**: For accessibility and SEO
4. **Consider responsive images**: Use different sizes for different devices
5. **Add lazy loading**: Add `loading="lazy"` for images below the fold

## Image Dimensions

For the image sections on the about and join pages:
- Width: The containers are set to max-width 600px
- Height: Set to 400px with object-fit: cover
- Recommended upload size: 1200px wide (2x for high-res displays) 