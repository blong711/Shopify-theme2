# Banner with Text Section

This Liquid corresponds to this HTML.

Path to HTML: shopify-theme2/sections-storage/23-banner-text/banner-text.html
Path to Liquid: shopify-theme2/sections-storage/23-banner-text/banner-text.liquid

## Description

A versatile banner section for the homepage that combines a large banner image with text content and a featured product lookbook. The section includes:
- Full-width banner image
- Featured product overlay with quick view functionality
- Text content with heading and subtext
- Call-to-action button

## Transformation Details

### Static Content → Dynamic Content
- Banner image replaced with customizable image picker
- Static banner link replaced with URL setting
- Featured product replaced with product picker
- Static text content replaced with editable settings
- Button text and link made customizable

### Added Functionality
- Proper image handling with Shopify's image_url filter
- Added width and height attributes to all images for better performance
- Translation support for quick view text
- JavaScript handler for quick view functionality
- Conditional rendering of featured product and button
- Alt text support for better accessibility

### Schema Settings
1. Banner Configuration
   - Banner image upload (1170 x 600px recommended)
   - Banner link URL
   - Featured product selection

2. Content Settings
   - Heading text
   - Subtext content
   - Button label
   - Button link URL

### Customization
The section is fully customizable through the theme editor with:
- Image selection
- Text content editing
- Product selection
- Link configuration
- Button customization

### Notes
- The section maintains the original design's responsive behavior
- Featured product overlay is optional and only shows when a product is selected
- All text content can be edited through the theme editor
- Images include recommended dimensions for optimal display 