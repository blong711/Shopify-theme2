## Prompt: Convert Style Assets to Shopify-Compatible Format

**Source Directory:** `/home/ryotaru/Shopify-theme2/vineta`  
**Objective:** Convert all CSS and style assets from the HTML theme into a Shopify-compatible format.

### Tasks:

1. **CSS Consolidation:**
   - Locate all CSS files, inline styles, and embedded `<style>` tags from the HTML theme.
   - Combine them into a single CSS file named `styles.css`.

2. **File Placement:**
   - Move `styles.css` to the `assets/` directory of the Shopify theme.

3. **Asset References:**
   - Update all paths inside `styles.css` to use Shopify’s asset filter:
     - Replace references like `url('images/bg.jpg')` with `url({{ 'bg.jpg' | asset_url }})` if used in `.liquid` files.
     - For plain CSS files, ensure paths are relative to the `assets/` folder.

4. **Fonts & Icons:**
   - Move all font files (e.g., `.woff`, `.ttf`) and icon files (e.g., `.svg`, `.png`) to the `assets/` folder.
   - Update font-face and image URLs in `styles.css` accordingly.

5. **JavaScript:**
   - This task does not include JS migration, only style-related files. Leave JS assets untouched unless they directly affect CSS (e.g., dynamic theme switching).

### Output:
- One consolidated file: `assets/styles.css`
- All related images and fonts relocated to `assets/`, with updated paths.

