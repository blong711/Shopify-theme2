# Header Conversion Guide: Home Electronic to Shopify Liquid

## 🎯 Objective
Convert vineta/header-home-electronic.html into a highly customizable Liquid section, precisely identifying all needed settings from the source HTML.

## 📥 Input & Output
- Input: vineta/header-home-electronic.html (electronic theme header HTML)
- Existing Component: sections-storage/02-header/header.liquid (from home1)
- Output: Header Liquid section with settings derived from input HTML

## 📋 Conversion Process

### Step 1: Analyze Input HTML to Identify Settings
1. Thoroughly examine header-home-electronic.html to identify:
   - Text content that should become settings
   - Images that need customization
   - Links that require adjustment
   - Repeating elements that could become blocks
   - Any other dynamic components

2. Create a specific list of required settings:
   
   [Create list based on HTML analysis]
   Example:
   - Logo (image_picker)
   - Announcement text (text)
   - Navigation menu (link_list)
   - Promotion badge text (text)
   - Hotline text (text)
   - Search placeholder (text)
   - etc.
   

### Step 2: Structure Schema for the Section
1. Organize settings into logical groups:
   
   {% schema %}
   {
     "name": "Header Electronic",
     "settings": [
       {
         "type": "header",
         "content": "Layout & Logo"
       },
       {
         "type": "select",
         "id": "layout",
         "label": "Header Layout",
         "options": [
           {"value": "default", "label": "Default"},
           {"value": "electronic", "label": "Electronic"}
         ],
         "default": "electronic"
       },
       {
         "type": "image_picker",
         "id": "logo",
         "label": "Logo"
       },
       // [Add settings based on HTML analysis]
       
       {
         "type": "header",
         "content": "Announcement Bar"
       },
       {
         "type": "text",
         "id": "announcement_text",
         "label": "Announcement Text",
         "default": "[Extract default from HTML]"
       },
       // [Continue adding settings from analysis]
     ],
     "blocks": [
       // [Define blocks if needed from HTML analysis]
     ],
     "presets": [
       {
         "name": "Header Electronic",
         "category": "Header"
       }
     ]
   }
   {% endschema %}
   

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

Quoc Bao Nguyen, [4/16/2025 11:07 AM]
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