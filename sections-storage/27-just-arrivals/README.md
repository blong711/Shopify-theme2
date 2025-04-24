# Just Arrivals Section

This Liquid corresponds to this HTML.

Path to HTML: shopify-theme2/sections-storage/27-just-arrivals/just-arrivals.html
Path to Liquid: shopify-theme2/sections-storage/27-just-arrivals/just-arrivals.liquid

## Description
This section displays a tabbed product showcase, typically used on the homepage to highlight newly arrived products. It includes a title section with tabs for different product categories (iPhone, Android, Personalized) and a swiper carousel for each tab showing product cards with images, prices, and interactive elements.

## HTML to Liquid Conversion Details

### Static Text → Dynamic Content
- Subtitle converted to `{{ section.settings.subtitle }}`
- Main title converted to `{{ section.settings.title }}`
- Tab titles converted to `{{ block.settings.tab_title }}`
- Product titles converted to `{{ product.title }}`
- Prices converted to `{{ product.price | money }}` and `{{ product.compare_at_price | money }}`

### Static Images → Dynamic Images
- Product images converted to `{{ product.featured_image | image_url }}`
- Hover images converted to `{{ product.images[1] | image_url }}`
- Variant images converted to `{{ variant.image | image_url }}`
- Added width and height attributes for better performance
- Added alt text handling with `{{ image.alt | escape }}`

### Blocks Implementation
- Converted static tabs to dynamic blocks
- Each tab is now customizable through the theme editor
- Added `block.shopify_attributes` for proper block identification
- Implemented collection selection for each tab
- Added configurable number of products to show per tab

### Schema Implementation
- Added settings for subtitle and main title
- Created a block type for tabs with settings for:
  - Tab title
  - Tab ID
  - Collection selection
  - Number of products to show
- Included presets with default content matching the original HTML

### Dynamic Features
- Sale percentage calculation
- Variant display for products with multiple variants
- Responsive swiper configuration
- Dynamic tab activation

### Simplifications
- Maintained original class structure for styling
- Kept the same HTML structure for consistency
- Preserved animation classes (wow fadeInUp)
- Maintained all interactive elements (cart, wishlist, quick view, compare) 