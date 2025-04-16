# Today's Picks Section

This section displays a carousel of featured products from a selected collection, showcasing them as "Today's Picks".

## Features

- Responsive product carousel with Swiper.js
- Product cards with images, titles, prices, and actions
- Quick view, add to cart, and wishlist functionality
- Sale price display when applicable
- Category links
- Wow.js animations
- Lazy loading for images

## Schema Settings

1. **Section Title**
   - Type: Text
   - Default: "Today's Picks"
   - Description: The main heading for the section

2. **Collection**
   - Type: Collection Picker
   - Description: Select the collection to display products from

3. **Number of Products**
   - Type: Range
   - Min: 4
   - Max: 12
   - Default: 8
   - Description: Set how many products to display in the carousel

## Swiper Configuration

The section uses Swiper.js with the following settings:

- Initial slides per view: 2
- Space between slides: 12px
- Navigation arrows and pagination dots
- Responsive breakpoints:
  - 768px: 3 slides
  - 1200px: 4 slides

## Product Card Features

Each product card includes:
- Product image with lazy loading
- Product title
- Category link
- Price (with sale price if applicable)
- Action buttons:
  - Wishlist
  - Add to cart
  - Quick view

## Usage

1. Add the section to your theme
2. Configure the section title
3. Select a collection to display products from
4. Set the number of products to show
5. Products will be displayed in a responsive carousel

## Dependencies

- Swiper.js (for carousel)
- Wow.js (for animations)
- Lazy loading for images
- Shopify's cart functionality
- Wishlist functionality (requires additional implementation)

## Notes

- The section is fully responsive
- Images are lazy loaded for better performance
- Product prices are formatted using Shopify's money filter
- Sale prices are automatically detected and displayed
- The first collection of each product is used for the category link
- Add to cart functionality uses Shopify's cart API 