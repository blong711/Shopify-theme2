# Limited Deals Section

This Liquid corresponds to this HTML.

Path to HTML: shopify-theme2/sections-storage/24-limited-deals/limited-deals.html
Path to Liquid: shopify-theme2/sections-storage/24-limited-deals/limited-deals.liquid

## Description
This section displays a collection of products with limited-time deals in a responsive slider. It's designed for the homepage to showcase discounted or special-offer products.

## HTML to Liquid Conversion Details

### Static Text → Dynamic Settings
- Title: Converted to `{{ section.settings.title }}`
- Description: Converted to `{{ section.settings.description }}`
- Sale badge text: Converted to `{{ block.settings.sale_badge_text }}`

### Static Images → Dynamic Images
- Product images: Converted to use Shopify's image_url filter
- Hover images: Made optional through block settings
- Color swatch images: Converted to use Shopify's image_url filter

### Added Features
1. Product Selection: Added ability to select products from Shopify store
2. Customizable Padding: Added top and bottom padding controls
3. Flexible Badges: Made sale badges optional and customizable
4. Size Options: Added toggle for size display with customizable sizes
5. Color Swatches: Added support for product color variations
6. Translation Support: Added translation keys for buttons and tooltips

### Schema Settings
- Title and description text
- Section padding controls
- Product selection
- Hover image selection
- Sale badge options
- Size display options
- Color swatch options

### Blocks
- Product blocks for adding multiple products
- Each block has settings for:
  - Product selection
  - Hover image
  - Sale badge
  - Sizes
  - Color swatches

### Presets
- Default configuration with 4 product blocks
- All settings have sensible defaults 