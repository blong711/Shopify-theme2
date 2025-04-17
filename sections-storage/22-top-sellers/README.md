# Top Sellers Section

This Liquid corresponds to this HTML.

Path to HTML: shopify-theme2/sections-storage/22-top-sellers/top-sellers.html
Path to Liquid: shopify-theme2/sections-storage/22-top-sellers/top-sellers.liquid

## Description

A tabbed product section for the homepage that displays products in three different categories:
- Top Sellers
- On Sale
- Trending

The section features a responsive grid layout that adapts from 2 columns on mobile to 4 columns on desktop. Each product card includes:
- Product images (main + hover)
- Sale badge (if applicable)
- Quick action buttons (cart, wishlist, quick view, compare)
- Size options (if available)
- Color swatches (if available)
- Product title and price

## Transformation Details

### Static Content → Dynamic Content
- Tab titles converted to editable settings in section schema
- Static product cards replaced with dynamic product loop using collection data
- Hard-coded images replaced with `product.featured_image` and `product.images[1]`
- Static prices replaced with `product.price` and `product.compare_at_price`
- Static product URLs replaced with `product.url`
- Static variants replaced with dynamic variant loop

### Added Functionality
- Dynamic sale badge calculation
- Proper handling of product variants (sizes and colors)
- Added width and height attributes to images for better performance
- Translation support for button labels
- JavaScript handlers for cart, wishlist, quick view, and compare actions

### Schema Settings
- Default active tab selection
- Per-tab settings:
  - Tab title
  - Tab ID
  - Collection selection
  - Number of products to display (4-12)

### Customization
The section is highly customizable through the theme editor with:
- 3 preset tabs (Top Sellers, On Sale, Trending)
- Ability to add/remove/reorder tabs
- Collection assignment per tab
- Product limit control per tab 