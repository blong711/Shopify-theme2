# Banner Section

This Liquid corresponds to this HTML.

Path to HTML: shopify-theme2/sections-storage/20-banner/banner.html
Path to Liquid: shopify-theme2/sections-storage/20-banner/banner.liquid

## Description
A responsive banner slider section that showcases promotional content with images, text, and call-to-action buttons. The section uses Swiper.js for smooth sliding functionality and is fully responsive, showing one slide on mobile and two slides on larger screens.

## Transformation Details

### Static Content to Dynamic Settings
- Banner images → `{{ block.settings.banner_image | image_url }}`
- Headings and subtext → Block-based settings
- Button text and URLs → Configurable through block settings

### Banner Structure
- Each banner is now a block in the section schema
- Added proper image dimensions and lazy loading
- Maintained hover effects and styling
- Preserved responsive behavior

### Slider Configuration
- Maintained original Swiper.js configuration
- Responsive breakpoints preserved:
  - Mobile: 1 slide
  - Tablet (768px+): 2 slides
  - Desktop (1200px+): 2 slides with increased spacing
- Added navigation and pagination controls

### Improvements
1. Added proper image dimensions for better performance
2. Implemented lazy loading for images
3. Made all content customizable through theme editor
4. Added proper alt text for accessibility
5. Maintained original animations and hover effects

### Required Assets
- swiper-bundle.min.css
- swiper-bundle.min.js

Note: These assets need to be added to the theme's assets directory. 