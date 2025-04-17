# Top Picks Section

This Liquid corresponds to this HTML.

**Path to HTML**: shopify-theme2/sections-storage/15-top-pick/top-pick.html
**Path to Liquid**: shopify-theme2/sections-storage/15-top-pick/top-pick.liquid

## Description
A featured products section that displays top-selling or curated products in a responsive slider format. This section is typically used on the homepage to showcase popular or trending products with rich product cards that include images, color variants, pricing, and quick action buttons.

## Transformation Details

### HTML to Liquid Conversion
1. Static content converted to dynamic settings:
   - Section title and description → `{{ section.settings.title }}` and `{{ section.settings.description }}`
   - Background and spacing classes → Dynamic settings with options
   - "View all" link → Configurable URL and text with toggle option

2. Product cards converted to blocks:
   - Each product card is now a block with configurable settings
   - Images use Shopify's image_url filter with proper width/height attributes
   - Prices use Shopify's money filter
   - Color swatches made dynamic through block settings

3. Interactive elements enhanced:
   - Added proper Shopify attributes for theme editor
   - Maintained Swiper slider configuration
   - Added translation support for button labels

### Schema Additions
1. Section Settings:
   - Title and description customization
   - Spacing and background color options
   - View all link configuration
   
2. Block Settings (Product):
   - Product details (title, URL, price)
   - Image settings (main and hover images)
   - Sale and trending badge options
   - Color swatch configuration

3. Presets:
   - Default configuration with 4 product blocks
   - Pre-configured section title and description

### Assumptions
1. Required CSS classes are available in the theme
2. Swiper slider JS is included in the theme
3. Icon font/library is already included
4. Bootstrap modal and offcanvas components are available
5. Translation files will be updated for product action buttons

### Notes
The section requires the following translations to be added to the locale files:
- products.product.add_to_cart
- products.product.add_to_wishlist
- products.product.quick_view
- products.product.add_to_compare 