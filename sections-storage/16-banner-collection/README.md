# Banner Collection Section

This Liquid corresponds to this HTML.

**Path to HTML**: shopify-theme2/sections-storage/16-banner-collection/banner-collection.html
**Path to Liquid**: shopify-theme2/sections-storage/16-banner-collection/banner-collection.liquid

## Description
A promotional banner section featuring a two-column layout with an image and content. This section is typically used to highlight specific collections or product categories with a compelling visual and call-to-action.

## Transformation Details

### HTML to Liquid Conversion
1. Static content converted to dynamic settings:
   - Banner image → `{{ section.settings.banner_image | image_url }}`
   - Title and subtitle → `{{ section.settings.title }}` and `{{ section.settings.subtitle }}`
   - Button text and URL → `{{ section.settings.button_text }}` and `{{ section.settings.button_url }}`

2. Image handling enhanced:
   - Added proper alt text handling
   - Added width and height attributes for better performance
   - Maintained lazyload functionality

3. Layout and styling:
   - Made spacing configurable through settings
   - Added banner style options
   - Preserved animation classes (wow, fadeInUp)

### Schema Additions
1. Image Settings:
   - Banner image picker
   - Alt text handling
   
2. Content Settings:
   - Title and subtitle fields
   - Button configuration (text, URL, visibility)
   
3. Style Settings:
   - Section spacing options
   - Banner style variants

4. Presets:
   - Default configuration with sample content
   - Pre-configured button settings

### Assumptions
1. Required CSS classes are available in the theme:
   - Layout classes (tf-grid-layout, tf-col-2)
   - Animation classes (wow, fadeInUp)
   - Button classes (tf-btn, btn-dark2, animate-btn)
2. Icon font is included for the arrow icon
3. Wow.js is included for animations 