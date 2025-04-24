# Grid Collection Section

This Liquid corresponds to this HTML.

Path to HTML: sections-storage/28-grid-collection/grid-collection.html
Path to Liquid: sections-storage/28-grid-collection/grid-collection.liquid

## Description
The Grid Collection section displays a grid of collection items with images and titles. It's typically used on the homepage to showcase different product categories or collections.

## Conversion Details

### HTML to Liquid Transformations:
1. Static text → Dynamic content using `{{ block.settings.title }}`
2. Static images → Dynamic images using `{{ block.settings.image | image_url }}`
3. Static links → Dynamic links using `{{ block.settings.link }}`
4. Added width and height attributes to img tags as per requirements
5. Converted static items to dynamic blocks using `{% for block in section.blocks %}`

### Schema Implementation:
- Created a block-based schema to allow for flexible number of collection items
- Each block contains:
  - Image picker for the collection image
  - Text field for the collection title
  - URL field for the collection link
- Added presets with default content matching the original HTML

### Simplifications/Assumptions:
- Maintained the original grid structure and styling classes
- Kept the same number of default items (4) in the presets
- Preserved the animation classes (wow fadeInUp)
- Maintained the same button styling and icon structure 