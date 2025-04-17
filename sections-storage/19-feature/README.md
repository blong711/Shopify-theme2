# Feature Section

This Liquid corresponds to this HTML.

Path to HTML: shopify-theme2/sections-storage/19-feature/feature.html
Path to Liquid: shopify-theme2/sections-storage/19-feature/feature.liquid

## Description
A featured products section for the homepage that displays products in a responsive Swiper slider. The section includes product cards with hover effects, color swatches, and quick action buttons (add to cart, wishlist, quick view, compare).

## Transformation Details

### Static Content to Dynamic Settings
- Button text "Featured Products" → `{{ section.settings.button_text }}`
- Heading text → `{{ section.settings.heading }}` with [br] tag support
- Product information → Block-based settings for each product

### Product Cards
- Each product card is now a block in the section schema
- Product images use Shopify's image_url filter
- Added width and height attributes to images for better performance
- Sale badges are optional and controlled via block settings
- Color swatches are configurable through an array setting

### Slider Configuration
- Maintained original Swiper.js configuration
- Responsive breakpoints preserved
- Added unique class names to prevent conflicts
- Navigation and pagination elements properly connected

### Improvements
1. Added lazy loading for better performance
2. Implemented proper Shopify translations
3. Added product picker in schema for easy product selection
4. Made color swatches fully customizable
5. Added proper alt text for accessibility

### Required Assets
- swiper-bundle.min.css
- swiper-bundle.min.js

Note: These assets need to be added to the theme's assets directory. 