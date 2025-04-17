# Marquee Announcement Section

This Liquid corresponds to this HTML.

**Path to HTML**: shopify-theme2/sections-storage/14-marquee/marquee.html
**Path to Liquid**: shopify-theme2/sections-storage/14-marquee/marquee.liquid

## Description
A marquee announcement section that displays scrolling text and icons, typically used at the top of the homepage to highlight important announcements, sales, or new arrivals.

## Transformation Details

### HTML to Liquid Conversion
1. Static background class converted to dynamic setting:
   - `bg-light-green-2` → `{{ section.settings.background_color }}`

2. Repeated announcement items converted to blocks:
   - Static text items → `{% if block.type == 'text' %}` with `{{ block.settings.text }}`
   - Static icons → `{% if block.type == 'icon' %}` with `{{ block.settings.icon_class }}`

3. Added block attributes for theme editor:
   - Added `{{ block.shopify_attributes }}` to each block item

### Schema Additions
1. Section Settings:
   - Background color selection with preset options
   
2. Block Types:
   - Text blocks for announcement messages
   - Icon blocks for decorative elements

3. Presets:
   - Default configuration with alternating text and icon blocks
   - Pre-configured with "50% Off" and "New Arrival" messages

### Assumptions
1. The original CSS classes are maintained and available in the theme
2. Icon font/library is already included in the theme
3. The marquee animation is handled by existing CSS/JS 