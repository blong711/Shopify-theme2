# Hero Slider Section

A dynamic, customizable hero slider section for Shopify themes. This section allows merchants to showcase their products, collections, or promotional content with beautiful, responsive slides.

## Features

- Fully responsive design
- Support for up to 5 slides
- Customizable content positioning (left, center, right)
- Fade or slide transition effects
- Autoplay with adjustable speed
- Touch-enabled for mobile devices
- Lazy loading images for better performance
- Customizable text and button content for each slide
- Built with Swiper.js for smooth transitions

## Dependencies

- Bootstrap Grid System (for layout)
- Swiper.js (for slider functionality)
- Font Awesome or custom icon set (for arrow icons)

## Section Settings

### Global Settings

| Setting | Type | Description | Default |
|---------|------|-------------|---------|
| Slider Effect | Select | Choose between fade or slide transition | Fade |
| Enable Autoplay | Checkbox | Toggle autoplay functionality | True |
| Autoplay Speed | Range | Set the duration between slides (3-10s) | 5s |

### Slide Block Settings

Each slide can be customized with the following settings:

| Setting | Type | Description | Default |
|---------|------|-------------|---------|
| Image | Image Picker | Upload slide background image | None |
| Heading | Text | Main slide heading | "Style Redefined" |
| Subtext | Textarea | Descriptive text below heading | "Discover the latest..." |
| Button Link | URL | CTA button destination | None |
| Button Text | Text | CTA button label | "Shop Collection" |
| Content Position | Select | Position of text content | Left |

## Usage

1. Add the "Hero Slider" section to your theme from the Theme Editor
2. Configure global settings for the slider behavior
3. Add up to 5 slides using the "Add Block" button
4. For each slide:
   - Upload a high-quality background image (recommended: 1920px wide)
   - Set the heading and subtext
   - Configure the CTA button
   - Choose content positioning

## Best Practices

1. **Images**
   - Use high-resolution images (1920x1080px recommended)
   - Optimize images for web to maintain fast loading times
   - Maintain consistent aspect ratios across slides

2. **Content**
   - Keep headings concise (1-3 words for best impact)
   - Use clear, action-oriented button text
   - Ensure text has sufficient contrast with background images

3. **Performance**
   - Limit the number of slides (3-5 recommended)
   - Use compressed images
   - Take advantage of lazy loading

## Customization

The section includes basic styles that can be customized through the theme's CSS. Key classes:

```css
.slider-fashion-1 /* Main slider container */
.slider-wrap /* Individual slide wrapper */
.box-content /* Content container */
.heading /* Slide heading */
.sub /* Slide subtext */
.tf-btn /* CTA button */
```

## Troubleshooting

1. **Images not loading:**
   - Verify image upload in Theme Editor
   - Check image size and format
   - Ensure proper permissions

2. **Slider not transitioning:**
   - Check if autoplay is enabled
   - Verify Swiper.js is properly loaded
   - Check console for JavaScript errors

3. **Content positioning issues:**
   - Verify Bootstrap grid classes
   - Check responsive breakpoints
   - Inspect content container positioning

## Version History

- 1.0.0: Initial release
- 1.0.1: Added content positioning options
- 1.0.2: Enhanced mobile responsiveness 