# Banner Tagline Section

This Liquid corresponds to this HTML.

Path to HTML: shopify-theme2/sections-storage/26-banner-tagline/banner-tagline.html
Path to Liquid: shopify-theme2/sections-storage/26-banner-tagline/banner-tagline.liquid

## Description
This section displays a banner with a tagline and feature list, typically used on the homepage to highlight key selling points of the product or service. It includes a background image, a main title, and a list of features with icons.

## HTML to Liquid Conversion Details

### Static Text → Dynamic Content
- Main title converted to `{{ section.settings.title }}`
- Feature headings converted to `{{ block.settings.heading }}`
- Feature descriptions converted to `{{ block.settings.text }}`

### Static Images → Dynamic Images
- Background image converted to `{{ section.settings.image | image_url }}`
- Added width and height attributes for better performance
- Added alt text handling with `{{ section.settings.image.alt | escape }}`

### Blocks Implementation
- Converted static feature list to dynamic blocks
- Each feature is now customizable through the theme editor
- Added `block.shopify_attributes` for proper block identification

### Schema Implementation
- Added settings for background image and main title
- Created a block type for features with settings for:
  - Icon class
  - Heading
  - Description text
- Included presets with default content matching the original HTML

### Simplifications
- Maintained original class structure for styling
- Kept the same HTML structure for consistency
- Preserved animation classes (wow fadeInUp) 