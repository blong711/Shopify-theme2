# Gear Up Section

This Liquid corresponds to this HTML.

Path to HTML: shopify-theme2/sections-storage/21-gear-up/gear-up.html
Path to Liquid: shopify-theme2/sections-storage/21-gear-up/gear-up.liquid

## Description
A product showcase section featuring cycling gear and equipment in a responsive slider format. The section includes product cards with advanced features like color swatches, countdown timers, and quick action buttons.

## Transformation Details

### Static Content to Dynamic Settings
- Button text "Gear Up" → `{{ section.settings.button_text }}`
- Heading text → `{{ section.settings.heading }}` with [br] tag support
- Product information → Block-based settings for each product

### Product Cards
- Each product card is now a block in the section schema
- Product images use Shopify's image_url filter
- Added width and height attributes to images
- Sale badges and countdown timers are optional
- Color swatches are fully configurable

### Slider Configuration
- Maintained original Swiper.js configuration
- Responsive breakpoints:
  - Mobile: 2 slides
  - Tablet (768px+): 3 slides
  - Desktop (1200px+): 4 slides
- Added unique class names to prevent conflicts
- Navigation and pagination elements properly connected

### Special Features
1. Countdown Timer
   - Optional per product
   - Configurable duration
   - Maintains original styling

2. Color Swatches
   - Dynamic color variants
   - Custom color values
   - Variant-specific images
   - Hover states preserved

### Improvements
1. Added lazy loading for better performance
2. Implemented proper Shopify translations
3. Added product picker in schema
4. Made countdown timer optional and configurable
5. Added proper alt text for accessibility

### Required Assets
- swiper-bundle.min.css
- swiper-bundle.min.js

Note: These assets need to be added to the theme's assets directory. 