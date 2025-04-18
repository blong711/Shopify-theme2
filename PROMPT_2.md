# 🗂 Banner Collection Conversion Guide: Adding Home Fashion 02 Layout

## 🎯 Objective
Extend the existing banner-collection.liquid section to support a new "Home Fashion 02" layout. The goal is to modify the current file with minimal changes while adding full support for the new layout alongside the existing ones.

---

## 📥 Input & Output

- Input HTML:  
  /home/ryotaru/Shopify-theme2/vineta/banner-collection-fashion-02.html (banner collection section from the "Home Fashion 02" page)

- Existing Component:  
  sections-storage/16-banner-collection/banner-collection.liquid (EXISTING FILE already supporting both "Home Electronic" and "Home Bicycle" layouts)
    - HTML of Banner Collection Home Bicycle: /home/ryotaru/Shopify-theme2/vineta/banner-collection-home-bicycle.html
    - HTML of Banner Collection Home Electronic: /home/ryotaru/Shopify-theme2/vineta/banner-collection-home-electronic.html

- Output:  
  Updated banner-collection.liquid with support for the "home-fashion-02" layout.

---

## 📋 Conversion Process

### Step 1: Analyze Existing banner-collection.liquid File
1. Identify the current structure of the file:
   - Common settings used across all layouts
   - How the file handles switching between different layouts (Home Electronic and Home Bicycle)
   - Identify existing blocks and their potential for reuse

2. Identify extension points:
   - Add "home-fashion-02" option to the layout settings (if applicable)
   - Determine where conditional logic needs to be added

### Step 2: Analyze Input HTML to Identify Required Settings

1. Open and study banner-collection-home-fashion-02.html:
   - Identify section structure and styling specific to the Fashion 02 layout
   - Note any repeating elements (e.g., multiple category tiles/cards)
   - Detect layout or style differences from the existing layouts

2. Create a list of required settings:
   - Determine which existing settings can be reused

---

### Step 3: Update Schema and Layout Options

1. Add the new layout option to the existing schema:
   
   {
     "type": "select",
     "id": "layout",
     "label": "Section Layout",
     "options": [
       { "value": "electronic", "label": "Electronic" },
       { "value": "bicycle", "label": "Bicycle" },
       { "value": "fashion-02", "label": "Fashion 02" }
     ],
     "default": "default"
   }

### Step 4: Integrate HTML into Liquid Template

1. Add conditional logic for the fashion 02 layout:
   
   {% if section.settings.layout == "electronic" %}
     <!-- Existing electronic layout code -->
   {% elsif section.settings.layout == "bicycle" %}
     <!-- Existing bicycle layout code -->
   {% elsif section.settings.layout == "fashion-02" %}
     <!-- New fashion 02 layout code -->
   {% endif %}

---

## 🔍 Important Notes
- The existing banner-collection.liquid file ALREADY has all the necessary if-else logic to support both Home 1 and Home 2 layouts
- Only add new style settings if they're specific to the fashion 02 layout and not available in existing settings

---

## 📋 Comprehensive Checklist

1. Existing File Analysis
   - [ ] Understand the current section settings structure
   - [ ] Identify how layouts are currently switched
   - [ ] Determine where new code needs to be added

2. Fashion 02 HTML Analysis
   - [ ] Identify the unique styling and structure of the fashion 02 layout
   - [ ] Determine if existing block types can be reused
   - [ ] Note any special features unique to the fashion 02 layout

3. Update Settings and Blocks
   - [ ] Add fashion 02 layout to layout options
   - [ ] Add only necessary style settings specific to fashion 02layout
   - [ ] Group new settings logically with existing ones

4. Implementation
   - [ ] Add conditional logic for fashion 02 layout
   - [ ] Ensure backward compatibility with existing layouts
   - [ ] Test all layouts to ensure they still work correctly

5. Documentation
   - [ ] Add comments explaining the new fashion 02 layout implementation
   - [ ] Document any new settings or blocks added

By following this guide, you'll extend the existing banner-collection.liquid file to support the new fashion 02 layout while reduced admin overhead. The approach ensures compatibility with current layouts while minimizing changes to the existing file.