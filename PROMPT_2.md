# 🗂 Icon box Conversion Guide: Adding Home Phonecase Layout

## 🎯 Objective
Extend the existing icon-box.liquid section to support a new "Home Phonecase" layout. The goal is to modify the current file with minimal changes while adding full support for the new layout alongside the existing ones.

---

## 📥 Input & Output

- Input HTML:  
  /home/ryotaru/Shopify-theme2/vineta/icon-box-home-phonecase.html (icon box section from the "Home Phonecase" page)

- Existing Component:  
  sections-storage/12-icon-box/icon-box.liquid (EXISTING FILE already supporting both "Home Default", "Home Fashion Women", "Home Fashion 02" layouts)
    - HTML of icon box Home Default: /home/ryotaru/Shopify-theme2/vineta/icon-box-home-default.html
    - HTML of icon box Home Electronic: /home/ryotaru/Shopify-theme2/vineta/icon-box-home-electronic.html
    - HTML of icon box Home Bicycle: /home/ryotaru/Shopify-theme2/vineta/icon-box-home-bicycle.html

- Output:  
  Updated icon-box.liquid with support for the "home-phonecase" layout.

---

## 📋 Conversion Process

### Step 1: Analyze Existing icon-box.liquid File
1. Identify the current structure of the file:
   - Common settings used across all layouts
   - How the file handles switching between different layouts (Home Default, Home Fashion Women and Home Fashion 02)
   - Identify existing blocks and their potential for reuse

2. Identify extension points:
   - Add "home-phonecase" option to the layout settings (if applicable)
   - Determine where conditional logic needs to be added

### Step 2: Analyze Input HTML to Identify Required Settings

1. Open and study icon-box-home-phonecase.html:
   - Identify section structure and styling specific to the Phonecase layout
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
       { "value": "default", "label": "Default" },
       { "value": "electronic", "label": "Electronic" },
       { "value": "phonecase", "label": "Phonecase" }
     ],
     "default": "default"
   }

### Step 4: Integrate HTML into Liquid Template

1. Add conditional logic for the fashion women layout:
   
   {% if section.settings.layout == "default" %}
     <!-- Existing default layout code -->
   {% elsif section.settings.layout == "electronic" %}
     <!-- Existing electronic layout code -->
   {% elsif section.settings.layout == "phonecase" %}
     <!-- New phonecase layout code -->
   {% endif %}

---

## 🔍 Important Notes
- The existing icon-box.liquid file ALREADY has all the necessary if-else logic to support both Home 1 and Home 2 layouts
- Only add new style settings if they're specific to the phonecase layout and not available in existing settings

---

## 📋 Comprehensive Checklist

1. Existing File Analysis
   - [ ] Understand the current section settings structure
   - [ ] Identify how layouts are currently switched
   - [ ] Determine where new code needs to be added

2. Phonecase HTML Analysis
   - [ ] Identify the unique styling and structure of the phonecase layout
   - [ ] Determine if existing block types can be reused
   - [ ] Note any special features unique to the phonecase layout

3. Update Settings and Blocks
   - [ ] Add phonecase layout to layout options
   - [ ] Add only necessary style settings specific to phonecase layout
   - [ ] Group new settings logically with existing ones

4. Implementation
   - [ ] Add conditional logic for phonecase layout
   - [ ] Ensure backward compatibility with existing layouts
   - [ ] Test all layouts to ensure they still work correctly

5. Documentation
   - [ ] Add comments explaining the new phonecase layout implementation
   - [ ] Document any new settings or blocks added

By following this guide, you'll extend the existing icon-box.liquid file to support the new phonecase layout while reduced admin overhead. The approach ensures compatibility with current layouts while minimizing changes to the existing file.