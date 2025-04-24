# Tab Product Section

This Liquid corresponds to this HTML.

Path to HTML: sections-storage/29-tab-product/tab-product.html
Path to Liquid: sections-storage/29-tab-product/tab-product.liquid

## Description
The Tab Product section displays products in a tabbed interface, allowing users to switch between different product collections. It's typically used on the homepage to showcase featured products, best sellers, and new arrivals.

## Conversion Details

### HTML to Liquid Transformations:
1. Static tabs → Dynamic tabs using `{% for block in section.blocks %}`
2. Static product data → Dynamic product data using Shopify's product object
3. Static images → Dynamic images using `{{ product.featured_image | image_url }}`
4. Static prices → Dynamic prices using `{{ product.price | money }}`
5. Added width and height attributes to img tags as per requirements
6. Implemented dynamic sale percentage calculation
7. Added support for hover images using product's second image

### Schema Implementation:
- Created a block-based schema for tabs
- Each tab block contains:
  - Tab title
  - Tab ID (for navigation)
  - Collection picker
  - Products limit setting
- Added presets with default tab titles matching the original HTML

### Simplifications/Assumptions:
- Maintained the original slider configuration
- Kept the same number of default tabs (3) in the presets
- Preserved all product card functionality (add to cart, wishlist, quick view, compare)
- Maintained the same styling and layout structure
- Implemented dynamic sale badge calculation
- Added support for hover images using product's second image 