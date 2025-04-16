# Collection Slider Section

This section implements a responsive collection slider that showcases different product categories with images and call-to-action buttons.

## Features

- Responsive slider with customizable breakpoints
- Collection images with hover effects
- Call-to-action buttons for each collection
- Mobile-friendly design with pagination dots
- Desktop navigation arrows
- Configurable transition speed
- Lazy loading for images

## Usage

1. Add the section to your theme
2. Configure the global slider settings:
   - Set transition speed
3. Add collections using the block system:
   - Upload collection images
   - Set collection titles
   - Add collection links

## Schema Settings

### Global Settings
- `speed`: Transition speed in milliseconds (100-2000ms)

### Collection Block Settings
- `image`: Collection background image
- `title`: Collection title text
- `link`: Collection destination URL

## Customization

The slider uses the following CSS classes for styling:
- `tf-swiper`: Main slider container
- `wg-cls`: Collection item wrapper
- `style-abs`: Absolute positioning for content
- `asp-1`: Aspect ratio class
- `hover-img`: Hover effect class
- `btn-cls`: Button styling
- `hover-dark`: Dark hover effect
- `hover-icon-2`: Icon hover animation

## Responsive Breakpoints

The slider automatically adjusts based on screen size:
- Mobile (< 575px): 1 slide
- Tablet (575px - 768px): 2 slides
- Desktop (768px - 1200px): 3 slides
- Large Desktop (> 1200px): 3 slides with increased spacing

## Dependencies

- Swiper.js for slider functionality
- Theme's base CSS for styling
- Font Awesome for icons

## Notes

- Images should be optimized for web use
- Recommended image dimensions: 800x1000px
- Collection titles should be concise for mobile viewing
- Ensure collection links are properly set up in Shopify 