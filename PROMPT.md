# Prompt for Cursor AI: Convert HTML to Shopify Liquid by Section

You are tasked with converting an HTML page into Shopify Liquid format, **section by section**.

## 🔧 Instructions:

### 1. Split the HTML into Sections
- Identify and extract each meaningful section of the HTML (e.g., `header`, `hero`, `features`, `testimonials`, `footer`, etc.).
- Treat each of these as a separate component for conversion.

### 2. For Each Section:
Create a new folder in the `sections-storage` directory using the format:  
**`[order]-[section-name]`** (e.g., `01-hero`, `02-features`)

Inside each folder, include the following files:

#### a. `[section-name].html`
- The raw HTML code for the section.
- Example: For a hero section, name it `hero.html`

#### b. `[section-name].liquid`
- The converted Shopify Liquid version of the HTML.
- Example: For a hero section, name it `hero.liquid`
- Follow Shopify's section structure:
  - Use `{% schema %}` to define editable settings (text, images, links, etc.).
  - Add any logic using Liquid syntax.
  - No need to add {% style %}.

#### c. `README.md`
- A markdown file to track:
  - Source of the HTML (file path and line numbers)
  - Where the section is used in the theme
  - Relationship between the HTML and Liquid versions
  - Any dependencies or related components

#### d. `url.md`
- A markdown file to track the source of the HTML:
  - Original template URL or marketplace link
  - Purchase information (if applicable)
  - Version or date of the template
  - Author or company credits
  - License information
  - Any modifications made to the original source

### 3. Using Blocks in Sections
When converting sections that contain repeated elements (like slides, features, testimonials, etc.), use Shopify's block system:

#### a. Block Structure
- Define blocks in the schema using the `blocks` array
- Each block should have:
  - `type`: Unique identifier for the block type
  - `name`: Display name in the theme editor
  - `settings`: Array of settings for the block
  - `limit`: Optional maximum number of blocks allowed

#### b. Block Settings
- Use appropriate setting types:
  - `image_picker` for images
  - `text` for short text
  - `textarea` for longer text
  - `url` for links
  - `select` for dropdown options
  - `color` for color pickers
  - `range` for numeric values

#### c. Block Rendering
- Use `{% for block in section.blocks %}` to iterate through blocks
- Add `{{ block.shopify_attributes }}` to each block's container
- Use `block.settings.[setting_id]` to access block settings
- Add conditional rendering for optional content

#### d. Block Presets
- Include `presets` in the schema to provide default block configurations
- Set up common use cases with pre-configured blocks

### 4. Guidelines
- Use clean, readable code.
- Use proper naming for settings (e.g., `settings.title`, `settings.button_link`).
- Maintain a consistent folder structure for easy integration.
- All section folders should be created within the `sections-storage` directory.
- Use descriptive, section-specific names for HTML and Liquid files.
- Focus on accurate conversion from HTML to Liquid, maintaining functionality.
- When using blocks, ensure proper error handling and fallbacks for missing content.
- Always include source attribution and licensing information in url.md.

### 5. Repeat
- Process the entire HTML page section by section using this structure until complete.

---

This structure will help keep your Liquid sections modular, maintainable, and Shopify-ready, while properly tracking and attributing the original source material. 