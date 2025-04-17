# 🧩 Slider Conversion Guide: Home Electronic to Shopify Liquid

## 🎯 Objective
Convert `vineta/slider-home-electronic.html` into a highly customizable Shopify Liquid section. The goal is to **reuse the existing section** by adding a new layout to support the "home-electronic" version that displays **hero slider**.

---

## 📥 Input & Output

- **Input HTML**:  
  `/home/ryotaru/Shopify-theme2/vineta/slider-home-electronic.html`  
  (slider section from the "Home Electronic" page)

- **Existing Component**:  
  `sections-storage/03-slider/slider.liquid` (used in "Home 1")

- **Output**:  
  Updated section (e.g., `slider.liquid`) with support for the `"home-electronic"` layout using dynamic settings and/or blocks.  
  **Collections and product sliders must be excluded in this layout.**

---

## 📋 Conversion Process

### Step 1: Analyze Input HTML

1. Open and study `slider-home-electronic.html`:
   - Identify dynamic text (e.g., headings, labels)
   - Extract customizable icons (could be image, SVG, or class name) and links
   - Note repeated slider elements (with no products or collections)
   - Determine visual differences in layout (e.g., spacing, shape, alignment)

2. Define required settings:
   - Section heading/subheading
   - Repeating blocks for slider:
     - icon class or image
     - title
     - optional link
   - Optional layout tweaks (e.g., text alignment, icon size, columns)

---

### Step 2: Extend Section Schema with New Layout Option

If this layout differs from default:

1. Add a layout setting to the schema:
   ```json
   {
     "type": "select",
     "id": "layout",
     "label": "Section Layout",
     "options": [
       { "value": "default", "label": "Default" },
       { "value": "home-electronic", "label": "Home Electronic (Slider)" }
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