# Shop Gram Section

A responsive gallery section that displays Instagram-style product images in a slider format.

## Features

- Responsive slider with configurable slides per view for different screen sizes
- Hover overlay effect with tooltips
- Lazy loading for images
- Animated fade-in effects
- Customizable pagination
- Dynamic content through Shopify blocks

## Settings

### Section Settings

- **Section Title**: Customize the section heading
- **Slider Settings**:
  - Slides per view (Mobile): 1-3 slides
  - Slides per view (Tablet): 2-4 slides
  - Slides per view (Desktop): 3-6 slides
  - Space between slides: 0-30px
  - Show/hide pagination

### Block Settings (Gallery Items)

Each gallery item can be configured with:
- Image
- Product link
- Custom tooltip text

## Usage

1. Add the section to your theme
2. Configure the section settings:
   - Set the section title
   - Adjust slider settings for different screen sizes
   - Toggle pagination visibility
3. Add gallery items:
   - Upload images
   - Set product links
   - Customize tooltip text

## Default Configuration

The section comes with a default preset that includes:
- 5 gallery items
- Mobile: 2 slides per view
- Tablet: 3 slides per view
- Desktop: 5 slides per view
- 10px space between slides
- Pagination enabled

## Styling

The section uses the following classes for styling:
- `flat-spacing-4`: Section spacing
- `wow fadeInUp`: Title animation
- `wow fadeInLeft`: Gallery item animations
- `hover-img hover-overlay`: Hover effects
- `img-style`: Image styling
- `box-icon hover-tooltip`: Tooltip styling

## Dependencies

- Swiper.js for the slider functionality
- WOW.js for animations
- Lazy loading for images 