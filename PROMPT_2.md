# 🗂 Slider Conversion Guide: Adding Home Bicycle Layout

## 🎯 Objective
Extend the existing slider.liquid section to support a new "Home Bicycle" layout. The goal is to modify the current file with minimal changes while adding full support for the new layout alongside the existing ones.

---

## 📥 Input & Output

- Input HTML:  
  /home/ryotaru/Shopify-theme2/vineta/slider-home-bicycle.html (slider section from the "Home Bicycle" page)

- Existing Component:  
  sections-storage/03-slider/slider.liquid (EXISTING FILE already supporting both "Home default", "Home Electronic" and "Home Fashion Women" layouts)
    - HTML of Slider Home default: /home/ryotaru/Shopify-theme2/vineta/slider-home-default.html
    - HTML of Slider Home Electronic: /home/ryotaru/Shopify-theme2/vineta/slider-home-electronic.html
    - HTML of Slider Home Fashion Women: /home/ryotaru/Shopify-theme2/vineta/slider-home-fashion-women.html

- Output:  
  Updated slider.liquid with support for the "home-bicycle" layout.

---

## 📋 Conversion Process

### Step 1: Analyze Existing slider.liquid File
1. Identify the current structure of the file:
   - Common settings used across all layouts
   - How the file handles switching between different layouts (Home Default, Home Electronic and Home Fashion Women)
   - Identify existing blocks and their potential for reuse

2. Identify extension points:
   - Add "home-bicycle" option to the layout settings (if applicable)
   - Determine where conditional logic needs to be added

### Step 2: Analyze Input HTML to Identify Required Settings

1. Open and study slider-home-bicycle.html:
   - Identify section structure and styling specific to the bicycle layout
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
       { "value": "bicycle", "label": "Bicycle" }
     ],
     "default": "default"
   }

### Step 4: Integrate HTML into Liquid Template

1. Add conditional logic for the bicycle layout:
   
   {% if section.settings.layout == "default" %}
     <!-- Existing default layout code -->
   {% elsif section.settings.layout == "electronic" %}
     <!-- Existing electronic layout code -->
   {% elsif section.settings.layout == "bicycle" %}
     <!-- New bicycle layout code -->
   {% endif %}

---

## 🔍 Important Notes
- The existing slider.liquid file ALREADY has all the necessary if-else logic to support both Home 1 and Home 2 layouts
- Only add new style settings if they're specific to the bicycle layout and not available in existing settings

---

## 📋 Comprehensive Checklist

1. Existing File Analysis
   - [ ] Understand the current section settings structure
   - [ ] Identify how layouts are currently switched
   - [ ] Determine where new code needs to be added

2. Bicycle HTML Analysis
   - [ ] Identify the unique styling and structure of the bicycle layout
   - [ ] Determine if existing block types can be reused
   - [ ] Note any special features unique to the bicycle layout

3. Update Settings and Blocks
   - [ ] Add bicycle layout to layout options
   - [ ] Add only necessary style settings specific to bicyclelayout
   - [ ] Group new settings logically with existing ones

4. Implementation
   - [ ] Add conditional logic for bicycle layout
   - [ ] Ensure backward compatibility with existing layouts
   - [ ] Test all layouts to ensure they still work correctly

5. Documentation
   - [ ] Add comments explaining the new bicycle layout implementation
   - [ ] Document any new settings or blocks added

By following this guide, you'll extend the existing slider.liquid file to support the new bicycle layout while reduced admin overhead. The approach ensures compatibility with current layouts while minimizing changes to the existing file.