# Hero Slider Section

This section implements a full-width hero slider with customizable slides, featuring images, headings, subheadings, and call-to-action buttons.

## Features

- Responsive slider with fade effect
- Customizable slides with images and text content
- Configurable autoplay and transition settings
- Mobile-friendly design
- Lazy loading for images
- Pagination dots for navigation

## Usage

1. Add the section to your theme
2. Configure the global slider settings:
   - Enable/disable autoplay
   - Enable/disable loop
   - Set transition speed
3. Add slides using the block system:
   - Upload slide images
   - Add headings and subheadings
   - Set button text and links

## Schema Settings

### Global Settings
- `autoplay`: Enable/disable automatic slide transitions
- `loop`: Enable/disable continuous looping
- `speed`: Transition speed in milliseconds (100-2000ms)

### Slide Block Settings
- `image`: Slide background image
- `heading`: Main heading text
- `subheading`: Supporting text
- `button_text`: Call-to-action button text
- `button_link`: Button destination URL

## Customization

The slider uses the following CSS classes for styling:
- `tf-slideshow`: Main slider container
- `slider-wrap`: Individual slide wrapper
- `bg-type-{n}`: Background type class (1-3)
- `fade-item`: Animation classes for content elements
- `tf-btn`: Button styling

## Dependencies

- Swiper.js for slider functionality
- Theme's base CSS for styling
- Font Awesome for icons

## Notes

- Images should be optimized for web use
- Recommended image dimensions: 1920x800px
- Text content should be concise for mobile viewing 