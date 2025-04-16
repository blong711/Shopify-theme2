# Prompt for Cursor AI: Convert HTML to Shopify Liquid by Section

Convert a full HTML page into Shopify Liquid, **section by section**, and document each conversion clearly.

## 📂 Folder Structure

For each section, create a folder in `vineta/sections-storage/` named:  
`[order]-[section-name]` (e.g., `01-hero`, `02-features`)

Inside each folder, include:

### 1. `[section-name].html`
- The raw HTML for the section.

### 2. `[section-name].liquid`
- The Shopify Liquid version of the HTML.
- Follow Shopify section conventions:
  - Use `{% schema %}` for editable settings.
  - Use `section.settings` and `section.blocks` properly.
  - Skip `{% style %}` unless required.

### 3. `README.md`
Document the conversion process. Must include:
- The sentence: **“This Liquid corresponds to this HTML.”**
- Paths to both files. Example:  
  `Path to HTML: vineta/sections-storage/01-hero/hero.html`  
  `Path to Liquid: vineta/sections-storage/01-hero/hero.liquid`
- What the section does and where it belongs (e.g., homepage).
- How the HTML was transformed into Liquid (e.g., static text → `{{ settings.title }}`).
- Any logic or simplification applied.

---

## 🧱 When Using Blocks

If the section includes repeated elements (e.g., slides, cards, testimonials):

- Use `blocks` in the schema.
- Render with `{% for block in section.blocks %}`.
- Use `block.settings.[id]` and `{{ block.shopify_attributes }}`.
- Add a `presets` array for default data.

---

## ✅ Guidelines

- Keep code clean and settings well-named (`settings.heading`, `settings.button_link`, etc.).
- Maintain folder and file naming consistency.
- Always include detailed notes in `README.md`.

---

Repeat this for all sections until the entire HTML is converted.

This will keep your Shopify theme modular, editable, and well-documented.
