# Announcement Bar Section

A customizable announcement bar for Shopify themes that allows merchants to display important messages, promotions, or announcements at the top of their store.

## Features

- Multiple announcements with slider functionality
- Customizable colors and styling
- Optional sticky positioning
- Icon support for visual emphasis
- Clickable announcements with custom links
- Responsive design
- Swiper.js integration for smooth transitions

## Dependencies

- Swiper.js (for slider functionality)
- Custom icon set (for announcement icons)

## Section Settings

### Global Settings

| Setting | Type | Description | Default |
|---------|------|-------------|---------|
| Show Announcement | Checkbox | Toggle announcement bar visibility | True |
| Sticky on Scroll | Checkbox | Keep announcement bar at top when scrolling | True |
| Background Color | Color | Set the background color | #000000 |
| Text Color | Color | Set the text color | #FFFFFF |

### Announcement Block Settings

Each announcement can be customized with:

| Setting | Type | Description | Default |
|---------|------|-------------|---------|
| Text | Text | Announcement message | "Free shipping..." |
| Link | URL | Optional click-through link | None |
| Icon | Select | Choose an icon (None/Delivery/Sale/Gift) | Truck |

## Usage

1. Add the "Announcement Bar" section through the Theme Editor
2. Configure global settings for appearance
3. Add announcement blocks for each message
4. For each announcement:
   - Enter the message text
   - Add an optional link
   - Select an icon (if desired)

## Best Practices

1. **Content**
   - Keep messages concise and clear
   - Use action words to encourage engagement
   - Limit the number of announcements (3-4 max)

2. **Design**
   - Ensure sufficient contrast between text and background
   - Choose appropriate icons that match the message
   - Maintain consistent spacing and alignment

3. **Performance**
   - Optimize transitions for smooth sliding
   - Consider mobile viewing experience
   - Test different screen sizes

## Customization

The section includes basic styles that can be customized through the theme's CSS:

```css
.announcement-bar /* Main container */
.announcement-bar__content /* Content wrapper */
.announcement-bar__text /* Message text */
.announcement-bar__icon /* Icon container */
.announcement-bar__link /* Clickable link */
```

## Troubleshooting

1. **Slider not working:**
   - Check Swiper.js integration
   - Verify autoplay settings
   - Check for JavaScript errors

2. **Icons not displaying:**
   - Verify icon font/SVG is loaded
   - Check icon class names
   - Ensure icon library is properly linked

3. **Responsive issues:**
   - Test on multiple devices
   - Check media queries
   - Verify text wrapping

## Version History

- 1.0.0: Initial release
- 1.0.1: Added icon support
- 1.0.2: Enhanced mobile responsiveness
- 1.0.3: Added color customization options 