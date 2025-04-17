# Latest Tips & Trends Section

**This Liquid corresponds to this HTML.**

Path to HTML: shopify-theme2/sections-storage/18-latest-tip/latest-tip.html
Path to Liquid: shopify-theme2/sections-storage/18-latest-tip/latest-tip.liquid

## Description
This section displays the latest blog posts in a responsive swiper slider format, intended for the homepage. It showcases recent tips, trends, and updates from the store's blog with a modern and engaging layout.

## HTML to Liquid Transformation

### Static Content Converted to Dynamic Settings
- Section title "Latest Tips & Trends" → `{{ section.settings.title }}`
- Description text → `{{ section.settings.description }}`
- Blog post image → `{{ article.image | img_url: 'master' }}`
- Blog post title → `{{ article.title }}`
- Blog post URL → `{{ article.url }}`

### Key Changes Made
1. Added schema settings for:
   - Customizable section title
   - Customizable description
   - Number of posts to display (3-12)
   - Blog selection option

2. Implemented dynamic blog post loop:
   - Replaced static blog post with `{% for article in blog.articles limit: section.settings.posts_limit %}`
   - Added proper image attributes (width, height, loading="lazy")
   - Maintained original swiper configuration for responsive design

3. Preserved original CSS classes and structure for consistent styling

### Assumptions
- The store has at least one blog set up
- Blog posts have featured images
- Maintained original swiper.js configuration for optimal responsive behavior 