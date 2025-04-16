# Categories Section

This section displays product categories in a tabbed interface, with separate tabs for Women's and Men's collections. Each tab contains a swiper carousel of category cards.

## Features

- Tabbed interface for Women's and Men's categories
- Swiper carousel for category display
- Responsive design with breakpoints
- Collection images with titles and product counts
- Navigation controls and pagination
- Lazy loading for images
- Wow.js animations

## Schema Settings

1. **Section Title**
   - Type: Text
   - Default: "Categories"
   - Description: The main heading for the section

2. **Women's Tab Text**
   - Type: Text
   - Default: "Womens"
   - Description: The text displayed on the Women's tab

3. **Men's Tab Text**
   - Type: Text
   - Default: "Mens"
   - Description: The text displayed on the Men's tab

4. **Women's Collections**
   - Type: Collection List
   - Limit: 6 collections
   - Description: Select up to 6 collections to display in the Women's tab

5. **Men's Collections**
   - Type: Collection List
   - Limit: 6 collections
   - Description: Select up to 6 collections to display in the Men's tab

## Swiper Configuration

The section uses Swiper.js with the following settings:

- Initial slides per view: 2
- Space between slides: 12px
- Navigation arrows and pagination dots
- Responsive breakpoints:
  - 575px: 3 slides
  - 768px: 4 slides
  - 1200px: 6 slides

## Usage

1. Add the section to your theme
2. Configure the section title and tab texts
3. Select collections for both Women's and Men's tabs
4. Each collection will display:
   - Collection featured image
   - Collection title
   - Number of products in the collection

## Dependencies

- Bootstrap 5 (for tabs)
- Swiper.js (for carousel)
- Wow.js (for animations)
- Lazy loading for images

## Notes

- The section is fully responsive
- Images are lazy loaded for better performance
- Placeholder SVG is shown if a collection has no featured image
- Collection links are automatically generated based on Shopify collection URLs
- Product counts are dynamically pulled from the collections 