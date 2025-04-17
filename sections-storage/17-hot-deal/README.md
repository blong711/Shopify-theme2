# Hot Deals Section

This Liquid corresponds to this HTML.

**Path to HTML**: shopify-theme2/sections-storage/17-hot-deal/hot-deal.html
**Path to Liquid**: shopify-theme2/sections-storage/17-hot-deal/hot-deal.liquid

## Description
A featured products section showcasing time-sensitive deals with countdown timers, product variants, and inventory status. This section is typically used on the homepage to create urgency and highlight special offers.

## Transformation Details

### HTML to Liquid Conversion
1. Static content converted to dynamic settings:
   - Section title and description → `{{ section.settings.title }}` and `{{ section.settings.description }}`
   - Background and spacing classes → Dynamic settings with options
   - Section countdown timer → Configurable timer with labels

2. Product cards converted to blocks:
   - Each product card is a block with extensive configuration options
   - Images use Shopify's image_url filter with proper width/height attributes
   - Prices use Shopify's money filter
   - Color swatches made dynamic through block settings
   - Individual product countdowns configurable per block

3. Enhanced features:
   - Progress bars with customizable colors and percentages
   - Available quantity display with color options
   - Sale badges with configurable text
   - Product variant swatches with images

4. Interactive elements:
   - Maintained Swiper slider configuration
   - Added proper Shopify attributes for theme editor
   - Added translation support for action buttons

### Schema Additions
1. Section Settings:
   - Title and description customization
   - Spacing and background color options
   - Section-wide countdown configuration
   
2. Block Settings (Product):
   - Product details (title, URL, images, prices)
   - Sale badge configuration
   - Individual countdown settings
   - Color swatch options
   - Progress bar customization
   - Inventory display options

3. Presets:
   - Default configuration with 4 product blocks
   - Pre-configured section countdown
   - Default text and styling options

### Assumptions
1. Required CSS classes are available in the theme:
   - Layout classes (card-product, style-center)
   - Animation classes (wow, fadeInUp)
   - Utility classes for colors and spacing
2. JavaScript dependencies are included:
   - Swiper slider
   - Countdown timer functionality
   - Bootstrap components (modal, offcanvas)
3. Icon font is included for product action buttons
4. Translation files will be updated for product action buttons

### Notes
The section requires the following translations to be added to the locale files:
- products.product.add_to_cart
- products.product.add_to_wishlist
- products.product.quick_view
- products.product.add_to_compare 