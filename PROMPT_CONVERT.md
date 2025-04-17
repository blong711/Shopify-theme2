# 🧩 Prompt for Cursor AI: Convert New Sections from HTML to Shopify Liquid

Convert **only new sections** from the HTML file `vineta/home-fashion-women.html` into Shopify Liquid, and document each conversion clearly.

---

## 📂 Folder Structure

For each **new** section, create a folder in:

shopify-theme2/sections-storage/[order]-[section-name]

Example:  
shopify-theme2/sections-storage/01-hero

Inside each folder, include the following files:

### 1. `[section-name].html`

- The raw HTML of the **new** section from `home-fashion-women.html`.
- Section has in HTML:
 - Top Bar(already converted): Line 50-162
 - Header(already converted): Line 163-1082
 - Slider(already converted): Line 1083-1201
 - Collection(already converted): Line 1202-1276
 - Top Sellers tab: Line 1277-3120
 - Banner with text: Line 3121-3168
 - Testimonial(already converted): Line 3169-3262
 - Brand(already converted): Line 3263-3322
 - Shop Gram(already converted): Line 3323-3413
 - Icon box(already converted): Line 3414-3480
 - Footer(already converted): Line 3481-3682

### 2. `[section-name].liquid`

- The Shopify Liquid version of the HTML.
- Follow Shopify section conventions:
  - Use `{% schema %}` for editable settings.
  - Use `section.settings` and `section.blocks` where appropriate.
  - Skip `{% style %}` unless absolutely required.

### 3. `README.md`

Document the conversion. Each README must include:

- The sentence:  
  **“This Liquid corresponds to this HTML.”**
- Paths to both files. Example:  
Path to HTML: shopify-theme2/sections-storage/01-hero/hero.html
Path to Liquid: shopify-theme2/sections-storage/01-hero/hero.liquid

- Description of what the section does and where it belongs (e.g., homepage, landing page).
- How the HTML was transformed into Liquid:
- Static text → `{{ settings.title }}`
- Static images → `{{ settings.image | image_url }}`
- Any simplifications or assumptions applied during conversion.

---

## ⛔ Skip Existing Sections

- Check the folders already in `shopify-theme2/sections-storage/`.
- Only convert **new** or **modified** sections from `vineta/home-fashion-women.html`.
- **Do not** duplicate sections that already exist.

---

## 🧱 When Using Blocks

If the section includes repeated elements (e.g., slides, testimonials, feature cards):

- Use `blocks` in the schema.
- Render using a `for` loop:

```liquid
{% for block in section.blocks %}
  {{ block.settings.[setting_name] }}
{% endfor %}
Use {{ block.shopify_attributes }}.

Include a presets array in the schema with default block content.

✅ Best Practices
Keep code clean, modular, and well-commented.

Use consistent, descriptive names for settings:

settings.title

settings.text

settings.button_url

block.settings.image

Maintain consistent folder and file naming.

Ensure README.md is comprehensive and helpful for future developers.

Repeat this process for every new section in vineta/home-fahsion-women.html.

This will ensure your Shopify theme remains modular, editable in the theme editor, and well-documented for long-term maintainability.