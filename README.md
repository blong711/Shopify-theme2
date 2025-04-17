//Prompt convert categories home 2 with categories home 1 as example

# 🗂️ Categories Conversion Guide: Home Electronic to Shopify Liquid

## 🎯 Objective
Convert `vineta/categories-home-electronic.html` into a highly customizable Shopify Liquid section. The goal is to **reuse the existing categories section** by adding a new layout to support the "home-electronic" (bicycle-style) version **that shows only collections, not products**.

---

## 📥 Input & Output

- **Input HTML**:  
  `/home/ryotaru/Shopify-theme2/vineta/categories-home-electronic.html`  
  (categories section from the "Home Electronic" page)

- **Existing Component**:  
  `sections-storage/07-categories/categories.liquid` (used in "Home 1")

- **Output**:  
  Updated `categories.liquid` with support for the `"home-electronic"` layout using dynamic settings and/or blocks.  
  **Product sliders must be excluded in this layout.**

---

## 📋 Conversion Process

### Step 1: Analyze Input HTML

1. Open and study `categories-home-electronic.html`:
   - Identify dynamic text (e.g., headings)
   - Extract customizable images and links
   - Note repeated collection blocks (no products shown)
   - Determine what differentiates this layout visually (e.g., spacing, image style, alignment)

2. Define required settings:
   - Reuse `collection` blocks from existing section
   - Add support for image style (circle/square)
   - Ensure the layout cleanly omits product display

---

### Step 2: Extend Section Schema with New Layout Option

If the layout differs from default:

1. Add a layout setting to the schema:
   ```json
   {
     "type": "select",
     "id": "layout",
     "label": "Section Layout",
     "options": [
       { "value": "default", "label": "Default" },
       { "value": "home-electronic", "label": "Home Electronic" }
     ],
     "default": "home-electronic"
   }

### Step 3: Convert HTML to Liquid Using Identified Settings
1. Replace static text with Liquid variables:
   
   <!-- Example from original HTML -->
   <div class="announcement-text">Free shipping on all orders over $50</div>
   
   <!-- Convert to -->
   <div class="announcement-text">{{ section.settings.announcement_text }}</div>
   

2. Replace static images:
   
   <!-- Example from original HTML -->
   <img src="assets/images/logo.png" alt="Logo">
   
   <!-- Convert to -->
   {% if section.settings.logo %}
     <img src="{{ section.settings.logo | img_url: '200x' }}" alt="{{ shop.name }}">
   {% else %}
     <span>{{ shop.name }}</span>
   {% endif %}
   

3. Replace static menus:
   
   <!-- Example from original HTML -->
   <ul class="menu">
     <li><a href="#">Home</a></li>
     <li><a href="#">Shop</a></li>
   </ul>
   
   <!-- Convert to -->
   <ul class="menu">
     {% for link in linklists[section.settings.menu].links %}
       <li>
         <a href="{{ link.url }}">{{ link.title }}</a>
         {% if link.links != blank %}
           <!-- Submenu logic -->
         {% endif %}
       </li>
     {% endfor %}
   </ul>
   

### Step 4: Compare with Existing Header
1. Compare settings from current header (home1) with newly identified settings:
   - Retain existing settings needed for default layout
   - Add new settings for electronic layout
   - Create common settings for both layouts where possible

## 🔍 Comprehensive Checklist

1. HTML Analysis
   - [ ] List all dynamic text to convert to settings
   - [ ] Identify all images requiring customization
   - [ ] Identify repeating elements (menus, announcements, etc.)
   - [ ] Identify special features of the electronic header

2. Create Settings
   - [ ] Group settings by function
   - [ ] Set default values from original HTML
   - [ ] Add descriptions for complex settings
   - [ ] Determine correct data types for each setting

3. Convert HTML to Liquid
   - [ ] Replace all static text with setting variables
   - [ ] Integrate dynamic menus
   - [ ] Handle images and links
   - [ ] Add display conditions based on settings

4. Integration with Existing Header
   - [ ] Ensure new settings don't conflict with existing ones
   - [ ] Create conditional logic based on layout

5. Testing and Documentation
   - [ ] Verify all settings work correctly
   - [ ] Update README with list of new settings
   - [ ] Describe how to use the electronic layout

## ✅ Notes
- Extract all text from HTML to create meaningful settings
- Name settings clearly and consistently (e.g., announcement_text, hotline_number)
- Reuse existing settings when possible instead of creating new ones
- Provide default values from the original HTML so the section works correctly when added

By following this guide, you'll create a highly customizable header section based on detailed analysis of the input HTML, optimizing code reuse from home1 and creating a manageable component.
------------------------------------------------------------
//Prompt convert categories home 3 with categories home 1 and 2 as example
# 🗂 Categories Conversion Guide: Adding Home Bicycle Layout with Collection Data

## 🎯 Objective
Extend the existing categories.liquid section to support a new "Home Bicycle" layout. The goal is to modify the current file with minimal changes while adding full support for the new layout alongside the existing ones. Importantly, use collection data instead of manual settings for images and titles to create a more dynamic and maintainable section.

---

## 📥 Input & Output

- Input HTML:  
  /home/ryotaru/Shopify-theme2/vineta/categories-home-bicycle.html (categories section from the "Home Bicycle" page)

- Existing Component:  
  sections-storage/07-categories/categories.liquid (EXISTING FILE already supporting both "Home 1" and "Home 2" layouts)
    - HTML of Categories Home 1: /home/ryotaru/Shopify-theme2/vineta/categories-home-default.html
    - HTML of Categories Home 2: /home/ryotaru/Shopify-theme2/vineta/categories-home-electronic.html

- Output:  
  Updated categories.liquid with support for the "home-bicycle" layout leveraging collection data for images and titles.

---

## 📋 Conversion Process

### Step 1: Analyze Existing categories.liquid File
1. Identify the current structure of the file:
   - Common settings used across all layouts
   - How the file handles switching between different layouts (Home 1 and Home 2)
   - Identify existing blocks and their potential for reuse

2. Identify extension points:
   - Add "home-bicycle" option to the layout settings (if applicable)
   - Determine where conditional logic needs to be added

### Step 2: Analyze Input HTML to Identify Required Settings

1. Open and study categories-home-bicycle.html:
   - Identify section structure and styling specific to the bicycle layout
   - Note any repeating elements (e.g., multiple category tiles/cards)
   - Detect layout or style differences from the existing layouts

2. Create a list of required settings:
   - Determine which existing settings can be reused
   - Use collection picker instead of manual image/title settings

---

### Step 3: Update Schema and Layout Options

1. Add the new layout option to the existing schema:
   
   {
     "type": "select",
     "id": "layout",
     "label": "Section Layout",
     "options": [
       { "value": "default", "label": "Default" },
       { "value": "electronic", "label": "Electronic" },
       { "value": "bicycle", "label": "Bicycle" }
     ],
     "default": "default"
   }
   

2. Ensure blocks utilize collection picker:
   
   {
     "type": "collection",
     "name": "Collection",
     "settings": [
       {
         "type": "collection",
         "id": "collection",
         "label": "Collection"
       },
       {
         "type": "select",
         "id": "button_style",
         "label": "Button Style",
         "options": [
           { "value": "light", "label": "Light" },
           { "value": "dark", "label": "Dark" }
         ],
         "default": "light"
       }
     ]
   }
   

### Step 4: Integrate HTML into Liquid Template

1. Add conditional logic for the bicycle layout:
   
   {% if section.settings.layout == "default" %}
     <!-- Existing default layout code -->
   {% elsif section.settings.layout == "electronic" %}
     <!-- Existing electronic layout code -->
   {% elsif section.settings.layout == "bicycle" %}
     <!-- New bicycle layout code using collection data -->
   {% endif %}
   

2. Implement collection-based rendering for category items:
   - Replace static content with dynamic collection data
   - Use collection images, titles, and URLs instead of manually configured content
   - Preserve the styling and structure from the bicycle layout HTML

---

## 🔍 Important Notes
- The existing categories.liquid file ALREADY has all the necessary if-else logic to support both Home 1 and Home 2 layouts
- Use collection data instead of manual settings for image and title content
- This approach improves maintainability by:
  1. Automatically updating when collection data changes
  2. Reducing the number of settings admins need to manage
  3. Ensuring consistency between the collection page and category showcases
- Ensure blocks use a collection picker setting rather than separate image and title settings
- Only add new style settings if they're specific to the bicycle layout and not available in existing settings
- When implementing the bicycle layout, use collection.featured_image for the category image, collection.title for the heading text, and collection.url for both image and button links
- This collection-based approach reduces the need for redundant content entry and helps maintain consistency across the theme

---

## 📋 Comprehensive Checklist

1. Existing File Analysis
   - [ ] Understand the current section settings structure
   - [ ] Identify how layouts are currently switched
   - [ ] Check if existing blocks already use collection picker (if so, reuse them)
   - [ ] Determine where new code needs to be added

2. Bicycle HTML Analysis
   - [ ] Identify the unique styling and structure of the bicycle layout
   - [ ] Determine if existing block types can be reused
   - [ ] Note any special features unique to the bicycle layout

3. Update Settings and Blocks
   - [ ] Add bicycle layout to layout options
   - [ ] Ensure blocks use collection picker instead of manual image/title settings
   - [ ] Add only necessary style settings specific to bicycle layout
   - [ ] Group new settings logically with existing ones

4. Implementation
   - [ ] Add conditional logic for bicycle layout
   - [ ] Implement bicycle layout HTML using collection data
   - [ ] Ensure backward compatibility with existing layouts
   - [ ] Test all layouts to ensure they still work correctly

5. Documentation
   - [ ] Add comments explaining the new bicycle layout implementation
   - [ ] Document any new settings or blocks added
   - [ ] Note the advantage of using collection data over manual settings

By following this guide, you'll extend the existing categories.liquid file to support the new bicycle layout while leveraging collection data for improved maintainability and reduced admin overhead. The approach ensures compatibility with current layouts while minimizing changes to the existing file.