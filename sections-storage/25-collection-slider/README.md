# Collection Slider Section

This Liquid corresponds to this HTML.

Path to HTML: shopify-theme2/sections-storage/25-collection-slider/collection-slider.html
Path to Liquid: shopify-theme2/sections-storage/25-collection-slider/collection-slider.liquid

## Description
This section creates a responsive slider showcasing collections with images and call-to-action buttons. It's designed for the homepage to highlight different product categories or collections.

## HTML to Liquid Conversion Details

### Static to Dynamic Changes:
1. Images:
   - Original: `<img src="images/slider/fashion/slider-fashion-2-1.png">`
   - Converted: `{{ block.settings.image | image_url }}`
   - Added width and height attributes for better performance
   - Added placeholder for when no image is selected

2. Button Text:
   - Original: Hardcoded text like "Shop Men", "Shop Women", "Shop Kid"
   - Converted: `{{ block.settings.button_text }}`

3. Button Links:
   - Original: Hardcoded `shop-default.html`
   - Converted: `{{ block.settings.button_link }}`

### Added Features:
1. Responsive Settings:
   - Added controls for slides per view on desktop, tablet, and mobile
   - Added spacing controls between slides
   - Added margin bottom control

2. Block System:
   - Converted static slides to dynamic blocks
   - Added limit of 5 slides
   - Each block has image, button text, and link settings

3. Presets:
   - Added default preset with 3 slides
   - Makes it easy to add the section with default content

### Technical Notes:
- Uses Swiper.js for slider functionality
- Maintains original CSS classes for styling
- Added Shopify attributes for proper block handling
- Includes responsive breakpoints for different screen sizes 